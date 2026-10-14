# AGENTS.md - twinelink-android

The Twine Android client - a hard fork of KDE Connect Android, rewritten to
Jetpack Compose. Stack: Kotlin, Jetpack Compose, Gradle 9.6, KSP, single module
(root project). Protocol identifiers stay `kdeconnect.*`.

## Upstream
`upstream` remote = KDE/kdeconnect-android. Hard fork: do NOT open upstream
merge requests.

## Build & test
- `./gradlew assembleDebug`
- `./gradlew testDebugUnitTest`
- `./gradlew lintDebug`
- Pending: `ktlint`, `detekt`, JaCoCo coverage.

## Continuity
See `twinelink-docs/docs/plan/session-log.md`.
## Working rules (all Twine repositories)
- Everything committed is in English (docs, code, comments, commits, PRs).
  The maintainer chats in Portuguese and uses a terse, compressed style.
- OpenSpec-first: every feature/fix is an OpenSpec change (proposal, specs,
  design, tasks) approved before code is written.
- Branches `feat|fix|chore`; Conventional Commits; SOLID; unit tests for new logic.
- Lint/format/static analysis per language; CI must stay green.
- Do NOT rename KDE Connect protocol identifiers (`kdeconnect.*`), the config
  directory or the DBus service (interop with stock KDE Connect).
- No performance claim without a measurement method.
