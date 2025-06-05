# TYPO3 Sitekit Base Distribution

This package provides a base distribution for the TYPO3 Sitekit ecosystem.
It installs a predefined set of extensions and configurations used in my
standard TYPO3 setup.

It serves a similar purpose to the official **TYPO3 CMS Base Distribution**,
but includes additional extensions and is intended to simplify development
and upgrades.

The Sitekit is developed for TYPO3 v13.4 and is designed as a modular,
upgradable structure. All included extensions are versioned together,
making it easier to upgrade to newer TYPO3 versions.

## Features

- Composer-based TYPO3 distribution
- Includes curated default extensions
- Additional extensions compared to the TYPO3 Base Distribution
- Suitable as a base for TYPO3 projects
- Supports easy upgrades across TYPO3 versions
- Designed for modular site development using additional Sitekit extensions
- Ready for TYPO3 v13.4 and newer


## Installation

You can install this distribution via Composer:

```bash
composer require oliverthiele/ot-sitekit-base-distribution
```

## License

This project is licensed under the GNU General Public License v2.0 or later
(GPL-2.0-or-later).
See the LICENSE file for details.


## Related projects

- [ot-febuild](https://github.com/oliverthiele/ot-febuild) –
  A minimal TYPO3 extension that serves as a target for Webpack-based frontend
  builds. It allows you to include compiled JS and CSS via `EXT:ot_febuild/...`
  paths in TypoScript, which avoids issues with `_assets/` URLs introduced in
  TYPO3 v12+. Useful when you want to keep build artifacts out of
  version control and separate from your sitepackage.
