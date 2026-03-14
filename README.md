# TYPO3 Sitekit Base Distribution — Composer-based TYPO3 base distribution

A curated base distribution for TYPO3 v13.4, providing a predefined set of
extensions for a standard Sitekit setup.

[![TYPO3](https://img.shields.io/badge/TYPO3-13.4-orange.svg)](https://typo3.org/)
[![Packagist Version](https://img.shields.io/packagist/v/oliverthiele/ot-sitekit-base-distribution.svg)](https://packagist.org/packages/oliverthiele/ot-sitekit-base-distribution)
[![PHP](https://img.shields.io/packagist/dependency-v/oliverthiele/ot-sitekit-base-distribution/php.svg)](https://php.net/)
[![License](https://img.shields.io/packagist/l/oliverthiele/ot-sitekit-base-distribution.svg)](LICENSE)
[![Changelog](https://img.shields.io/badge/Changelog-CHANGELOG.md-blue.svg)](CHANGELOG.md)

## Features

- Composer-based TYPO3 distribution
- Curated set of default extensions for a standard Sitekit setup
- Extends the official TYPO3 Base Distribution with additional packages
- Designed for modular site development with additional Sitekit extensions
- Versioned together for easier upgrades across TYPO3 versions

## Requirements

| Requirement | Version |
|-------------|---------|
| TYPO3       | ^13.4   |
| PHP         | ^8.3    |
| Composer    | ^2.0    |

## Installation

```bash
composer create-project oliverthiele/ot-sitekit-base-distribution your-project-dir
```

Or add it to an existing project:

```bash
composer require oliverthiele/ot-sitekit-base-distribution
```

## Included Extensions

| Package                         | Description                                                                                                                                                                                                                                                                          |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b13/container`                 | Container content elements                                                                                                                                                                                                                                                           |
| `friendsoftypo3/content-blocks` | Content Blocks API                                                                                                                                                                                                                                                                   |
| `helhum/typo3-console`          | Extended CLI for TYPO3                                                                                                                                                                                                                                                               |
| `ichhabrecht/content-defender`  | Restrict allowed content element types                                                                                                                                                                                                                                               |
| `oliverthiele/ot-febuild`       | Frontend build target extension                                                                                                                                                                                                                                                      |
| `oliverthiele/ot-irrebuttons`   | Additional inline relational record buttons                                                                                                                                                                                                                                          |
| `plan2net/webp`                 | Automatic WebP image conversion                                                                                                                                                                                                                                                      |
| `vlucas/phpdotenv`              | `.env` file support                                                                                                                                                                                                                                                                  |
| TYPO3 Core extensions           | backend, belog, beuser, dashboard, extbase, extensionmanager, felogin, filelist, filemetadata, fluid, fluid-styled-content, form, frontend, impexp, info, install, linkvalidator, reactions, recycler, rte-ckeditor, scheduler, seo, setup, sys-note, tstemplate, viewpage, webhooks |

## License

This project is licensed under the GNU General Public License v2.0 or later (
GPL-2.0-or-later).
See the [LICENSE](LICENSE) file for details.

## Author

Oliver Thiele — [oliver-thiele.de](https://www.oliver-thiele.de)

## Related projects

- [ot-febuild](https://github.com/oliverthiele/ot-febuild) —
  A minimal TYPO3 extension that serves as a target for Webpack-based frontend
  builds.
  It allows including compiled JS and CSS via `EXT:ot_febuild/...` paths in
  TypoScript,
  avoiding issues with `_assets/` URLs introduced in TYPO3 v12+.
