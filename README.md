# Daytona (daytona-io)

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

Daytona is open-source, secure, and elastic infrastructure for running AI-generated code. Daytona sandboxes spin up in under 90 milliseconds and provide isolated Linux, Windows, and macOS environments where autonomous agents and developer workflows can execute untrusted code, perform file system and Git operations, run language servers, drive virtual desktops, and persist state via snapshots and volumes. The platform exposes a control-plane REST API (sandboxes, snapshots, volumes, organizations, runners, webhooks) and an in-sandbox Toolbox API (file system, Git, LSP, process execution, PTY, computer use, interpreter), with official SDKs for TypeScript, Python, Ruby, Go, and Java, plus a Go CLI and Homebrew/Windows installers.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/daytona-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/daytona-io/refs/heads/main/apis.yml)

## Tags

- AI
- Agents
- Artificial Intelligence
- Cloud
- Code Execution
- Computer Use
- Developer Tools
- Infrastructure
- Open Source
- Sandbox
- Secure Execution

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Daytona Sandbox API

Create, start, stop, archive, resize, and destroy isolated sandboxes that boot in under 90 milliseconds. The Sandbox API manages the full sandbox lifecycle, exposes labels and metadata, and provides operations for network access, backups, auto-stop / auto-archive policies, and SSH access keys. The legacy /workspace namespace is included as an alias of /sandbox for backwards compatibility.

