# PROJECT STATUS

> Use this file for a **single work item** (feature, fix, chore, docs) on its own branch.
> Copy into `docs/`, fill in the Current Work Item, reset the checklist to unchecked, and start at the INIT stage.
> For whole-codebase architecture, target, and roadmap, see `project.md`.

## Project

See `project.md` for Project Name, Repository, and Tech Stack.
(For a standalone task with no `project.md`, fill those in here instead.)

---

## Current Work Item

Work Item Name: TBD

Description: TBD

---

## Current Stage

INIT

Available Stages:

- INIT
- SPEC
- TASK
- IMPLEMENTATION
- VERIFICATION

---

## Stage Definitions

### INIT

Goal:

Set up this task's context before any requirements work.

Output:

Filled header of this file (Project + Current Work Item).

Allowed:

- Confirm Branch
- Set Work Item Name / Description
- Inherit Tech Stack from project.md
- Agree Task Boundary / Scope Line

Not Allowed:

- Requirements / MVP Definition
- Task Planning
- Source Code

Exit Criteria:

- Branch created
- Work Item Name + Description filled
- Tech Stack confirmed
- Scope boundary agreed

---

### SPEC

Goal:

Define requirements and MVP.

Output:

docs/specs/<name>.md

Allowed:

- Business Goal
- User Story
- MVP
- Scope Definition
- Acceptance Criteria

Not Allowed:

- Source Code
- Detailed Task Planning
- Implementation Discussion

Exit Criteria:

- MVP is clearly defined
- Scope is agreed
- Success criteria exist

---

### TASK

Goal:

Break the work item into implementable tasks.

Output:

docs/tasks/<name>.md

Allowed:

- Task Breakdown
- Dependencies
- Priorities
- Development Order

Not Allowed:

- Source Code

Exit Criteria:

- Tasks are small and actionable
- Each task can be completed independently

---

### IMPLEMENTATION

Goal:

Build the work item.

Output:

Source Code

Allowed:

- Data / Storage Changes
- Core / Logic Code
- UI / Interface Code
- Tests

Not Allowed:

- New Scope Changes

Exit Criteria:

- All tasks completed
- Code committed
- Tests added

---

### VERIFICATION

Goal:

Confirm implementation matches specification.

Output:

Verification Result

Allowed:

- Testing
- Code Review
- Spec Coverage Check
- Bug Fixes

Exit Criteria:

- Implementation matches Spec
- Tests pass
- CI passes (required if Delivery Policy in project.md sets CI Required = yes)
- No critical issues remain

---

## Delivery (after VERIFICATION)

> Not a stage. Runs once VERIFICATION is done.

Flow (only if project.md Delivery Policy sets Pull Request Required = yes):

1. `open pr` — confirm, then push branch and open a PR to main.
2. Wait for CI green + review approval.
3. Merge the PR.
4. `finish` — switch to main and delete the branch.

If Pull Request Required = no, skip straight to `finish`.

---

## Current Checklist

### INIT

- [ ] Branch Created
- [ ] Work Item Name + Description
- [ ] Tech Stack Confirmed
- [ ] Scope Boundary Agreed

### SPEC

- [ ] Business Goal
- [ ] User Story
- [ ] MVP Defined
- [ ] Scope Defined
- [ ] Acceptance Criteria

### TASK

- [ ] Core / Logic Tasks
- [ ] UI / Interface Tasks
- [ ] Data / Storage Tasks
- [ ] Test Tasks

### IMPLEMENTATION

- [ ] Data / Storage Changes
- [ ] Core / Logic Changes
- [ ] UI / Interface Changes
- [ ] Unit Tests
- [ ] Docs/README updated

### VERIFICATION

- [ ] Work Item Tested
- [ ] Spec Coverage Verified
- [ ] CI Passed (required if project.md Delivery Policy sets CI Required = yes)

---

## Current Task

TBD

---

## Next Action

TBD

---

## AI Instructions

Always read this file first.

Rules:

1. Follow the Current Stage.
2. Do not jump to later stages.
3. Prefer MVP solutions.
4. Avoid over-engineering.
5. Suggest architecture changes only when absolutely necessary.
6. Focus on completing the current stage before moving forward.
7. On `goto next stage`, commit the current changes before advancing.
8. On `goto init`, reset this file to its init state: set Current Stage to INIT, set Work Item Name/Description/Current Task/Next Action to TBD, and uncheck every checklist item.
9. On `open pr`, always show the PR title and description and ask for explicit user confirmation; only open the PR after the user approves.
10. On `report` while on a work branch, summarize progress from this file only (current stage + checklist); do not read `project.md`.

---

## Commands

report   (on a work branch: summarize this work item's progress from status.md only; do not read project.md)

goto init   (reset this file to init state: stage=INIT, header fields=TBD, all checkboxes unchecked)

goto spec

goto task

goto implementation

goto verification

goto next stage

open pr   (after VERIFICATION done: push branch and open a PR to main; requires CI green if project.md sets CI Required = yes; must be confirmed by the user before the PR is actually opened)

finish (switch to main branch and delete the current branch)
