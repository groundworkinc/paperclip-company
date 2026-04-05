---
name: crm-management
description: Maintain pipeline hygiene, track deals, and manage lead data in HubSpot CRM.
allowed-tools:
  - Read
  - Write
  - Edit
tags:
  - sales
  - crm
  - pipeline
---

# CRM Management

You are managing the sales pipeline in HubSpot CRM for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when updating deal stages, logging activities, generating pipeline reports, or ensuring CRM data hygiene.

## Pipeline Stages

| Stage | Definition | Exit Criteria |
|-------|-----------|---------------|
| Lead Identified | New prospect added to target list | ICP score assigned |
| Contacted | First outreach sent | At least one touch completed |
| Engaged | Prospect responded or showed interest | Two-way communication established |
| Discovery Scheduled | Call booked | Calendar invite sent, prep doc created |
| Discovery Complete | Call happened | Summary sent, next step agreed |
| Audit Proposed | Audit proposal sent | Proposal delivered with deadline |
| Audit In Progress | Paid audit underway | Audit kickoff completed |
| Build Proposed | Build SOW sent | SOW delivered with deadline |
| Closed Won | Contract signed | Payment terms agreed |
| Closed Lost | Deal dead | Loss reason documented |

## Data Hygiene Rules

- Every contact must have: name, company, title, email, ICP score, lead source.
- Every deal must have: stage, expected close date, deal value, next step with deadline, assigned owner.
- Update deal stages within 24 hours of any stage change.
- Log every outreach touch (email, call, LinkedIn) as an activity on the contact record.
- Review and clean stale deals (no activity in 30+ days) weekly.

## Weekly Pipeline Report

Include: total pipeline value by stage, new leads added this week, stage movements, deals at risk (no activity in 14+ days), discovery calls booked, and forecast for next 30/60/90 days.
