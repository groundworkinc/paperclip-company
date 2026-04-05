---
name: accessibility-review
description: Audit designs and implementations for WCAG 2.1 AA compliance.
allowed-tools:
  - Read
  - Grep
tags:
  - design
  - accessibility
  - quality
---

# Accessibility Review

You are conducting an accessibility review for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when auditing a design comp, reviewing an implemented page, or checking a component for WCAG 2.1 AA compliance.

## Accessibility Checklist

### Visual
- [ ] Color contrast meets 4.5:1 for normal text, 3:1 for large text (18px+ or 14px+ bold)
- [ ] Information is not conveyed by color alone (use icons, labels, or patterns as secondary indicators)
- [ ] Text is resizable to 200% without loss of content or functionality
- [ ] No content flashes more than 3 times per second

### Keyboard
- [ ] All interactive elements are reachable via Tab key
- [ ] Focus order follows a logical reading sequence
- [ ] Focus indicators are visible (not just browser default — custom focus rings preferred)
- [ ] No keyboard traps (user can always Tab out of any element)
- [ ] Modal dialogs trap focus appropriately and return focus on close

### Screen Reader
- [ ] All images have meaningful alt text (or empty alt for decorative images)
- [ ] Form inputs have associated labels
- [ ] Heading hierarchy is logical (H1 > H2 > H3, no skipped levels)
- [ ] ARIA landmarks are used appropriately (nav, main, aside, footer)
- [ ] Dynamic content changes are announced (aria-live regions where needed)

### Interactive
- [ ] Buttons and links are clearly distinguished
- [ ] Error messages are associated with their form fields
- [ ] Required fields are indicated before form submission, not only after validation
- [ ] Touch targets are at least 44x44px on mobile

## Output Format

Accessibility reviews should list each issue found with: the element or location, the WCAG criterion violated, the severity (must-fix / should-fix), and a specific remediation recommendation.
