## Why

The Android app UI is legacy XML/Activities and does not match the modern,
consistent experience Twine targets. The backend plugins work well; only the
presentation needs a rewrite.

## What Changes

- Introduce a Jetpack Compose + Material 3 UI shell.
- Port existing plugin screens (clipboard, files, notifications, media, input) to
  Compose without changing their backend contracts.
- Define shared design tokens aligned with the desktop UI.
- Migrate incrementally; legacy screens remain until replaced.

## Capabilities

### New Capabilities

- `mobile-ui`: the Compose-based presentation layer and its design system.

### Modified Capabilities

<!-- none: presentation only, no protocol/behavior change -->

## Impact

- Android app module UI layer; navigation; themes.
- No control-plane or protocol changes.
