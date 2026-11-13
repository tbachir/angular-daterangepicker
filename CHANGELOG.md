# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This file was reconstructed from the git history (tags and commit messages), so
entries are summaries by theme and may not list every commit.

> **Note on coverage:** the history available locally starts at tag `0.1.5`
> (2014-06-16), because the repository clone is shallow. Anything earlier than
> that is not covered here. There is no `0.1.6` tag in the repository.

## [Unreleased]

Changes made after `0.2.2` and not yet tagged.

### Added
- CommonJS compatibility (#190).
- README: a block with options examples (#239) and instructions on how to
  change the date format (#240).
- README: "Maintainer needed!" notice, updated list of contributors and
  clarified instructions on how to send pull requests.

### Changed
- Dependencies in `package.json` now match those in `bower.json`.
- Merged pull requests #209, #219, #226 and #227.

### Fixed
- Exception when the model variable is undefined.
- Parser now uses start/end of day for dates.
- `dateRangePickerConfig` is deep-copied instead of being shared.
- The `applyClass` option now works (#244).
- README example corrected according to issue #234 (#235).

## [0.2.2] - 2015-12-05

### Fixed
- Model update not being applied.
- The `opts` object is updated when the model date is set (#129, #133).
- Model is set properly when using `singleDatePicker`.
- Input showing "invalid date".

### Changed
- Demo updated.

## [0.2.1] - 2015-11-08

### Fixed
- Single dates are stored as a Date object, without `startDate`/`endDate`
  properties, and are no longer returned as an empty string (#111, #116).
- coffeelint errors.

### Changed
- Multiple event binding code revised in CoffeeScript.
- README: throughput graph added.
- Rebuilt `dist` files; configs and contributors list updated.

## [0.2.0] - 2015-10-11

### Added
- `CONTRIBUTORS.md`.
- README: version compatibility notes.
- `coffeelint` Grunt task; `angular-messages` is now a devDependency.

### Changed
- Upgraded to bootstrap-daterangepicker 2.0 (#103), with updates to better
  follow the Angular `ngModelController` flow.
- Locale and options are now merged with a custom `mergeOpts` function.
- Event callbacks run in `$evalAsync` (#101).
- README updates.

### Fixed
- Deep watch on the `options` attribute, so property changes trigger the
  `$watch` handler (#96).

## [0.1.17] - 2015-08-14

### Fixed
- `clearable` option (#85).

## [0.1.16] - 2015-06-14

### Added
- `clearable` option (#72, #73), with an example in `example.html`.
- README: build command and instructions for event handler support (#71).

### Changed
- CoffeeScript formatting unified.

## [0.1.15] - 2015-06-07

### Added
- Easy way to attach event handlers to the picker (#62, #70).

### Fixed
- The picker is only removed when the dropdown was initialized (#63).
- `_picker` is set earlier so an old instance is not kept (#68).
- Issue #58 (#60).

### Changed
- README: preferred way of submitting pull requests.

## [0.1.14] - 2015-05-26

### Fixed
- Bug in initialization: check whether `_picker` is already defined (#57).

### Changed
- The example uses the non-minified version.

## [0.1.13] - 2015-05-24

Merges a batch of pull requests from upstream forks (#38, #39, #48, #51, #54).

### Added
- Watch on `ngModel` to reset start and end dates when changed by code.
- `coffeelint.json`; code reformatted.
- Label is also appended to the scope.

### Changed
- Uses bootstrap-daterangepicker with datepicker 1.3.21.
- Options are watched more deeply.
- Options passed to the directive are collected into `customOpts`.
- License clarified.
- README typo fixes.

### Fixed
- `endDate` is kept on or after `startDate`.
- Dates are no longer converted from moment to `Date` when set.
- `data('daterangepicker')` being undefined (#35).

## [0.1.12] - 2015-02-12

### Added
- Support for the `singleDatePicker` option (#24).

### Fixed
- A clean config is used for each picker, and the directive cleans up after
  itself when the scope is destroyed (#26, #32).
- Uses a newer bootstrap-daterangepicker version.

## [0.1.11] - 2014-12-16

### Changed
- AngularJS dependency resolution changed to `^`.
- Change suggested in #17.

## [0.1.10] - 2014-10-28

### Added
- ngAnnotate introduced; Grunt tasks are loaded automatically.

### Changed
- Dependencies upgraded.

### Fixed
- Options not correctly initialized (#15, #16).

## [0.1.9] - 2014-10-09

### Changed
- Forward compatibility with AngularJS 1.3.0 (#9), tested with 1.3.0-rc.5.
- Keeps up with the latest Bootstrap and daterangepicker.

### Fixed
- Paths to moment and jQuery in `example.html`.

## [0.1.8] - 2014-07-05

### Changed
- Uses wiredep for dependencies.
- Uses a callback instead of the `apply.daterangepicker` event, which only
  fires when the Apply button is pressed and so missed custom ranges (#6).

## [0.1.7] - 2014-06-27

### Fixed
- Better keyboard input behaviour.
- `bower.json` points to the non-minified version.

## [0.1.5] - 2014-06-16

Earliest release available in the local history.

[Unreleased]: https://github.com/fragaria/angular-daterangepicker/compare/0.2.2...HEAD
[0.2.2]: https://github.com/fragaria/angular-daterangepicker/compare/0.2.1...0.2.2
[0.2.1]: https://github.com/fragaria/angular-daterangepicker/compare/0.2.0...0.2.1
[0.2.0]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.17...0.2.0
[0.1.17]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.16...0.1.17
[0.1.16]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.15...0.1.16
[0.1.15]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.14...0.1.15
[0.1.14]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.13...0.1.14
[0.1.13]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.12...0.1.13
[0.1.12]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.11...0.1.12
[0.1.11]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.10...0.1.11
[0.1.10]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.9...0.1.10
[0.1.9]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.8...0.1.9
[0.1.8]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.7...0.1.8
[0.1.7]: https://github.com/fragaria/angular-daterangepicker/compare/0.1.5...0.1.7
[0.1.5]: https://github.com/fragaria/angular-daterangepicker/releases/tag/0.1.5
