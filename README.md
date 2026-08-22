# Smithery (smithery-ai)

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
