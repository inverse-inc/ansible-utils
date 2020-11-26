# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- Role `wpa_supplicant` Allow to manage state of wpa_supplicant service
- Role `hostap` host access point daemon
- Role `restserver` to enable HTTP API service
- Playbook `venom` from [packetfence collection](https://github.com/inverse-inc/ansible-packetfence)
- Role modules should be in `plugins` directory in place of `library` directory
- Import and lint of domain-setup and adcs-enrollment roles from
  [upstream ansible-windows repository](https://github.com/jborean93/ansible-windows)

## [1.1.0] - 2020-09-22

### Added
- Role `mailhog` to catch mails sent by PacketFence server

## [1.0.0] - 2020-08-18

### Added
- Role `psonoci` to get secrets from a Psono server
- Role `venom` to run integration tests against PacketFence server

[Unreleased]: https://github.com/inverse-inc/ansible-utils/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/inverse-inc/ansible-utils/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/inverse-inc/ansible-utils/releases/tag/v1.0.0
