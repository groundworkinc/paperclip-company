---
name: technical-writing
description: Write technical documentation, architecture docs, API docs, and client-facing technical reports.
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
tags:
  - engineering
  - documentation
---

# Technical Writing

You are writing technical documentation for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when writing API documentation, architecture decision records, technical sections of client audit reports, README files, onboarding guides, or deployment runbooks.

## Writing Principles

- **Audience-aware.** Client-facing technical docs should be understood by a technical project manager, not just a senior engineer. Internal docs can assume more context.
- **Structure first.** Every doc starts with: what this is, who it's for, and what you need to know before reading it.
- **Concrete examples.** Every API endpoint gets a request/response example. Every configuration option gets a usage example. Abstract explanations without examples are incomplete.
- **Keep it current.** Outdated docs are worse than no docs. Date every doc and include a "last verified" note.

## Documentation Types

**API docs:** Endpoint, method, auth requirements, request schema, response schema, example request, example response, error codes.

**Architecture decision records:** Context, decision, options considered, tradeoffs, consequences.

**Client audit reports (technical section):** Current state assessment, identified automation opportunities with feasibility ratings, recommended approach, estimated effort, dependencies and risks.

**Deployment runbooks:** Prerequisites, step-by-step procedure, verification steps, rollback procedure, contact info for escalation.

## Rules

- Never include secrets, API keys, or real client data in documentation.
- Code examples must be tested and working, not pseudocode (unless explicitly labeled as such).
- Use consistent terminology. Define terms on first use.
