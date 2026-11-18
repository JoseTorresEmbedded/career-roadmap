# Milestones

A dated log of things that are genuinely **done**. This is the proof-of-progress
record — entries are only added once an achievement is real, never in
advance.

> **Note on dates:** This repository was created on 2026-07-22. Milestones
> achieved before that date are logged retroactively with that same date,
> since no earlier tracking system existed to record the exact original
> date. Every milestone from this point forward will carry its true
> completion date.

## 2026-07-22

- **Development environment fully configured.** Windows 11, WSL, Ubuntu,
  VS Code, Git, GitHub SSH, GitHub CLI, Claude Code, and Starship are all
  set up and working together as a stable daily-driver environment.
- **`embedded-foundations` repository created.** The first engineering
  repository — laboratories, source code, and technical documentation for
  hands-on embedded learning.
- **A01 - Compilation Process completed**, in `embedded-foundations`. First
  completed learning module of the embedded track.
- **`career-roadmap` repository created.** Created on GitHub and cloned
  locally as the project management center tying the engineering journey
  together. Initial content is drafted; the first commit is still pending
  as of this date.

## 2026-07-23

- **`embedded-workstation` initial release shipped.** The repository is
  public on GitHub, and its first release has been committed and pushed to
  `origin/main`.
- **`embedded-workstation` validated end-to-end on a second, clean
  machine.** Verified from a clean Ubuntu-Learning WSL2 distribution at the
  office: full environment verification passed with PASS: 25, WARN: 0,
  FAIL: 0, covering Git, SSH, GitHub CLI, Claude Code, GCC, GDB, Make,
  CMake, Python, Starship, shell utilities, and VS Code (including
  Remote-WSL settings and extensions, now managed by `embedded-workstation`).
  Validation surfaced and fixed five issues in `embedded-workstation` itself
  (a `setup.sh` abort after initial verification, an unsafe `sed` expression
  in managed-block replacement, non-transactional config application,
  missing regression tests, and unautomated VS Code remote settings) — see
  that repository's own `CHANGELOG.md` for implementation detail.

## 2026-11-17

- **Make laboratory completed**, in `embedded-foundations` (PR #1). A01's
  hand-written Makefile evolved step by step into a generic one: pattern
  rules and automatic variables, automatic header dependencies
  (`-MMD -MP`), out-of-tree builds in `build/`, validated `debug`/`release`
  modes in separate directories, and a guarded `clean`. First laboratory
  integrated through a self-reviewed pull request.

## 2026-11-18

- **Introduction to CMake completed**, in `embedded-foundations` (PR #2).
  `CMakeLists.txt` for A01 with a static `math` library, strict C11 (no GNU
  extensions), warnings on both targets, and per-configuration build
  directories; `PRIVATE`/`PUBLIC` propagation verified in the generated
  build.
- **A02 - Memory Layout completed**, in `embedded-foundations` (PR #3),
  with its documentation (`docs/A02_MemoryLayout.md`): eight experiments
  with binary evidence (`nm`, `objdump`, `/proc/self/maps`) covering
  section placement, linkage, optimization effects, `_FORTIFY_SOURCE`,
  ASLR/PIE load base, and writes to `const` data.
- **`-Wcast-qual` added to every laboratory build** (Makefiles and
  `CMakeLists.txt`); it immediately caught a `const`-discarding cast in
  A02.
- **Corrected an unverified claim in A01's documentation**: with GCC 11.4,
  an uninitialized global is reported by `nm` as `B`, not `C` (common
  symbols require `-fcommon`).

## How entries are added

- One entry per milestone, under the date it was actually completed.
- A milestone is something *finished*, not something started — starting a
  module belongs in `TODO.md`, not here.
- Entries are never removed, only added, so this file is an append-only
  record of progress over years.
