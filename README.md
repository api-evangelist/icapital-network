# iCapital Network

iCapital (Institutional Capital Network, Inc.), founded 2013 and headquartered in New York, operates
the alternative investments marketplace and the operating infrastructure behind it — private markets
funds, hedge funds, structured investments, annuities, model portfolios and separately managed
accounts — for wealth managers, RIAs, family offices, institutional investors, and the asset managers
who distribute through them. iCapital Marketplace advertises access to funds from 700+ asset managers
and reports $945B+ in global platform assets.

- Website: https://icapital.com/
- Marketplace: https://marketplace.icapital.com/
- GitHub: https://github.com/icapitalnetwork
- Forge Global secondary-market listing: https://forgeglobal.com/icapital-network_stock/

## API surface — none published (verified 2026-08-01)

iCapital publishes **no public API**. The enrichment pass ran the full contract-discovery sweep and
every probe missed:

- No developer portal, API reference, quickstart or docs host. `developer.`, `developers.`, `docs.`,
  `api.`, `apis.`, `dlt.`, `platform.`, `portal.` and `partners.icapital.com` do **not resolve in DNS**.
- No OpenAPI/Swagger: `/openapi.json`, `/openapi.yaml`, `/swagger.json`, `/v1/openapi.json`,
  `/api-docs`, `/docs`, `/redoc` all 404 on `icapital.com`, `marketplace.icapital.com` and
  `icapitalnetwork.com`.
- No GraphQL surface, no AsyncAPI, no webhook catalog, no MCP server, no A2A agent card.
- No `/.well-known/` document of any kind (see `well-known/`), so no `security.txt`, no OIDC/OAuth
  discovery metadata, no api-catalog.
- No first-party SDKs: nothing on npm, PyPI or in the GitHub org, which holds 5 repos of internal
  tooling and open-source forks.
- No status page. `status.icapital.com` resolves only via a wildcard HubSpot CNAME and returns a
  Cloudflare 1034 error — it is not a status page.

iCapital does describe **iCapital DLT** as "an API-first distributed ledger technology platform"
(built on the Canton Network) and states that "iCapital offers comprehensive API documentation and
technical support from our team of experts to assist with the integration process." That documentation
is not published on the open web — it is delivered to integration partners under a commercial
relationship. Partner integration is otherwise described as SSO into advisor workstations plus embedded
fund/model investing inside portfolio-management and UMA platforms.

## Artifacts in this repo

| Path | Type | Method |
|---|---|---|
| `apis.yml` | APIs.json 0.20 index | identity |
| `conformance/icapital-network-conformance.yml` | Conformance | searched |
| `llms/icapital-network-llms.txt` | LLMsTxt | generated |
| `security/icapital-network-domain-security.yml` | DomainSecurity | probed |
| `well-known/icapital-network-well-known.yml` | probe record (no pointer — zero documents found) | probed |

No `Compliance`, `TrustCenter`, `Security`, `VulnerabilityDisclosure` or `WellKnown` pointer is wired,
because none of those things is publicly evidenced. Re-run the pipeline if iCapital ever opens a
developer portal for DLT.
