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

This alone will fail to resolve `ichhabrecht/content-defender`. Composer reads
`repositories` and stability flags **only from the root package** — the
definitions shipped in this distribution are ignored once it is installed as a
dependency. Add both to your project's own `composer.json`:

```json
{
    "require": {
        "oliverthiele/ot-sitekit-base-distribution": "^2.4",
        "ichhabrecht/content-defender": "dev-develop"
    },
    "repositories": {
        "ichhabrecht/content-defender": {
            "type": "vcs",
            "url": "https://github.com/oliverthiele/content_defender.git"
        }
    }
}
```

The explicit root requirement sets the `dev` stability flag for this single
package, which is preferable to lowering `minimum-stability` for the whole
project. Once an upstream TYPO3 v14 release of `ichhabrecht/content-defender`
is tagged, both entries can be dropped.

## Included Extensions

| Package                         | Description                                                                                                                                                                                                                                                                          |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b13/container`                 | Container content elements                                                                                                                                                                                                                                                           |
| `friendsoftypo3/content-blocks` | Content Blocks API                                                                                                                                                                                                                                                                   |
| `helhum/typo3-console`          | Extended CLI for TYPO3                                                                                                                                                                                                                                                               |
| `ichhabrecht/content-defender`  | Restrict allowed content element types                                                                                                                                                                                                                                               |
| `oliverthiele/ot-febuild`       | Frontend build target extension                                                                                                                                                                                                                                                      |
| `oliverthiele/ot-iconselector`  | Icon selection field for the TYPO3 backend                                                                                                                                                                                                                                           |
| `oliverthiele/ot-icons`         | Icon set for the Sitekit setup                                                                                                                                                                                                                                                       |
| `oliverthiele/ot-irrebuttons`   | Additional inline relational record buttons                                                                                                                                                                                                                                          |
| `plan2net/webp`                 | Automatic WebP image conversion                                                                                                                                                                                                                                                      |
| `vlucas/phpdotenv`              | `.env` file support                                                                                                                                                                                                                                                                  |
| TYPO3 Core extensions           | backend, belog, beuser, dashboard, extbase, extensionmanager, felogin, filelist, filemetadata, fluid, fluid-styled-content, form, frontend, impexp, info, install, linkvalidator, reactions, recycler, rte-ckeditor, scheduler, seo, setup, sys-note, tstemplate, viewpage, webhooks |

`ichhabrecht/content-defender` is pulled from the fork at
[oliverthiele/content_defender](https://github.com/oliverthiele/content_defender)
(`dev-develop`) until a TYPO3 v14 compatible release is tagged upstream. The
required VCS repository is already declared in `composer.json`.

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
