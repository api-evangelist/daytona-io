# Daytona (daytona-io)

Daytona is open-source, secure, and elastic infrastructure for running AI-generated code. Daytona sandboxes spin up in under 90 milliseconds and provide isolated Linux, Windows, and macOS environments where autonomous agents and developer workflows can execute untrusted code, perform file system and Git operations, run language servers, drive virtual desktops, and persist state via snapshots and volumes. The platform exposes a control-plane REST API and an in-sandbox Toolbox API, with official SDKs for TypeScript, Python, Ruby, Go, and Java, plus a Go CLI and Homebrew/Windows installers.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/daytona-io/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Agents, Artificial Intelligence, Cloud, Code Execution, Computer Use, Developer Tools, Infrastructure, Open Source, Sandbox, Secure Execution

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## At a Glance

| Item | Value |
|---|---|
| Cold start | < 90 milliseconds |
| OS targets | Linux, Windows, macOS (Computer-Use desktops) |
| Languages | Python, TypeScript, Ruby, Go, Java |
| Control-plane base URL | `https://app.daytona.io/api` |
| Toolbox base URL | `https://proxy.app.daytona.io/toolbox` |
| Auth | Bearer API key (`Authorization: Bearer <DAYTONA_API_KEY>`) |
| Open-source license | AGPL-3.0 (platform), Apache-2.0 (OpenAPI spec) |
| Free credit | $200 on signup, plus first 5 GiB storage free |
| Billing | Per-second pay-as-you-go (vCPU, memory, storage, GPU) |

## APIs

### Daytona Sandbox API
Create, start, stop, archive, resize, and destroy isolated sandboxes that boot in under 90 milliseconds. Manages the full sandbox lifecycle, labels and metadata, network access, backups, auto-stop / auto-archive policies, and SSH access keys. The legacy `/workspace` namespace is included as an alias of `/sandbox`.

