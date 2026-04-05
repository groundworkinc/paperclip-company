# Groundwork AI — Paperclip Company

An AI-native company built on [Paperclip](https://paperclip.dev), the agent company framework. This repo defines Groundwork AI's entire organizational structure — agents, skills, teams, and operating principles — as code.

**Mission:** Make AI practical, not theoretical, for every business. Educate first, build second, optimize always.

## What is This?

This is a real, operating AI consultancy defined declaratively. Every role, workflow, and capability is codified in markdown and YAML. Paperclip reads these definitions and runs the company as a coordinated team of AI agents — each with its own personality, expertise, decision-making framework, and tools.

Think of it as infrastructure-as-code, but for an entire business.

## Company at a Glance

| | |
|---|---|
| **Industry** | AI consultancy & education |
| **Services** | Workshops, workflow audits, custom AI builds, managed optimization |
| **Approach** | Education-first — we teach businesses AI, then build it for them |
| **Tech Stack** | Next.js, FastAPI, Claude, Vercel AI SDK, Supabase, pgvector |
| **Framework** | [Paperclip](https://paperclip.dev) agent company platform |

## Agents

Seven agents form the core team, each with a defined soul (personality + decision framework), tools, and heartbeat (operating rhythm):

| Agent | Role |
|---|---|
| **CEO** | Strategy, client relationships, workshops, proposals. Founder-operator who leads with education and delegates execution. |
| **Founding Engineer** | Architecture, AI pipelines, technical delivery. Pragmatic builder — boring infrastructure, novel AI. |
| **BizDev** | Outbound sales, lead qualification, partnerships. Consultative seller with a structured ICP scoring framework. |
| **Designer** | Brand, UX, design system. Owns the visual identity and accessibility standards. |
| **Marketer** | Content, SEO, demand gen. Builds the inbound engine and maintains brand voice. |
| **Project Manager** | Sprint management, delivery coordination, resource planning. Translates strategy into execution. |
| **QA Engineer** | Testing, accessibility, release readiness. The quality gate — nothing ships without sign-off. |

Each agent is defined by four files:

- `SOUL.md` — Personality, voice, decision-making framework, and working relationships
- `AGENTS.md` — Role metadata and schema definition
- `TOOLS.md` — Available tools and integrations
- `HEARTBEAT.md` — Operating cadence and check-in rhythms

## Skills

30 skills define the company's capabilities — reusable, structured workflows that agents execute:

**Sales & Client**
`client-discovery` · `lead-qualification` · `outbound-sales` · `partnership-development` · `proposal-writing` · `crm-management`

**Engineering**
`ai-pipeline-development` · `code-architecture` · `code-review`

**Design & Brand**
`brand-design` · `design-system` · `ui-design` · `accessibility-review`

**Marketing & Content**
`content-strategy` · `email-marketing` · `seo-writing` · `social-media` · `technical-writing`

**Project Management**
`sprint-planning` · `status-reporting` · `resource-planning` · `strategic-planning` · `issue-triage`

**Quality Assurance**
`accessibility-testing` · `api-testing` · `regression-testing` · `test-planning` · `review`

**Analytics & Workshops**
`analytics` · `workshop-design`

## Team Structure

```
CEO
├── Founding Engineer
│   └── QA Engineer
├── BizDev
├── Designer
├── Marketer
└── Project Manager
```

The CEO sets strategic direction. The Project Manager translates it into sprints. BizDev fills the pipeline, Marketer builds inbound, Designer owns the brand, the Founding Engineer builds, and QA makes sure it works.

Communication is async-first with structured check-ins: daily async standups, weekly CEO status review, biweekly retros.

## How It Works

1. **Clone this repo** and install [Paperclip](https://paperclip.dev)
2. **Configure secrets** — set `ANTHROPIC_API_KEY` (required) and optionally `GH_TOKEN`
3. **Run agents** — Paperclip reads `.paperclip.yaml` and spins up agents using Claude as the underlying model
4. **Assign work** — agents operate within their defined roles, skills, and team structure

```yaml
# .paperclip.yaml — each agent runs on Claude via local adapter
agents:
  ceo:
    adapter:
      type: claude_local
      config:
        model: claude-sonnet-4-6
```

## Operating Principles

- Never propose a build without a completed audit
- Education before implementation — always
- Outcome-based pricing available; we share risk with clients
- All changes via PR, conventional commits, squash merges
- Ship working systems, not decks

## License

MIT
