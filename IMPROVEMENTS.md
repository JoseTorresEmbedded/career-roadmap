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

---

## Develop each laboratory on a branch and integrate it through a self-reviewed PR

**Identified:** 2026-11-17

Until now, laboratory work was committed straight to `main`, with no review
step and no record of how a piece of work evolved.

**Change:** Each laboratory in `embedded-foundations` now lives on its own
branch (`lab/<module>-<topic>`), with one commit per step, and is integrated
into `main` through a pull request that is reviewed in "Files changed"
before merging. Merges use `--merge` (not squash) to preserve the
step-by-step history. Applied to PRs #1–#3. It also practices the review
workflow used in professional teams.

---

## Status tracking lapsed for four months

**Identified:** 2026-11-18

The standing habit of updating status the moment work completes (see the
first entry in this file) did not hold: between 2026-07-23 and 2026-11-17
there was no tracked engineering activity, and `CURRENT_STATUS.md` kept
describing A02 as "not started" throughout.

**Change:** Status was brought up to date on 2026-11-18 in the same sitting
as A02's completion. No new mechanism adopted yet; whether the original
habit holds from here is the thing to watch.

---

## Guided laboratories: one step and one question at a time

**Identified:** 2026-11-17

During the Make laboratory, receiving several sub-steps and three to five
questions per message made it hard to answer them; outputs were being
pasted without the explanations.

**Change:** Guided laboratory sessions with Claude Code now present one
small step and one question per message, and move on only after the
answer.
