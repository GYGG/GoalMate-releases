# GoalMate Desktop Changelog

This repository hosts signed and notarized GoalMate desktop release artifacts.

Dates are in UTC. Each version links to the public GitHub release that contains the macOS DMG, ZIP, blockmaps, and `latest-mac.yml` update metadata.

## 0.1.8 - 2026-07-10

Release: [GoalMate 0.1.8](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.8)  
Source: [GYGG/GoalMate@7351730](https://github.com/GYGG/GoalMate/commit/73517301674d26a7dbc8521b91a18bc8b24632df)

### Added

- Global floating Runtime Chat entry that follows the Multica-style chat experience.
- Runtime Chat sessions that use `goalmatecli` context so GoalMate Agent can answer across Goals, ActivityEvents, and local GoalMate state.
- Chat rendering for assistant reasoning, tool calls, tool results, quick prompts, file/image attachments, and compact composer interactions.

### Changed

- Chat is no longer locked to a single selected Goal; it is a global assistant surface for GoalMate-supported agents.
- Qoder and QoderWork Runtime settings entries are hidden until their chat runtime path is fully proven.
- Desktop application version is bumped to `0.1.8`.

### Fixed

- Packaged the bundled OpenCode Bun single-file runtime as an archive and extracted it into user data at runtime.
- Avoided macOS notarization failures from unsigned embedded Runtime executables while also preventing code-signing mutation from breaking the Bun runtime.
- Added release workflow archive checks to verify the bundled Runtime before publishing.

### Release Artifacts

- `GoalMate-0.1.8-arm64.dmg`
- `GoalMate-0.1.8-arm64.zip`
- `GoalMate-0.1.8-arm64.dmg.blockmap`
- `GoalMate-0.1.8-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.7 - 2026-07-08

Release: [GoalMate 0.1.7](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.7)  
Source: [GYGG/GoalMate@140ac28](https://github.com/GYGG/GoalMate/commit/140ac286901b28ba0de1dcc1b6b32724ea7c47bd)

### Fixed

- Reduced packaged app startup memory pressure by streaming and bounding activity archive loading.
- Kept archived ActivityEvents and attribution records bounded when merging them into desktop state.
- Refreshed the signed desktop package after validating startup against real local activity data.
- Made release artifact upload non-blocking so published assets are not treated as failed solely because of GitHub artifact quota.

### Release Artifacts

- `GoalMate-0.1.7-arm64.dmg`
- `GoalMate-0.1.7-arm64.zip`
- `GoalMate-0.1.7-arm64.dmg.blockmap`
- `GoalMate-0.1.7-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.6 - 2026-07-08

Release: [GoalMate 0.1.6](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.6)  
Source: [GYGG/GoalMate@b5be17a](https://github.com/GYGG/GoalMate/commit/b5be17acf36e2f756986d093e29f73c0f433be49)

### Added

- Public GoalMate CLI surface for `help`, `goal`, and `activity`.
- `goal list`, `goal get`, `goal create`, `goal update`, and `goal delete` commands for AI Coding Agent access.
- `activity list` and `activity get` commands with compact semantic output, goal filtering, date range filtering, and explicit expansion flags.
- Dedicated Settings page for the CLI, including install, reinstall, and status refresh actions.
- CLI install status feedback in Settings, including checking state and the resolved installed path.
- Packaged CLI wrapper that runs through Electron Node mode so CLI calls do not briefly activate the macOS app UI.

### Changed

- Activity CLI output now exposes semantic evidence pointers by default instead of raw event payloads.
- `goal get` returns `progressBriefs` and `relatedActivities` to keep progress and activity evidence distinct.
- `daily-evidence` remains internal and is not exposed as a public CLI command.
- Beta packaging now includes the same CLI resource helper as release packaging.

### Release Artifacts

- `GoalMate-0.1.6-arm64.dmg`
- `GoalMate-0.1.6-arm64.zip`
- `GoalMate-0.1.6-arm64.dmg.blockmap`
- `GoalMate-0.1.6-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.5 - 2026-07-08

Release: [GoalMate 0.1.5](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.5)  
Source: [GYGG/GoalMate@713defd](https://github.com/GYGG/GoalMate/commit/713defd5a29722a09d201ad0c074a3c482ab418c)

### Changed

- Bumped the desktop application version to `0.1.5`.
- Integrated the activity and goal integrity release work.
- Improved Settings auxiliary status refresh behavior.
- Split and cached runtime status checks to reduce repeated Settings-page latency.
- Kept beta package identity aligned with the regular GoalMate app identity.

### Release Artifacts

- `GoalMate-0.1.5-arm64.dmg`
- `GoalMate-0.1.5-arm64.zip`
- `GoalMate-0.1.5-arm64.dmg.blockmap`
- `GoalMate-0.1.5-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.4 - 2026-07-06

Release: [GoalMate 0.1.4](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.4)  
Release workflow source: [GYGG/GoalMate@61e1b59](https://github.com/GYGG/GoalMate/commit/61e1b5997c21b74c325f8f5806f2755a9fe31a55)

### Fixed

- Improved packaged app startup reliability around icon loading.
- Reduced startup rendering friction for local validation packages.

### Release Artifacts

- `GoalMate-0.1.4-arm64.dmg`
- `GoalMate-0.1.4-arm64.zip`
- `GoalMate-0.1.4-arm64.dmg.blockmap`
- `GoalMate-0.1.4-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.3 - 2026-07-05

Release: [GoalMate 0.1.3](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.3)  
Release workflow source: [GYGG/GoalMate@9394635](https://github.com/GYGG/GoalMate/commit/93946355fcaaa419b4b8da9e8dc790a0039daadc)

### Fixed

- Avoided collector port conflicts blocking the main window.
- Improved packaged app startup behavior for desktop validation.

### Release Artifacts

- `GoalMate-0.1.3-arm64.dmg`
- `GoalMate-0.1.3-arm64.zip`
- `GoalMate-0.1.3-arm64.dmg.blockmap`
- `GoalMate-0.1.3-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.2 - 2026-07-05

Release: [GoalMate 0.1.2](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.2)  
Release workflow source: [GYGG/GoalMate@8d88bba](https://github.com/GYGG/GoalMate/commit/8d88bbabb3b5f1b7092256b0a4b4b23051b440d7)

### Fixed

- Fixed packaged app IPC registration race conditions.
- Improved app startup order for signed desktop builds.

### Release Artifacts

- `GoalMate-0.1.2-arm64.dmg`
- `GoalMate-0.1.2-arm64.zip`
- `GoalMate-0.1.2-arm64.dmg.blockmap`
- `GoalMate-0.1.2-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.1 - 2026-07-05

Release: [GoalMate 0.1.1](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.1)  
Release workflow source: [GYGG/GoalMate@1650d37](https://github.com/GYGG/GoalMate/commit/1650d37faceb751dccb1670d9508feff46e8b766)

### Changed

- Prepared the next signed desktop validation package.
- Continued validating the GitHub release artifact flow for GoalMate desktop updates.

### Release Artifacts

- `GoalMate-0.1.1-arm64.dmg`
- `GoalMate-0.1.1-arm64.zip`
- `GoalMate-0.1.1-arm64.dmg.blockmap`
- `GoalMate-0.1.1-arm64.zip.blockmap`
- `latest-mac.yml`

## 0.1.0 - 2026-07-03

Release: [GoalMate 0.1.0](https://github.com/GYGG/GoalMate-releases/releases/tag/v0.1.0)

### Added

- Initial public signed and notarized macOS desktop release for GoalMate.
- Auto-update metadata via `latest-mac.yml`.
- DMG and ZIP distribution artifacts for Apple Silicon Macs.

### Release Artifacts

- `GoalMate-0.1.0-arm64.dmg`
- `GoalMate-0.1.0-arm64.zip`
- `GoalMate-0.1.0-arm64.dmg.blockmap`
- `GoalMate-0.1.0-arm64.zip.blockmap`
- `latest-mac.yml`
