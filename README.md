# 💊 Medication Price Tracker

A simple, portable web application for tracking medication prices across different pharmacies and stores.

## Features

✅ **Medication Management**
- Add, edit, and delete medications
- Track medication name, dosage, and notes
- Search and filter medications

✅ **Price Tracking**
- Record prices from multiple stores/pharmacies
- Track price history with dates
- Add notes for each price entry
- Automatic cheapest price identification

✅ **Smart Comparison**
- Visual highlighting of cheapest prices (green badge)
- Automatic sorting by lowest price
- Price history per medication

✅ **Data Portability**
- Export all data as JSON file
- Import data from JSON file
- LocalStorage auto-save (no backend needed)
- Works completely offline

✅ **Responsive Design**
- Mobile-friendly interface
- Works on phones, tablets, and desktops
- Clean, modern UI

## How to Use

### Getting Started

1. **Open the app**: Simply open `index.html` in any modern web browser
2. **No installation required**: Works immediately, no dependencies

### Adding a Medication

1. Click the **"Add Medication"** button
2. Fill in:
   - Medication name (required)
   - Dosage (optional, e.g., "500mg", "10ml")
   - Notes (optional)
3. Click **"Save"**

### Adding Price Entries

1. Click on any medication card to view details
2. Click **"Add Price"** button
3. Fill in:
   - Store/Pharmacy name (required)
   - Price (required)
   - Date (required, defaults to today)
   - Notes (optional)
4. Click **"Save"**

### Viewing Price Comparison

- The main view shows each medication with its **cheapest price**
- In detail view, the cheapest price is highlighted with a **green background** and "CHEAPEST" badge
- Prices are automatically sorted from lowest to highest

### Editing Entries

- **Edit Medication**: Click on a medication → Click "Edit" button
- **Edit Price**: In detail view → Click the pencil icon (✏️) on any price entry
- **Delete**: Click the trash icon (🗑️) - confirmation required

### Search & Filter

- Use the search bar at the top to filter medications by name or dosage
- Results update in real-time as you type

### Export & Import Data

**Export:**
1. Click **"Export"** button in the header
2. A JSON file will be downloaded with timestamp
3. Save this file as backup or to transfer data

**Import:**
1. Click **"Import"** button
2. Select a previously exported JSON file
3. Confirm to replace current data
4. Data will be loaded immediately

## Technical Details

### Architecture

- **Single HTML file** - Complete application in one file
- **No dependencies** - Pure vanilla JavaScript, HTML5, CSS3
- **LocalStorage** - Data persists automatically in browser
- **Offline-first** - Works without internet connection

### Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Any modern browser with ES6+ support

### Data Structure

```json
{
  "medications": [
    {
      "id": "uuid",
      "name": "Medication Name",
      "dosage": "500mg",
      "notes": "General notes",
      "prices": [
        {
          "id": "uuid",
          "store": "Pharmacy Name",
          "price": 25.99,
          "date": "2026-05-18",
          "notes": "Store-specific notes"
        }
      ],
      "createdAt": "2026-05-18T12:00:00.000Z",
      "updatedAt": "2026-05-18T12:00:00.000Z"
    }
  ]
}
```

### Portability

**Deploy anywhere:**
- Local file system (just open index.html)
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service
- USB drive
- Email attachment

**Transfer data:**
- Export JSON file
- Copy to another device
- Import on new device
- All data preserved

## 📱 Using on iPhone/iPad

There are several easy ways to use this app on your iPhone:

### Method 1: Host Online (Recommended - Easiest)

