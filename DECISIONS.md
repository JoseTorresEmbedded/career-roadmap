# Decisions

A record of engineering and career decisions, in the order they were made,
with the reasoning behind them. The goal is to never have to re-litigate a
settled trade-off from memory — if a decision is revisited, it's revisited
against what's written here, not against a vague recollection.

Entries are append-only. If a decision is later reversed, a new entry is
added explaining the reversal — old entries are never deleted or rewritten.

---

## D001 — Separate project management from engineering content

**Date:** 2026-07-22
**Status:** Active

**Decision:** Create `career-roadmap` as a dedicated repository for project
management (status, roadmap, backlog, decisions, milestones), completely
separate from repositories that hold actual engineering work.

**Reasoning:** `embedded-foundations` holds laboratories, source code, and
technical documentation — content about *how things work*. As the number of
engineering repositories grows over the years, mixing planning content
(*what I'm doing, why, and what's next*) into technical repositories would
make both harder to maintain: technical docs would get cluttered with status
updates, and status would be scattered across every repo instead of living
in one place.

---

## D002 — `career-roadmap` is public

**Date:** 2026-07-22
**Status:** Active

**Decision:** The repository is public on GitHub.

**Reasoning:** This was an explicit choice. A public roadmap also doubles as a visible,
dated record of progress and decision-making — useful as a professional
artifact, not just a private planning tool.

---

## D003 — Ecosystem naming convention

**Date:** 2026-07-22
**Status:** Active

**Decision:** Repositories in this ecosystem use descriptive, hyphenated,
lowercase names that state their purpose (`embedded-foundations`,
`career-roadmap`, planned `embedded-workstation`), rather than abbreviations
or personal branding.

**Reasoning:** With a multi-year, multi-repository plan, names need to be
self-explanatory years later without relying on memory of context that made
sense only at creation time.

---

## D004 — Repository structure: flat markdown files over nested wikis or issue trackers

**Date:** 2026-07-22
**Status:** Active

**Decision:** Project management state (status, roadmap, backlog, decisions,
milestones) is tracked as version-controlled markdown files in this
repository, not in GitHub Issues/Projects or an external wiki/PM tool.

**Reasoning:** Markdown files are diffable, greppable, and carry full history
through Git alone, without depending on a third-party tool's data model or
availability. A small, fixed set of top-level files (rather than deeply
nested folders) keeps the structure easy to hold in memory and cheap to
maintain over years. GitHub Issues/Projects remain available later for
finer-grained task tracking if the need arises, without being required now.

---

## D005 — `embedded-workstation` is deferred, not scoped yet

**Date:** 2026-07-22
**Status:** Active

**Decision:** `embedded-workstation` is recorded as a planned future
repository but is not created or scoped yet.

**Reasoning:** Defining its structure now, before enough real toolchain usage
exists from working through `embedded-foundations`, would mean guessing at
requirements instead of documenting an environment that's actually in use.
It is tracked in [`BACKLOG.md`](BACKLOG.md) until there is enough real usage
to scope it accurately.

---

## D006 — `embedded-workstation` moves from deferred to active design review

**Date:** 2026-07-22
**Status:** Active

**Decision:** An initial design review of `embedded-workstation` has been
conducted, producing concrete architectural decisions (D007–D009). The
repository has since been created with an initial scaffold, ahead of a
first commit.

**Reasoning:** This updates D005's "not scoped yet" status now that a
design review has actually happened. D005 is not deleted or rewritten — it
remains the accurate record of why scoping waited until now; this entry
just marks that the wait is over, scoping is underway, and the repository
exists as a local scaffold. See [`ROADMAP.md`](ROADMAP.md) Phase 2 for
current status.

---

## D007 — Modularize `embedded-workstation` configuration by tool

**Date:** 2026-07-22
**Status:** Active

**Decision:** Configuration in `embedded-workstation` is organized into
per-tool directories (`bash/`, `git/`, `starship/`, `vscode/`, and further
directories as tools are added), rather than placed directly under a single
flat `config/` directory.

