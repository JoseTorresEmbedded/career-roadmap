# Repository Ecosystem

`career-roadmap` is the hub. It never duplicates the content of other
repositories — it links to them and tracks status *about* them. This file is
the map of everything in the ecosystem and how the pieces relate.

## Map

| Repository | Purpose | Contains | Status |
|---|---|---|---|
| [`career-roadmap`](https://github.com/JoseTorresEmbedded/career-roadmap) | Project management hub | Roadmap, status, backlog, decisions, milestones | Active (this repository) — initial commit pending |
| [`embedded-foundations`](https://github.com/JoseTorresEmbedded/embedded-foundations) | Embedded systems learning track | Laboratories, source code, technical documentation, experiments | Active — see `CURRENT_STATUS.md` for current module |
| `embedded-workstation` | Complete embedded development environment | Toolchains, debug tooling, board configs, build systems | Planned — see `BACKLOG.md` |

## Relationship between repositories

- **`career-roadmap`** answers *where am I, what's next, and why* — for the
  whole engineering journey, across every repository.
- **`embedded-foundations`** (and future technical repositories) answer
  *how does this work* — the actual engineering content: code, labs, and
  documentation for a specific subject area.
- **`embedded-workstation`** (planned) will answer *what does my environment
  look like* — the reusable development setup, separate from any one
  learning track.

The rule of thumb: if content explains or implements engineering work, it
belongs in a technical repository. If content is about tracking, planning,
or deciding, it belongs here.

## Adding a new repository to the ecosystem

When a new repository is created:

1. Add a row to the table above.
2. Add an entry to [`CHANGELOG.md`](../CHANGELOG.md).
3. If it fulfills a `BACKLOG.md` or `ROADMAP.md` item, update those files
   and, if appropriate, log a milestone.