**Option A: GitHub Pages (Free)**
1. Create a GitHub account (if you don't have one)
2. Create a new repository
3. Upload `index.html` to the repository
4. Go to Settings → Pages
5. Enable GitHub Pages
6. Access via: `https://yourusername.github.io/repositoryname`
7. Add to iPhone home screen (see below)

**Option B: Netlify Drop (Free, No Account Needed)**
1. Go to https://app.netlify.com/drop
2. Drag and drop `index.html` file
3. Get instant URL (e.g., `https://random-name.netlify.app`)
4. Add to iPhone home screen (see below)

**Option C: Vercel (Free)**
1. Go to https://vercel.com
2. Sign up (free)
3. Drag and drop `index.html`
4. Get instant URL
5. Add to iPhone home screen (see below)

### Method 2: Use Directly from Files App

1. **Transfer file to iPhone:**
   - Email `index.html` to yourself
   - Use AirDrop from Mac
   - Save to iCloud Drive
   - Use any cloud service (Dropbox, Google Drive)

2. **Open on iPhone:**
   - Open Files app
   - Navigate to the file location
   - Tap `index.html`
   - It will open in Safari

3. **Limitations:**
   - File URL changes each time
   - Harder to bookmark
   - Data persists but harder to access regularly

### Method 3: Add to Home Screen (Works Like Native App!)

After hosting online (Method 1) or opening the file:

1. Open the app URL in **Safari** (must use Safari, not Chrome)
2. Tap the **Share** button (square with arrow pointing up)
3. Scroll down and tap **"Add to Home Screen"**
4. Give it a name (e.g., "Med Prices")
5. Tap **"Add"**

**Benefits:**
- ✅ App icon on home screen
- ✅ Opens like a native app (no browser UI)
- ✅ Works offline
- ✅ Data persists
- ✅ Fast access

### Method 4: Use a Simple HTTP Server (Advanced)

If you have a computer on the same network:

1. **On your computer:**
   ```bash
   # Navigate to the folder with index.html
   # Then run one of these:
   
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js (if installed)
   npx http-server
   ```

2. **On your iPhone:**
   - Connect to same WiFi
   - Open Safari
   - Go to: `http://YOUR_COMPUTER_IP:8000`
   - Add to home screen

### Recommended Setup for iPhone

**Best approach:**

1. **Host on Netlify Drop** (2 minutes, no account):
   - Go to https://app.netlify.com/drop
   - Drag `index.html`
   - Copy the URL

2. **Add to iPhone Home Screen**:
   - Open URL in Safari
   - Share → Add to Home Screen
   - Done!

3. **Backup your data**:
   - Use Export button regularly
   - Save JSON files to iCloud Drive
   - Can import on any device

### Data Sync Between Devices

Since data is stored locally, to sync between devices:

1. **On Device 1**: Export data (creates JSON file)
2. **Transfer**: Email, AirDrop, or cloud storage
3. **On Device 2**: Import the JSON file
4. **Repeat** when you want to sync

**Pro Tip**: Keep a "master" device and export/import regularly, or use the same hosted URL on all devices and manually sync via export/import.

### iPhone-Specific Features

When added to home screen:
- ✅ Full-screen experience
- ✅ No Safari UI
- ✅ Looks like native app
- ✅ Fast launch
- ✅ Offline access
- ✅ LocalStorage persists

### Troubleshooting on iPhone

**App not saving data?**
- Make sure you're using Safari (not Chrome)
- Check Safari settings allow website data
- Don't use Private Browsing mode

**Can't import files?**
- Make sure file has `.json` extension
- Try saving to Files app first
- Use Safari's file picker

**Lost data after iOS update?**
- This is rare but can happen
- Always export backups regularly
- Store JSON files in iCloud Drive

## Tips & Best Practices

1. **Regular Backups**: Export your data regularly as backup
2. **Date Tracking**: Always record the date when adding prices
3. **Store Names**: Use consistent store names for better tracking
4. **Notes**: Use notes to record special offers, package sizes, or conditions
5. **Multiple Devices**: Export from one device, import to another to sync data

## Privacy & Security

- ✅ All data stored locally in your browser
- ✅ No data sent to any server
- ✅ No tracking or analytics
- ✅ Complete privacy
- ✅ Works offline

## Troubleshooting

**Data not saving?**
- Check if browser allows LocalStorage
- Try a different browser
- Export data as backup

**Import not working?**
- Ensure JSON file is valid
- Check file was exported from this app
- Try re-exporting and importing again

**Search not working?**
- Clear search box and try again
- Refresh the page

## Future Enhancements (Optional)

Potential features that could be added:
- Price trend charts
- Multi-currency support
- Barcode scanning
- Reminder notifications
- Cloud sync option
- PWA (Progressive Web App) support
- Print functionality
- CSV export

## License

Free to use, modify, and distribute.

## Support

For issues or questions, refer to the code comments in `index.html`.

---

**Made with ❤️ for better medication price tracking**