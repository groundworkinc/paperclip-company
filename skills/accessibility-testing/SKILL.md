---
name: accessibility-testing
description: Execute accessibility testing against WCAG 2.1 AA standards using manual and automated methods.
allowed-tools:
  - Read
  - Grep
  - Bash
tags:
  - quality
  - accessibility
  - testing
---

# Accessibility Testing

You are executing accessibility testing for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when testing a page, component, or feature for WCAG 2.1 AA compliance. This covers both automated scanning and manual verification.

## Testing Process

### Automated Scan
1. Run axe-core or Lighthouse accessibility audit on the page.
2. Document all violations with their WCAG criteria and severity.
3. Note: automated tools catch approximately 30-40% of accessibility issues. Manual testing is essential.

### Keyboard Testing
1. Tab through the entire page. Verify every interactive element is reachable.
2. Check that focus order follows visual/logical reading order.
3. Verify focus indicators are visible on every focusable element.
4. Test that Enter/Space activates buttons and links.
5. Test that Escape closes modals and dropdowns.
6. Verify no keyboard traps exist.

### Screen Reader Testing
1. Navigate the page with VoiceOver (macOS) or NVDA (Windows).
2. Verify all images have meaningful alt text.
3. Verify form inputs are properly labeled.
4. Verify heading hierarchy is logical and complete.
5. Verify dynamic content changes are announced (aria-live regions).
6. Verify ARIA landmarks (nav, main, aside) are present and correctly used.

### Visual Testing
1. Check color contrast with a tool (WebAIM Contrast Checker or browser DevTools).
2. Verify information is not conveyed by color alone.
3. Zoom to 200% and verify no content is lost or overlaps.
4. Verify text remains readable at all zoom levels.

## Severity Classification

- **Must-fix:** Blocks a user group from completing a task (missing form labels, keyboard traps, zero-contrast text)
- **Should-fix:** Degrades experience significantly (poor focus indicators, missing alt text on informational images, illogical heading order)
- **Nice-to-fix:** Minor improvements (decorative images with unnecessary alt text, overly verbose ARIA labels)

## Rules

- Every WCAG 2.1 AA violation is a bug, minimum severity Medium.
- File accessibility bugs with the specific WCAG success criterion referenced (e.g., "Fails WCAG 1.4.3 Contrast Minimum").
- Test with real assistive technology, not just automated tools.
- Re-test all fixed accessibility bugs to verify the fix doesn't introduce new issues.
