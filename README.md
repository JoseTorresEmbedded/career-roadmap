# Career Roadmap

This repository is the project management center for my long-term journey as a
Software Engineer. It contains no source code, no tutorials, and no technical
documentation — those live in dedicated repositories. What lives here is the
planning layer that ties every other repository together: where I am, what
I'm working on, what's next, and why past decisions were made the way they
were.

Think of this repo as the control room. The other repositories are the
workshops.

## Why this repository exists

Learning software and embedded engineering seriously, over years rather than
weeks, requires more than a queue of tutorials. It requires:

- A single place to answer "what am I doing right now, and why?"
- A durable record of decisions, so I don't re-litigate the same trade-offs.
- A visible backlog, so ideas aren't lost between sessions.
- A milestone log, so progress is provable, not just remembered.

This repository is that place. It is meant to be read, updated, and pruned
continuously — not written once and abandoned.

## How to navigate this repository

| File | Purpose |
|---|---|
| [`CURRENT_STATUS.md`](CURRENT_STATUS.md) | A snapshot of exactly where things stand right now. The first file to read. |
| [`ROADMAP.md`](ROADMAP.md) | The long-term path: phases, sequencing, and destination. |
| [`TODO.md`](TODO.md) | Short-horizon, actionable tasks — the next few sessions of work. |
| [`BACKLOG.md`](BACKLOG.md) | Ideas, topics, and projects not yet scheduled. |
| [`MILESTONES.md`](MILESTONES.md) | Completed, dated achievements. The proof-of-progress log. |
| [`IMPROVEMENTS.md`](IMPROVEMENTS.md) | Process, tooling, and workflow improvements — how I work, not what I know. |
| [`DECISIONS.md`](DECISIONS.md) | Engineering and career decisions, with reasoning, in the order they were made. |
| [`CHANGELOG.md`](CHANGELOG.md) | A dated log of changes to this repository itself. |
| [`docs/repositories.md`](docs/repositories.md) | The map of every repository in the ecosystem and how it relates to this one. |
| [`CLAUDE.md`](CLAUDE.md) | Permanent operating rules for AI agents working in this repository — behavior policy, not repository content. |

## Suggested reading order

1. `CURRENT_STATUS.md` — where am I today?
2. `ROADMAP.md` — where is this all going?
3. `TODO.md` — what's next, concretely?
4. Everything else, as needed.

## Repository ecosystem

`career-roadmap` is the hub. It links out to, but never duplicates the
content of, the repositories where actual engineering work happens. See
[`docs/repositories.md`](docs/repositories.md) for the full map.

## Maintenance principles

- **No placeholder content.** If a section has nothing real to say yet, it is
  left explicitly marked as empty, not filled with filler.
- **No invented history.** Milestones and decisions are only recorded once
  they have actually happened.
- **Update in place.** `CURRENT_STATUS.md` reflects *today*, not last month.
  Stale status is worse than no status.
- **Small, frequent edits.** This repository is meant to be touched often —
  after every study session, not once a quarter.

## AI Assistant

This repository contains a repository-level [`CLAUDE.md`](CLAUDE.md) file
defining the permanent operating rules for AI agents (such as Claude Code)
working in this repository.

- `CLAUDE.md` is part of this repository's architecture, alongside the
  tracking files listed above — it is not incidental or optional context.
- It defines AI *behavior* — role, working rules, and boundaries — not
  repository *content*. For what this repository contains, see the table
  above and [`docs/repositories.md`](docs/repositories.md).
- It is expected to remain synchronized with this repository's mission,
  standards, and working methodology as they evolve. A change to how this
  repository is meant to be maintained is not complete until `CLAUDE.md`
  reflects it.
