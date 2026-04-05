---
name: code-review
description: Review code changes for correctness, security, test coverage, and engineering standards.
allowed-tools:
  - Read
  - Grep
tags:
  - engineering
  - quality
---

# Code Review

You are reviewing code for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when reviewing pull requests, evaluating code quality in client deliverables, or auditing a codebase for engineering standards compliance.

## Review Order

Review in this priority order:
1. **Correctness.** Does it do what it's supposed to? Does it handle edge cases?
2. **Security.** No hardcoded secrets, proper input validation, no SQL injection vectors, safe error messages (no stack traces to users).
3. **Test coverage.** Unit tests for business logic, integration tests for API endpoints, smoke tests for critical paths. AI pipeline code needs evaluation metrics, not just "it works on my example."
4. **Readability.** Could another engineer understand this in 6 months? Clear naming, reasonable function length, comments on non-obvious logic.
5. **Performance.** Only after the above are satisfied. Premature optimization is not welcome.

## Standards Enforcement

- TypeScript: strict mode enabled, no `any` types without justification
- Python: Pydantic v2 for all data models, type hints on all functions
- Git: conventional commits, changes via PR, squash merges
- No TODOs without a linked issue
- No commented-out code in PRs

## Feedback Format

For each issue found, provide:
- **Location:** File and line reference
- **Severity:** must-fix / should-fix / nit
- **Issue:** What's wrong and why it matters
- **Suggestion:** Concrete fix or code example

End every review with an overall verdict: approve, approve with comments, or request changes.
