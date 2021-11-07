# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v2.2.0...HEAD)

## [2.2.0] - 2021-11-07

### Changed

- Added support for Gatsby v4

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v2.1.1...v2.2.0)

## [2.1.1] - 2021-08-24

### Changed

- Updated `dts-css-modules-loader` from v1.2.2 to v1.2.4

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v2.1.0...v2.1.1)

## [2.1.0] - 2021-05-24

### Fixed

- Updated `dts-css-modules-loader` from v1.2.1 to v1.2.2, to support a breaking change in `gatsby` v3.5.1 introduced by `css-loader` v3.2.5, which leads to empty d.ts files.

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v2.0.0...v2.1.0)

## [2.0.0] - 2021-04-12

### Fixed

- If multiple `css-loader` are used in the same project (e.g. if Storybook is part of the project), it now tries to find the path to `css-loader` from gatsby's point of view, instead of the CWD.

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.2.0...v2.0.0)

## [1.2.0] - 2021-03-23

### Added

- [`dts-css-modules-loader` options](https://github.com/Megaputer/dts-css-modules-loader#options) are configurable now

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.1.3...v1.2.0)

## [1.1.3] - 2021-03-18

### Changed

- Updated information regarding replacing `gatsby-plugin-scss-typescript` and `gatsby-plugin-typescript-css-modules` in the README.md

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.1.2...v1.1.3)

## [1.1.2] - 2021-03-18

### Added

- Added basic prevention that the `dts-css-modules-loader` is attached to non-modules-stylesheets

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.1.1...v1.1.2)

## [1.1.1] - 2021-03-17

### Changed

- Changed `keywords` in `package.json` to get the plugin listed on the [Gatsby website](https://www.gatsbyjs.com/plugins/gatsby-plugin-dts-css-modules/)

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.1.0...v1.1.1)

## [1.1.0] - 2021-03-16

### Added

- Added instructions on how to replace `gatsby-plugin-typescript-css-modules`

### Removed

- Removed Gatsby v2 support

[Show all code changes](https://github.com/jens-duttke/gatsby-plugin-dts-css-modules/compare/v1.0.0...v1.1.0)

## [1.0.0] - 2021-03-15

Initial commit
