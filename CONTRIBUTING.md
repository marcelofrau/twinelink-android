# Contributing to twinelink Android

Thanks for your interest in contributing.

## Ground Rules

- All committed artifacts (code, comments, commits, PRs) are in English.
- Protocol identifiers stay `kdeconnect.*` — interop with stock KDE Connect
  is a hard requirement. Do not rename them, the config directory, or the
  DBus service.
- Every feature or fix goes through an OpenSpec change (proposal, specs,
  design, tasks) approved before code is written. The OpenSpec store lives in
  the [twinelink-docs](https://github.com/marcelofrau/twinelink-docs)
  repository.
- Branches use `feat|fix|chore` prefixes. Commits follow
  [Conventional Commits](https://www.conventionalcommits.org/).
- New logic needs unit tests. CI must stay green
  (`assembleDebug`, `testDebugUnitTest`, `lintDebug`).
- No performance claim without a measurement method.

## Development Setup

- Android Studio (latest stable), JDK 17+, Android SDK.
- The build is a single-module Gradle project: `./gradlew assembleDebug`.

## Pull Requests

- Keep PRs focused; one concern per PR.
- Describe what changed and how it was verified (tests, device runs).
- Code review is required before merge.

## Code of Conduct

By participating you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).
