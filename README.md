# Lunar Energy (lunar-energy)

Lunar Energy is a Mountain View, California residential clean-energy company founded in August 2020 by former Tesla Energy executive Kunal Girotra. The company sells the Lunar System — a modular 15–30 kWh home battery (9.6 kW continuous / 15 kW peak), Lunar Inverter, Lunar Maximizers, Lunar Bridge, and Eaton AbleEdge smart breakers — controlled by the Lunar App with Lunar AI optimization. Its Gridshare platform is a grid-edge DERMS and virtual power plant engine that manages 130,000+ residential distributed energy resources representing 1.2 GWh of connected storage across multiple manufacturers and third-party operators.

**URL:** [Visit APIs.yml](https://raw.githubusercontent.com/api-evangelist/lunar-energy/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Energy, Home Battery, Solar, Virtual Power Plant, DERMS, Distributed Energy Resources, Grid Services, Demand Response, Storage, Inverter, Smart Home, Energy Management, Tariffs, Telemetry, VPP, Flex Events

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Gridshare Partner API

The operator-facing surface for utilities, retailers, and DER aggregators managing residential distributed energy resources at fleet scale. Covers Sites, Devices, Telemetry, Operation Mode, Overlay Plans, Periodical Tariffs, Dynamic Tariffs, Flex Groups, Flex Events, Flex Dispatches, Prognoses with Diff Requests and Diff Orders, Counterfactuals, and on-site Visits. OAuth 2.0 client-credentials against an Amazon Cognito user pool.

**Human URL:** [https://developers.gridshare.com/reference/authentication](https://developers.gridshare.com/reference/authentication)

- [Documentation — Authentication](https://developers.gridshare.com/reference/authentication)
- [Documentation — Fleet Management](https://developers.gridshare.com/reference/fleet-management)
- [Documentation — Virtual Power Plants](https://developers.gridshare.com/reference/vpp)
- [OpenAPI](openapi/gridshare-partner-api-openapi.yml)
- [Naftiko Capability — Sites](capabilities/gridshare-partner-sites.yaml)
- [Naftiko Capability — Devices](capabilities/gridshare-partner-devices.yaml)
- [Naftiko Capability — Flex Groups](capabilities/gridshare-partner-flex-groups.yaml)
- [Naftiko Capability — Flex Events](capabilities/gridshare-partner-flex-events.yaml)
- [Naftiko Capability — Tariffs](capabilities/gridshare-partner-tariffs.yaml)
- [Naftiko Capability — Visits](capabilities/gridshare-partner-visits.yaml)

### Gridshare Customer API

The homeowner-delegated surface that lets partner apps read or control devices on behalf of a specific Lunar Energy customer once consent has been granted via OAuth 2.0 Authorization Code flow against the `lunar-customer` Cognito pool. v2 endpoints cover Sites, Site Topology, Devices, Telemetry, Operation Mode, and Overlay Plans. Four scopes: `lunar/device.read`, `lunar/device.write`, `lunar/plan.read`, `lunar/plan.write`.

**Human URL:** [https://developers.gridshare.com/reference/authentication-customer](https://developers.gridshare.com/reference/authentication-customer)

- [Documentation — Customer Authentication](https://developers.gridshare.com/reference/authentication-customer)
- [Documentation — Topology Key Concepts](https://developers.gridshare.com/reference/topology-key-concepts)
- [Documentation — Telemetry Key Concepts](https://developers.gridshare.com/reference/telemetry-key-concepts)
- [Documentation — Home Energy Management](https://developers.gridshare.com/reference/energy-management)
- [OpenAPI](openapi/gridshare-customer-api-openapi.yml)
- [Naftiko Capability — Sites](capabilities/gridshare-customer-sites.yaml)
- [Naftiko Capability — Devices](capabilities/gridshare-customer-devices.yaml)
- [Naftiko Capability — Plans](capabilities/gridshare-customer-plans.yaml)

### Gridshare Remote MCP Server

Gridshare publishes a remote Model Context Protocol (MCP) server that exposes the Customer API as MCP tools for AI agents. Authenticated with the same Cognito-issued bearer tokens as the Customer API.

**Human URL:** [https://developers.gridshare.com/reference/customer-remote-mcp](https://developers.gridshare.com/reference/customer-remote-mcp)

## Common Properties

- [Website — lunarenergy.com](https://www.lunarenergy.com)
- [Portal — gridshare.com](https://www.gridshare.com)
- [Portal — Gridshare Developer Portal](https://developers.gridshare.com)
- [Documentation — API Reference](https://developers.gridshare.com/reference)
- [GettingStarted](https://developers.gridshare.com/reference/authentication)
- [Product — Lunar System (Home Battery)](https://www.lunarenergy.com/lunar-system)
- [Product — Gridshare DERMS / VPP](https://www.gridshare.com)
- [Documentation — Installer Hub](https://installerhub.lunarenergy.com)
- [Documentation — Telemetry Key Concepts](https://developers.gridshare.com/reference/telemetry-key-concepts)
- [Documentation — Topology Key Concepts](https://developers.gridshare.com/reference/topology-key-concepts)
- [Documentation — Fleet Management](https://developers.gridshare.com/reference/fleet-management)
- [Documentation — Home Energy Management](https://developers.gridshare.com/reference/energy-management)
- [Documentation — Virtual Power Plants](https://developers.gridshare.com/reference/vpp)
- [Documentation — WebSocket Connections](https://developers.gridshare.com/reference/websocket-connection)
- [Documentation — Remote MCP](https://developers.gridshare.com/reference/customer-remote-mcp)
- [Support — developers@gridshare.com](mailto:developers@gridshare.com)
- [Support — business@lunarenergy.com](mailto:business@lunarenergy.com)
- [Contact](https://www.lunarenergy.com/contact)
- [Careers](https://www.lunarenergy.com/careers)
- [LinkedIn](https://www.linkedin.com/company/lunar-energy)
- [Twitter](https://twitter.com/Lunar_Energy)
- [YouTube](https://www.youtube.com/@lunar_energy)
- [GitHubOrganization](https://github.com/lunarenergy)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Gridshare Partner API](openapi/gridshare-partner-api-openapi.yml)
- [Gridshare Customer API](openapi/gridshare-customer-api-openapi.yml)

### JSON Schema

- [Gridshare Device](json-schema/gridshare-device-schema.json)
- [Gridshare Telemetry](json-schema/gridshare-telemetry-schema.json)
- [Gridshare Flex Event](json-schema/gridshare-flex-event-schema.json)

### JSON-LD

- [Lunar Energy Context](json-ld/lunar-energy-context.jsonld)

### Capabilities (Naftiko)

Partner API:
- [Sites](capabilities/gridshare-partner-sites.yaml)
- [Devices](capabilities/gridshare-partner-devices.yaml)
- [Flex Groups](capabilities/gridshare-partner-flex-groups.yaml)
- [Flex Events](capabilities/gridshare-partner-flex-events.yaml)
- [Tariffs](capabilities/gridshare-partner-tariffs.yaml)
- [Visits](capabilities/gridshare-partner-visits.yaml)

Customer API:
- [Sites](capabilities/gridshare-customer-sites.yaml)
- [Devices](capabilities/gridshare-customer-devices.yaml)
- [Plans](capabilities/gridshare-customer-plans.yaml)

### Spectral Rules

- [Gridshare Rules](rules/gridshare-rules.yml)

### Vocabulary

- [Lunar Energy / Gridshare DERMS Vocabulary](vocabulary/lunar-energy-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/lunar-energy-plans-pricing.yml)
- [Rate Limits](rate-limits/lunar-energy-rate-limits.yml)
- [FinOps Definition](finops/lunar-energy-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