- **Human URL:** [https://www.daytona.io/docs/en/tools/api/](https://www.daytona.io/docs/en/tools/api/)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- AI
- Agents
- Sandbox
- Lifecycle

#### Properties

- [Documentation](https://www.daytona.io/docs/en/sandboxes)
- [API Reference](https://www.daytona.io/docs/en/tools/api/)
- [OpenAPI](openapi/daytona-sandbox-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-sandbox-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-sandbox-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/daytona-sandbox-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/daytona-sandbox-structure.json)
- [Example](examples/daytona-sandbox-create-example.json)

### Daytona Sandbox Toolbox API

The Toolbox API is the in-sandbox surface for agents. It provides file system operations (list, read, write, move, delete, search, replace, permissions), Git operations (clone, status, commit, push, branch), Process and PTY execution, Language Server Protocol bridging for code intelligence, computer-use control for GUI desktops, an interpreter for inline Python/TypeScript snippets, port and proxy management, and server metadata. Reach it via the platform proxy or directly inside a sandbox.

- **Human URL:** [https://www.daytona.io/docs/en/agent-tools/file-system](https://www.daytona.io/docs/en/agent-tools/file-system)
- **Base URL:** `https://proxy.app.daytona.io/toolbox`

#### Tags

- AI
- Agents
- Computer Use
- File System
- Git
- LSP
- Process Execution
- Toolbox

#### Properties

- [Documentation](https://www.daytona.io/docs/en/agent-tools/file-system)
- [Documentation](https://www.daytona.io/docs/en/agent-tools/git)
- [Documentation](https://www.daytona.io/docs/en/agent-tools/language-server-protocol)
- [Documentation](https://www.daytona.io/docs/en/agent-tools/process-execution)
- [Documentation](https://www.daytona.io/docs/en/agent-tools/computer-use)
- [OpenAPI](openapi/daytona-sandbox-toolbox-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-sandbox-toolbox-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-sandbox-toolbox-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/daytona-toolbox-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-toolbox-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-toolbox-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Snapshots API

Capture, list, restore, share, and destroy sandbox snapshots. Snapshots persist sandbox state — file system, processes, environment — so an agent can resume an interrupted workflow or fan out parallel branches from a common base image. Includes operations for setting snapshot images, managing snapshot organization scope, and bulk lifecycle actions.

- **Human URL:** [https://www.daytona.io/docs/en/snapshots](https://www.daytona.io/docs/en/snapshots)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- AI
- Sandbox
- Snapshots
- State

#### Properties

- [Documentation](https://www.daytona.io/docs/en/snapshots)
- [OpenAPI](openapi/daytona-snapshots-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-snapshots-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-snapshots-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Volumes API

Create and manage persistent volumes that can be attached to one or more sandboxes for shared, durable storage across the sandbox lifecycle. Supports listing, fetching, creating, updating, and deleting volumes and inspecting their mount state.

- **Human URL:** [https://www.daytona.io/docs/en/volumes](https://www.daytona.io/docs/en/volumes)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- AI
- Sandbox
- Storage
- Volumes

#### Properties

- [Documentation](https://www.daytona.io/docs/en/volumes)
- [OpenAPI](openapi/daytona-volumes-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-volumes-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-volumes-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Preview API

Expose ports running inside a sandbox to the public internet via Daytona's secure preview proxy. Useful for showing a running web app, a Jupyter notebook, an LSP gateway, or any agent-produced HTTP service to an end-user without provisioning a domain or load balancer.

- **Human URL:** [https://www.daytona.io/docs/en/preview](https://www.daytona.io/docs/en/preview)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- AI
- Sandbox
- Preview
- Networking

#### Properties

- [Documentation](https://www.daytona.io/docs/en/preview)
- [OpenAPI](openapi/daytona-preview-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Daytona Webhooks API

Configure webhooks so external systems receive callback notifications when sandbox lifecycle events occur (sandbox created/started/stopped/destroyed, snapshot created, etc.). Includes endpoints for listing, fetching, creating, and removing webhook subscriptions.

- **Human URL:** [https://www.daytona.io/docs/en/webhooks](https://www.daytona.io/docs/en/webhooks)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- AI
- Eventing
- Webhooks

#### Properties

- [Documentation](https://www.daytona.io/docs/en/webhooks)
- [OpenAPI](openapi/daytona-webhooks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Organizations API

Manage organizations, members, roles, invitations, suspensions, and per-organization quotas. The Organizations API is the multi-tenant control surface for Daytona Cloud — every sandbox, snapshot, key, and runner belongs to an organization.

- **Human URL:** [https://www.daytona.io/docs/en/account-management/organizations](https://www.daytona.io/docs/en/account-management/organizations)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- Administrative
- Organizations
- Roles
- Quotas

#### Properties

- [Documentation](https://www.daytona.io/docs/en/account-management/organizations)
- [OpenAPI](openapi/daytona-organizations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-organizations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-organizations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona API Keys API

Create, list, rotate, and revoke organization-scoped API keys used to authenticate requests against the Daytona platform. API keys are bearer tokens passed as Authorization headers and can be scoped by role and permissions.

- **Human URL:** [https://www.daytona.io/docs/en/account-management/api-keys](https://www.daytona.io/docs/en/account-management/api-keys)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- Administrative
- API Keys
- Authentication

#### Properties

- [Documentation](https://www.daytona.io/docs/en/account-management/api-keys)
- [OpenAPI](openapi/daytona-api-keys-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-api-keys-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-api-keys-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Users API

Manage user profiles, linked accounts (GitHub, GitLab, Bitbucket), and notification preferences. The Users API governs the human side of Daytona — identity, profile, and personal settings — independent of the organization-level admin surface.

- **Human URL:** [https://www.daytona.io/docs/en/account-management/linked-accounts](https://www.daytona.io/docs/en/account-management/linked-accounts)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- Administrative
- Users
- Linked Accounts

#### Properties

- [Documentation](https://www.daytona.io/docs/en/account-management/linked-accounts)
- [OpenAPI](openapi/daytona-users-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-users-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-users-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Admin API

Platform-level administration covering runners (compute pools), regions, Docker registry configuration, object storage, jobs, audit logs, and global config. Used by operators of customer-managed compute, by self-hosted open-source deployments, and by Daytona staff for managed-service operations.

- **Human URL:** [https://www.daytona.io/docs/en/deployments/customer-managed-compute](https://www.daytona.io/docs/en/deployments/customer-managed-compute)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- Administrative
- Audit
- Configuration
- Docker Registry
- Jobs
- Object Storage
- Regions
- Runners

#### Properties

- [Documentation](https://www.daytona.io/docs/en/deployments/customer-managed-compute)
- [Documentation](https://www.daytona.io/docs/en/security/audit-logs)
- [OpenAPI](openapi/daytona-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Daytona Health API

Liveness and readiness probes for the Daytona control plane. Returns 200 when the API is healthy and ready to serve traffic. Used by infrastructure monitors, load balancers, and Kubernetes deployments running the open-source Daytona platform.

- **Human URL:** [https://www.daytona.io/docs/en/observability/opentelemetry-collection](https://www.daytona.io/docs/en/observability/opentelemetry-collection)
- **Base URL:** `https://app.daytona.io/api`

#### Tags

- Health
- Observability

#### Properties

- [Documentation](https://www.daytona.io/docs/en/observability/opentelemetry-collection)
- [OpenAPI](openapi/daytona-health-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/daytona-health-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/daytona-health-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Developer Portal](https://www.daytona.io/)
- [Documentation](https://www.daytona.io/docs)
- [Getting Started](https://www.daytona.io/docs/en/getting-started)
- [Quickstart](https://www.daytona.io/docs/en)
- [API Reference](https://www.daytona.io/docs/en/tools/api/)
- [Console](https://app.daytona.io/)
- [Sign Up](https://app.daytona.io/)
- [Login](https://app.daytona.io/)
- [Authentication](https://www.daytona.io/docs/en/account-management/api-keys)
- [Rate Limits](https://www.daytona.io/docs/en/account-management/limits)
- [Regions](https://www.daytona.io/docs/en/sandbox/regions)
- [Blog](https://www.daytona.io/dotfiles)
- [Newsletter](https://www.daytona.io/dotfiles)
- [YouTube](https://youtube.com/@daytonaio)
- [Support](https://go.daytona.io/slack)
- [Contact](https://www.daytona.io/contact)
- [Status Page](https://status.app.daytona.io/)
- [Trust Center](https://trust.daytona.io/)
- [Terms of Service](https://www.daytona.io/terms-of-service)
- [Privacy Policy](https://www.daytona.io/privacy-policy)
- [Security](https://www.daytona.io/docs/en/security/security-exhibit)
- [GitHub Organization](https://github.com/daytonaio)
- [GitHub Repository](https://github.com/daytonaio/daytona)
- [X (Twitter)](https://twitter.com/daytonaio)
- [LinkedIn](https://www.linkedin.com/company/daytonaio/)
- [SDK](https://pypi.org/project/daytona/)
- [SDK](https://www.npmjs.com/package/@daytonaio/sdk)
- [SDK](https://rubygems.org/gems/daytona)
- [SDK](https://pkg.go.dev/github.com/daytonaio/daytona)
- [SDK](https://central.sonatype.com/artifact/io.daytona/daytona-sdk)
- [C L I](https://www.daytona.io/docs/en/tools/cli)
- [C L I](https://github.com/daytonaio/homebrew-cli)
- [Resources](https://github.com/daytonaio/helm-charts)
- [Resources](https://github.com/daytonaio/terraform-modules)
- [Spectral Rules](rules/daytona-rules.yml)
- [Vocabulary](vocabulary/daytona-io-vocabulary.yml)
- [JSON-LD](json-ld/daytona-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Plans](plans/daytona-io-plans-pricing.yml)
- [Rate Limits](rate-limits/daytona-io-rate-limits.yml)
- [Fin Ops](finops/daytona-io-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://kinlane.com
