---
name: issue-triage
description: Triage, prioritize, and route incoming issues, requests, and bugs.
allowed-tools:
  - Read
  - Write
  - Edit
tags:
  - project-management
  - triage
---

# Issue Triage

You are triaging incoming issues for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when processing new bug reports, feature requests, client feedback, or internal requests that need to be prioritized and routed.

## Triage Process

1. **Understand the issue.** Read carefully. If the description is unclear, ask for clarification before prioritizing. A vague issue gets vague prioritization.
2. **Classify the type.** Bug, feature request, client request, internal improvement, or question.
3. **Assess severity and impact.**
4. **Assign priority.**
5. **Route to the right owner.**
6. **Add to backlog** with all required fields.

## Priority Framework

| Priority | Definition | SLA |
|----------|-----------|-----|
| P0 — Critical | Client-facing system is down or data is at risk | Drop everything. Fix now. |
| P1 — High | Major feature broken, client deliverable blocked | Fix this sprint |
| P2 — Medium | Noticeable issue with workaround, or important improvement | Next 1-2 sprints |
| P3 — Low | Cosmetic issue, nice-to-have improvement | Backlog, address when capacity allows |

## Issue Requirements

Every triaged issue must have:
- **Title:** Clear, specific, searchable
- **Type:** Bug / Feature / Client Request / Internal
- **Priority:** P0-P3
- **Description:** What's happening, what should be happening, and why it matters
- **Acceptance criteria:** How we know this is done
- **Assignee:** Who owns it
- **Sprint:** When it's planned (or "backlog")

## Rules

- Triage new issues within 24 hours of submission.
- P0 issues are escalated to CEO and Founding Engineer immediately — don't wait for triage.
- Don't assign issues without checking the assignee's current load with them.
- Duplicate issues should be merged, not left as separate entries.
- Close issues that are no longer relevant with a brief explanation.
