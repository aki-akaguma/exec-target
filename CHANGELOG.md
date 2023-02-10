# Changelog: exec-target

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] *
### Removed
* `COPYING`

### Changed
* refactored `Makefile`

### Fixed
* `LICENSE-APACHE`, `LICENSE-MIT`


## [0.2.8] (2023-01-31)
### Added
* `.github/workflows/test-ubuntu.yml`
* `.github/workflows/test-macos.yml`
* `.github/workflows/test-windows.yml`
* test status badges into `README.tpl`
* `rust-version = "1.56.0"` into `Cargo.toml`

### Changed
* edition: "2018" to "2021"

### Fixed
* clippy: `uninlined_format_args`, `needless_borrow`, `needless_return`
* clippy: `redundant_static_lifetimes`, `assertions_on_constants`
* bug: test result FAILED on macos

## [0.2.7] (2023-01-10)
### Changed
* bump version: 0.2.7

## [0.2.6] (2023-01-10)
### Added
* badges into `README.md`

### Changed
* reformat `CHANGELOG.md`

### Fixed
* clippy: needless_borrowed_reference

## [0.2.5] (2021-12-18)
### Changed
* `LD_LIBRARY_PATH` leaves an execution environment.

## [0.2.4] (2021-11-14)
### Added
* more documents

## [0.2.3] (2021-07-03)
### Changed
* to github.com

## 0.2.2 (2021-07-03)
### Added
* documents

### Changed
* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-cat")`
* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-env")`
* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-grep")`
* minimum support rustc 1.43.0
* remove build.rs

## 0.2.1 (2021-06-23)
### Changed
* update depend: rustc_version(0.4)

## 0.2.0 (2021-04-02)
### Changed
* update depend: rustc_version(0.3)

## 0.1.6 (2020-11-17)
### Added
* README.md, COPYING, LICENSE-APACHE, LICENSE-MIT

### Fixed
* bug: not match https in help text on test-unix

## 0.1.5 (2020-11-12)
### Added
* support rustc 1.41

### Changed
* downgrade rustc_version

## 0.1.4 (2020-05-10)
### Changed
* change edition 2015 to 2018

## 0.1.3 (2019-06-09)
### Added
* support of workspace and cargo make
* doc comments

### Removed
* remove cfg-if

### Fixed
* bug: fn fotmat_diff_add_rem()

## 0.1.2 (2019-05-30)
### Added
* test with exe-stab and cargo make support

### Changed
* switch to cargo workspace
* modify env: AsRef<OsStr>

## 0.1.1 (2018-03-22)
### Added
* exec_target_with_env_in

### Changed
* rename exec_target to exec-target
* a lot of things...

## 0.1.0 (2017-11-06)
* first commit

[Unreleased]: https://github.com/aki-akaguma/exec-target/compare/v0.2.8..HEAD
[0.2.8]: https://github.com/aki-akaguma/exec-target/compare/v0.2.7..v0.2.8
[0.2.7]: https://github.com/aki-akaguma/exec-target/compare/v0.2.6..v0.2.7
[0.2.6]: https://github.com/aki-akaguma/exec-target/compare/v0.2.5..v0.2.6
[0.2.5]: https://github.com/aki-akaguma/exec-target/compare/v0.2.4..v0.2.5
[0.2.4]: https://github.com/aki-akaguma/exec-target/compare/v0.2.3..v0.2.4
[0.2.3]: https://github.com/aki-akaguma/exec-target/releases/tag/v0.2.3
