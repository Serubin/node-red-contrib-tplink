# Changelog

All notable changes to this project will be documented in this file.

Bear in mind that the [GIT version](https://github.com/caseyjhol/node-red-contrib-tplink) *(source-code)* is always bleeding edge and may *(in most cases, will)* have changes that won't reflect in NPM/[release](https://github.com/caseyjhol/node-red-contrib-tplink/releases) version.

## 1.0.1 (2022-12-28)

### Changed

- Correct documentation for startMeterEvents (https://github.com/caseyjhol/node-red-contrib-tplink/pull/59)

### Fixed

- Allow bulb to return to HSB mode from temperature mode (https://github.com/caseyjhol/node-red-contrib-tplink/pull/66)
- Resolve "Node Object is not a node-red Node Stack" error (https://github.com/caseyjhol/node-red-contrib-tplink/issues/64)

## 1.0.0 (2020-09-13)

### Changed

- Version bump

## 1.0.0-alpha.1 (2020-08-06)

### Changed

- Only log error if debug option is enabled

### Fixed

- Fix memory leak caused by failure to properly close
- Use deviceType to determine if setLedState can be used ([#33])

[#33]: https://github.com/caseyjhol/node-red-contrib-tplink/issues/33

## 1.0.0-alpha.0 (2020-07-08)

### Changed

- Upgraded to tplink-smarthome-api@3.0.0-beta
- smart-plug and smart-light combined into one node called "kasa"
- getXxxxEvents changed to startXxxxEvents
- Events output "XxxxEvents" on msg.event instead of "getXxxxEvents"
- clearEvents changed to stopAllEvents
- Node status reflects number of devices connected if more than one

### Added

- stopXxxxEvents to match the startXxxxEvents
- Multiple devices allowable per node (using msg.topic on input)
- Individual plugs on multi-plug devices can be accessed
- Polling can be turned off if not needed

## 0.4.3 (2020-06-08)

### Fixed

- getMeterInfo no longer throws an error
- getInfoEvents works again (broken in v0.3.0)
- getMeterEvents works again (broken in v0.3.0)

### Added

- Debug property to help debug issues with devices

## 0.4.2 (2020-06-05)

### Fixed

- Set payload defaults to ensure same functionality as older versions
- Fix error when passing a boolean as payload
- Fix error catching if an error is encountered while running a command

## 0.4.1 (2020-06-04)

### Fixed

- Set payload defaults to ensure same functionality as older versions

## 0.4.0 (2020-06-04)

### Added

- Errors are now catchable
- Payload property can now be set - defaults to getInfo, so it's the same as in earlier versions

### Fixed

- Support using `'|'` for passing events again
- Support setting state to switch again

## 0.3.0 (2020-06-03)

### Added

- Hue, Saturation, and Brightness (HSB) support for multicolor bulbs
- HS300 (multi-plug) support

### Changed

- Separated getPowerEvents/getInUseEvents from getPowerUpdateEvents/getInUseUpdateEvents

### Fixed

- Fix emission of online/offline events in smart-plug node

## 0.2.1

### Changed

- Resized SVG icon
- Default name when adding a new device now includes its alias (e.g. Bedroom Light - HS220)

### Fixed

- Included SVG icon in package.json to ensure it is visible

## 0.2.0

### Added

- HS220 brightness support
- Support for turning off LED status light on switches

### Changed

- Payload can now be a JSON object to allow multiple settings to be changed at once
- Updated tplink-smarthome-api to v2
- Removed separate compiled files (moved files into nodes folder)
- Use SVG for icon instead of PNG

### Fixed

- Fix metering messages for plugs

### Breaking

- npm minimum version changed to v3.0.0
- node minimum version changed to v10.0.0

## 0.1.8 - Unreleased

### Added

- This file.
- Get most common info with **`getQuickInfo`** - *such as cloud account, power state, power consumption,  schedule, and many more*.
- **Filetree** hardcoded in `package.json` *(GIT builds clean now)*.
- Google **compiled code** in main `.js` files and formatted code in `.bak.js` files *- harder, better, faster, stronger*.

### Changed

- Fixed some typos *( @rajamalw )*.
- Commands sanity for `brightness` and `temperature` *- won't trigger unless device supports it ( @rajamalw )*.
- Updated documentation.

### Removed

Nothing but bad vibes.