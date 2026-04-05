---
name: test-planning
description: Create comprehensive test plans for features, AI pipelines, and client deliverables.
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
tags:
  - quality
  - testing
  - planning
---

# Test Planning

You are creating a test plan for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when a new feature, AI pipeline, client deliverable, or site deployment needs a structured test plan before QA execution begins.

## Test Plan Structure

1. **Scope.** What's being tested? List the features, endpoints, or pages in scope. Explicitly state what's NOT in scope.
2. **Test environment.** Browser/device matrix, staging URLs, test accounts, API keys needed.
3. **Test cases by category:**
   - **Happy path:** Standard user workflows that should work correctly
   - **Edge cases:** Boundary values, empty inputs, maximum lengths, special characters
   - **Error handling:** Network failures, invalid inputs, expired sessions, rate limits
   - **Accessibility:** Keyboard navigation, screen reader, color contrast, focus management
   - **Cross-browser/device:** Chrome, Firefox, Safari, Edge; mobile, tablet, desktop
   - **Performance:** Load times, Core Web Vitals, no layout shifts
4. **AI-specific test cases (when applicable):**
   - Accuracy against evaluation dataset (minimum 20 test cases)
   - Varied input quality (clean, messy, adversarial, non-English)
   - Latency under normal and peak load
   - Token usage and cost per request
   - Failure mode behavior (LLM timeout, rate limit, garbage output)
   - Consistency (same input, 10 runs, acceptable variance)
5. **Acceptance criteria.** What must pass for this to ship?
6. **Risk areas.** Where are bugs most likely to hide? Focus extra testing there.

## Test Case Format

| ID | Category | Description | Steps | Expected Result | Priority |
|----|----------|-------------|-------|-----------------|----------|
| TC-001 | Happy path | User submits valid form | 1. Fill all fields 2. Click submit | Success message displayed, data saved | High |

## Rules

- No testing without a test plan. Ad hoc "click around and see" is not QA.
- Test plans must be created before testing begins, not after.
- Every test case must have an expected result — "see what happens" is not a test case.
- For AI features, subjective assessment ("looks right") is insufficient. Define measurable criteria.
