# Current Status

> Last updated: 2026-11-18

This file is a snapshot, not a history. It always reflects *today*. For the
history of how status has changed over time, see [`CHANGELOG.md`](CHANGELOG.md)
and [`MILESTONES.md`](MILESTONES.md).

## Where I am today

**The single active engineering task is to begin A03 - Stack in
`embedded-foundations`.** A01 - Compilation Process and A02 - Memory Layout
are complete; A03 has not started yet.

Between A01 and A02, a build-system laboratory (Make, then an introduction
to CMake) was completed on A01's example code — see
[`MILESTONES.md`](MILESTONES.md) and [`DECISIONS.md`](DECISIONS.md) D010.

`embedded-workstation` remains in maintenance/evolution, with one newly
identified need (an SSH agent, see [`BACKLOG.md`](BACKLOG.md)) and no
engineering work in progress there.

## Environment status

| Component | Status |
|---|---|
| Windows 11 | ✔ Configured |
| WSL | ✔ Configured |
| Ubuntu (WSL) | ✔ Configured |
| VS Code | ✔ Configured |
| Git | ✔ Configured |
| GitHub SSH | ✔ Configured — the key's passphrase is requested on every push (no SSH agent yet) |
| GitHub CLI | ✔ Configured |
| Claude Code | ✔ Configured |
| Starship prompt | ✔ Configured |

The environment is stable. The only open environment item is the SSH agent
listed in [`BACKLOG.md`](BACKLOG.md).

## Repository status

| Repository | Status |
|---|---|
| `embedded-foundations` | ✔ Active — A01 and A02 complete, A03 next; `main` synced with `origin/main` after PR #3 |
| `career-roadmap` | ✔ This repository — tracking files updated as of the date above |
| `embedded-workstation` | ✔ Complete — public, initial release shipped and validated; in maintenance/evolution, no active engineering work |

## Where things stand, by category

### Active work

- **Track:** `embedded-foundations`
- **Completed modules:** A01 - Compilation Process, A02 - Memory Layout
- **Completed side laboratory:** build systems (Make, introduction to CMake),
  on A01's example code
- **Next module:** A03 - Stack (not yet started)
- **Workflow:** each laboratory is developed on its own branch and integrated
  into `main` through a self-reviewed pull request (PRs #1–#3 so far) — see
  [`IMPROVEMENTS.md`](IMPROVEMENTS.md).

### Maintenance and evolution (no active engineering work)

- **Track:** `embedded-workstation`
- Repository is public; its initial release has been committed and pushed
  to `origin/main`.
- Validated end-to-end on a second, clean Ubuntu-Learning WSL2 distribution
  at the office: full environment verification passed with PASS: 25,
  WARN: 0, FAIL: 0 — see [`MILESTONES.md`](MILESTONES.md) and that
  repository's own `CHANGELOG.md` for detail.
- Newly identified need: an SSH agent (e.g. `keychain`) so the GitHub key's
  passphrase is not requested on every push. Not yet scheduled — see
  [`BACKLOG.md`](BACKLOG.md).

### Future planned work

- Further `embedded-foundations` modules (A03 onward) follow the module
  list in that repository's `README.md` — see [`ROADMAP.md`](ROADMAP.md).

## Immediate next action

Begin **A03 - Stack** in `embedded-foundations`. See [`TODO.md`](TODO.md)
for the concrete breakdown.
