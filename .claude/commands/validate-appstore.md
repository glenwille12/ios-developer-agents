---
description: Validate iOS app against App Store Review Guidelines
argument-hint: Optional path to specific files to check
---

Run the iOS App Store Validator agent on this project.

First, read the full agent prompt from `agents/app-store-validator/app-store-validator.md` in this repository.

Then analyze this iOS project following the validation process in that prompt:

1. Fetch current App Store Review Guidelines
2. Scan technical configuration (Info.plist, Privacy Manifest, entitlements)
3. Validate metadata requirements
4. Check privacy and legal compliance
5. Validate in-app purchases if applicable

Provide the structured output format specified in the agent prompt.

$ARGUMENTS
