# Improvements

A log of identified improvements to *how I work* — process, tooling, and
workflow — as distinct from *what I know* (which lives in the technical
repositories) and *what I've decided* (`DECISIONS.md`).

Each entry describes a friction point or opportunity, and what changed (or
should change) in response. Entries are kept even after being acted on, so
this file also serves as a record of process evolution.

## Format

Each entry: **Identified** (date), a short description of the problem or
opportunity, and the resulting change (or planned change).

---

## Update project status at the moment work completes, not in batches

**Identified:** 2026-07-22

Status tracking tends to fail not because tools are missing, but because
updates get deferred and then forgotten. The plan going forward: the moment
a module (e.g. `embedded-foundations` A01, A02, ...) is completed,
`CURRENT_STATUS.md`, `TODO.md`, and `MILESTONES.md` in this repository get
updated in the same sitting — not batched for "later."

**Change:** Adopted as a standing habit starting with this repository's
creation. Its effectiveness will be visible in whether `CURRENT_STATUS.md`
stays accurate over time.

---

## Use Claude Code as the maintenance mechanism for this repository

**Identified:** 2026-07-22

A project-management repository is only useful if it's actually kept
current, and manual upkeep is exactly the kind of task that quietly gets
skipped. Using Claude Code as an active collaborator for maintaining this
repository (updating status, drafting milestone/decision entries, keeping
the roadmap honest) lowers the friction enough to make continuous upkeep
realistic.

**Change:** This repository was created and structured with Claude Code
acting as engineering project manager. Future updates to it are expected to
follow the same pattern.

---

## Conduct a design review before scaffolding a new repository

**Identified:** 2026-07-22

While working out the structure for `embedded-workstation`, it became clear
that settling on structure only after starting to create files risks
locking in choices that don't hold up as the repository grows — a flat
`config/` directory, for instance, works fine for a handful of files but
becomes hard to navigate once several tools' configurations are mixed
together in it.

**Change:** Adopted a standing practice of conducting an explicit design
review — covering structure, entry points, and conventions — before
scaffolding any new repository, rather than starting from file creation.
`embedded-workstation` is the first repository this was applied to; see
`DECISIONS.md` D006–D008.

---

## Give every repository its own `CLAUDE.md` instead of relying on session memory

**Identified:** 2026-07-22

The `embedded-workstation` design review made it clear that
repository-specific context — conventions, structure, constraints — was
otherwise left for Claude Code to reconstruct from scratch each session, or
for the user to repeat manually. That doesn't scale as more repositories
come online.

**Change:** Every repository in the ecosystem will include a root-level
`CLAUDE.md` documenting its own conventions and structure, so that context
is durable and co-located with the repository it describes. See
`DECISIONS.md` D009.
