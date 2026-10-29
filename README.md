# Clover Health

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Clover Health is a Medicare Advantage health insurer that runs a public developer program built on healthcare interoperability standards. Its public FHIR R4 API exposes a Formulary service (covered drugs, tiers, and utilization management) and a Provider Directory service (practitioners, organizations, locations, healthcare services, and insurance plans), and a separate consent-based Patient Access API delivers a member's clinical and claims data in FHIR-native format via CareEvolution. The APIs implement the CMS Interoperability and Patient Access final rule (CMS-9115-F); Clover was the first payer to go live on a CMS-aligned/TEFCA network. Developers register for approved credentials and authenticate with HTTP Basic or a session cookie.

**Areas:** Company · Healthcare · Health Insurance · Medicare Advantage · FHIR · Interoperability · Provider Directory · Formulary · Patient Access · Payers

## Clover Health on APIs.io

Everything profiled for Clover Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/clover-health/](https://apis.io/providers/clover-health/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Clover Health Fhir R4 Formulary API](https://apis.io/apis/clover-health/clover-health-fhir-r4-formulary-api-api/) — The fhir-r4-formulary-api API from Clover Health — 5 operation(s) for fhir-r4-formulary-api.
- [Clover Health FHIR R4 ProviderDirectory API](https://apis.io/apis/clover-health/clover-health-fhir-r4-providerdirectory-api-api/) — The FHIR R4 ProviderDirectory API API from Clover Health — 17 operation(s) for fhir r4 providerdirectory api.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [clover-health-fhir](https://apis.io/servers/clover-health/clover-health-fhir/)

#### Collections (2)

Postman and Open Collection request collections.

- [FHIR fhir-r4-formulary-api API](https://apis.io/collections/clover-health/open-clover-health-fhir-r4-formulary-api-api/)
- [FHIR fhir-r4-formulary-api FHIR R4 ProviderDirectory API API](https://apis.io/collections/clover-health/open-clover-health-fhir-r4-providerdirectory-api-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Clover Health Fhir Overlay](https://apis.io/overlays/clover-health/clover-health-fhir-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Clover Health Authentication](https://apis.io/security/clover-health/clover-health-authentication/)
- [Clover Health Domain Security](https://apis.io/security/clover-health/clover-health-domain-security/)
- [Clover Health Vulnerability Disclosure](https://apis.io/security/clover-health/clover-health-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cloverhealth.com)
- [Documentation](https://public-api.cloverhealth.com/swagger)
- [API reference](https://public-api.cloverhealth.com/swagger)
- [Sign up](https://docs.google.com/forms/d/1qhbMWXYYn3lpBg8026mW20rxGHE9SL2sHNLzVoyOS0g/edit)
- [Blog](https://www.cloverhealth.com/blog)
- [Security](https://www.cloverhealth.com/.well-known/security.txt)
- [Terms of service](https://www.cloverhealth.com/developers/termsofuse)
- [Privacy policy](https://www.cloverhealth.com/privacy-policy)
- [GitHub](https://github.com/CloverHealth)

## API Evangelist rating

**Kin Score 39.6** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 44.7 |
| Contract governance | 4.5 |
| Operational transparency | 7.9 |
| Developer ergonomics | 47.0 |
| Access clarity | 34.2 |

**Agent readiness 24.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | — |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 34.4** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/clover-health/](https://apis.io/providers/clover-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Clover Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/clover-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
