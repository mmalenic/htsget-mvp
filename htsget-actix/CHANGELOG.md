# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/mmalenic/htsget-rs/compare/htsget-actix-v0.1.4...htsget-actix-v0.2.0) - 2023-04-27

### Added
- *(test)* add multiple resolvers for server tests and test resolution
- *(config)* add automatic config inference for local and s3 storage, and rearrange modules
- [**breaking**] simplify storage config by allowing untagged enum representation

### Other
- a few style changes, changed default resolver
- [**breaking**] rename `HttpTicketFormatter` and remove `UrlFormatter` implementation for it
- [**breaking**] move htsget structs to config, and resolve storage type in config

## [0.1.1](https://github.com/umccr/htsget-rs/compare/htsget-actix-v0.1.0...htsget-actix-v0.1.1) - 2023-01-27

### Other
- Set MSRV on all sub-crates (#146)
- Better CI (#98)
