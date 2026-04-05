---
name: api-testing
description: Test API endpoints for correctness, error handling, security, and performance.
allowed-tools:
  - Read
  - Grep
  - Bash
tags:
  - quality
  - testing
  - api
---

# API Testing

You are testing API endpoints for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when testing REST API endpoints, webhook integrations, or AI pipeline API interfaces for client projects or internal platform.

## API Test Categories

### Functional Testing
- **Happy path:** Send valid requests, verify correct response status, body, and headers.
- **Input validation:** Test with missing required fields, wrong data types, empty strings, extremely long values, special characters, and SQL injection attempts.
- **Authentication:** Test with valid token, expired token, invalid token, missing token, and wrong permission level.
- **Pagination:** Test first page, last page, out-of-range page, and zero/negative page numbers.
- **Idempotency:** For POST/PUT/DELETE, verify repeated identical requests produce expected behavior.

### Error Handling
- Verify all error responses include: appropriate HTTP status code, clear error message, and consistent error format.
- Verify error messages don't leak internal details (stack traces, database queries, file paths).
- Test rate limiting: verify 429 responses include Retry-After headers.
- Test with malformed JSON, wrong Content-Type, and oversized payloads.

### Performance
- Measure response times under normal load. Document P50, P95, and P99 latencies.
- For AI pipeline endpoints: measure and document token usage, cost per request, and end-to-end latency.
- Identify endpoints that degrade under concurrent requests.

### Security
- Verify CORS headers are correctly configured.
- Verify sensitive data is not included in response headers or error messages.
- Test for authorization bypass: can User A access User B's resources?
- Verify all endpoints require authentication (unless intentionally public).

## Test Reporting Format

For each endpoint tested:
- **Endpoint:** Method + path
- **Test cases executed:** Count by category
- **Pass/fail summary**
- **Issues found:** With severity and reproduction steps
- **Performance baseline:** P50/P95 response times

## Rules

- Every API endpoint needs tests for both valid and invalid inputs.
- Never test against production data or production databases.
- Document the expected response schema for every endpoint — test against the schema, not just "it returned 200."
- AI pipeline endpoints need cost and latency documentation, not just correctness.
