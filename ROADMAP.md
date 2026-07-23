# Roadmap

This document describes the long-term path, organized into phases. Phases are
sequential in emphasis but may overlap in practice. Unlike
[`CURRENT_STATUS.md`](CURRENT_STATUS.md), this file changes slowly — it
describes direction, not day-to-day state.

## Phase 0 — Environment & Foundations

**Goal:** A stable, professional development environment and a repository
structure capable of supporting years of work.

- [x] Windows 11 configured
- [x] WSL configured
- [x] Ubuntu configured
- [x] VS Code configured
- [x] Git configured
- [x] GitHub SSH configured
- [x] GitHub CLI configured
- [x] Claude Code configured
- [x] Starship configured
- [x] `embedded-foundations` repository created
- [x] `career-roadmap` repository created (this repository) — committed
      and synced with `origin/main`

**Status:** Complete.

## Phase 1 — Embedded Foundations

**Goal:** Build a solid, from-first-principles understanding of what happens
between writing C code and running it on hardware — compilation, memory,
linking, and the execution model — before relying on frameworks that hide
these details.

Tracked module-by-module inside `embedded-foundations`. This roadmap tracks
only the top-level sequence; module-level detail belongs in that repository.

- [x] A01 - Compilation Process
- [ ] A02 - Memory Layout *(next)*
- [ ] Further modules — to be defined as A02 completes and the
      `embedded-foundations` curriculum is extended. Not enumerated here in
      advance to avoid inventing structure that doesn't exist yet.

**Status:** In progress.

## Phase 2 — Development Workstation

**Goal:** Consolidate the full embedded development environment (toolchains,
debuggers, board configurations, build systems) into a dedicated,
version-controlled repository: `embedded-workstation`.

- [x] Conduct an initial design review of `embedded-workstation`
- [x] Create the repository and its initial scaffold
- [x] Finish applying the reviewed architecture and get it reviewed/approved
- [x] First commit — initial release committed and pushed; repository is
      public
- [x] Validate the environment end-to-end on a second, clean machine
      (Ubuntu-Learning WSL2, office) — full verification passed with
      PASS: 25, WARN: 0, FAIL: 0
- [x] Automate VS Code Remote-WSL settings and extension installation
- [ ] Migrate/document further toolchain setup used in `embedded-foundations`
      as new needs arise

**Status:** Core goal achieved. `embedded-workstation` is implemented,
public, has shipped its first release, and has been validated end-to-end on
a second, clean machine — see [`MILESTONES.md`](MILESTONES.md) for the
validation record. The repository has moved from active architecture
refinement into maintenance and incremental evolution; the one remaining
item (migrating further toolchain setup) continues as `embedded-foundations`
surfaces real needs, rather than on a fixed schedule.

## Phase 3 and beyond

Not yet defined. This roadmap will be extended phase-by-phase as Phase 1 and
Phase 2 mature and the next direction (e.g. RTOS, specific hardware
platforms, broader software engineering topics) becomes concrete rather than
speculative. Speculative ideas belong in [`BACKLOG.md`](BACKLOG.md), not
here, until they are actually scheduled.

## How this roadmap is maintained

- A phase is marked complete only when every listed item is genuinely done.
- New phases are added only when their goal is concrete enough to state in
  one sentence.
- This file answers "what's the destination and the sequence?" — for "what am
  I doing this week?" see [`TODO.md`](TODO.md).
