# Changelog

All notable public FoldLink releases are documented here.

## [0.3.0] - 2026-08-11

### Changed

- Batch preview no longer creates real short links: previewing in
  Short-link format or with a template referencing `{{shortUrl}}` shows
  cleaned URLs without consuming provider quota, and the dialog explains
  that short links are generated when you copy.
- Copying from the batch preview dialog generates the real output
  (short links included) instead of pasting the side-effect-free preview.
- The batch Copy buttons show the exact number of links that will be
  copied (after deduplication), matching the success message.
- Enabling "Remove duplicates" in batch mode no longer unselects tabs in
  other windows; deduplication applies only when copying.
- Right-clicking a link and copying it as Markdown now uses the link's
  anchor text as the title instead of the page's current selection.

### Fixed

- Settings saved concurrently from two pages (e.g. Options and Popup) no
  longer overwrite each other's template or tracking-parameter changes.
- Clicking Share on a toast that was exiting no longer shares the newest
  toast's text.
- Share and close button labels are translated instead of hard-coded
  English.

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
