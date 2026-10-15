# Changelog

All notable changes to the USCIS Case Tracker will be documented in this file.

## [1.1.0] - 2026-10-14

### Added
- 👥 Profiles: track cases from several USCIS accounts, each with its own receipts, snapshots, titles, timeline, stats and export; account switcher in the timeline header when there is more than one profile
- 📥 One-click account import: a bookmarklet reads all receipts from my.uscis.gov/account/applicant, fetches Case, Status and Location for each and sends the bundle to the tracker (clipboard fallback for local files); bundles can also be pasted into Step 2
- 📝 Case status tracking via the `case_status` endpoint
- 📍 Location tracking via the `receipt_info` endpoint (service center / field office changes on the timeline and cards)
- 🔗 Per-receipt Case / Status / Location buttons on hover; auto-detection of which endpoint pasted JSON came from, with a manual override
- 🚦 Pasting JSON for a receipt owned by another profile offers to file it there
- 🚪 "Sign out of USCIS" link for switching accounts
- 🙈 Completed cases are hidden by default, with a "Show completed" toggle
- 🏷️ Custom case titles, shown after the receipt number on cards, chips and the timeline
- 🔗 Every timeline item names its receipt; the receipt links to the case card
- 📅 Receipt date on case cards; cards and chips ordered newest first
- 💾 Backup and Restore buttons next to "Export for Reddit": move all profiles between browsers or devices as one JSON file
- 📦 Compact storage: later snapshots are stored as change lists; storage meters under the USCIS account bar and in the stats bar
- 🪗 "Get Case Data from USCIS" card is collapsible, with Open account / Paste JSON shortcuts when collapsed
- ✉️ Each USCIS account can store its login email; New and Update open a dialog with Title and Email fields, and the account dropdown shows the email

### Changed
- Existing data is migrated into a "Default" profile automatically; "Clear data" clears only the active profile
- Status and location timeline items are dated from the USCIS payload, never from the import time
- HTML in USCIS status fields is rendered as plain text; API wrapper messages are ignored
- Receipt chips look the same in the open and collapsed states of Step 1; remove asks for confirmation
- Bulk "Open API tabs" removed in favour of the account import
- Removed the placeholder "No status available" line from case cards (the Case endpoint carries no status text; the Status row does)
- Smaller header with a single-line tagline; footer is a single row of four columns
- The account bar's "Rename" button is now "Update"

### Fixed
- Timeline crashed when rendering again after the empty state (first paste required a reload)
- "Case completed" items for cases without a top-level updatedAtTimestamp were dated at import time
- Date group headers were one day early west of UTC
- Location objects were printed as JSON on the card
- Corrupted localStorage entries no longer break page load
- Pasted USCIS text is HTML-escaped in the timeline and cards; "View JSON" works when values contain apostrophes
- Chip actions stayed open after clicking a button
- Restore dropped each account's login email

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
