# PFOS - Windows Setup Guide

## 🚀 Quick Start (3 Options)

### Option 1: Instant Preview (No Installation Required)
1. Open `demo.html` in your web browser
2. This is a fully functional demo showing all UI features
3. No Node.js or npm required!

### Option 2: Full Installation (Recommended)
1. **Install Node.js**
   - Download from: https://nodejs.org/
   - Choose LTS version (recommended)
   - Run installer and follow prompts

2. **Install PFOS**
   - Double-click `install.bat`
   - Wait for installation to complete

3. **Start PFOS**
   - Double-click `start.bat`
   - Browser will open automatically at http://localhost:3000

### Option 3: Manual Installation
```bash
# Open Command Prompt or PowerShell in the pfos folder
cd pfos
npm install
npm start
```

## 📋 System Requirements

- **Operating System**: Windows 10 or later
- **RAM**: 4GB minimum (8GB recommended)
- **Disk Space**: 500MB for application + data
- **Browser**: Chrome, Firefox, Edge, or Safari

## 🎯 Features Overview

### Dashboard Features
✅ **Summary Cards** - Quick overview of expenses, tasks, documents, vault
✅ **Filters** - Date range and category filtering
✅ **Export** - PDF, Excel, CSV export options
✅ **Custom Dashboard** - Toggle widgets on/off
✅ **Multi-Currency** - Support for USD, EUR, PKR, custom currencies (SCU, FCU, etc.)

### Available Sections
1. **Home Dashboard** - Overview of everything
2. **Documents** - Scan, store, track expiry dates
3. **Finance** - Multi-currency expense tracking
4. **Tasks** - To-dos and appointments
5. **Vault** - Secure password storage
6. **Settings** - Customize your experience

## 🔧 Troubleshooting

### Issue: "Node.js is not installed"
**Solution**: Download and install Node.js from https://nodejs.org/

### Issue: "npm install fails"
**Solution**: 
1. Run Command Prompt as Administrator
2. Navigate to pfos folder
3. Run: `npm cache clean --force`
4. Run: `npm install`

### Issue: "Port 3000 is already in use"
**Solution**: 
1. Close other applications using port 3000
2. Or change port: `set PORT=3001 && npm start`

### Issue: Browser doesn't open automatically
**Solution**: Manually open http://localhost:3000 in your browser

## 📊 Using the Dashboard

### Filters
- **Date Range**: Filter data by Today, Week, Month, Year, or Custom
- **Category**: Filter by All, Documents, Finance, Tasks, or Vault

### Export Reports
- **PDF**: Full report with charts and summaries
- **Excel**: Spreadsheet format for analysis
- **CSV**: Raw data for custom processing

### Customize Dashboard
1. Click "Customize Dashboard" button
2. Check/uncheck widgets to show/hide
3. Available widgets:
   - Upcoming Expiries
   - Pending Tasks
   - Recent Expenses
   - Summary Cards
   - Analytics Charts

## 🔐 Security Features

- **Local-First**: All data stored on your computer
- **Offline-First**: Works without internet
- **Encrypted Vault**: Passwords stored securely
- **Zero-Knowledge**: You own your data

## 💡 Tips & Tricks

1. **Quick Scan**: Use the "Scan Document" button for instant document capture
2. **Priority Tasks**: High-priority tasks show in red
3. **Expiry Alerts**: Critical expiries (< 30 days) highlighted in red
4. **Multi-Currency**: Add custom currencies in Settings
5. **Family Sharing**: Coming in Phase 2

## 📱 Future Features

### Phase 2 (Coming Soon)
- Family sharing (5 users)
- Cloud backup (encrypted)
- Mobile app (iOS/Android)
- Advanced rules engine

### Phase 3 (Planned)
- Digital will
- Emergency access
- Queue estimation
- API integrations

## 🆘 Support

For issues or questions:
1. Check this guide first
2. Review README.md for technical details
3. Check database schema in `src/database/schema.sql`

## 📝 Development

### Project Structure
```
pfos/
├── demo.html          # Standalone demo (no installation needed)
├── install.bat        # Windows installation script
├── start.bat          # Windows start script
├── public/            # Static files
├── src/
│   ├── components/    # React components
│   ├── database/      # Database schema
│   └── App.js         # Main application
└── package.json       # Dependencies
```

### Build for Production
```bash
npm run build
```

This creates an optimized build in the `build/` folder that can be:
- Hosted on a web server
- Packaged as a desktop app with Electron
- Deployed to cloud platforms

## 🎉 You're Ready!

Choose your preferred option above and start managing your life with PFOS!

---

**Need help?** Open `demo.html` first to see what PFOS can do!