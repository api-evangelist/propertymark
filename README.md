# Propertymark (propertymark)

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

Propertymark is the United Kingdom's largest professional body for property agents, formed in 2017 from the merger of the National Association of Estate Agents (NAEA), the Association of Residential Letting Agents (ARLA), the Institute of Commercial and Business Agents (ICBA) and the National Association of Valuers and Auctioneers (NAVA), and representing "over 19,000 members" across residential sales, lettings, commercial property, inventories, auctions and valuation. Its home market is the United Kingdom — England, Scotland, Wales, Northern Ireland and the Channel Islands. In the property value chain it sits on the agent-accreditation and consumer-protection side, not the listings side: it publishes the Conduct and Membership Rules, operates a government-approved Client Money Protection scheme, runs Propertymark Qualifications as the sector's specialist awarding organisation, and lobbies government on estate and letting agency regulation. Its API posture is the flat, honest zero — no developer portal, no documented API, no SDK, no webhooks and no published machine-readable contract of any kind.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/propertymark/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/propertymark/refs/heads/main/apis.yml)

## Tags

- Real Estate
- United Kingdom
- Industry Body
- Estate Agents
- Rentals
- Property Management
- Standards
- Certification
- Client Money Protection
- Commercial Real Estate
- Valuation
- PropTech

## Timestamps

- **Created:** 2026-07-26
- **Modified:** 2026-07-26

## APIs

None. Propertymark publishes no API.

Every developer-shaped hostname fails DNS resolution — `developer.`, `developers.`, `api.`, `data.`, `standards.`, `my.`, `portal.`, `members.`, `login.` and `identity.propertymark.co.uk` all return curl exit 000. Every developer-shaped path on `www.propertymark.co.uk` returns a genuine HTTP 404: `/openapi.json`, `/swagger.json`, `/swagger/v1/swagger.json`, `/api-docs`, `/api`, `/api/v1`, `/apis`, `/developers`, `/developer`, `/docs`, `/rest`, `/graphql`, `/swagger`, `/swagger-ui`, `/$metadata`, `/odata` and `/llms.txt`. The site is a Preside CMS build behind Cloudflare that serves honest, differentiated status codes rather than WAF challenges, so these negatives are measurements rather than guesses.

Two real but unpublished surfaces were found and are deliberately **not** listed as APIs:

- An undocumented Preside CMS handler at `/page-types/find_an_expert/getSearchResultForMap/` returns HTTP 200 and 193,017 bytes of JSON carrying 200 member-branch records behind the public Find an Expert directory. No documentation, no terms, no versioning, no contract.
- The Propertymark Learning Learner Portal runs on Nhost (Hasura GraphQL + Nhost auth) behind an AWS API Gateway. Every anonymous probe returns HTTP 403 `{"message":"Missing Authentication Token"}`.

See [`review.yml`](review.yml) for the full probe log.

## RESO Posture

**No RESO reference found. Not RESO-certified.**

RESO is a North American construct tied to NAR-affiliated MLSs. The United Kingdom has no MLS, so there is no listing-data certification layer for a professional body to be certified against — this is absence, not unreachability.

- Propertymark's own site search returns `result: 0 of 0` for both **RESO** and **OData**.
- No Web API certification, no Data Dictionary certification at any version (1.7 / 2.0 / 2.1).
- No OData `$metadata` document; `/$metadata` and `/odata` both return HTTP 404.
- No Universal Property Identifier. Propertymark identifies member firms by internal GUIDs; UK property identity is carried by HM Land Registry title numbers and Ordnance Survey UPRN/TOID.
- Not in the RESO certification directory — `https://www.reso.org/certificates/` (HTTP 200, 51,430 bytes) contains zero occurrences of "Propertymark" or "United Kingdom".

The one thread back to the RESO world is financial, not technical. Propertymark Connect Ltd states verbatim that it "is supported by REACH, the growth accelerator programme of Second Century Ventures, a global technology fund backed by the National Association of REALTORS®" — NAR's venture arm backs a Propertymark subsidiary while NAR's standards arm has no presence in this market at all.

## Access Gate

**`none-published`** — there is nothing published to sign, apply for, or join.

| To do this | You must |
| --- | --- |
| Read the Conduct and Membership Rules | Nothing — free anonymous PDF download (HTTP 200, 672,154 bytes, 37 pages) |
| Get an API key | Impossible — no developer registration, application form, API terms, pricing page or key issuance exists |
| Reach the member area | Be a Propertymark member; `/members.html` returns HTTP 401 and the member area is SAML-gated |
| Get a technology relationship | Industry Supplier membership — a paid marketing directory listing (42 companies), with no published criteria, fee schedule or technical requirements |

## Open Data

**No.** Propertymark publishes no open, unlicensed, publicly callable dataset. Its Housing Insight Report and policy work are PDFs and news pages, not endpoints. The genuinely open UK property data layer belongs to the public sector — HM Land Registry Price Paid Data under the Open Government Licence, and Ordnance Survey's addressing and mapping products.

## Auth Model

- **Public surface:** none. No API, no keys, no OAuth 2, no scopes. `/.well-known/openid-configuration` returns HTTP 404.
- **Member area:** SAML SSO into the Preside CMS. Evidenced by the published `/samlssobadrequest.html` error page and an HTTP 401 on `/members.html`. No SAML metadata is published.
- **Learner portal:** Nhost auth + Hasura GraphQL behind AWS API Gateway. Private application backend; HTTP 403 to every anonymous probe.

Propertymark authenticates members and learners. It authenticates no developers, because it has no developers.

## Standards Publishing

Freely downloadable, but not machine-readable. The Conduct and Membership Rules PDF downloads anonymously with no login and no EULA. Nothing Propertymark publishes exists as a JSON Schema, XSD, data dictionary or exchange format — the sharpest contrast with RICS, the other UK body in this study, which publishes the MIT-licensed RICS Data Standard as JSON Schema and XSD on GitHub.

## Market Seam

Propertymark confirms the UK seam. There is no MLS, no cooperative listing pool and no shared data standard for the market this body governs. Residential listings reach consumers through the Rightmove/Zoopla duopoly via agency CRM software — and that entire layer appears inside Propertymark not as an integration programme but as a marketing directory. Of the 42 Industry Suppliers listed: Reapit, Street, MRI Software, Dezrez, AgentOS, Loftyworks, Prospector Pro, Coadjute and Rightmove itself.

This inverts the US pattern. In the United States a mandated machine-readable contract exists and is unreachable without an MLS agreement. In the United Kingdom there is no mandate and no contract, but the rulebook is a free anonymous download and the government publishes the actual property data openly.

## Adjacent, but not Propertymark

- **Open Property Data Association (OPDA) / Property Data Trust Framework** — [openpropdata.org.uk](https://openpropdata.org.uk/), [github.com/Property-Data-Trust-Framework](https://github.com/Property-Data-Trust-Framework). The closest thing the UK has to a machine-readable property data standard. A separate, independent body; no OPDA or PDTF reference was found on propertymark.co.uk. Profile it as its own provider.
- **HM Land Registry and Ordnance Survey** — the real open UK property data APIs.
- **Vendor APIs on supplier pages** — PropAlt and Inventory Base mention their own APIs on Propertymark marketing pages. Those are the vendors' APIs, not Propertymark's.

## Maintainers

- Kin Lane — kin@apievangelist.com
