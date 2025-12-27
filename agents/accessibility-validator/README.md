# Accessibility Validator

A comprehensive iOS accessibility audit agent that ensures your app is usable by everyone, including people with visual, auditory, motor, and cognitive disabilities.

## Capabilities

- **VoiceOver Compatibility**: Validates labels, hints, traits, reading order, and custom actions
- **Dynamic Type Support**: Checks text scaling, layout adaptation, and font usage
- **Color Contrast Analysis**: Verifies WCAG 2.2 contrast ratios for text and UI elements
- **Motion Sensitivity**: Audits animations and Reduce Motion support
- **Touch Target Sizing**: Ensures minimum 44x44pt interactive elements
- **Alternative Input Support**: Checks Switch Control, Voice Control, and keyboard navigation
- **Cognitive Accessibility**: Reviews clarity, predictability, and error prevention

## Standards Coverage

| Standard | Coverage |
|----------|----------|
| Apple Human Interface Guidelines | Full |
| WCAG 2.2 Level A | Full |
| WCAG 2.2 Level AA | Full |
| Section 508 | Supported |
| European Accessibility Act (EAA) | Supported |

## Accessibility Settings Validated

- Dynamic Type (all sizes including AX1-AX5)
- Reduce Motion
- Reduce Transparency
- Increase Contrast
- Bold Text
- Differentiate Without Color
- VoiceOver
- Switch Control
- Voice Control
- Full Keyboard Access

## Usage

1. Open `accessibility-validator.md`.
2. Scroll to the bottom to the **Project Specific Context** section.
3. Replace the placeholder text with details about your app:
   - App type and target audience
   - Custom UI components used
   - Media content (video, audio, images)
   - Complex interaction patterns
   - Compliance requirements (if any)
4. Copy the entire file content.
5. Paste it into your LLM chat (Cursor, Claude, ChatGPT, etc.) while your project is open.
6. Ask the agent: *"Please audit my app for accessibility compliance."*

## Example Questions

- "Check if all my interactive elements have proper accessibility labels"
- "Audit my app's Dynamic Type support at the largest text sizes"
- "Verify color contrast ratios meet WCAG AA standards"
- "Check if my animations respect the Reduce Motion setting"
- "Review my custom components for VoiceOver compatibility"

## Testing Recommendations

After running the audit, test on a real device with:

1. **VoiceOver**: Navigate your entire app using VoiceOver
2. **Dynamic Type**: Set text size to AX5 (largest) and verify layouts
3. **Reduce Motion**: Enable and verify animations are disabled/reduced
4. **Switch Control**: Navigate using switches or Auto Scanning
5. **Accessibility Inspector**: Run Xcode's audit on your app

## References

- [Apple Human Interface Guidelines: Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)
- [WCAG 2.2 Specification](https://www.w3.org/TR/WCAG22/)
- [Apple Accessibility Programming Guide](https://developer.apple.com/documentation/accessibility)
