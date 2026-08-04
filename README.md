# Zenodo (zenodo)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zenodo is a free, open research data repository operated by CERN and co-developed under the European OpenAIRE program. It enables researchers to deposit, share, and preserve any research output — including datasets, software, papers, preprints, presentations, and multimedia — regardless of format, size, or discipline. Every upload receives a persistent DOI for citation and long-term discoverability. Zenodo provides a REST API for programmatic deposit management, record search and retrieval, and file management, as well as an OAI-PMH endpoint for bulk metadata harvesting. The platform is built on InvenioRDM and stores all data at the CERN Data Centre in Geneva with replicas and nightly tape backups.

APIs.json: [https://raw.githubusercontent.com/api-evangelist/zenodo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zenodo/refs/heads/main/apis.yml)

Naftiko: [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=zenodo-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=zenodo-api-evangelist&utm_content=repo)

## Tags

Research, Open Data, Repository, DOI, Datasets, Software, CERN, OpenAIRE, InvenioRDM, Open Science, Metadata, Harvesting

## APIs

### Zenodo REST API

The primary REST API for Zenodo allowing programmatic deposit creation, file upload, record publication, and record search and retrieval. Authenticates via OAuth 2.0 personal access tokens (Bearer tokens). Provides endpoints for deposits, records, files, communities, funders, grants, and licenses.

- Documentation: https://developers.zenodo.org/
- Base URL: https://zenodo.org/api
- Sandbox: https://sandbox.zenodo.org

### Zenodo OAI-PMH API

Open Archives Initiative Protocol for Metadata Harvesting endpoint for bulk harvesting of Zenodo metadata in formats including oai_dc, marcxml, and oai_datacite4. Supports selective harvesting by community set.

- Documentation: https://developers.zenodo.org/#oai-pmh
- Base URL: https://zenodo.org/oai2d

## Plans, Rate Limits, and FinOps

### Plans

Zenodo is fully free. All registered users receive the same access level with no paid tiers.

- 50 GB storage per record (up to 100 files)
- 150 GB additional allowance distributable across records
- One-time quota increase up to 200 GB per record available on request
- Full REST API and OAI-PMH access included

Details: [plans/zenodo-plans-pricing.yml](plans/zenodo-plans-pricing.yml)

### Rate Limits

| Scope | Limit | Window |
|---|---|---|
| REST API (authenticated) | 100 requests | per minute |
| REST API (authenticated) | 5,000 requests | per hour |
| REST API (guest) | 60 requests | per minute |
| REST API (guest) | 2,000 requests | per hour |
| Search API | 30 requests | per minute |
| OAI-PMH | 30 requests | per minute |
| Sandbox (guest) | 133 requests | per minute |

Throttle response: HTTP 429. Headers: `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`.

Details: [rate-limits/zenodo-rate-limits.yml](rate-limits/zenodo-rate-limits.yml)

### FinOps

Zenodo is free with no billing. FinOps guidance focuses on storage quota visibility, rate-limit optimization through authentication, and fair-use policy compliance.

Details: [finops/zenodo-finops.yml](finops/zenodo-finops.yml)

## Timestamps

- Created: 2026-06-12
- Modified: 2026-06-12

## Common Properties

| Type | URL |
|---|---|
| Website | https://zenodo.org/ |
| Documentation | https://help.zenodo.org/docs/ |
| Developer Portal | https://developers.zenodo.org/ |
| GitHub Organization | https://github.com/zenodo |
| Blog | https://blog.zenodo.org/ |
| Status Page | https://stats.uptimerobot.com/vlYOVuWgM/ |
| X / Twitter | https://x.com/ZENODO_ORG |
| Support | https://support.zenodo.org/ |
| About | https://about.zenodo.org/ |

## Maintainers

**Kin Lane** — kin@apievangelist.com
