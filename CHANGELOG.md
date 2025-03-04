# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.8.0] - 2021-09-03
### Added
- Add a configuration file ([#5](https://github.com/orhun/gpg-tui/issues/5))
- Support global locations for the configuration file
- Check `GPG_TUI_CONFIG` environment variable for config file
- Add manpage for the configuration file (`gpg-tui.toml.5`)
- Add `:style` command for changing styles

### Changed
- Add `libxkbcommon-dev` as build dependency for CI/CD
- Rename the shell completions binary
- Use the correct name for completions binary
- Update the example shell completions command
- Update README.md about the configuration file
- Update CI/CD to build and publish Docker images
- Bump the Rust version in Dockerfile
- Bump dependencies

### Fixed
- Disable tests for the completions binary
- Build only the main binary in Dockerfile
- Update the build dependencies for the docker image

## [0.7.4] - 2021-08-07
### Added
- Add config for splash screen to check SHA256 hash of assets

### Changed
- Bump `rust-embed` to `6.0.0`
- Bump `tui` to `0.16.0`
- Bump `gpgme` to `0.10.0`
- Center the options menu title

### Fixed
- Mark the unsupported algorithms as unrecognized/unknown
- Fix the failing test about options menu title

## [0.7.3] - 2021-07-25
### Added
- Add Wayland clipboard support (#30)
- Add 'in the media' section to README.md

### Changed
- Import the test key from keyserver in CI workflow

### Fixed
- Handle clipboard errors

## [0.7.2] - 2021-07-20
### Added
- Add the missing views for signature notations

### Changed
- Mark the default signing key with a symbol

### Fixed
- Override the default key for all gpg fallback commands
- Sleep the event handler thread if input is disabled (#29)

## [0.7.1] - 2021-07-17
### Added
- Add an example for selection mode to README.md

### Changed
- Update README.md about `libxkbcommon-dev` dependency (#26)

### Fixed
- Run the terminal on stderr and use stdout for output (#27)

## [0.7.0] - 2021-07-07
### Added
- Add `--select` option (#24)

### Changed
- Extend the FromStr implementation of CopyType
- Rename clipboard module and CopyType struct to 'selection'

## [0.6.2] - 2021-06-27
### Changed
- Bump the Rust version in Dockerfile
- Use entrypoint for the docker container
- Update the docker command for quickly launching the app

## [0.6.1] - 2021-06-26
### Changed
- Run the container as non-root/dedicated user
- Update the docker alias in README.md

## [0.6.0] - 2021-06-25
### Added
- Support importing keys from the clipboard (#3)
- Add git-cliff configuration file

### Changed
- Update the keyserver link

### Fixed
- Apply clippy lints
- Update application command tests

## [0.5.0] - 2021-06-13
### Added
- Support setting the default signing key via options menu

### Changed
- Update Dockerfile about crate dependency location
- Update COMMANDS.md about getting/setting default signing key
- Update README.md about setting the default signing key

## [0.4.1] - 2021-06-09
### Fixed
- Expand tilde character to the home directory (fixes #22)

## [0.4.0] - 2021-06-07
### Changed
- Extract get_output_file from export_keys method
- Support exporting secret subkeys (#15)
- Update COMMANDS.md about export command
- Update README.md about exporting secret subkeys

## [0.3.0] - 2021-06-05
### Added
- Add packaging status badge to README.md
- Add Matrix room link to social media section in README.md

### Changed
- Display notations of the signatures (#8)
- Update README.md about Docker alias
- Update README.md about the format of notations
- Update the example notation in README.md
- Update the style of flags

### Fixed
- Run container process as unprivileged user

## [0.2.0] - 2021-06-02
### Added
- Add installation instructions for FreeBSD
- Add Homebrew instructions to README.md
- Add NetBSD instructions to README.md

### Changed
- Update table of contents
- Support xplr for file selection (closes #2)
- Use eprintln macro while printing errors
- Update README.md about the use of xplr

## [0.1.5] - 2021-05-31
### Added
- Add dependency installation instructions for Void Linux (#11)

### Changed
- Mention distribution-specific dependencies in README.md (#10)
- Update the formatting of requirements in README.md
- Update README.md about installation for Arch Linux

## [0.1.4] - 2021-05-29
### Removed
- Remove cargo-bloat workflow

## [0.1.3] - 2021-05-29
### Added
- Add Arch Linux installation instructions to README.md

### Changed
- Update the commands style in README.md
- Update link checker job to exclude AUR links
- Split audit workflow into two

## [0.1.2] - 2021-05-29
### Fixed
- Mark test_gpg_key as gpg-tests
- Test the detail commands if gpg-tests feature is enabled

## [0.1.1] - 2021-05-28
### Added
- Add release badges to README.md
- Add CD badge to README.md
- Add documentation badge to README.md

### Changed
- Use release flag while generating completions
- Update the release image
- Update documentation field in Cargo.toml
- Update Patreon badges in README.md
- Update CD workflow about the HTML syntax of release images
- Update FUNDING.yml

## [0.1.0] - 2021-05-28
Initial release.
