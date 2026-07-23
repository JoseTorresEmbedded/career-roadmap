# Current Status

> Last updated: 2026-07-22

This file is a snapshot, not a history. It always reflects *today*. For the
history of how status has changed over time, see [`CHANGELOG.md`](CHANGELOG.md)
and [`MILESTONES.md`](MILESTONES.md).

## Where I am today

The foundational development environment is fully configured, and hands-on
embedded engineering work has begun. The current focus is systems-level
fundamentals — starting with the compilation process and moving into memory
layout — inside the `embedded-foundations` repository. In parallel,
`embedded-workstation` is under architecture refinement following its
initial design review, ahead of its first commit.

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
| `embedded-foundations` | ✔ Created — active, in progress |
| `career-roadmap` | ✔ Created — this repository (initial content drafted, first commit pending) |
| `embedded-workstation` | Architecture refinement in progress |

## Where things stand, by category

### Active work

- **Track:** `embedded-foundations`
- **Completed module:** A01 - Compilation Process
- **Current module:** A02 - Memory Layout (next up)

### Architecture refinement

- **Track:** `embedded-workstation`
- Repository created; initial scaffold completed (structure, docs, scripts,
  `CLAUDE.md`).
- Architecture review completed: modular per-tool configuration, `setup.sh`
  as the single entry point, and a `CLAUDE.md` convention — see
  [`DECISIONS.md`](DECISIONS.md) D006–D009.
- Repository refactoring pending: finishing and verifying the reviewed
  architecture before it is reviewed, approved, and given its first commit.

### Future planned work

- Nothing beyond the above is currently scheduled. Further
  `embedded-workstation` phases (Linux/Windows environment rollout, embedded
  toolchains, debugging, automation) and further `embedded-foundations`
  modules (A03 onward) will be defined only as the work above completes —
  see [`ROADMAP.md`](ROADMAP.md).

## Immediate next action

Begin **A02 - Memory Layout** in `embedded-foundations`. See
[`TODO.md`](TODO.md) for the concrete breakdown.
