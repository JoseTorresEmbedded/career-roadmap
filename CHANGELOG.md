# Changelog

A dated log of changes to **this repository** — its structure and content,
not the engineering journey it tracks. For achievements in the journey
itself, see [`MILESTONES.md`](MILESTONES.md).

Format loosely follows [Keep a Changelog](https://keepachangelog.com/):
newest entry first, grouped by date.

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
