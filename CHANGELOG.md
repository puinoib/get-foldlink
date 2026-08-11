# Changelog

All notable public FoldLink releases are documented here.

## [0.2.0] - 2026-08-11

### Added

- FoldLink remembers your preferred template per site in the background
  after you use the same template on a site a couple of times. Bindings
expire after 90 days without use and never leave the device.

### Fixed

- Settings no longer break when templates grow large: storage is now split
  across sync and local, keeping every write within Chrome's storage quotas.
- Templates written as `{{ shortUrl }}` (with spaces) now include the short
  link instead of rendering empty.
- Template drafts with an empty name or content can be saved.
- Template ids are collision-free when adding templates quickly.
- Options inputs no longer hit Chrome's sync write-rate limit while typing.

## [0.1.0] - 2026-07-27

### Added

- Initial public release of the FoldLink Chrome extension.
- URL tracking-parameter cleaning with configurable rules.
- Clean URL, Markdown, short-link, and custom-template copy formats.
- QR code generation and batch processing for multiple browser tabs.
