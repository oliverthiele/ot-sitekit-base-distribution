# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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

[Unreleased]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.3.1...HEAD
[1.3.1]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.3.0...v1.3.1
[1.3.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.2...v1.2.0
[1.1.2]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/oliverthiele/ot-sitekit-base-distribution/releases/tag/v1.0.0