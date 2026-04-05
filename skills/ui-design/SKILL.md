---
name: ui-design
description: Design user interfaces for marketing sites, client dashboards, and AI-powered tools.
allowed-tools:
  - Read
  - Write
  - Edit
tags:
  - design
  - ui
  - ux
---

# UI Design

You are designing user interfaces for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when creating page layouts, component designs, user flows, wireframes, or interactive prototypes for the marketing site, client-facing dashboards, or AI tool interfaces.

## Design Principles

- **Clarity over decoration.** Every element earns its space. If it doesn't help the user understand or take action, remove it.
- **Progressive disclosure.** Show the most important information first. Let users drill deeper on demand. This is especially important for AI-generated outputs — don't dump everything at once.
- **Consistent patterns.** Use the design system. Every interaction pattern (forms, modals, navigation, data display) should feel familiar across the product.
- **Mobile-first.** Design for 375px first, then expand. Not the other way around.

## Page Design Process

1. **Define the user goal.** What is the user trying to accomplish on this page? Write it in one sentence.
2. **Content hierarchy.** List the content blocks in priority order. The most important information should be visible without scrolling.
3. **Wireframe.** Block out the layout at low fidelity. Focus on information architecture, not visual polish.
4. **Component mapping.** Map each content block to an existing design system component. Only propose a new component if nothing in the system fits.
5. **Visual design.** Apply color, typography, and spacing from the design tokens. Review against brand guidelines.
6. **Responsive check.** Verify the design works at mobile (375px), tablet (768px), and desktop (1280px+).

## AI Interface Patterns

When designing interfaces for AI-powered features:
- Always show the user what inputs the AI received (transparency).
- Provide a way to see the AI's confidence or sources (trust).
- Make it easy to correct or override AI outputs (control).
- Show loading states that set expectations for response time (patience).
