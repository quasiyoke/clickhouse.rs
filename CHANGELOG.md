# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- Support for `bool` values storage ([quasiyoke](https://quasiyoke.me)).
- `array`s' binding to SQL queries — useful at [`IN` operators](https://clickhouse.tech/docs/en/sql-reference/operators/in/), [etc](https://clickhouse.tech/docs/en/sql-reference/functions/array-functions/) ([quasiyoke](https://quasiyoke.me)).
- `String` values binding to SQL queries ([quasiyoke](https://quasiyoke.me)).

## [0.6.2] - 2021-04-12
### Fixed
- watch: bind fileds of the type param

## [0.6.1] - 2021-04-09
### Fixed
- compression: decompress error messages (@ods)

## [0.6.0] - 2021-03-24
### Changed
- Use tokio v1, hyper v0.14, bytes v1

## [0.5.1] - 2020-11-22
### Added
- Decompression: lz4.

## [0.5.0] - 2020-11-19
### Added
- Decompression: gzip, zlib and brotli.

## [0.4.0] - 2020-11-17
### Added
- `Query::fetch_one()`, `Watch::fetch_one()`.
- `Query::fetch()` as a replacement for `Query::rows()`.
- `Watch::fetch()` as a replacement for `Watch::rows()`.
- `Watch::only_events().fetch()` as a replacement for `Watch::events()`.

### Changed
- `Error` is `StdError + Send + Sync + 'static` now.

## [0.3.0] - 2020-10-28
### Added
- Expose cursors (`query::RowCursor`, `watch::{RowCursor, EventCursor}`).

## [0.2.0] - 2020-10-14
### Added
- `Client::inserter()` for infinite inserting into tables.
- `Client::watch()` for `LIVE VIEW` related queries.

### Changed
- Renamed `Query::fetch()` to `Query::rows()`.
- Use `GET` requests for `SELECT` statements.

## [0.1.0] - 2020-10-14
### Added
- Support basic types.
- `Client::insert()` for inserting into tables.
- `Client::query()` for selecting from tables and DDL statements.

[unreleased]: https://github.com/loyd/clickhouse.rs/compare/v0.6.2...HEAD
[0.6.2]: https://github.com/loyd/clickhouse.rs/compare/v0.6.1...v0.6.2
[0.6.1]: https://github.com/loyd/clickhouse.rs/compare/v0.6.0...v0.6.1
[0.6.0]: https://github.com/loyd/clickhouse.rs/compare/v0.5.1...v0.6.0
[0.5.1]: https://github.com/loyd/clickhouse.rs/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/loyd/clickhouse.rs/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/loyd/clickhouse.rs/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/loyd/clickhouse.rs/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/loyd/clickhouse.rs/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/loyd/clickhouse.rs/releases/tag/v0.1.0
