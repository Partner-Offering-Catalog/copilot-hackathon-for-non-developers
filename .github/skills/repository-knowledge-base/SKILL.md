---
name: repository-knowledge-base
description: Creates or updates verified repository documentation for setup, usage, navigation, maintenance, deployment, operations, and organizational handover.
---

# Repository knowledge base

Build a concise, repository-owned source of truth that enables a new team to
set up, operate, maintain, deploy, secure, and govern the application without
depending on Copilot session history.

## Discover before documenting

Inspect the repository's README, manifests, lockfiles, scripts, CI workflows,
deployment definitions, configuration examples, architecture, tests, and
existing documentation. Use repository evidence as the source of truth. Ask
maintainers about ownership, environments, access, recovery, and operational
details that cannot be inferred.

Never invent commands, URLs, credentials, support commitments, or deployment
steps. Mark unresolved information as `TODO` with an owner or question. Use
placeholders for secrets and explain where they are configured securely.

## Required coverage

Adapt the structure to the project while covering:

- purpose, audience, capabilities, and system context;
- prerequisites and a verified local setup;
- configuration and secret names without secret values;
- common usage and supported workflows;
- repository map and important entry points;
- architecture, data flows, integrations, and major decisions;
- tests, quality checks, and troubleshooting;
- routine dependency, data, and operational maintenance;
- build, release, deployment, rollback, and environment promotion;
- monitoring, alerts, backup, recovery, and incident entry points;
- security, privacy, accessibility, compliance, and known risks;
- ownership, support boundaries, change process, and onboarding; and
- a handover-readiness checklist with explicit gaps.

Prefer a short README entry point linked to focused documents under the
repository's established documentation directory. Preserve useful existing
documentation and avoid duplicating facts across files.

## Validate and hand over

Run every safe setup, validation, and documentation command that the current
environment supports. Distinguish commands personally verified from those that
require organizational infrastructure. Check internal links and ensure no
generated documentation contains secrets or environment-specific credentials.

Summarize files changed, evidence used, commands verified, assumptions, and
open handover gaps. Ask the intended maintainers to review ownership,
deployment, recovery, and compliance details before declaring the knowledge
base ready.
