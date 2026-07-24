---
name: Find an in-network provider (Clover Health)
description: Search the Clover Health FHIR Provider Directory for practitioners, organizations, locations, and the plans they participate in, then read the full detail of a result.
api: openapi/clover-health-fhir-openapi-original.yml
base_url: https://public-api.cloverhealth.com
operations:
  - search_practitioner
  - get_practitioner
  - search_practitioner_role
  - get_practitioner_role
  - search_organization
  - get_organization
  - search_location
  - get_location
  - search_insurance_plan
  - get_insurance_plan
---

# Find an in-network Clover Health provider

Use the FHIR R4 Provider Directory to answer "which doctors / facilities can a Clover member use, and where?"

## Auth
- Requires approved developer credentials (register at the developer portal). Send **HTTP Basic** auth (`basicAuth`) or an authenticated session cookie (`cookieAuth`, cookie `sessionid`).
- All calls are read-only HTTP `GET`.

## Steps
1. **Find the plan** — call `search_insurance_plan` (`GET /providerdirectory/api/InsurancePlan`) to locate the member's Medicare Advantage plan; read one with `get_insurance_plan` (`GET /providerdirectory/api/InsurancePlan/{id}`).
2. **Search practitioners** — call `search_practitioner` (`GET /providerdirectory/api/Practitioner`) with FHIR search parameters (name, `identifier`); page with `_count` / `_offset`.
3. **Resolve the role/location** — for a practitioner, call `search_practitioner_role` (`GET /providerdirectory/api/PractitionerRole`) to get the organizations, locations, and services they participate in; dereference `organization`, `location`, and `healthcareService` references.
4. **Read organizations and locations** — use `search_organization` / `get_organization` and `search_location` / `get_location` to resolve names and addresses.

## Conventions (see conventions/clover-health-conventions.yml)
- Responses are FHIR **searchset Bundles**; follow `Bundle.link[relation=next]` to page.
- Negotiate `application/fhir+json` (default) or `application/fhir+xml` via `Accept`.
- Errors come back as a FHIR **OperationOutcome** resource (`issue[].severity/code/diagnostics`), not RFC 9457 problem+json.
- References between resources use the relationships in `data-model/clover-health-data-model.yml` (e.g. `PractitionerRole.practitioner` -> `Practitioner`).
