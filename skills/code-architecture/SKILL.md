---
name: code-architecture
description: Design system architecture, make technology decisions, and structure codebases for AI consultancy projects.
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
  - Bash
tags:
  - engineering
  - architecture
---

# Code Architecture

You are making architectural decisions for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when designing a new system, evaluating a technology choice, structuring a codebase, or reviewing an architectural proposal for a client project or internal platform.

## Architecture Principles

- **Boring infrastructure, novel AI.** Use proven, well-supported tools for infrastructure (Next.js, FastAPI, Supabase, Vercel). Reserve innovation for the AI layer where it creates real client value.
- **Composition over inheritance.** Build systems from small, composable modules. Every component should do one thing well.
- **Explicit over implicit.** Dependencies, configuration, and data flow should be visible and traceable. No magic.
- **Observable by default.** Every system must include logging, error tracking, and performance monitoring from day one. For AI pipelines, add LLM-specific tracing (Langfuse).
- **Client-deliverable quality.** Every architecture should be maintainable by a competent team after Groundwork hands it off. No clever tricks that only the original author understands.

## Standard Stack

- **Frontend:** Next.js 15 (App Router), Tailwind CSS, shadcn/ui
- **Backend:** FastAPI (Python), Pydantic v2
- **AI/LLM:** Claude (primary), Vercel AI SDK
- **Database:** Supabase (PostgreSQL + pgvector)
- **Infrastructure:** Vercel, Railway, Docker
- **Monitoring:** Sentry, Langfuse, PostHog

## Decision Template

When proposing an architecture decision, document: the decision, the context (why now), the options considered (at least 2), the tradeoffs of each, the recommendation with rationale, and the reversibility (easy to change later or a one-way door).
