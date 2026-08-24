# TYPO3 Sitekit Base Distribution — Composer-based TYPO3 base distribution

A curated base distribution for TYPO3 v14.3, providing a predefined set of
extensions for a standard Sitekit setup.

[![TYPO3](https://img.shields.io/badge/TYPO3-14.3-orange.svg)](https://typo3.org/)
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
| TYPO3       | ^14.3   |
| PHP         | ^8.4    |
| Composer    | ^2.0    |

## Installation

### As a new project

```bash
composer create-project oliverthiele/ot-sitekit-base-distribution your-project-dir
```

This composer.json becomes the root package, so no further setup is needed.

### In an existing project

```bash
composer require oliverthiele/ot-sitekit-base-distribution
```

Every dependency resolves from Packagist, so the project's own `composer.json`
needs no additional `repositories` entry and no stability flag.

## Included Extensions

| Package                         | Description                                                                                                                                                                                                                                                                          |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b13/container`                 | Container content elements                                                                                                                                                                                                                                                           |
| `friendsoftypo3/content-blocks` | Content Blocks API                                                                                                                                                                                                                                                                   |
| `helhum/typo3-console`          | Extended CLI for TYPO3                                                                                                                                                                                                                                                               |
| `oliverthiele/ot-febuild`       | Frontend build target extension                                                                                                                                                                                                                                                      |
| `oliverthiele/ot-iconselector`  | Icon selection field for the TYPO3 backend                                                                                                                                                                                                                                           |
| `oliverthiele/ot-icons`         | Icon set for the Sitekit setup                                                                                                                                                                                                                                                       |
| `oliverthiele/ot-irrebuttons`   | Additional inline relational record buttons                                                                                                                                                                                                                                          |
| `plan2net/webp`                 | Automatic WebP image conversion                                                                                                                                                                                                                                                      |
| `vlucas/phpdotenv`              | `.env` file support                                                                                                                                                                                                                                                                  |
| TYPO3 Core extensions           | backend, belog, beuser, dashboard, extbase, extensionmanager, felogin, filelist, filemetadata, fluid, fluid-styled-content, form, frontend, impexp, info, install, linkvalidator, reactions, recycler, rte-ckeditor, scheduler, seo, setup, sys-note, tstemplate, viewpage, webhooks |

Restricting the allowed content element types per backend layout column no
longer needs `ichhabrecht/content-defender`. TYPO3 v14.1 covers it in the core
(feature #108623, which also reads content_defender's `allowed.CType` syntax),
and `b13/container` handles its own container columns from 4.1 onwards —
including `maxitems`, which the core does not provide. `b13/container` is
therefore required at `^4.1`.

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
