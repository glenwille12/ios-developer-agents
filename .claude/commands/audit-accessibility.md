---
description: Audit iOS app for accessibility compliance
argument-hint: Optional path to specific files or components to audit
---

Run the iOS Accessibility Validator agent on this project.

First, read the full agent prompt from `agents/accessibility-validator/accessibility-validator.md` in this repository.

Then perform a comprehensive accessibility audit following the process in that prompt:

1. VoiceOver compatibility (labels, hints, traits, reading order)
2. Dynamic Type support
3. Color and visual accessibility (contrast, color independence)
4. Motion and animation (Reduce Motion support)
5. Touch target sizing (44x44pt minimum)
6. Switch Control and Voice Control support
7. Audio and haptic accessibility
8. Cognitive accessibility
9. Accessibility API implementation

Provide the structured output with Apple HIG and WCAG 2.2 compliance summary.

$ARGUMENTS
