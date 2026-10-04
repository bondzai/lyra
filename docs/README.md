# Lyra documentation

Grouped by whether a document describes something that **runs**, something that was **intended**,
or something that is **history**. The distinction matters here: several files in this directory
spent months describing a product that no longer existed, and the only reliable way to stop that
happening again is to say, on the index, which kind each one is.

**New here — including if you are an AI agent picking this up:** start with
[`CLAUDE.md`](../CLAUDE.md) in the repo root. It is the orientation the code cannot give you: the
invariants, the mistakes already made here, what the gate is, and what "done" means. This index tells
you where things are documented; that file tells you what will bite you.

## Where things are

Four folders, by the question you are asking.

| If you want to know | Look in |
|---|---|
| how it is built | [`architecture/`](./architecture/) |
| what it does | [`features/`](./features/) |
| how to run, deploy or move it | [`operations/`](./operations/) |
| why it was ever meant to look like this | [`intent/`](./intent/) — **older than the code** |

## How it is built

| Document | Description |
|---|---|
| [Architecture](./architecture/architecture.md) | The real topology, the four ways into Lyra's data, and where inference happens |
| [API server](./architecture/api-server.md) | The Rust API — stack, route groups, auth, and the two hazards |
| [Core engine](./architecture/core-engine.md) | Entity, Tracker, Schedule and Relation — and why `schedules` is not the job queue |
| [Jobs](./architecture/jobs.md) | The queue: lanes, leases, idempotency, backoff, the dead letter, and how to add a kind |
| [Modules](./architecture/modules.md) | The sidebar, the Projects type, and the DeFi page rewrite |

## What it does

| Document | Description |
|---|---|
| [Notifications](./features/notifications.md) | Groups, routing, channels, schedules, and the sealed webhook credential — how anything reaches your phone |
| [Systems](./features/systems.md) | Lyra as chief of staff: the other systems it speaks for, the decision inbox, and the hub |
| [Second brain](./features/second-brain.md) | One index over your notes and markdown files, FTS5 search, backlinks, and why not embeddings first |
| [Alerts](./features/alerts.md) | `lyra-alerts`: rules, digests, the Telegram and Discord channels, and their containment |
| [Telegram](./features/telegram.md) | The command bot — the assistant's front door: money, life and queue commands |
| [MCP](./features/mcp.md) | The research desk: the read-only invariant, and the three things called "MCP" here |
| [Workspaces](./features/workspaces.md) | Context you author per area of life — where it lives, how it is assembled, and what it is for |

## Running it

| Document | Description |
|---|---|
| [Setup](./operations/setup.md) | Getting it running on a development machine |
| [Deployment](./operations/deployment.md) | The mini PC — the one binary, the systemd unit, the CI pipeline that feeds it, moving the database, backups |
| [Handoff to the mini PC](./operations/handoff-to-the-mini-pc.md) | The one-time cutover: merge, move the database, stop the Mac, start the box — in that order |
| [Parity harness](./operations/parity.md) | Gating the Rust port against the Python oracle |

## What happens next

| Document | Description |
|---|---|
| [Assistant roadmap](./assistant-roadmap.md) | The plan, its decisions, and what each is blocked on |

## Why it looks like this

[`intent/`](./intent/) holds the documents written **before** the code — the vision, the assistant's
intended voice, the earlier design specifications. They are useful for *why* and are
[never to be cited for *what is*](./intent/README.md).
