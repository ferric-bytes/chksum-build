# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.3] - 2023-01-02

### Changed

- Changed `cargo:rust-env` to use quotes.
- Changed years range in license file.

### Fixed

- Fixed treating version channel as stable one.

## [0.0.2] - 2022-12-28

### Added

- Added *unsafe forbidden* badge.
- Added *MSRV* badge.

### Changed

- Disabled code coverage for internal `info` module.
- Added logos to README badges.
- Changed comments in TOML code examples.
- Changed documentation headers.
- Changed README headers.

### Fixed

- Replaced status badge (check [badges/shields#8671](https://github.com/badges/shields/issues/8671) for more informations).

## [0.0.1] - 2022-12-14

### Added

- Added tests with MSRV toolchain in Rust workflow.

### Changed

- Replaced branch checks state with workflow status for branch.

### Fixed

- Fixed coverage job in Rust workflow.
- Fixed lifetimes for constant `str`s.
- Fixed MSRV to `1.58.0`.
- Fixed Cargo build script commands (misspelled `rustup` instead of `rustc`).

### Removed

- Removed `strip` option for release profile.
- Removed tests with `beta` toolchain in Rust workflow.

## [0.0.0] - 2022-11-27

### Added

- Initial release.

[0.0.3]: https://github.com/ferric-bytes/chksum-build/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/ferric-bytes/chksum-build/compare/v0.0.1...v0.0.2
[0.0.1]: https://github.com/ferric-bytes/chksum-build/compare/v0.0.0...v0.0.1
[0.0.0]: https://github.com/ferric-bytes/chksum-build/releases/tag/v0.0.0
