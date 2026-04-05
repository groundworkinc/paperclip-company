---
name: design-system
description: Build and maintain the Groundwork AI component library with design tokens, components, and patterns.
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
  - Bash
tags:
  - design
  - engineering
  - components
---

# Design System

You are working on the Groundwork AI design system — a shared component library built on shadcn/ui + Radix primitives.

## When to Use This Skill

Use this skill when creating new components, updating design tokens, documenting component usage, or ensuring design system compliance in implementations.

## Design Tokens

All visual values must reference tokens, never hardcoded values:

```
colors:
  primary: #1B3A2E    (Deep Forest)
  accent: #D97706     (Amber)
  surface: #FAFAF8    (Parchment)

typography:
  display: Sohne
  body: Inter
  mono: JetBrains Mono

spacing: 4px base unit (4, 8, 12, 16, 24, 32, 48, 64)

radii: 4px (sm), 8px (md), 12px (lg)
```

## Component Standards

Every component must:
1. Accept a `className` prop for composition.
2. Forward refs when wrapping interactive elements.
3. Include keyboard navigation support.
4. Meet WCAG 2.1 AA: 4.5:1 contrast for normal text, 3:1 for large text, visible focus states.
5. Work at all responsive breakpoints (375px, 768px, 1280px+).
6. Have a documented usage example.

## Component Creation Process

1. Check if shadcn/ui or Radix already provides the primitive.
2. If yes, wrap it with Groundwork tokens and document any customizations.
3. If no, build from scratch following the Radix pattern: unstyled primitive + styled wrapper.
4. Write at least one usage example.
5. Test with keyboard navigation and a screen reader.
6. Add to the component index.

## Rules

- Never create a custom component when a shadcn/ui primitive exists.
- Never hardcode colors, spacing, or typography values — always use tokens.
- Every new component needs QA review for accessibility before merging.
