# Smithery (smithery-ai)

Smithery is an MCP server registry and hosting platform that lets developers discover, publish, and connect to Model Context Protocol servers from any AI agent. The platform combines a public registry of thousands of community MCP servers with a managed gateway that handles OAuth, credential storage, session state, protocol compliance, and webhook triggers — so agents can call tools across servers via a single stateless Connect API. Smithery also distributes a CLI, a TypeScript API client, a local runner, a Skills Registry, deep-linking integrations for popular MCP clients (Claude Desktop, Cursor, Continue), and uplink support for exposing local servers as hosted connections.

**URL:** [Visit APIs.yml](https://raw.githubusercontent.com/api-evangelist/smithery-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- AI, Agents, MCP, Model Context Protocol, Registry, Hosting, Tools, Skills, Marketplace, Developer Platform

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Platform Overview

Smithery exposes a single REST surface at `https://api.smithery.ai` covering two complementary concerns:

| Concern | Resource | Purpose |
|---|---|---|
| **Registry** | `/servers`, `/skills`, `/tools`, `/namespaces`, `/organizations/{orgId}/api-keys`, `/tokens` | Discover, publish, and govern MCP servers and Skills. |
| **Connect** | `/connect/{namespace}/...`, `/connect/{namespace}/{connectionId}/mcp` | Stateless runtime — create connections to hosted servers, invoke MCP JSON-RPC, manage triggers and subscriptions. |

Both surfaces share a Bearer-token security scheme and a namespace model (user- or organization-owned).

## APIs

### Smithery Registry API

Discover, publish, and manage MCP (Model Context Protocol) servers and Agent Skills on Smithery. Browse the public registry of thousands of community MCP servers, search tools across servers, publish your own server releases (URL or MCPB bundle), manage release logs and runtime logs, set server secrets, manage custom domains, create namespaces, manage organization API keys, and mint scoped service tokens for machine-to-machine access.

**Human URL:** [https://smithery.ai/docs](https://smithery.ai/docs)

- [Documentation](https://smithery.ai/docs)
- [Upstream OpenAPI](https://smithery.ai/docs/openapi.json)
- [OpenAPI (this repo)](openapi/smithery-registry-api-openapi.yml)

Representative endpoints:

| Method | Path | Summary |
|---|---|---|
| `GET` | `/servers` | List or search MCP servers in the public registry |
| `GET` | `/servers/{qualifiedName}` | Get a server by `namespace/server` qualified name |
| `PUT` | `/servers/{qualifiedName}` | Create a server (idempotent) |
| `PUT` | `/servers/{qualifiedName}/releases` | Publish a release (URL or MCPB bundle) |
| `GET` | `/servers/{qualifiedName}/releases/{id}/stream` | Stream release logs over SSE |
| `GET` | `/servers/{qualifiedName}/logs` | List runtime logs |
| `PUT` | `/servers/{qualifiedName}/secrets` | Set a server secret |
| `GET` | `/skills` | List or search Skills |
| `GET` | `/tools` | Search tools across the entire registry |
| `POST` | `/namespaces` | Create a namespace (or use PUT for a specified name) |
| `POST` | `/organizations/{orgId}/api-keys` | Create a team API key (admin only) |
| `POST` | `/tokens` | Create a scoped service token |

### Smithery Connect API

Connect AI agents to any MCP server hosted on Smithery without managing OAuth flows, credential storage, or session state. Create stateless connections under a namespace, execute MCP JSON-RPC against a Smithery-managed gateway, list and call tools, manage trigger definitions exposed by a server, and subscribe (or unsubscribe) to trigger events that fire as webhooks. The Connect API is the runtime counterpart to the Registry — it is how agents actually talk to the servers they discover.

**Human URL:** [https://smithery.ai/docs/usage/connect](https://smithery.ai/docs/usage/connect)

- [Documentation](https://smithery.ai/docs/usage/connect)
- [OpenAPI (this repo)](openapi/smithery-connect-api-openapi.yml)
- [Naftiko Capability — Discover and Connect](capabilities/discover-and-connect.yaml)

Representative endpoints:

| Method | Path | Summary |
|---|---|---|
| `POST` | `/connect/{namespace}` | Create a connection with a generated ID |
| `PUT` | `/connect/{namespace}/{connectionId}` | Create or update a connection with a specified ID |
| `GET` | `/connect/{namespace}` | List connections in a namespace |
| `GET` | `/connect/{namespace}/{connectionId}` | Get connection details |
| `DELETE` | `/connect/{namespace}/{connectionId}` | Delete a connection and terminate the MCP session |
| `POST` | `/connect/{namespace}/{connectionId}/mcp` | Execute MCP JSON-RPC against the connected server |
| `GET` | `/connect/{namespace}/{connectionId}/.triggers` | List triggers exposed by the server |
| `POST` | `/connect/{namespace}/{connectionId}/.triggers/{triggerName}` | Subscribe to / refresh a trigger |
| `POST` | `/connect/{namespace}/.subscriptions` | Create a namespace-wide subscription |

## Schemas, Vocabulary, and Examples

- [JSON Schema — Server](json-schema/smithery-server-schema.json)
- [JSON Schema — Connection](json-schema/smithery-connection-schema.json)
- [JSON-LD Context](json-ld/smithery-ai-context.jsonld)
- [Vocabulary](vocabulary/smithery-ai-vocabulary.yml)
- [Spectral Rules](rules/smithery-ai-rules.yml)
- [Example — List Servers](examples/smithery-list-servers-example.json)
- [Example — Create Connection](examples/smithery-create-connection-example.json)
- [Example — MCP JSON-RPC Invoke](examples/smithery-mcp-invoke-example.json)

## Commercial Surface

- [Plans](plans/smithery-ai-plans-pricing.yml) — External listings free; Hobby, Pro, Custom paid hosting tiers (free hosted plan sunset 2026-03-01).
- [Rate Limits](rate-limits/smithery-ai-rate-limits.yml) — Bearer-token auth with per-namespace and per-connection scopable service tokens; numeric per-endpoint quotas not publicly documented.
- [FinOps](finops/smithery-ai-finops.yml) — FOCUS-aligned subscription billing per hosted server-month. Observability insights free across all hosting modes.

## SDK, CLI, and Tooling

- [Smithery CLI](https://github.com/smithery-ai/cli) — `smithery` command for managing MCP servers, skills, and connections (npm / Homebrew / Scoop).
- [smithery runner](https://github.com/smithery-ai/runner) — local MCP launcher for stdio servers.
- [TypeScript API client](https://github.com/smithery-ai/typescript-api) — Apache-2.0.
- [Smithery CLI MCP](https://github.com/smithery-ai/smithery-cli-mcp) — official MCP server for the Smithery CLI itself.
- [Cookbook](https://github.com/smithery-ai/smithery-cookbook) — recipes and reference implementations.
- [migration-guide-mcp](https://github.com/smithery-ai/migration-guide-mcp) — STDIO → Streamable HTTP migration assistant.
- [agent.pw](https://github.com/smithery-ai/agent.pw) — share APIs with agents without sharing secrets.
- [mouseless](https://github.com/smithery-ai/mouseless) — Rust MCP server for macOS desktop control.
- [hylo](https://github.com/smithery-ai/hylo) + [hylo-plugins](https://github.com/smithery-ai/hylo-plugins) — workflow engine with managed-agent and cloud-claude plugins.
- [render-markdown](https://github.com/smithery-ai/render-markdown) — local markdown to styled HTML preview.

## Client Integrations

Smithery integrates with MCP-compatible clients via deep links and the Connect API:

- Claude Desktop, Cursor, Continue, Cline, Zed, mcp-chat (reference client)
- [Vercel AI SDK integration](https://smithery.ai/docs/integrations/vercel_ai_sdk)
- Any MCP client via Streamable HTTP at `https://api.smithery.ai/connect/{namespace}/{connectionId}/mcp`

## Key Features

- Public MCP server registry with thousands of community-published servers
- Server publishing via URL (Streamable HTTP) or MCPB bundle for stdio-based servers
- Managed gateway handling MCP protocol compliance, metadata enrichment, and caching
- Auto-generated OAuth UI modals for servers requiring API keys or user configuration
- Stateless Connect API — agents talk to MCP servers without holding session state client-side
- Zero OAuth setup with encrypted credential storage and automatic credential refresh
- Skills Registry — reusable prompt-based skills installable via `npx skills add`
- Namespaces for grouping servers, connections, and skills under a user or organization
- Triggers — expose MCP server events as webhooks; per-connection or per-namespace subscriptions
- Uplink — expose a local MCP server as a hosted connection without deploying it
- Deep linking for one-click client integration
- Scoped service tokens with per-namespace and per-connection scoping
- Team API keys with admin-only create/list/revoke under organization namespaces
- Custom domains for hosted MCP servers
- Per-server secrets management
- Release management with logs, streaming SSE log feed, and resume-on-paused-release support
- Cross-server tool search at `/tools`

## Maintainers

- **Kin Lane** — [API Evangelist](https://apievangelist.com) — [@apievangelist](https://twitter.com/apievangelist) — info@apievangelist.com
