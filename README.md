# Lunar Energy (lunar-energy)

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

Lunar Energy is a Mountain View, California-based residential clean-energy company founded in August 2020 by former Tesla Energy executive Kunal Girotra. The company designs and manufactures the Lunar System — a modular home battery (15–30 kWh, 9.6 kW continuous / 15 kW peak), Lunar Inverter, Lunar Maximizers (module-level power optimizers), Lunar Bridge meter socket adapter, and Eaton AbleEdge smart-breaker integration — controlled by the Lunar App with Lunar AI optimization. Its Gridshare platform is a grid-edge DERMS (Distributed Energy Resource Management System) and virtual power plant engine that manages 130,000+ residential distributed energy resources representing 1.2 GWh of connected storage across multiple manufacturers and third-party operators. Gridshare powers utility demand response and VPP programs through flex groups, flex dispatches, prognoses, dynamic and periodical tariffs, and per-device remote operation-mode control. Lunar Energy is backed by SunPower and Sunrun partnerships; SoftBank Energy is a major investor. The Gridshare Partner API and Customer API are gated behind business onboarding — credentials are issued by Lunar Energy after contacting developers@gridshare.com.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lunar-energy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lunar-energy/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Energy
- Home Battery
- Solar
- Virtual Power Plant
- DERMS
- Distributed Energy Resources
- Grid Services
- Demand Response
- Storage
- Inverter
- Smart Home
- Energy Management
- Tariffs
- Telemetry
- VPP
- Flex Events

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Gridshare Partner API

The Gridshare Partner API is the operator-facing surface for utilities, DER aggregators, and energy retailers to manage residential distributed energy resources at fleet scale. v1 endpoints cover Sites, Devices, Telemetry, Operation Mode, Overlay Plans, Periodical Tariffs, Dynamic Tariffs, Flex Groups (participants and bulk membership), Flex Events and Flex Dispatch opt-outs, Prognoses with Diff Requests and Diff Orders, Counterfactuals, and on-site Visits. Authenticated via OAuth 2.0 client-credentials against Amazon Cognito; tokens expire after 1 hour. Regional production servers are developer-api.partner.us.mygridshare.com (US) and developer-api.partner.mygridshare.com (rest of world).

- **Human URL:** [https://developers.gridshare.com/reference/authentication](https://developers.gridshare.com/reference/authentication)

#### Tags

- Partner
- Fleet Management
- Virtual Power Plant
- Flex Groups
- Flex Events
- Tariffs
- Devices
- Sites

#### Properties

- [Documentation](https://developers.gridshare.com/reference/authentication)
- [Documentation](https://developers.gridshare.com/reference/fleet-management)
- [Documentation](https://developers.gridshare.com/reference/vpp)
- [OpenAPI](openapi/gridshare-partner-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gridshare-partner-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gridshare-partner-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gridshare Customer API

The Gridshare Customer API is the homeowner-delegated surface for partners that need to read or control devices on behalf of a specific Lunar Energy customer. It implements OAuth 2.0 Authorization Code flow against the lunar-customer Amazon Cognito user pool with four scopes — `lunar/device.read`, `lunar/device.write`, `lunar/plan.read`, `lunar/plan.write`. v2 endpoints expose lightweight Site listing, Site Topology (a sensor tree usable to drive telemetry queries), Device listing and retrieval, Telemetry (per-sensor time-bucketed readings with energy_Wh_increment / energy_Wh_decrement when include=energy), Operation Mode (Simple / Schedule / Smart), Overlay Plans for short-term device control, and partial device updates. Production servers developer-api.customer.mygridshare.com.

- **Human URL:** [https://developers.gridshare.com/reference/authentication-customer](https://developers.gridshare.com/reference/authentication-customer)

#### Tags

- Customer
- Home Energy Management
- Devices
- Telemetry
- Topology
- Operation Mode
- Overlay Plans

#### Properties

- [Documentation](https://developers.gridshare.com/reference/authentication-customer)
- [Documentation](https://developers.gridshare.com/reference/topology-key-concepts)
- [Documentation](https://developers.gridshare.com/reference/telemetry-key-concepts)
- [Documentation](https://developers.gridshare.com/reference/energy-management)
- [OpenAPI](openapi/gridshare-customer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gridshare-customer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gridshare-customer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Gridshare Remote MCP Server

Gridshare publishes a remote Model Context Protocol (MCP) server that exposes the Customer API as MCP tools for AI agents. Authenticated with the same Cognito-issued bearer tokens as the Customer API.

- **Human URL:** [https://developers.gridshare.com/reference/customer-remote-mcp](https://developers.gridshare.com/reference/customer-remote-mcp)

#### Tags

- MCP
- Model Context Protocol
- Remote MCP
- AI Agents
- Customer

#### Properties

- [Documentation](https://developers.gridshare.com/reference/customer-remote-mcp)
- [Postman Collection](collections/gridshare-customer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gridshare-customer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/gridshare-partner-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gridshare-partner-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.lunarenergy.com)
- [Portal](https://www.gridshare.com)
- [Portal](https://developers.gridshare.com)
- [Documentation](https://developers.gridshare.com/reference)
- [Getting Started](https://developers.gridshare.com/reference/authentication)
- [Product](https://www.lunarenergy.com/lunar-system)
- [Product](https://www.gridshare.com)
- [Documentation](https://installerhub.lunarenergy.com)
- [Documentation](https://developers.gridshare.com/reference/telemetry-key-concepts)
- [Documentation](https://developers.gridshare.com/reference/topology-key-concepts)
- [Documentation](https://developers.gridshare.com/reference/fleet-management)
- [Documentation](https://developers.gridshare.com/reference/energy-management)
- [Documentation](https://developers.gridshare.com/reference/vpp)
- [Documentation](https://developers.gridshare.com/reference/websocket-connection)
- [Documentation](https://developers.gridshare.com/reference/customer-remote-mcp)
- [Support](mailto:developers@gridshare.com)
- [Support](mailto:business@lunarenergy.com)
- [Contact](https://www.lunarenergy.com/contact)
- [Careers](https://www.lunarenergy.com/careers)
- [LinkedIn](https://www.linkedin.com/company/lunar-energy)
- [Twitter](https://twitter.com/Lunar_Energy)
- [YouTube](https://www.youtube.com/@lunar_energy)
- [GitHub Organization](https://github.com/lunarenergy)
- [Features](undefined)
- [Plans](plans/lunar-energy-plans-pricing.yml)
- [Rate Limits](rate-limits/lunar-energy-rate-limits.yml)
- [Fin Ops](finops/lunar-energy-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
