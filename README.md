# Smithery (smithery-ai)

Smithery is an MCP server registry and hosting platform that lets developers discover, publish, and connect to Model Context Protocol servers from any AI agent. The platform combines a public registry of thousands of community MCP servers with a managed gateway that handles OAuth, credential storage, session state, protocol compliance, and webhook triggers — so agents can call tools across servers via a single stateless Connect API. Smithery also distributes a CLI, a TypeScript API client, a local runner, a Skills Registry, deep-linking integrations for popular MCP clients (Claude Desktop, Cursor, Continue), and uplink support for exposing local servers as hosted connections.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/smithery-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/smithery-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Producing
- **Access:** 3rd-Party

## Tags

- AI
- Agents
- MCP
- Model Context Protocol
- Registry
- Hosting
- Tools
- Skills
- Marketplace
- Developer Platform

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Smithery Registry API

Discover, publish, and manage MCP (Model Context Protocol) servers and Agent Skills on Smithery. Browse the public registry of thousands of MCP servers, search tools across servers, publish your own server releases (URL or MCPB bundle), manage release logs and runtime logs, set server secrets, manage custom domains, create namespaces, manage organization API keys, and mint scoped service tokens for machine-to-machine access.

- **Human URL:** [https://smithery.ai/docs](https://smithery.ai/docs)
- **Base URL:** `https://api.smithery.ai`

#### Tags

- MCP
- Registry
- Servers
- Skills
- Tools
- AI
- Agents

#### Properties

- [Documentation](https://smithery.ai/docs)
- [OpenAPI](https://smithery.ai/docs/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/smithery-registry-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smithery-registry-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smithery-registry-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/smithery-server-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/smithery-server-structure.json)
- [JSON-LD](json-ld/smithery-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/smithery-ai-vocabulary.yml)
- [Spectral Rules](rules/smithery-ai-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)

### Smithery Connect API

Connect AI agents to any MCP server hosted on Smithery without managing OAuth flows, credential storage, or session state. Create stateless connections under a namespace, execute MCP JSON-RPC against a Smithery-managed gateway, list and call tools, manage trigger definitions exposed by a server, and subscribe (or unsubscribe) to trigger events that fire as webhooks. The Connect API is the runtime counterpart to the Registry — it is how agents actually talk to the servers they discover.

- **Human URL:** [https://smithery.ai/docs/usage/connect](https://smithery.ai/docs/usage/connect)
- **Base URL:** `https://api.smithery.ai`

#### Tags

- MCP
- Connections
- Triggers
- Webhooks
- AI
- Agents

#### Properties

- [Documentation](https://smithery.ai/docs/usage/connect)
- [OpenAPI](openapi/smithery-connect-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/smithery-connect-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smithery-connect-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/smithery-connection-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/smithery-connection-structure.json)

## Common Properties

- [Portal](https://smithery.ai)
- [Documentation](https://smithery.ai/docs)
- [Getting Started](https://smithery.ai/docs/main)
- [OpenAPI](https://smithery.ai/docs/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://smithery.ai/docs/llms.txt)
- [Documentation](https://smithery.ai/docs/mcp)
- [Documentation](https://smithery.ai/docs/concepts/what_is_mcp)
- [Documentation](https://smithery.ai/docs/concepts/namespaces)
- [Documentation](https://smithery.ai/docs/concepts/cli)
- [Documentation](https://smithery.ai/docs/build)
- [Documentation](https://smithery.ai/docs/build/publish)
- [Documentation](https://smithery.ai/docs/build/triggers)
- [Documentation](https://smithery.ai/docs/usage/connect)
- [Documentation](https://smithery.ai/docs/usage/deep-linking)
- [Documentation](https://smithery.ai/docs/usage/uplink)
- [Documentation](https://smithery.ai/docs/usage/token-scoping)
- [Documentation](https://smithery.ai/docs/usage/listing_your_client)
- [Documentation](https://smithery.ai/docs/integrations/vercel_ai_sdk)
- [Code Examples](https://smithery.ai/docs/cookbooks/typescript_oauth_client)
- [GitHub Organization](https://github.com/smithery-ai)
- [C L I](https://github.com/smithery-ai/cli)
- [Tool](https://github.com/smithery-ai/runner)
- [SDK](https://github.com/smithery-ai/typescript-api)
- [Tool](https://github.com/smithery-ai/registry)
- [Tool](https://github.com/smithery-ai/smithery-cli-mcp)
- [Code Examples](https://github.com/smithery-ai/smithery-cookbook)
- [Tool](https://github.com/smithery-ai/mcp-chat)
- [Tool](https://github.com/smithery-ai/agent.pw)
- [Tool](https://github.com/smithery-ai/mouseless)
- [Tool](https://github.com/smithery-ai/render-markdown)
- [Tool](https://github.com/smithery-ai/mcp-to-cli)
- [Tool](https://github.com/smithery-ai/migration-guide-mcp)
- [Tool](https://github.com/smithery-ai/agent-hook)
- [Documentation](https://github.com/smithery-ai/homebrew-smithery)
- [Documentation](https://github.com/smithery-ai/scoop-smithery)
- [Tool](https://github.com/smithery-ai/skills)
- [Tool](https://github.com/smithery-ai/hylo)
- [Plugins](https://github.com/smithery-ai/hylo-plugins)
- [Tool](https://github.com/smithery-ai/mouseless)
- [Tool](https://github.com/smithery-ai/familysearch-mcp)
- [Tool](https://github.com/smithery-ai/mcp-server-7)
- [Tool](https://github.com/smithery-ai/mcp-multilspy)
- [Tool](https://github.com/smithery-ai/mcp-oauth-debug)
- [Tool](https://github.com/smithery-ai/openchat)
- [Tool](https://github.com/smithery-ai/okay-error)
- [Tool](https://github.com/smithery-ai/workers-biscuit)
- [Documentation](https://github.com/smithery-ai/rfm)
- [Documentation](https://github.com/modelcontextprotocol)
- [Documentation](https://modelcontextprotocol.io)
- [Pricing](https://smithery.ai/pricing)
- [Plans](https://plans/smithery-ai-plans-pricing.yml)
- [Rate Limits](https://rate-limits/smithery-ai-rate-limits.yml)
- [Fin Ops](https://finops/smithery-ai-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
