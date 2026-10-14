# USCIS Case Tracker - Free Privacy-Focused Immigration Status Tracker

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Privacy First](https://img.shields.io/badge/Privacy-First-green.svg)]()
[![No Tracking](https://img.shields.io/badge/Tracking-None-success.svg)]()

A free, open-source, privacy-focused USCIS case tracking tool that runs entirely in your browser. Track multiple immigration cases (I-485, I-765, I-131, and more), view unified timelines, and monitor updates without sending any data to external servers.

**🔗 Live Demo:** [https://enase.github.io/uscis-case-tracker/](https://enase.github.io/uscis-case-tracker/)

## Why Use This USCIS Tracker?

✅ **Completely Free** - No subscriptions, no fees, forever
✅ **100% Private** - Your immigration data never leaves your browser
✅ **No Account Required** - Start tracking immediately
✅ **Track Unlimited Cases** - Monitor multiple applications simultaneously
✅ **Smart Insights** - Understand officer vs system updates
✅ **Community Friendly** - Export for Reddit with privacy protection
✅ **Open Source** - Transparent, auditable code

## Features

### 🔒 Privacy First
- 100% client-side processing
- Zero data sent to servers
- All data stored locally in your browser
- No tracking, no analytics

### 📋 Case Management
- Track multiple USCIS cases
- Unified timeline across all cases
- Automatic date grouping
- Receipt number masking for sharing

### 🔍 Smart Insights
- Identifies system vs. officer updates
- Detects biometric and FBI check patterns
- Highlights supervisor reviews
- Shows case completion status

### 📊 Timeline Analysis
- View JSON data for each update
- Compare changes between updates
- Track case progression
- Monitor status changes

### 💡 Smart Features
- Business hours detection
- Automatic timezone conversion
- Reddit-friendly export
- Receipt number validation

## How to Use

1. **Add Cases**
   - Enter your USCIS receipt numbers
   - Click "Add" to save them locally
   - Receipt numbers are stored in your browser

2. **Get Updates**
   - Log in to [myaccount.uscis.gov](https://myaccount.uscis.gov/sign-in)
   - Click "Open API tabs" to load case data
   - Copy the JSON from each tab

3. **Save Snapshots**
   - Paste the JSON into the tracker
   - Each snapshot is saved with timestamp
   - View changes in the timeline

4. **Monitor Progress**
   - See all updates in chronological order
   - Track officer interactions (👋)
   - Monitor system updates (⚙️)
   - Celebrate completions (🎉)

### Multiple USCIS Accounts

The tracker supports **profiles**, one per USCIS login (for example "Me" and "Spouse"). Use the **USCIS account** bar at the top to create, rename, delete, or switch profiles. Each profile has its own receipts, snapshots, timeline, stats, and Reddit export. Profiles are labels only; no USCIS credentials are stored.

Before opening API tabs for a profile, make sure you are signed in to USCIS as that account. To switch accounts, sign out of USCIS first (there is a link in Step 2). If you paste JSON for a receipt that belongs to another profile, the tracker offers to save it there.

### Case Status and Location Data

Besides the main case endpoint, each receipt has two more USCIS endpoints you can snapshot the same way (open the tab while signed in, copy the JSON, paste it in Step 2):

| Data | URL pattern | What it shows |
|------|-------------|---------------|
| Case data | `https://my.uscis.gov/account/case-service/api/cases/<receipt>` | Events, notices, timestamps |
| Case status | `https://my.uscis.gov/account/case-service/api/case_status/<receipt>` | Current status text |
| Location | `https://my.uscis.gov/secure-messaging/api/case-service/receipt_info/<receipt>` | Service center or field office handling the case (`null` means it is still at the center on your receipt notice) |

Each receipt chip has **Case**, **Status**, and **Location** buttons, and the "Open API tabs" button has a selector for which endpoint (or all three) to open. The paste box auto-detects which endpoint the JSON came from; if it cannot, pick the data type manually. Status and location changes appear on the timeline and on the case cards.

## Understanding Updates

### Event Codes
- **FTA0**: Biometric or other actions completed
  - Often appears in pairs for FBI and biometric checks
  - Isolated FTA0 after weeks could be a good sign
- **SA**: Status Adjusted (Case approved ✅)
- **FTA1**: Supervisor Review 👀

### Update Types
- **Officer Updates**: Shows 👋 for updates during business hours
- **System Updates**: Shows ⚙️ for automated updates
- **Case Completion**: Shows 🎉 when case is completed

## Sharing Updates

1. Click "Export for Reddit" to generate a shareable timeline
2. Receipt numbers are automatically masked (e.g., IOE09326XXXXX)
3. Copy and paste directly into Reddit or other platforms

## Privacy & Security

- No data leaves your browser
- No cookies or tracking
- No external dependencies
- Works offline after initial load
- Source code is open for review

## Supported Immigration Forms

This tracker works with all USCIS forms, including:

- **I-485** - Adjustment of Status (Green Card Application)
- **I-765** - Employment Authorization Document (Work Permit/EAD)
- **I-131** - Travel Document (Advance Parole/Re-entry Permit)
- **I-140** - Immigrant Worker Petition
- **I-130** - Family-Based Immigration Petition
- **N-400** - Naturalization Application (Citizenship)
- **I-129** - Nonimmigrant Worker Petition (H-1B, L-1)
- **I-129F** - Fiancé(e) Visa Petition
- **I-90** - Green Card Renewal/Replacement
- **I-751** - Remove Conditions on Residence
- **I-539** - Extension/Change of Nonimmigrant Status
- And all other USCIS case types

## Technical Details

- **Pure HTML/CSS/JavaScript** - No frameworks or dependencies
- **Client-side only** - Zero server communication
- **localStorage** - All data stored locally in your browser
- **Timezone aware** - Automatic ET conversion
- **Responsive design** - Works on all devices
- **PWA Ready** - Install as app on mobile/desktop
- **SEO Optimized** - Enhanced discoverability

## SEO & Discoverability

This project includes comprehensive SEO optimization:

- ✅ Complete meta tags (Open Graph, Twitter Cards)
- ✅ Structured data (Schema.org JSON-LD)
- ✅ Semantic HTML with proper heading hierarchy
- ✅ Sitemap.xml for search engine indexing
- ✅ Robots.txt for crawler guidance
- ✅ PWA manifest for app discoverability
- ✅ Keyword-rich content and footer
- ✅ Fast loading and performance optimized

**Key Search Terms:**
USCIS case tracker, immigration status tracker, green card tracker, I-485 tracker, I-765 tracker, work permit tracker, advance parole tracker, USCIS timeline, case status checker, free immigration tracker

## Deployment

### GitHub Pages (Recommended)

1. Fork this repository
2. Go to Settings → Pages
3. Select branch and folder
4. Your site will be live at `https://yourusername.github.io/uscis-case-tracker/`

### Other Platforms

The tracker works on any static hosting:
- Netlify
- Vercel
- Cloudflare Pages
- AWS S3 + CloudFront
- Any web server

## Contributing

Found a bug or want to suggest a feature? Please open an issue or submit a pull request.

### Development

1. Clone the repository
2. Open `index.html` in your browser
3. Make changes and test locally
4. Submit a pull request

## Star History

If you find this tool helpful, please consider giving it a star ⭐ on GitHub!

## License

MIT License - Feel free to use, modify, and distribute as needed.

---
*Note: This is not an official USCIS tool. Always refer to official USCIS communications for important case decisions.*
