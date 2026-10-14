# Changelog

All notable changes to the USCIS Case Tracker will be documented in this file.

## [1.1.0] - 2026-10-14

### Added
- 👥 Profiles: track cases from several USCIS accounts, each with its own receipts, timeline, stats, and export
- 📍 Location tracking via the `receipt_info` endpoint (service center / field office changes on the timeline and cards)
- 📝 Case status tracking via the `case_status` endpoint
- 🔗 Per-receipt Case / Status / Location buttons and an endpoint selector for "Open API tabs"
- 🧭 Auto-detection of which endpoint pasted JSON came from, with a manual override
- 🚦 Pasting JSON for a receipt owned by another profile offers to file it there
- 🚪 "Sign out of USCIS" link for switching accounts

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
