# USCIS Case Tracker

A privacy-focused, client-side USCIS case tracking tool that runs entirely in your browser. Track multiple immigration cases, view unified timelines, and monitor updates without sending any data to external servers.

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

## Technical Details

- Pure HTML/CSS/JavaScript
- No external libraries or frameworks
- Uses browser's localStorage for data
- Handles timezone conversion (ET)
- Responsive design for all devices

## Contributing

Found a bug or want to suggest a feature? Please open an issue or submit a pull request.

## License

MIT License - Feel free to use, modify, and distribute as needed.

---
*Note: This is not an official USCIS tool. Always refer to official USCIS communications for important case decisions.*