**Human URL:** [https://www.daytona.io/docs/en/tools/api/](https://www.daytona.io/docs/en/tools/api/)

- [OpenAPI](openapi/daytona-sandbox-api-openapi.yml)
- [JSON Schema — Sandbox](json-schema/daytona-sandbox-schema.json)
- [JSON Structure — Sandbox](json-structure/daytona-sandbox-structure.json)
- [Example — Create Sandbox](examples/daytona-sandbox-create-example.json)
- [Example — Sandbox Response](examples/daytona-sandbox-response-example.json)
- [Naftiko Capability — Sandbox Lifecycle](capabilities/sandbox-lifecycle.yaml)
- [Naftiko Capability — Legacy Workspace Control](capabilities/sandbox-control.yaml)

### Daytona Sandbox Toolbox API
The in-sandbox surface for agents: file system, Git, process and PTY execution, Language Server Protocol bridging, computer-use control, an inline interpreter for Python/TypeScript snippets, port and proxy management, and server metadata. Reach it via the platform proxy or directly inside a sandbox.

**Human URL:** [https://www.daytona.io/docs/en/agent-tools/file-system](https://www.daytona.io/docs/en/agent-tools/file-system)

- [OpenAPI — In-Sandbox Toolbox](openapi/daytona-sandbox-toolbox-api-openapi.yml)
- [OpenAPI — Proxied Toolbox](openapi/daytona-toolbox-api-openapi.yml)
- [Example — File System Write](examples/daytona-toolbox-filesystem-write-example.json)
- [Example — Process Execute](examples/daytona-toolbox-process-execute-example.json)
- [Naftiko Capability — File System](capabilities/sandbox-filesystem.yaml)
- [Naftiko Capability — Process Execution](capabilities/sandbox-process-execution.yaml)
- [Naftiko Capability — Git](capabilities/sandbox-git.yaml)
- [Naftiko Capability — Computer Use](capabilities/sandbox-computer-use.yaml)

### Daytona Snapshots API
Capture, list, restore, share, and destroy sandbox snapshots. Snapshots persist sandbox state — file system, processes, environment — so an agent can resume an interrupted workflow or fan out parallel branches from a common base image.

**Human URL:** [https://www.daytona.io/docs/en/snapshots](https://www.daytona.io/docs/en/snapshots)

- [OpenAPI](openapi/daytona-snapshots-api-openapi.yml)
- [JSON Schema — Snapshot](json-schema/daytona-snapshot-schema.json)
- [JSON Structure — Snapshot](json-structure/daytona-snapshot-structure.json)
- [Example — Create Snapshot](examples/daytona-snapshot-create-example.json)
- [Naftiko Capability — Snapshots](capabilities/snapshots.yaml)

### Daytona Volumes API
Create and manage persistent volumes that can be attached to one or more sandboxes for shared, durable storage across the sandbox lifecycle.

**Human URL:** [https://www.daytona.io/docs/en/volumes](https://www.daytona.io/docs/en/volumes)

- [OpenAPI](openapi/daytona-volumes-api-openapi.yml)
- [JSON Schema — Volume](json-schema/daytona-volume-schema.json)
- [JSON Structure — Volume](json-structure/daytona-volume-structure.json)
- [Example — Create Volume](examples/daytona-volume-create-example.json)
- [Naftiko Capability — Volumes](capabilities/volumes.yaml)

### Daytona Preview API
Expose ports running inside a sandbox to the public internet via Daytona's secure preview proxy. Useful for showing a running web app, a Jupyter notebook, an LSP gateway, or any agent-produced HTTP service.

**Human URL:** [https://www.daytona.io/docs/en/preview](https://www.daytona.io/docs/en/preview)

- [OpenAPI](openapi/daytona-preview-api-openapi.yml)
- [Naftiko Capability — Preview](capabilities/preview.yaml)

### Daytona Webhooks API
Configure webhooks so external systems receive callback notifications when sandbox lifecycle events occur (sandbox created/started/stopped/destroyed, snapshot created, etc.).

**Human URL:** [https://www.daytona.io/docs/en/webhooks](https://www.daytona.io/docs/en/webhooks)

- [OpenAPI](openapi/daytona-webhooks-api-openapi.yml)
- [JSON Schema — Webhook](json-schema/daytona-webhook-schema.json)
- [JSON Structure — Webhook](json-structure/daytona-webhook-structure.json)
- [Example — Create Webhook](examples/daytona-webhook-create-example.json)
- [Naftiko Capability — Webhooks](capabilities/webhooks.yaml)

### Daytona Organizations API
Manage organizations, members, roles, invitations, suspensions, and per-organization quotas. The multi-tenant control surface for Daytona Cloud — every sandbox, snapshot, key, and runner belongs to an organization.

**Human URL:** [https://www.daytona.io/docs/en/account-management/organizations](https://www.daytona.io/docs/en/account-management/organizations)

- [OpenAPI](openapi/daytona-organizations-api-openapi.yml)
- [JSON Schema — Organization](json-schema/daytona-organization-schema.json)
- [JSON Structure — Organization](json-structure/daytona-organization-structure.json)
- [Naftiko Capability — Organizations](capabilities/organizations.yaml)

### Daytona API Keys API
Create, list, rotate, and revoke organization-scoped API keys used to authenticate requests against the Daytona platform.

**Human URL:** [https://www.daytona.io/docs/en/account-management/api-keys](https://www.daytona.io/docs/en/account-management/api-keys)

- [OpenAPI](openapi/daytona-api-keys-api-openapi.yml)
- [JSON Schema — API Key](json-schema/daytona-api-key-schema.json)
- [JSON Structure — API Key](json-structure/daytona-api-key-structure.json)
- [Naftiko Capability — API Keys](capabilities/api-keys.yaml)

### Daytona Users API
Manage user profiles, linked accounts (GitHub, GitLab, Bitbucket), and notification preferences. Governs the human side of Daytona — identity, profile, and personal settings — independent of organization-level admin.

**Human URL:** [https://www.daytona.io/docs/en/account-management/linked-accounts](https://www.daytona.io/docs/en/account-management/linked-accounts)

- [OpenAPI](openapi/daytona-users-api-openapi.yml)
- [JSON Schema — User](json-schema/daytona-user-schema.json)
- [JSON Structure — User](json-structure/daytona-user-structure.json)
- [Naftiko Capability — Users](capabilities/users.yaml)

### Daytona Admin API
Platform-level administration covering runners (compute pools), regions, Docker registry configuration, object storage, jobs, audit logs, and global config. Used by operators of customer-managed compute, by self-hosted open-source deployments, and by Daytona staff for managed-service operations.

**Human URL:** [https://www.daytona.io/docs/en/deployments/customer-managed-compute](https://www.daytona.io/docs/en/deployments/customer-managed-compute)

- [OpenAPI](openapi/daytona-admin-api-openapi.yml)
- [Naftiko Capability — Runners](capabilities/admin-runners.yaml)
- [Naftiko Capability — Audit and Config](capabilities/admin-audit.yaml)
- [Naftiko Capability — Docker Registry](capabilities/admin-docker-registry.yaml)

### Daytona Health API
Liveness and readiness probes for the Daytona control plane. Returns 200 when the API is healthy and ready to serve traffic.

**Human URL:** [https://www.daytona.io/docs/en/observability/opentelemetry-collection](https://www.daytona.io/docs/en/observability/opentelemetry-collection)

- [OpenAPI](openapi/daytona-health-api-openapi.yml)

## Common Properties

- [DeveloperPortal — daytona.io](https://www.daytona.io/)
- [Documentation — docs.daytona.io](https://www.daytona.io/docs)
- [GettingStarted](https://www.daytona.io/docs/en/getting-started)
- [Quickstart](https://www.daytona.io/docs/en)
- [APIReference](https://www.daytona.io/docs/en/tools/api/)
- [Console — app.daytona.io](https://app.daytona.io/)
- [SignUp — app.daytona.io](https://app.daytona.io/)
- [Login — app.daytona.io](https://app.daytona.io/)
- [Authentication — API Keys](https://www.daytona.io/docs/en/account-management/api-keys)
- [RateLimits — Limits](https://www.daytona.io/docs/en/account-management/limits)
- [Regions](https://www.daytona.io/docs/en/sandbox/regions)
- [Blog — Dotfiles Insider](https://www.daytona.io/dotfiles)
- [Newsletter — Dotfiles Insider](https://www.daytona.io/dotfiles)
- [YouTube — @daytonaio](https://youtube.com/@daytonaio)
- [Support — Slack Community](https://go.daytona.io/slack)
- [Contact — Talk to Our Team](https://www.daytona.io/contact)
- [StatusPage — status.app.daytona.io](https://status.app.daytona.io/)
- [TrustCenter — trust.daytona.io](https://trust.daytona.io/)
- [TermsOfService](https://www.daytona.io/terms-of-service)
- [PrivacyPolicy](https://www.daytona.io/privacy-policy)
- [Security — Security Exhibit](https://www.daytona.io/docs/en/security/security-exhibit)
- [GitHubOrganization — daytonaio](https://github.com/daytonaio)
- [GitHubRepository — daytonaio/daytona](https://github.com/daytonaio/daytona)
- [X — @daytonaio](https://twitter.com/daytonaio)
- [LinkedIn — daytonaio](https://www.linkedin.com/company/daytonaio/)
- [SDK — Daytona Python SDK](https://pypi.org/project/daytona/)
- [SDK — Daytona TypeScript SDK](https://www.npmjs.com/package/@daytonaio/sdk)
- [SDK — Daytona Ruby SDK](https://rubygems.org/gems/daytona)
- [SDK — Daytona Go SDK](https://pkg.go.dev/github.com/daytonaio/daytona)
- [SDK — Daytona Java SDK](https://central.sonatype.com/artifact/io.daytona/daytona-sdk)
- [CLI — Daytona CLI Docs](https://www.daytona.io/docs/en/tools/cli)
- [CLI — Daytona Homebrew CLI Formula](https://github.com/daytonaio/homebrew-cli)
- [Resources — Daytona Helm Charts](https://github.com/daytonaio/helm-charts)
- [Resources — Daytona Terraform Modules](https://github.com/daytonaio/terraform-modules)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Daytona Sandbox API](openapi/daytona-sandbox-api-openapi.yml)
- [Daytona Sandbox Toolbox API (in-sandbox)](openapi/daytona-sandbox-toolbox-api-openapi.yml)
- [Daytona Toolbox API (proxied)](openapi/daytona-toolbox-api-openapi.yml)
- [Daytona Snapshots API](openapi/daytona-snapshots-api-openapi.yml)
- [Daytona Volumes API](openapi/daytona-volumes-api-openapi.yml)
- [Daytona Preview API](openapi/daytona-preview-api-openapi.yml)
- [Daytona Webhooks API](openapi/daytona-webhooks-api-openapi.yml)
- [Daytona Organizations API](openapi/daytona-organizations-api-openapi.yml)
- [Daytona API Keys API](openapi/daytona-api-keys-api-openapi.yml)
- [Daytona Users API](openapi/daytona-users-api-openapi.yml)
- [Daytona Admin API](openapi/daytona-admin-api-openapi.yml)
- [Daytona Health API](openapi/daytona-health-api-openapi.yml)

### JSON Schema

- [Sandbox](json-schema/daytona-sandbox-schema.json)
- [Snapshot](json-schema/daytona-snapshot-schema.json)
- [Volume](json-schema/daytona-volume-schema.json)
- [Organization](json-schema/daytona-organization-schema.json)
- [User](json-schema/daytona-user-schema.json)
- [API Key](json-schema/daytona-api-key-schema.json)
- [Webhook](json-schema/daytona-webhook-schema.json)

### JSON Structure

- [Sandbox](json-structure/daytona-sandbox-structure.json)
- [Snapshot](json-structure/daytona-snapshot-structure.json)
- [Volume](json-structure/daytona-volume-structure.json)
- [Organization](json-structure/daytona-organization-structure.json)
- [User](json-structure/daytona-user-structure.json)
- [API Key](json-structure/daytona-api-key-structure.json)
- [Webhook](json-structure/daytona-webhook-structure.json)

### JSON-LD

- [Daytona Context](json-ld/daytona-io-context.jsonld)

### Examples

- [Create Sandbox](examples/daytona-sandbox-create-example.json)
- [Sandbox Response](examples/daytona-sandbox-response-example.json)
- [Create Snapshot](examples/daytona-snapshot-create-example.json)
- [Create Volume](examples/daytona-volume-create-example.json)
- [Create Webhook](examples/daytona-webhook-create-example.json)
- [Toolbox — File System Write](examples/daytona-toolbox-filesystem-write-example.json)
- [Toolbox — Process Execute](examples/daytona-toolbox-process-execute-example.json)

### Capabilities (Naftiko)

- [Sandbox Lifecycle](capabilities/sandbox-lifecycle.yaml)
- [Sandbox Legacy Workspace Control](capabilities/sandbox-control.yaml)
- [Sandbox Filesystem](capabilities/sandbox-filesystem.yaml)
- [Sandbox Process Execution](capabilities/sandbox-process-execution.yaml)
- [Sandbox Git](capabilities/sandbox-git.yaml)
- [Sandbox Computer Use](capabilities/sandbox-computer-use.yaml)
- [Snapshots](capabilities/snapshots.yaml)
- [Volumes](capabilities/volumes.yaml)
- [Preview](capabilities/preview.yaml)
- [Webhooks](capabilities/webhooks.yaml)
- [Organizations](capabilities/organizations.yaml)
- [API Keys](capabilities/api-keys.yaml)
- [Users](capabilities/users.yaml)
- [Admin — Runners](capabilities/admin-runners.yaml)
- [Admin — Audit and Config](capabilities/admin-audit.yaml)
- [Admin — Docker Registry](capabilities/admin-docker-registry.yaml)

### Spectral Rules

- [Daytona Spectral Ruleset](rules/daytona-rules.yml)

### Vocabulary

- [Daytona Vocabulary](vocabulary/daytona-io-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/daytona-io-plans-pricing.yml)
- [Rate Limits](rate-limits/daytona-io-rate-limits.yml)
- [FinOps Definition](finops/daytona-io-finops.yml)

## Maintainers

- **Kin Lane** — kin@apievangelist.com — [https://kinlane.com](https://kinlane.com)
