# Decisions

A record of engineering and career decisions, in the order they were made,
with the reasoning behind them. The goal is to never have to re-litigate a
settled trade-off from memory — if a decision is revisited, it's revisited
against what's written here, not against a vague recollection.

Entries are append-only. If a decision is later reversed, a new entry is
added explaining the reversal — old entries are never deleted or rewritten.

---

## D001 — Separate project management from engineering content

**Date:** 2026-07-22
**Status:** Active

**Decision:** Create `career-roadmap` as a dedicated repository for project
management (status, roadmap, backlog, decisions, milestones), completely
separate from repositories that hold actual engineering work.

**Reasoning:** `embedded-foundations` holds laboratories, source code, and
technical documentation — content about *how things work*. As the number of
engineering repositories grows over the years, mixing planning content
(*what I'm doing, why, and what's next*) into technical repositories would
make both harder to maintain: technical docs would get cluttered with status
updates, and status would be scattered across every repo instead of living
in one place.

---

## D002 — `career-roadmap` is public

**Date:** 2026-07-22
**Status:** Active

**Decision:** The repository is public on GitHub.

**Reasoning:** This was an explicit choice. A public roadmap also doubles as a visible,
dated record of progress and decision-making — useful as a professional
artifact, not just a private planning tool.

---

## D003 — Ecosystem naming convention

**Date:** 2026-07-22
**Status:** Active

**Decision:** Repositories in this ecosystem use descriptive, hyphenated,
lowercase names that state their purpose (`embedded-foundations`,
`career-roadmap`, planned `embedded-workstation`), rather than abbreviations
or personal branding.

**Reasoning:** With a multi-year, multi-repository plan, names need to be
self-explanatory years later without relying on memory of context that made
sense only at creation time.

---

## D004 — Repository structure: flat markdown files over nested wikis or issue trackers

**Date:** 2026-07-22
**Status:** Active

**Decision:** Project management state (status, roadmap, backlog, decisions,
milestones) is tracked as version-controlled markdown files in this
repository, not in GitHub Issues/Projects or an external wiki/PM tool.

**Reasoning:** Markdown files are diffable, greppable, and carry full history
through Git alone, without depending on a third-party tool's data model or
availability. A small, fixed set of top-level files (rather than deeply
nested folders) keeps the structure easy to hold in memory and cheap to
maintain over years. GitHub Issues/Projects remain available later for
finer-grained task tracking if the need arises, without being required now.

---

## D005 — `embedded-workstation` is deferred, not scoped yet

**Date:** 2026-07-22
**Status:** Active

**Decision:** `embedded-workstation` is recorded as a planned future
repository but is not created or scoped yet.

**Reasoning:** Defining its structure now, before enough real toolchain usage
exists from working through `embedded-foundations`, would mean guessing at
requirements instead of documenting an environment that's actually in use.
It is tracked in [`BACKLOG.md`](BACKLOG.md) until there is enough real usage
to scope it accurately.
