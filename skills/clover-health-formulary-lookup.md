---
name: Check drug coverage in the Clover Health formulary
description: Look up whether a medication is covered by a Clover Health plan, its tier, and utilization-management detail, using the FHIR Formulary API.
api: openapi/clover-health-fhir-openapi-original.yml
base_url: https://public-api.cloverhealth.com
operations:
  - list_formulary
  - list_formulary_item
  - search_medication_knowledge
  - get_medication_knowledge
  - get_formulary_api_metadata
---

# Check Clover Health drug formulary coverage

Use the FHIR R4 Formulary API to answer "is this drug covered, on what tier, with what restrictions?"

## Auth
- Requires approved developer credentials. Send **HTTP Basic** (`basicAuth`) or authenticated session cookie (`cookieAuth`, cookie `sessionid`).
- All calls are read-only HTTP `GET`.

## Steps
1. **(Optional) Discover capabilities** — call `get_formulary_api_metadata` (`GET /formulary/api/metadata`) to read the FHIR CapabilityStatement and confirm supported search parameters.
2. **Find the formulary list** — call `list_formulary` (`GET /formulary/api/List`) to enumerate the plan's covered-drug List resources; read one with `list_formulary_item` (`GET /formulary/api/List/{id}`).
3. **Search the drug** — call `search_medication_knowledge` (`GET /formulary/api/MedicationKnowledge`) using search parameters (`item`, `identifier`, `status`); page with `_count` / `_offset`.
4. **Read coverage detail** — call `get_medication_knowledge` (`GET /formulary/api/MedicationKnowledge/{id}`) for tier, cost, and utilization-management (prior auth / step therapy / quantity limits).

## Conventions (see conventions/clover-health-conventions.yml)
- Results are FHIR **searchset Bundles**; page via `Bundle.link[relation=next]` and `_count` / `_offset`.
- Content negotiation between `application/fhir+json` (default) and `application/fhir+xml`.
- Errors return a FHIR **OperationOutcome** resource, not RFC 9457 problem+json.
- A `List` groups `MedicationKnowledge` entries via `entry.item` (see data-model/clover-health-data-model.yml).