**Reasoning:** The repository exists to hold configuration for a growing
number of independent tools, each with its own files, install/link targets,
and update cadence. A flat `config/` directory mixes all of that together
and gets harder to reason about as tools are added — it becomes unclear
which files belong to which tool, and changing one tool's setup risks
touching files that belong to another. Grouping by tool keeps each tool's
configuration self-contained, so a tool can be added, changed, or removed
without touching anything unrelated — consistent with this ecosystem's
existing preference (D004) for structure that stays easy to hold in memory
without relying on it.

---

## D008 — `setup.sh` replaces `bootstrap.sh` as the primary installation entry point

**Date:** 2026-07-22
**Status:** Active

**Decision:** `embedded-workstation`'s primary entry point script is named
`setup.sh`, not `bootstrap.sh`.

**Reasoning:** "Bootstrap" describes a one-time, first-run action, but the
actual need is a script that gets run more than once — to configure a new
machine, and to re-apply or update configuration on a machine already set
up. Naming it `bootstrap.sh` would describe only the first use case and
misrepresent the second. `setup.sh` reflects the script's real, repeated
usage pattern, in line with this ecosystem's existing preference (D003) for
names that state actual purpose rather than following convention or habit.

---

## D009 — Every repository in the ecosystem includes a root-level `CLAUDE.md`

**Date:** 2026-07-22
**Status:** Active

**Decision:** Every repository in this ecosystem — starting with
`embedded-workstation`, and extended to every other repository, existing or
future — includes its own repository-level `CLAUDE.md` file, documenting
that repository's own conventions, structure, and constraints.

**Reasoning:** Claude Code is already the standing collaborator for
maintaining this repository (see [`IMPROVEMENTS.md`](IMPROVEMENTS.md)), and
that role extends naturally to the other repositories in the ecosystem.
Without in-repo context, each session has to either rediscover a
repository's conventions from scratch or rely on the user repeating them,
which doesn't hold up as the number of repositories grows. A per-repository
`CLAUDE.md` gives each repository the same kind of durable, written record
for AI-assisted work that `DECISIONS.md` and `README.md` already give for
human-directed project management — and keeps that context co-located with
the repository it describes, rather than centralized here where it would go
stale or grow unwieldy.

---

## D010 — Build-system laboratory (Make, then CMake) before finishing A02

**Date:** 2026-11-17
**Status:** Active

**Decision:** Pause A02 to run a build-system laboratory on A01's example
code: first deepen GNU Make by evolving A01's Makefile, then introduce
CMake. The resulting generic Makefile is reused by every later module.

**Reasoning:** CMake generates Makefiles, so understanding Make first makes
CMake's output readable instead of opaque — consistent with
`embedded-foundations`' principle that understanding comes before
automation. Make is also used directly by projects on the long-term path
(the Linux kernel, Buildroot, U-Boot). The laboratory was time-boxed and
ended by reusing its Makefile to finish A02.

---

## D011 — A02 covers the memory layout; ELF section detail moves to A05

**Date:** 2026-11-18
**Status:** Active

**Decision:** A02 - Memory Layout covers where each kind of variable is
placed and the memory map of a running process (runtime addresses, heap,
stack, ASLR, permissions). The detailed study of ELF sections (`readelf -S`,
`size`, why `.bss` takes no file space, compiler-generated sections) belongs
to A05 - Sections.

**Reasoning:** The first half of the A02 laboratory (section placement with
`nm` and `objdump`) overlapped heavily with A05's stated topic. Without an
explicit split, A05 would have repeated A02. The split is also recorded in
`embedded-foundations`' `README.md`.

---

## D012 — `-Wcast-qual` is part of the standard laboratory flags

**Date:** 2026-11-18
**Status:** Active

**Decision:** Every laboratory build in `embedded-foundations` (Makefiles and
`CMakeLists.txt`) uses `-std=c11 -Wall -Wextra -Wcast-qual -Werror`. The
flag list in that repository's `CLAUDE.md` was updated accordingly.

**Reasoning:** An A02 experiment showed that writing to a `const` object
after casting away `const` compiles silently under `-Wall -Wextra -Werror`
and only fails at runtime (a segmentation fault on Linux; possibly a silent
corruption on a microcontroller). `-Wcast-qual` turns this into a compile
error and matches MISRA C:2012 Rule 11.8. It caught a real case in A02's own
code as soon as it was enabled.
