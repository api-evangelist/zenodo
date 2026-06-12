# Zenodo (zenodo)

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
