---
name: regression-testing
description: Execute regression test suites to verify existing functionality after changes.
allowed-tools:
  - Read
  - Grep
  - Bash
tags:
  - quality
  - testing
  - regression
---

# Regression Testing

You are running regression tests for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill before any production deployment, after merging significant changes, or when verifying that bug fixes haven't introduced new issues.

## Regression Test Suite

Maintain a checklist of critical paths that must pass before every release:

### Marketing Site
- [ ] Homepage loads correctly, all sections render
- [ ] Navigation links work (all pages reachable)
- [ ] Contact form submits successfully
- [ ] Blog posts render with correct formatting
- [ ] Workshop registration flow works end-to-end
- [ ] Mobile responsive at 375px, 768px, 1280px
- [ ] Analytics events fire on key pages (PostHog)
- [ ] SEO elements present: meta tags, OG images, sitemap, robots.txt
- [ ] No broken images or 404 links
- [ ] Core Web Vitals within acceptable range

### Client AI Pipelines (per engagement)
- [ ] Pipeline accepts valid input and returns expected output
- [ ] Error handling works for invalid/empty/oversized input
- [ ] Response times within documented SLA
- [ ] Token usage within documented budget
- [ ] Evaluation dataset accuracy has not degraded
- [ ] Monitoring and alerting are functional (Langfuse, Sentry)

### Authentication and Security
- [ ] Login flow works
- [ ] Unauthorized access is properly rejected
- [ ] API authentication tokens are validated
- [ ] No sensitive data in client-visible responses

## Regression Testing Process

1. **Identify scope.** What changed? Map the changes to potentially affected areas.
2. **Select test cases.** Run the full regression suite for major releases. For targeted changes, run the relevant subset plus any areas that share dependencies.
3. **Execute tests.** Follow each test case exactly. Don't skip steps, even for familiar tests.
4. **Document results.** Pass/fail for each case. For failures: file a bug immediately with reproduction steps.
5. **Make the call.** If all critical paths pass: approve for deployment. If any critical path fails: block deployment and escalate.

## Rules

- The full regression suite runs before every production deployment. No exceptions.
- A previously fixed bug that reappears is automatically P1 severity.
- Add new regression test cases whenever a bug is fixed — the fix's test case joins the permanent suite.
- Regression suite should take no more than 2 hours for a single tester. If it exceeds this, prioritize automation for the most stable test cases.
- Never skip regression testing to meet a deadline. Escalate to PM and CEO if there's pressure to do so.
