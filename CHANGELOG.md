# Changelog

A dated log of changes to **this repository** — its structure and content,
not the engineering journey it tracks. For achievements in the journey
itself, see [`MILESTONES.md`](MILESTONES.md).

Format loosely follows [Keep a Changelog](https://keepachangelog.com/):
newest entry first, grouped by date.

## 2026-11-18

### Added

- `MILESTONES.md`: entries for 2026-11-17 (Make laboratory, PR #1) and
  2026-11-18 (introduction to CMake, PR #2; A02 - Memory Layout, PR #3;
  `-Wcast-qual` in all laboratory builds; correction of A01's
  documentation).
- `DECISIONS.md`: D010 (build-system laboratory before finishing A02), D011
  (A02/A05 scope split), D012 (`-Wcast-qual` as a standard laboratory
  flag).
- `IMPROVEMENTS.md`: branch-and-PR workflow for laboratories, the four-month
  status-tracking lapse, and one-step-one-question guided laboratories.
- `BACKLOG.md`: SSH agent for the GitHub key, to be added through
  `embedded-workstation`.

### Changed

- `CURRENT_STATUS.md`: A01 and A02 complete, A03 - Stack is the active
  task; GitHub SSH row notes the passphrase prompt; removed the claim that
  all three repositories were clean and synchronized, which no longer
  applied.
- `ROADMAP.md` Phase 1: build-system laboratory and A02 checked, A03 marked
  as next; the remaining module list now points to `embedded-foundations`'
  `README.md`, which owns it.
- `TODO.md`: next task is A03; added a review of A02's personal
  documentation sections.

## 2026-07-23

### Added

- Recorded `embedded-workstation`'s initial release and its first
  successful clean-machine validation (Ubuntu-Learning WSL2, office;
  PASS: 25, WARN: 0, FAIL: 0) in `MILESTONES.md`.

### Changed

- Updated `CURRENT_STATUS.md`, `ROADMAP.md` Phase 2, `BACKLOG.md`, and
  `docs/repositories.md` to reflect that `embedded-workstation` is
  implemented, public, has shipped its first release, and has been
  validated on a clean machine — moving it from "under architecture
  refinement" into maintenance and evolution.
- Reviewed `TODO.md`'s immediate next task (starting A02 - Memory Layout)
  against the confirmed A02 status; already accurate, no change needed.

### Fixed

- Corrected stale wording in `CURRENT_STATUS.md`, `ROADMAP.md` Phase 0,
  `BACKLOG.md`, and `docs/repositories.md` that still described
  `career-roadmap` itself as awaiting its first commit. `origin/main`
  already carries three commits for this repository, so "first commit
  pending" was inaccurate and has been corrected to reflect that this
  repository is already committed and synced.

## 2026-07-22

### Added

- Initial repository structure: `README.md`, `ROADMAP.md`,
  `CURRENT_STATUS.md`, `TODO.md`, `BACKLOG.md`, `MILESTONES.md`,
  `DECISIONS.md`, `IMPROVEMENTS.md`, and `docs/repositories.md`.
- Recorded the current state of the engineering environment and the
  `embedded-foundations` progress (A01 complete, A02 next) as the repository's
  starting baseline.
- Logged the first career-related engineering decisions in `DECISIONS.md`
  (repository split, structure choices).
- Recorded the outcome of `embedded-workstation`'s initial design review in
  `DECISIONS.md` (D006–D009): scoping resumes, per-tool configuration
  directories (`bash/`, `git/`, `starship/`, `vscode/`) over a flat
  `config/`, `setup.sh` as the primary installation entry point in place of
  `bootstrap.sh`, and a `CLAUDE.md` convention for every repository in the
  ecosystem.
- Logged two process improvements identified during that review in
  `IMPROVEMENTS.md`: reviewing architecture before scaffolding a new
  repository, and giving every repository its own `CLAUDE.md`.
- Added `CLAUDE.md`, defining the permanent operating rules for AI agents
  working in this repository.

### Changed

- Updated `ROADMAP.md` Phase 2 to reflect that `embedded-workstation` is now
  under architecture refinement following its initial design review, rather
  than not yet started.
- Brought `BACKLOG.md` and `docs/repositories.md` into alignment with
  D006–D009: removed "deferred"/"planned" language for
  `embedded-workstation`, described it as under architecture refinement,
  and clarified each repository's responsibilities in
  `docs/repositories.md`.
- Updated `CURRENT_STATUS.md`: the repository status table and a new
  "Where things stand, by category" section now reflect that
  `embedded-workstation` has been created with an initial scaffold and is
  under architecture refinement, replacing the earlier "Planned — not yet
  created."
- Corrected `ROADMAP.md`, `DECISIONS.md` (D006), `docs/repositories.md`, and
  `BACKLOG.md`, which still stated the `embedded-workstation` repository
  "has not been created yet" — now aligned with the fact that it exists
  locally with an initial scaffold, pending review and its first commit.
- Updated `README.md` with a new "AI Assistant" section and a file-overview
  entry for `CLAUDE.md`, integrating it into the repository's documented
  structure.
