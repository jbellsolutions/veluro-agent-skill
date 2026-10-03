---
name: veluro-platform-operator
description: Operate and advise on the Veluro AI marketing and lead-generation platform (veluro.ai; often heard as "Velero"). Use when a task mentions Veluro, its Growth Engine, ad campaigns, High-Intent Buyers, Demand Map, Leads CRM, Nurture Campaigns, Creative Studio, pixels, funnels, landing pages, SEO/GEO, LinkedIn prospecting, the Veluro partner/reseller program, or its internal API, or when an agent must run a client's approved growth program inside Veluro through the UI or API.
---

# Veluro platform operator

An agent skill for operating the Veluro platform safely and accurately. It carries a research baseline dated **2026-09-08**: 42 feature runbooks, an agent operating contract, an API guide, and a verification register that says what was tested and what was not.

This is an independent, unofficial reference. It is not published or endorsed by Veluro. The platform changes, so re-check the live UI before relying on any stored detail.

## How to use this skill

Read in this order, loading only what the task needs:

1. [docs/AGENT_INSTRUCTIONS.md](docs/AGENT_INSTRUCTIONS.md) — the operating contract. Read it first, every session.
2. [docs/VERIFICATION.md](docs/VERIFICATION.md) — what is proven, conflicting, blocked or unverified.
3. [docs/runbooks/INDEX.md](docs/runbooks/INDEX.md) — pick the one runbook for the feature in play (for example `docs/runbooks/campaigns.md`, `intent.md`, `growth.md`, `leads.md`).
4. [docs/api/API_GUIDE.md](docs/api/API_GUIDE.md) — only when using the API rather than the UI. Search [docs/api/endpoint-catalog.json](docs/api/endpoint-catalog.json) for the exact call shape.
5. [docs/MANUAL.md](docs/MANUAL.md) — platform architecture, account setup, partner/reseller terms, service boundaries.
6. [docs/MAINTENANCE.md](docs/MAINTENANCE.md) — how to refresh this knowledge when the platform changes.

For one-file ingestion by another agent, use [docs/llms-full.txt](docs/llms-full.txt) (everything) or [docs/llms.txt](docs/llms.txt) (map).

## Non-negotiable rules

- **No spend or send without authorization.** A platform button, an AI recommendation, or a sales demo is not approval. Budgets, audiences, senders, and publishing scope must come from the client's approved record. Never invent a default budget.
- **Confirm identity first.** Verify the logged-in account and the client's business and provider account IDs before any change. Partner staff, recruited resellers, and client workspaces are different relationships.
- **Smallest verified change.** For edits, send the minimal update and compare the full read-back. A name-only campaign update preserved copy in testing; replaying the full create body did not. Do not generalise that to other fields.
- **Respect evidence labels.** *Tested*, *UI observed*, *Source observed*, *Vendor described*, *Unverified / gated*. Never promote a lower label to Tested without running and checking the operation.
- **Treat Business Health numbers as untrusted.** The reviewed account showed revenue and campaign figures with no connected services. No budget or financial action may rely on them until their origin is reconciled.
- **The internal API is not a supported contract.** It was discovered from the shipped web client. Prefer the UI or a vendor-approved interface for production integrations, and keep the catalog as dated research.
- **Never store passwords or session tokens.** Keep audit checkpoints sanitized.
- **Done means independently verified**: provider state, destination, and tracking for ads; delivery events for email; the served page for pages; real counts for imports.

## Known gates (as of 2026-09-08)

Meta one-click ad launch and auto-posting awaited app review; Local Listings was Coming Soon; LinkedIn Compose is manual-send copy; live ads, outbound delivery, account connections, generated media, public publishing, and unattended optimisation were not certified. Re-check each in the live product.

## Keeping it current

Follow [docs/MAINTENANCE.md](docs/MAINTENANCE.md): compare the live product with the runbook, record each change with its evidence level, preserve conflicts rather than overwrite them, and keep the prior version for rollback.
