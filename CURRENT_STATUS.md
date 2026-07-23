# Current Status

> Last updated: 2026-07-23

This file is a snapshot, not a history. It always reflects *today*. For the
history of how status has changed over time, see [`CHANGELOG.md`](CHANGELOG.md)
and [`MILESTONES.md`](MILESTONES.md).

## Where I am today

**The single active engineering task is to begin A02 - Memory Layout in
`embedded-foundations`.** A01 - Compilation Process is complete; A02 has
not started yet.

Everything else is settled, not active work: `embedded-workstation` is
**complete** — implemented, public, released, and validated — and is now in
maintenance/evolution only, with no engineering work in progress there.
`career-roadmap` (this repository) is **up to date** as of the date above;
its tracking files agree with each other and with the state described here.

## Environment status

| Component | Status |
|---|---|
| Windows 11 | ✔ Configured |
| WSL | ✔ Configured |
| Ubuntu (WSL) | ✔ Configured |
| VS Code | ✔ Configured |
| Git | ✔ Configured |
| GitHub SSH | ✔ Configured |
| GitHub CLI | ✔ Configured |
| Claude Code | ✔ Configured |
| Starship prompt | ✔ Configured |

The environment is stable. No outstanding environment work is planned unless
a new need arises.

## Repository status

| Repository | Status |
|---|---|
| `embedded-foundations` | ✔ Created — active, in progress (only repository with engineering work under way) |
| `career-roadmap` | ✔ Created — this repository, up to date, committed and synced with `origin/main` |
| `embedded-workstation` | ✔ Complete — public, initial release shipped and validated; in maintenance/evolution, no active engineering work |

## Where things stand, by category

### Active work

- **Track:** `embedded-foundations`
- **Completed module:** A01 - Compilation Process
- **Next module:** A02 - Memory Layout (not yet started)

### Maintenance and evolution (no active engineering work)

- **Track:** `embedded-workstation`
- Repository is public; its initial release has been committed and pushed
  to `origin/main`.
- Validated end-to-end on a second, clean Ubuntu-Learning WSL2 distribution
  at the office: full environment verification passed with PASS: 25,
  WARN: 0, FAIL: 0, covering Git, SSH, GitHub CLI, Claude Code, GCC, GDB,
  Make, CMake, Python, Starship, shell utilities, and VS Code.
- VS Code extensions were installed on the validated machine, and
  Remote-WSL settings are now managed by `embedded-workstation`.
- Validation surfaced and fixed five issues in `embedded-workstation`
  itself (a `setup.sh` abort after initial verification, an unsafe `sed`
  expression in managed-block replacement, non-transactional config
  application, missing regression tests, and unautomated VS Code remote
  settings) — see [`MILESTONES.md`](MILESTONES.md) and that repository's
  own `CHANGELOG.md` for detail.
- All three repositories in the ecosystem (`career-roadmap`,
  `embedded-foundations`, `embedded-workstation`) are cloned, clean,
  synchronized with `origin/main`, and contain their own `CLAUDE.md`.

### Future planned work

- Nothing beyond the above is currently scheduled. Further
  `embedded-workstation` evolution (further toolchain migration as
  `embedded-foundations` needs arise) and further `embedded-foundations`
  modules (A03 onward) will be defined only as the work above completes —
  see [`ROADMAP.md`](ROADMAP.md).

## Immediate next action

Begin **A02 - Memory Layout** in `embedded-foundations`. See
[`TODO.md`](TODO.md) for the concrete breakdown.
