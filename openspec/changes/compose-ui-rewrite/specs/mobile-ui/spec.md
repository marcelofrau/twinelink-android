# mobile-ui

## ADDED Requirements

### Requirement: Compose presentation layer

The Android app SHALL render its screens with Jetpack Compose and Material 3.

#### Scenario: Launch

- **WHEN** the user opens the app
- **THEN** the main screen is a Compose screen
- **AND** it uses Material 3 theming

### Requirement: Incremental migration

Existing plugin screens SHALL be migrated to Compose without changing backend
behavior, and unmigrated screens SHALL remain functional during migration.

#### Scenario: Partially migrated build

- **WHEN** some screens are migrated and others are not
- **THEN** all screens remain reachable and functional

### Requirement: Shared design tokens

The Android UI SHALL use design tokens (color, spacing, typography, shape)
aligned with the desktop UI.

#### Scenario: Token change

- **WHEN** a token value changes
- **THEN** it is updated in one place and applied across screens
