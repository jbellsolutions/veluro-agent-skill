# Veluro Agent Skill

An installable agent skill plus a full operating knowledge base for the **Veluro** AI marketing and lead-generation platform (veluro.ai).

> **Spelling note:** the product is **Veluro**. It is often heard or transcribed as "Velero", "Veloro" or "Valuro".
>
> **Unofficial.** This is an independent research reference. It is not published, endorsed or supported by Veluro, and "Veluro" is the property of its owner. Platform behaviour changes; re-check the live product before relying on any detail here.

## What you get

| | |
|---|---|
| **A skill** | [SKILL.md](SKILL.md) — a drop-in skill for Claude Code, Codex and other agents that read `SKILL.md`. It triggers on Veluro tasks and routes the agent to the right document. |
| **An operating contract** | [docs/AGENT_INSTRUCTIONS.md](docs/AGENT_INSTRUCTIONS.md) — the rules an agent follows: client record, session start, UI vs API, spend and send authorisation, checkpoints, completion standard. |
| **42 feature runbooks** | [docs/runbooks/](docs/runbooks/INDEX.md) — when to use each module, prerequisites, observed fields and controls, success checks, recovery. |
| **An API reference** | [docs/api/](docs/api/API_GUIDE.md) — auth, tested campaign operations, 662 source-observed call templates, a 28-path OpenAPI subset, model and service catalogs. |
| **A verification register** | [docs/VERIFICATION.md](docs/VERIFICATION.md) — what was tested, what was only observed, what is blocked. |
| **A searchable reader** | [docs/index.html](docs/index.html) — open locally in a browser; searches runbooks and individual API calls. |
| **Agent ingestion files** | [docs/llms.txt](docs/llms.txt) (map) and [docs/llms-full.txt](docs/llms-full.txt) (everything in one file). |

Research date: **2026-09-08**.

## Install as a skill

**Claude Code**

```bash
git clone https://github.com/jbellsolutions/veluro-agent-skill ~/.claude/skills/veluro-platform-operator
```

**Codex**

```bash
git clone https://github.com/jbellsolutions/veluro-agent-skill ~/.codex/skills/veluro-platform-operator
```

The folder name should match the skill name in the `SKILL.md` frontmatter (`veluro-platform-operator`). Update later with `git pull` inside that folder. For agents without skill support, point them at `docs/llms-full.txt`.

## Repository map

```
SKILL.md                  skill entry point (frontmatter + routing + hard rules)
README.md                 this file
LICENSE                   MIT, plus a note on the Veluro name
docs/
  README.md               original knowledge-base overview and key findings
  AGENT_INSTRUCTIONS.md   operating contract for an agent
  MANUAL.md               architecture, account setup, partner/reseller terms, limits
  VERIFICATION.md         proven / conflicting / blocked / unverified
  MAINTENANCE.md          how to keep the knowledge current
  DEMO_FINDINGS.md        what the demo call showed vs. the live product
  EVIDENCE_INDEX.md       what evidence was gathered and how it is packaged
  runbooks/               one file per module (INDEX.md lists all 42)
  api/                    API guide, endpoint/model/service catalogs, OpenAPI subset
  index.html              searchable offline reader
  llms.txt, llms-full.txt agent-friendly entry points
  downloads/              the docs as a single zip
  module-registry.json, coverage-summary.json
```

## Evidence labels

Every claim carries one of these. Do not treat a lower level as a higher one.

- **Tested** — executed and checked in the reviewed account.
- **UI observed** — a screen or control was inspected; its final effect may not have been exercised.
- **Source observed** — present in the shipped browser code; not a backend guarantee.
- **Vendor described** — stated in built-in help or the demo.
- **Unverified / gated** — production behaviour could not be established.

Runbooks cite source files under an `evidence/` path. Those raw research captures (account-specific responses, the meeting transcript) are **not** part of this repository by design; the citations are provenance only.

## Important caveats

- The "API" documented here is the app's **internal** API, discovered from the shipped web client. No published, versioned developer contract was found. Treat it as dated research, not a compatibility promise, and prefer a vendor-approved interface for production integrations.
- Live advertising, outbound delivery, account connections, generated media, public publishing and unattended optimisation were **not** certified in this baseline.
- Credentials and session tokens are excluded. Account-specific record identifiers were replaced with placeholders.

## Contributing / updating

Follow [docs/MAINTENANCE.md](docs/MAINTENANCE.md): compare the live product with the runbook, record each change with its evidence level, preserve conflicts, and keep the previous version for rollback.

## License

[MIT](LICENSE) for the documentation and skill text in this repository. This does not grant any rights in Veluro's name, software or marks.
