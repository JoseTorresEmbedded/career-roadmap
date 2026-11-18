# Backlog

Ideas, topics, and future projects that are real but **not yet scheduled**.
Items move from here into [`ROADMAP.md`](ROADMAP.md) or [`TODO.md`](TODO.md)
once they have a concrete place in the sequence — not before.

This file is allowed to be sparse. An empty category means exactly that:
nothing has been identified yet, not that something was forgotten.

## Future repositories

Nothing queued. `embedded-workstation` has moved out of the backlog and
into [`ROADMAP.md`](ROADMAP.md) Phase 2 — the repository has been created,
publicly released, and validated end-to-end on a clean machine (see
[`MILESTONES.md`](MILESTONES.md) and [`DECISIONS.md`](DECISIONS.md)
D006–D009). Its one remaining task (migrating further toolchain setup used
in `embedded-foundations`) is tracked there, not here.

## Study topics

Nothing queued beyond the current `embedded-foundations` sequence
(see [`ROADMAP.md`](ROADMAP.md)). New topics will be added here as they come
up during study, before being sequenced into the roadmap.

## Tooling & environment

- **SSH agent for the GitHub key** (identified 2026-11-18). The key's
  passphrase is requested on every `git push`/`fetch`. Add an agent (e.g.
  `keychain`) through `embedded-workstation` — package plus bash
  configuration — rather than editing `~/.bashrc` by hand, since that file
  is managed by `embedded-workstation`. Belongs to `ROADMAP.md` Phase 2's
  open item (further toolchain setup as needs arise).

## Process improvements

Nothing pending beyond what is already tracked in
[`IMPROVEMENTS.md`](IMPROVEMENTS.md).

## How to use this file

- Add an idea as soon as it occurs, even half-formed — that's what this file
  is for.
- Review it periodically (e.g. when a roadmap phase completes) and promote
  anything that has become concrete.
- Don't delete an idea just because it's been sitting here a while; delete it
  only if it's no longer actually wanted.
