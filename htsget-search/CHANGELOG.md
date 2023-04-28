# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/mmalenic/htsget-rs/compare/htsget-search-v0.1.4...htsget-search-v0.2.0) - 2023-04-27

### Added
- *(test)* add multiple resolvers for server tests and test resolution
- use serve_at in data server rather than a constant
- *(config)* add automatic config inference for local and s3 storage, and rearrange modules
- [**breaking**] simplify storage config by allowing untagged enum representation

### Other
- *(search)* add additional tests for searching resolvers and from storage
- *(search)* implement `ResolveResponse` on `HtsGetFromStorage`
- [**breaking**] rename `HttpTicketFormatter` and remove `UrlFormatter` implementation for it
- [**breaking**] move htsget structs to config, and resolve storage type in config

## [0.1.1](https://github.com/umccr/htsget-rs/compare/htsget-search-v0.1.0...htsget-search-v0.1.1) - 2023-01-27

### Fixed
- fixes for byte range ends
- fix IOError name
- fixes & model improvements & bam search progress
- fixes & model improvements & bam search progress
- fix docs

### Other
- Set MSRV on all sub-crates (#146)
- Better CI (#98)
- Merge branch 'main' of https://github.com/umccr/htsget-rs into more-flexible-config-rename
- add test for long resolvers from environment variable config
- clippy and fmt
- allow specifying tags, reference names, fields with an 'All' value
- reduce some options for cors, remove repeated code when configuring cors
- fix tests affected by config, change some default values and move around config options
- apply changes to other crates from reworked config
- deserialize empty string as None value
- move cors config to separate file
- fix errors relating to new config
- add tests for checking for contained value in interval
- add safe cast for conversion between i64 and u64
- move fields, tags, no tags, query, and interval to config
- Make search structs public
- Remove ReferenceSequenceInfo
- Remove unused code and logic
- Add tests for no end position
- Remove requirement for default end position when converting to noodles interval
- Merge branch 'main' of https://github.com/umccr/htsget-rs into exports
- Export some functions for use as a dependency
- Re-export htsget-config as a dependency from other crates
- Update non-noodles dependencies
- Http and tls server test uses test utils
- Convert preflight server test to test utils
- Convert data server test to use test utils
- Implement http test traits for data server
- Add CorsLayer responses to htsget-http-lambda
- Move configure_cors to module file
- Bump deps for noodles and simplify logic around maximum reference sequence length using new noodles types
- List out allowed methods rather than sending wildcard
- Add ticket server cors tests
- Add cors options request test
- Fix tests implementation
- Can't use base directory function in test
- Implement additional cors test
- Add base path only function in tests for code reuse
- Add cors tests
- Layer should go after merge
- Implement cors for data server
- Rename ticket server to data server
- Move data server config to separate struct
- Implement cors for htsget-http-actix.
- Changes to deployment (#116)
- Remove some trace log details to avoid making them overly long.
- Add more detail to gzi traces.
- Add more spans and tracing calls.
- Add buffered reading to bai and gzi.
- Add buffered reading to cram search.
- Remove logging chunks as it is too noisy.
- Emit trace logs from functions.
- Add some more instrument targets, use span in_scope.
- Remove sleep call.
- Add a few more tracing span targets.
- Add span tracing to test timings.
- Small changes related to indices (#114)
- Bump dependencies, fix clippy warnings.
- Avoid reading index unless it is required.
- Remove some unnecessary unwraps.
- Improve errors so that they are more informative.
- Remove RangeBounds on BytesPosition as its use is less readable with classes.
- Fix tests related to response class.
- Remove headers from response if empty.
- Simplify JsonUrl logic.
- Responses should contain a class for all ranges, or no ranges.
- Fix tests.
- Implement RangeBounds for BytesPosition.
- Perform byte position merging when creating data blocks.
- Byte position records class, Header for only header bytes, Body for only body bytes, and None if there is a mix of bytes.
- Allow BytesPosition to record its own class.
- Fix unneseccary storage queries (#107)
- Simplify querying for all records by determining file size.
- Server benchmarks should use non-tls ticket server as this is a fairer comparison to the htsget-refserver.
- Clean up code, format, update dependencies.
- Tests run independently by using dynamic port allocation.
- The GC info field should have a Float type rather than an Integer type.
- Implement non-tls ticket server alongside tls ticket server.
- Rename some traits and structs to clarify their purpose.
- Bump many deps (except querymap) and avoid pulling full tokio in, we just need macros and rt-multi-thread (#96)
- Out of order urls (#95)
- Pinning to noodles-tabix =0.9.0 as suggested in https://github.com/zaeleus/noodles/issues/90#issuecomment-1150361623 as a result of getting CI errors on https://github.com/umccr/htsget-rs/runs/6803593182?check_suite_focus=true#step:6:90
- Fix eof errors (#87)
- Add benchmarks (#59)
- Fix localstorage path (#86)
- Fix tests and errors (#83)
- Deploy htsget-http-lambda. (#81)
- Enable choosing between storage types. (#80)
- Remove file from localstorage (#79)
- Spawn s3-server once so that tests don't have to be run on one thread. (#78)
- Remove blocking (#77)
- Htsget http lambda (#76)
- Storage class for s3 (#74)
- Decouple File struct from Search trait. (#70)
- Fix runtime panics from curl (#69)
- Bump all tokio versions and stay on track with Noodles versioning instead of working from its git /cc @andrewpatto
- Implement id resolver (#60)
- Convert Storage and HtsGet traits to use async/await (#56)
- Bump up noodles across crates, otherwise several versions get mixed up
- Add the service info endpoints (#54)
- Add the htsget-http-core and htsget-http-actix crates (#45)
- Track crates.io version of noodles (#53)
- Use file size for end bytes ranges.
- Refactor commonalities across all formats.
- Providing the file size through the Storage abstraction. (#49)
- Implement CRAM search backend. (#44)
- Add BCF support (#43)
- Improve the bytes ranges for the BAM header (#42)
- VCF search interface implementation (/variants endpoint) (#37)
- Adapt tests to noodles changes (#41)
- Htsget tests (#40)
- Calculate BAM byte ranges more accurately (#35)
- Remove duplicity in Query, UrlOptions and Url (#29)
- Fix Local Storage always adding the Range header (#31)
- Storage model tests (#28)
- Merge pull request #25 from chris-zen/vcf_bcf_test_data
- Add some tests for LocalStorage::url (#22)
- Add the rest of the builder methods to Query (#21)
- Implement class attribute for reads. (#19)
- Update references and README (#18)
- add tests for BytesRange (#14)
- merge byte ranges
- some renames
- Fix BAM search for unmapped & clippy errors
- add search by reference name and range
- add TODO for BamSearch::url tests
- add TODO for BamSearch::url tests
- added test for HtsGetFromStorage
- added 2 tests for BamSearch
- preparing tests for BamSearch
- add tests and fixes for LocalStorage
- reorganized + rustdocs
- introduced the concept of Storage
- failed attempt to use a BAI index
- work in progress
