# PROJECT STATUS

## Project

Project Name: TBD

Repository: TBD

Tech Stack:

- Frontend: TBD
- Backend: TBD
- Database: TBD
- Cloud: TBD

---

## Current Feature

Feature Name: TBD

Description: TBD

---

## Current Stage

SPEC

Available Stages:

- SPEC
- TASK
- IMPLEMENTATION
- VERIFICATION

---

## Stage Definitions

### SPEC

Goal:

Define requirements and MVP.

Output:

docs/specs/<feature>.md

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

Break the feature into implementable tasks.

Output:

docs/tasks/<feature>.md

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

Build the feature.

Output:

Source Code

Allowed:

- Database Changes
- Backend Code
- Frontend Code
- Tests

Not Allowed:

- New Feature Scope Changes

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

- Feature matches Spec
- CI passes
- No critical issues remain

---

## Current Checklist

### SPEC

- [ ] Business Goal
- [ ] User Story
- [ ] MVP Defined
- [ ] Scope Defined
- [ ] Acceptance Criteria

### TASK

- [ ] Backend Tasks
- [ ] Frontend Tasks
- [ ] Database Tasks
- [ ] Test Tasks

### IMPLEMENTATION

- [ ] Database Changes
- [ ] Backend Changes
- [ ] Frontend Changes
- [ ] Unit Tests
- [ ] Docs/README.md updated

### VERIFICATION

- [ ] Feature Tested
- [ ] Spec Coverage Verified
- [ ] CI Passed

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

---

## Commands

show current stage

show current feature

goto spec

goto task

goto implementation

goto verification

goto next stage

finish current stage

finish (switch to main branch and delete the current branch)
