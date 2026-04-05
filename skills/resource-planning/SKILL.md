---
name: resource-planning
description: Manage team capacity, forecast resource needs, and prevent overcommitment.
allowed-tools:
  - Read
  - Write
  - Edit
tags:
  - project-management
  - capacity
  - planning
---

# Resource Planning

You are managing resource allocation for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when assessing whether the team can take on new work, planning staffing for upcoming client engagements, or balancing internal vs. client work allocation.

## Capacity Model

For each team member, track:
- **Total available hours/week** (typically 40, minus PTO and recurring meetings)
- **Client work allocation** (target: 60-70% for delivery roles)
- **Internal work allocation** (target: 20-30% for platform, process, content)
- **Buffer** (10% unallocated — for unexpected requests and context switching)

## Resource Planning Process

1. **Map current commitments.** List every active engagement and internal initiative with: team members involved, estimated hours/week, and expected end date.
2. **Calculate available capacity.** Total capacity minus current commitments = available capacity per team member.
3. **Forecast incoming demand.** Review BizDev pipeline: which deals are likely to close in the next 30/60/90 days? What resources will they require?
4. **Identify conflicts.** Where does forecasted demand exceed available capacity? Flag these to CEO with options: delay new work, extend timelines, or hire.
5. **Make recommendations.** Present the tradeoffs clearly. "We can take on the Acme build starting May 1 if we extend the Beta Corp timeline by 2 weeks, or we need a contract engineer."

## Utilization Targets

| Role | Client Work | Internal | Buffer |
|------|------------|----------|--------|
| Founding Engineer | 60% | 30% | 10% |
| Designer | 50% | 40% | 10% |
| QA Engineer | 60% | 30% | 10% |
| Marketer | 20% | 70% | 10% |
| BizDev | 10% | 80% | 10% |

## Rules

- Never commit the team to work without verifying capacity first. Overcommitting damages quality and burns people out.
- Flag capacity conflicts to CEO at least 2 weeks before they become critical.
- When capacity is tight, protect client delivery over internal initiatives.
- Track actual vs. planned hours monthly to improve future estimates.
