## Context

KDE Connect Android uses XML layouts and Activities. Twine adds a remote desktop
client and Wake-on-LAN and needs a UI that can host them cleanly and match the
desktop design language.

## Decisions

### D1: Compose + Material 3

Chosen for a modern, maintainable, testable UI and adaptive layouts.

### D2: Incremental migration

Screens are ported one at a time; the app stays shippable throughout.

### D3: Shared tokens

A small token set (color, spacing, typography, shape) is shared conceptually with
the desktop UI so the two platforms stay visually consistent.

## Alternatives considered

- **Keep XML/Views.** Rejected: poor fit for the new features and design goals.
- **Rewrite everything (incl. backend) at once.** Rejected: high risk, no need.

## Risks / Trade-offs

- Maintaining two UI systems during migration: mitigated by migrating the
  highest-traffic screens first.

## Migration

Screens migrate in priority order; no data or pairing migration required.
