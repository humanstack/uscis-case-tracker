# Changelog

All notable changes to the USCIS Case Tracker will be documented in this file.

## [1.3.0] - 2026-10-14

### Added
- 💾 Backup and Restore buttons next to "Export for Reddit": move all profiles between browsers or devices as one JSON file
- 🔀 Account switcher in the timeline header when there is more than one profile
- 📦 Total storage meter under the USCIS account bar
- 🪗 "Get Case Data from USCIS" card is collapsible, with Open account / Paste JSON shortcuts when collapsed

### Changed
- Footer is a single row of four columns with less height
- Receipt chips look the same in the open and collapsed states of Step 1; Case / Status / Location and remove buttons appear on hover or keyboard focus (always on touch screens); remove asks for confirmation
- Custom titles shown on receipt chips; chips ordered newest first like the cards
- Removed the placeholder "No status available" line from case cards (the Case endpoint carries no status text; the Status row does)

### Fixed
- Chip actions stayed open after clicking a button

## [1.2.0] - 2026-10-14

### Added
- 📥 One-click account import: a bookmarklet reads all receipts from my.uscis.gov/account/applicant, fetches Case, Status and Location for each and sends the bundle to the tracker (clipboard fallback for local files); bundles can also be pasted into Step 2
- 🙈 Completed cases are hidden by default, with a "Show completed" toggle
- 🏷️ Custom case titles, shown after the receipt number on cards, chips and the timeline
- 🔗 Every timeline item names its receipt; the receipt links to the case card
- 📅 Receipt date on case cards; cards and chips ordered newest first
- 💾 Compact storage: later snapshots are stored as change lists, with a Storage figure in the stats bar

### Changed
- Status and location timeline items are dated from the USCIS payload, never from the import time
- HTML in USCIS status fields is rendered as plain text; API wrapper messages are ignored
- Bulk "Open API tabs" removed in favour of the account import; per-receipt buttons remain
- Smaller header with a single-line tagline

### Fixed
- "Case completed" items for cases without a top-level updatedAtTimestamp were dated at import time
- Date group headers were one day early west of UTC
- Location objects were printed as JSON on the card

## [1.1.0] - 2026-10-14

### Added
- 👥 Profiles: track cases from several USCIS accounts, each with its own receipts, timeline, stats, and export
- 📍 Location tracking via the `receipt_info` endpoint (service center / field office changes on the timeline and cards)
- 📝 Case status tracking via the `case_status` endpoint
- 🔗 Per-receipt Case / Status / Location buttons (the bulk "Open API tabs" button was removed in favour of the account import)
- 🧭 Auto-detection of which endpoint pasted JSON came from, with a manual override
- 🚦 Pasting JSON for a receipt owned by another profile offers to file it there
- 🚪 "Sign out of USCIS" link for switching accounts
- 📥 One-click account import: a bookmarklet reads all receipts from my.uscis.gov/account/applicant, fetches all three endpoints per case and sends the bundle to the tracker (clipboard fallback for local files); bundles can also be pasted into Step 2

### Changed
- "Clear data" now clears only the active profile
- Existing data is migrated into a "Default" profile automatically

### Fixed
- Timeline crashed when rendering again after the empty state (first paste required a reload)
- Corrupted localStorage entries no longer break page load
- Pasted USCIS text is HTML-escaped in the timeline and cards; "View JSON" works when values contain apostrophes

## [1.0.0] - 2026-01-23

### Added
- 🎨 Modern, responsive UI with improved UX
- 📊 Quick stats dashboard showing case overview
- ➕ Floating action button for adding cases
- 🎯 Step-by-step guided onboarding flow
- 📈 Case summary cards with key metrics
- 🗂️ Auto-collapsing sections when data exists
- 🧹 Clear data button for easy reset
- 🔍 Enhanced SEO with comprehensive meta tags
- 📱 PWA support with manifest.json
- 🤖 Structured data for better search indexing
- 📄 Sitemap and robots.txt for search engines
- 🎪 Modal workflow for adding new cases
- 💬 Improved empty states with helpful guidance
- 🏷️ Better timeline visualization with badges
- ⚡ Performance optimizations

### Changed
- Improved visual design with modern color palette
- Enhanced typography and spacing system
- Better mobile responsiveness
- Optimized card layouts and interactions
- Refined timeline display with clearer hierarchy
- Updated header with descriptive title
- Improved button states and transitions

### Fixed
- Better form validation feedback
- Improved accessibility with ARIA labels
- Enhanced keyboard navigation
- Fixed timezone conversion accuracy

## [0.1.0] - Initial Release

### Added
- Basic USCIS case tracking functionality
- Client-side only processing
- localStorage for data persistence
- JSON data comparison
- Timeline view
- Reddit export feature
- Business hours detection
- Event code insights
- Receipt number validation

---

## Legend

- 🎨 Design / UI
- 📊 Features
- 🐛 Bug Fixes
- 🔍 SEO / Discoverability
- 📱 Mobile / Responsive
- ⚡ Performance
- 🔐 Security / Privacy
- 📝 Documentation
