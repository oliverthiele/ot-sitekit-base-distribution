# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.4.0] — 2026-07-30

### Added

- Add `oliverthiele/ot-icons` at `^2.1`
- Add `oliverthiele/ot-iconselector` at `^1.0`
- Re-add `ichhabrecht/content-defender` at `dev-develop`, sourced from the VCS repository
  `https://github.com/oliverthiele/content_defender.git` until a TYPO3 v14 compatible release is tagged

### Changed

- Update `oliverthiele/ot-irrebuttons` from `^4.0` to `^4.1`
- Pin `typo3/coding-standards` (dev) from `dev-main` back to `^0.9`
- Update README: list the newly added packages, drop the now empty
  "Temporarily removed extensions" section (`plan2net/webp` is back since 2.1.0),
  and document the extra root-level `repositories` and requirement entries needed
  when installing the distribution into an existing project

---

## [2.3.0] — 2026-07-22

### Changed

- Update `friendsoftypo3/content-blocks` from `^2.3` to `^2.4`
- Update `helhum/typo3-console` from `^8.3.1` to `^9.0`
- Update `plan2net/webp` from `^14.4` to `^14.8`
- Relax `vlucas/phpdotenv` from `^5.6.3` to `^5.6`
- Update `typo3/coding-standards` (dev) from `^0.8.0` to `dev-main`
- Extend `.editorconfig` TS/JS ruleset to also apply to `.vue` files
- Remove redundant `config.platform.php` pin (`8.4.0`) — `require.php: ^8.4` already covers PHP 8.4 and 8.5

---

## [2.2.0] — 2026-05-22

### Changed

- Upgrade `b13/container` from `^3.2.3` to `^4.0` — fixes drag & drop into containers in TYPO3 v14 (new Core `DataHandlerContentElementRestrictionHook`)

---

## [2.1.0] — 2026-05-19

### Added

- Re-add `plan2net/webp` at `^14.4` — TYPO3 v14 compatible release is now available

### Changed

- Update `.editorconfig` to match current TYPO3 Core configuration

---

## [2.0.0] — 2026-04-26

### Changed

- Raise TYPO3 core packages to `^14.3`
- Raise PHP requirement and platform version to `^8.4`
- Raise `friendsoftypo3/content-blocks` to `^2.3.1`

### Removed

- Temporarily remove `ichhabrecht/content-defender` because no TYPO3 v14 compatible release is available yet
- Temporarily remove `plan2net/webp` because no TYPO3 v14 compatible release is available yet

---

## [1.3.1] — 2026-04-25

### Fixed

- Downgrade `friendsoftypo3/content-blocks` to `^1.5.1` —
  v2.3.1 requires TYPO3 v14.3 and is incompatible with this v13 distribution

---

## [1.3.0] — 2026-04-25

### Changed

- Raise `oliverthiele/ot-irrebuttons` constraint to `^4.0`
- Raise PHP platform to `^8.4`

---

## [1.2.0] — 2026-03-14

### Added

- Added `php: ^8.3` to `require` section for explicit PHP version constraint

### Changed

- PHP platform requirement raised from 8.2 to 8.3
- Removed `v` prefix from all version constraints for consistency with Composer standard
- Sorted `require` packages alphabetically
- Added README and CHANGELOG following project documentation standards

## [1.1.2] — 2025-11-29

### Changed

- Updated package versions in project configuration

## [1.1.1] — 2025-10-13

### Added

- Added EditorConfig for consistent coding style

### Changed

- Updated dependency version constraints

## [1.1.0] — 2025-10-13

### Fixed

- Updated image processing library dependency (plan2net/webp)

### Changed

- Updated dependency versioning for better stability

## [1.0.0] — 2025-06-05

### Added

- Initial release with curated set of extensions for TYPO3 v13.4 Sitekit setup

[Unreleased]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v2.3.0...HEAD
[2.3.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v2.2.0...v2.3.0
[2.2.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v2.1.0...v2.2.0
[2.1.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.3.1...v2.0.0
[1.3.1]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.3.0...v1.3.1
[1.3.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.2...v1.2.0
[1.1.2]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/releases/tag/v1.0.0
