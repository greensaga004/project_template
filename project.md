# PROJECT OVERVIEW

> Use this file for a **whole new codebase**.
> Fill it in once at project start to define the architecture, final target, and roadmap.
> Each roadmap item is later implemented on its own branch using `status.md`.

## Init Status

Status: TEMPLATE

> TEMPLATE = not yet defined; DEFINED = initialization complete.
> Set to DEFINED only after Final Target, Architecture, and Roadmap are filled in.
> This marker is the single source of truth for "is project.md defined?".

---

## Project

Project Name: TBD

Repository: TBD  (optional — leave empty for local-only; if using GitHub, create an empty repo and `git clone` before copying this template in)

Owner: TBD

Project Type: TBD  (e.g. Web App / Desktop App (Windows/macOS/Linux) / Mobile App (Android/iOS) / CLI Tool / Library/SDK / Backend Service / Embedded)

Target Platforms: TBD

Tech Stack:

- Language(s): TBD
- Framework / UI: TBD
- Data / Storage: TBD
- Backend / Services: TBD
- Build / Packaging: TBD
- Infrastructure / Distribution: TBD  (optional — CI/CD only if publishing to GitHub or similar)

---

## Delivery Policy

> Decided once, after this file is defined. Governs how work branches land.

- Main Branch Protected: TBD  (yes / no)
- Pull Request Required: TBD  (yes / no — if main is protected, yes)
- CI Required: TBD  (yes if Pull Request Required; must pass before merge)
- Merge Method: TBD  (e.g. squash / merge / rebase)

If Pull Request Required is **no** (local-only), work branches may merge directly and CI is optional.

---

## Branch Naming

Pattern: `<type>/<short-name>`  (base branch: main or master)

Types:

- feature/ — new functionality
- fix/ — bug fix
- chore/ — tooling, deps, refactor, config
- docs/ — documentation only

Each branch carries one `status.md` and one work item from the Roadmap, regardless of type.

---

## Repository Layout

```
docs/
  project.md          (this file — whole-project overview, read once)
  status.md           (per-task workflow, one copy per branch)
  specs/<name>.md     (SPEC stage output)
  tasks/<name>.md     (TASK stage output)
<source>/             (application/source code)
```

---

## Final Target

Vision:

TBD

Problem Statement:

TBD

Success Definition (Done means):

- TBD

Out of Scope:

- TBD

---

## Architecture

High-Level Overview:

TBD

Components:

| Component | Responsibility | Tech |
| --- | --- | --- |
| TBD | TBD | TBD |

Data Flow:

TBD

Key Decisions:

- TBD

Constraints / Non-Functional Requirements:

- Performance: TBD
- Security: TBD
- Scalability: TBD

---

## Roadmap / Todo List

> Each item becomes a work branch. On start, copy `status.md` into `docs/`,
> set the work item, reset items to TBD, and begin at the INIT stage.

| # | Work Item | Priority | Depends On | Status |
| --- | --- | --- | --- | --- |
| 1 | TBD | TBD | - | TODO |
| 2 | TBD | TBD | 1 | TODO |
| 3 | TBD | TBD | - | TODO |

Status values: TODO / IN PROGRESS / DONE / BLOCKED

---

## Milestones

- [ ] M1: TBD
- [ ] M2: TBD
- [ ] M3: TBD

---

## AI Instructions

Read this file **once** to initialize the project (architecture, final target, roadmap).
After initialization, do **not** read or update it again during work on a branch — use `status.md` on the work branch instead.
Re-read this file only when: (a) the user explicitly asks to modify it, or (b) the user says `report` while on the `main` (or `master`) branch.

Detecting whether the project is defined:

- If `docs/project.md` is missing → not defined; initialize first.
- If it exists but `Init Status` is `TEMPLATE` → not defined; finish initialization.
- If `Init Status` is `DEFINED` → already defined; do not re-initialize.

Initializing (`init`):

- If `Init Status` is already `DEFINED`, do nothing unless the user asks to modify.
- For an existing codebase: scan the repo (languages, frameworks, structure, build files) and draft the empty fields — Project Type, Target Platforms, Tech Stack, Architecture summary.
- For an empty project: interview the user to fill the same fields.
- Always present the drafted values for confirmation; set `Status: DEFINED` only after the user approves.
- Never invent Final Target or Roadmap from a scan — those come from the user.

Rules:

1. Define architecture and final target before writing any code.
2. Keep the roadmap as the single source of truth for what to build next.
3. Prefer MVP solutions and avoid over-engineering.
4. Suggest architecture changes only when absolutely necessary; record them under Key Decisions.
5. Do not start a work item until it exists in the Roadmap.
6. When starting a work item, hand off to `status.md` (per-task workflow) on a new branch.
7. During work branches, ignore this file; it is only revisited when the user asks to modify it, or via `report` on main/master.

---

## Commands

init   (scan the codebase to draft empty fields — or interview if empty project — confirm, then set Init Status = DEFINED)

show final target

show architecture

show roadmap

add roadmap item

start <type>/<name>   (copy status.md to docs/, reset to INIT stage; type = feature/fix/chore/docs)

report   (only on main/master: re-read this file and summarize roadmap progress)
