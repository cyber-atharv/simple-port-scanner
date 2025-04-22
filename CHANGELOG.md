# Changelog

All notable changes to simple-port-scanner are documented here.

### [2025-12-15]
- docs: update license headers and author metadata

### [2025-12-20]
- docs: update license headers and author metadata

### [2025-12-24]
- fix: resolve memory leak in idle connection reaper

### [2026-01-03]
- perf: optimize memory allocation in buffer pool

### [2026-02-03]
- test: verify backward compatibility with legacy message format

### [2026-02-23]
- security: enforce strict bounds checking on dynamic byte slices

### [2026-03-11]
- refactor: use enum types for status codes instead of magic numbers

### [2026-03-30]
- docs: clarify prerequisite installation steps in README

### [2026-03-31]
- test: add fuzzing harness for packet decoding routine

### [2026-04-01]
- feat: improve error logging with contextual debug traces

### [2026-04-09]
- fix: correct endianness conversion in raw packet parser

### [2026-04-28]
- docs: add example configuration commands to quickstart guide

### [2026-05-07]
- test: verify backward compatibility with legacy message format

### [2026-05-15]
- feat: add support for custom timeout configuration via CLI flags

### [2026-05-19]
- fix: handle nil pointer dereference on unexpected connection close

### [2026-05-19]
- fix: handle nil pointer dereference on unexpected connection close

### [2026-05-31]
- chore: streamline build flags and compiler optimization settings

### [2026-07-14]
- perf: replace linear search with hash map lookup for fast querying

### [2026-07-15]
- chore: update internal constants and clean up legacy comments

### [2026-07-31]
- security: sanitize input strings to mitigate format string risks

### [2026-08-18]
- docs: update license headers and author metadata

### [2026-09-01]
- style: clean up trailing whitespace and fix alignment

### [2026-09-05]
- fix: handle malformed HTTP header parsing without crashing

