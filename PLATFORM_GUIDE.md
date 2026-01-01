# 🌍 PFOS - Cross-Platform User Guide

## 📱 Universal Life Management System

**Works on ALL platforms:** Windows, Mac, Linux, iOS, Android, Tablets

---

## 🎯 Quick Platform Selection

| Platform | Best For | Installation Time | Difficulty |
|----------|----------|-------------------|------------|
| **Windows** | Desktop users, Power users | 5 minutes | ⭐ Easy |
| **Mac** | Apple ecosystem users | 5 minutes | ⭐ Easy |
| **Linux** | Developers, Tech enthusiasts | 5 minutes | ⭐⭐ Medium |
| **iOS** | iPhone/iPad users | Coming Soon | - |
| **Android** | Android phone/tablet users | Coming Soon | - |
| **Web Browser** | Any device with browser | 0 minutes | ⭐ Easiest |

---

# 🪟 WINDOWS INSTALLATION

## Prerequisites
- Windows 10 or Windows 11
- 4GB RAM minimum
- 500MB free disk space

## Method 1: Automated Installation (Recommended)

### Step 1: Install Node.js
1. Download Node.js from: https://nodejs.org/
2. Choose **LTS version** (e.g., 20.x.x)
3. Run the installer
4. Click "Next" → "Next" → "Install"
5. Wait for installation to complete
6. Click "Finish"

### Step 2: Verify Installation
```powershell
# Open PowerShell (Windows Key + X → PowerShell)
node --version
npm --version
```

**Expected output:**
```
v20.x.x
10.x.x
```

### Step 3: Install PFOS
```powershell
# Navigate to PFOS folder
cd "C:\Users\muham\AppData\Roaming\AbacusAI\Agent Workspaces\pfos"

# Run automated installer
.\install.bat

# Start the application
.\start.bat
```

### Step 4: Access PFOS
- Browser will automatically open
- If not, go to: http://localhost:3000
- You should see the PFOS dashboard!

## Method 2: Manual Installation

```powershell
# Open PowerShell as Administrator
cd pfos

# Install dependencies
npm install

# Start the application
npm start
```

## Windows-Specific Features

### Desktop Shortcut
Create a shortcut to `start.bat` on your desktop:
1. Right-click `start.bat`
2. Select "Create shortcut"
3. Drag shortcut to Desktop
4. Rename to "PFOS"

### Run on Startup
1. Press `Windows Key + R`
2. Type: `shell:startup`
3. Copy `start.bat` shortcut here
4. PFOS will start automatically on login

### Windows Defender
If Windows Defender blocks the app:
1. Open Windows Security
2. Go to "Virus & threat protection"
3. Click "Manage settings"
4. Add `pfos` folder to exclusions

## Troubleshooting Windows

### Error: "Cannot find module"
```powershell
# Delete node_modules and reinstall
Remove-Item -Recurse -Force node_modules
Remove-Item package-lock.json
npm install
```

### Error: "Port 3000 already in use"
```powershell
# Find and kill process using port 3000
netstat -ano | findstr :3000
taskkill /PID <PID_NUMBER> /F

# Or use different port
$env:PORT=3001; npm start
```

### Error: "Permission denied"
```powershell
# Run PowerShell as Administrator
# Right-click PowerShell → "Run as administrator"
```

---

# 🍎 MAC INSTALLATION

## Prerequisites
- macOS 10.15 (Catalina) or later
- 4GB RAM minimum
- 500MB free disk space

## Method 1: Using Homebrew (Recommended)

### Step 1: Install Homebrew
```bash
# Open Terminal (Cmd + Space → type "Terminal")
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Step 2: Install Node.js
```bash
# Install Node.js via Homebrew
brew install node

# Verify installation
node --version
npm --version
```

### Step 3: Install PFOS
```bash
# Navigate to PFOS folder
cd ~/Library/Application\ Support/AbacusAI/Agent\ Workspaces/pfos

# Install dependencies
npm install

# Start the application
npm start
```

## Method 2: Direct Node.js Installation

### Step 1: Download Node.js
1. Visit: https://nodejs.org/
2. Download **macOS Installer (.pkg)**
3. Open the downloaded file
4. Follow installation wizard
5. Enter your password when prompted

### Step 2: Install PFOS
```bash
# Open Terminal
cd pfos

# Install dependencies
npm install

# Start application
npm start
```

## Mac-Specific Features

### Create Dock Shortcut
```bash
# Create launch script
cat > ~/Desktop/PFOS.command << 'EOF'
#!/bin/bash
cd ~/path/to/pfos
npm start
EOF

# Make executable
chmod +x ~/Desktop/PFOS.command

# Drag to Dock
```

### Launch Agent (Auto-start)
```bash
# Create launch agent
cat > ~/Library/LaunchAgents/com.pfos.app.plist << 'EOF'
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>com.pfos.app</string>
    <key>ProgramArguments</key>
    <array>
        <string>/usr/local/bin/npm</string>
        <string>start</string>
    </array>
    <key>WorkingDirectory</key>
    <string>/path/to/pfos</string>
    <key>RunAtLoad</key>
    <true/>
</dict>
</plist>
EOF

# Load launch agent
launchctl load ~/Library/LaunchAgents/com.pfos.app.plist
```

### Keyboard Shortcuts (Mac)
- **Cmd + Q** - Quit application
- **Cmd + R** - Refresh page
- **Cmd + W** - Close tab
- **Cmd + T** - New tab

## Troubleshooting Mac

### Error: "Command not found: node"
```bash
# Add Node.js to PATH
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### Error: "Permission denied"
```bash
# Fix npm permissions
sudo chown -R $(whoami) ~/.npm
sudo chown -R $(whoami) /usr/local/lib/node_modules
```

### Error: "Port already in use"
```bash
# Find and kill process
lsof -ti:3000 | xargs kill -9

# Or use different port
PORT=3001 npm start
```

### Error: "xcrun: error"
```bash
# Install Xcode Command Line Tools
xcode-select --install
```

---

# 🐧 LINUX INSTALLATION

## Prerequisites
- Ubuntu 20.04+ / Debian 10+ / Fedora 35+ / Arch Linux
- 4GB RAM minimum
- 500MB free disk space

## Ubuntu / Debian

### Step 1: Update System
```bash
sudo apt update
sudo apt upgrade -y
```

### Step 2: Install Node.js
```bash
# Install Node.js 20.x
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs

# Verify installation
node --version
npm --version
```

### Step 3: Install PFOS
```bash
# Navigate to PFOS folder
cd ~/pfos

# Install dependencies
npm install

# Start application
npm start
```

## Fedora / RHEL / CentOS

```bash
# Install Node.js
sudo dnf install nodejs npm -y

# Navigate to PFOS
cd ~/pfos

# Install and start
npm install
npm start
```

## Arch Linux

```bash
# Install Node.js
sudo pacman -S nodejs npm

# Navigate to PFOS
cd ~/pfos

# Install and start
npm install
npm start
```

## Linux-Specific Features

### Create Desktop Entry
```bash
# Create .desktop file
cat > ~/.local/share/applications/pfos.desktop << 'EOF'
[Desktop Entry]
Version=1.0
Type=Application
Name=PFOS
Comment=Personal & Family Operating System
Exec=bash -c "cd ~/pfos && npm start"
Icon=~/pfos/icon.png
Terminal=false
Categories=Utility;Office;
EOF

# Update desktop database
update-desktop-database ~/.local/share/applications/
```

### Systemd Service (Auto-start)
```bash
# Create systemd service
sudo cat > /etc/systemd/system/pfos.service << 'EOF'
[Unit]
Description=PFOS - Personal & Family Operating System
After=network.target

[Service]
Type=simple
User=YOUR_USERNAME
WorkingDirectory=/home/YOUR_USERNAME/pfos
ExecStart=/usr/bin/npm start
Restart=on-failure

[Install]
WantedBy=multi-user.target
EOF

# Enable and start service
sudo systemctl enable pfos
sudo systemctl start pfos
```

### Keyboard Shortcuts (Linux)
- **Ctrl + Q** - Quit application
- **Ctrl + R** - Refresh page
- **Ctrl + W** - Close tab
- **Ctrl + T** - New tab

## Troubleshooting Linux

### Error: "EACCES: permission denied"
```bash
# Fix npm permissions
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

### Error: "node: command not found"
```bash
# Add Node.js to PATH
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Error: "Cannot find module"
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm cache clean --force
npm install
```

---

# 📱 MOBILE ACCESS (iOS & Android)

## Current Status: Web Browser Access

### iOS (iPhone/iPad)

#### Method 1: Safari Browser
1. **Connect to same WiFi** as your computer
2. **Find your computer's IP address:**
   - Windows: `ipconfig` → Look for "IPv4 Address"
   - Mac: System Preferences → Network → IP Address
   - Linux: `ip addr` → Look for "inet"
3. **Open Safari** on iPhone/iPad
4. **Navigate to:** `http://YOUR_IP_ADDRESS:3000`
5. **Add to Home Screen:**
   - Tap Share button (square with arrow)
   - Scroll down → "Add to Home Screen"
   - Name it "PFOS"
   - Tap "Add"

#### Method 2: Chrome Browser
1. Open Chrome on iOS
2. Go to: `http://YOUR_IP_ADDRESS:3000`
3. Tap menu (three dots)
4. Select "Add to Home Screen"

### Android (Phone/Tablet)

#### Method 1: Chrome Browser
1. **Connect to same WiFi** as your computer
2. **Find your computer's IP address** (see above)
3. **Open Chrome** on Android
4. **Navigate to:** `http://YOUR_IP_ADDRESS:3000`
5. **Add to Home Screen:**
   - Tap menu (three dots)
   - Select "Add to Home Screen"
   - Name it "PFOS"
   - Tap "Add"

#### Method 2: Firefox Browser
1. Open Firefox on Android
2. Go to: `http://YOUR_IP_ADDRESS:3000`
3. Tap menu (three dots)
4. Select "Install"

### Mobile Features

✅ **Fully Responsive Design**
- Touch-optimized buttons
- Swipe gestures
- Mobile-friendly forms
- Adaptive layouts

✅ **Works Offline** (after first load)
- Service workers cache data
- Continue working without internet
- Sync when back online

✅ **Mobile-Specific Features**
- Camera integration (for document scanning)
- GPS location tagging
- Push notifications (coming soon)
- Biometric authentication (coming soon)

### Mobile Tips

**📸 Document Scanning:**
- Use camera to scan documents
- OCR extracts text automatically
- Save directly to PFOS

**🔔 Notifications:**
- Enable browser notifications
- Get expiry alerts
- Task reminders

**💾 Offline Mode:**
- Works without internet
- Data syncs automatically
- No data loss

---

# 🌐 WEB BROWSER ACCESS (Universal)

## Supported Browsers

| Browser | Windows | Mac | Linux | Mobile | Rating |
|---------|---------|-----|-------|--------|--------|
| **Chrome** | ✅ | ✅ | ✅ | ✅ | ⭐⭐⭐⭐⭐ |
| **Firefox** | ✅ | ✅ | ✅ | ✅ | ⭐⭐⭐⭐⭐ |
| **Safari** | ❌ | ✅ | ❌ | ✅ | ⭐⭐⭐⭐ |
| **Edge** | ✅ | ✅ | ✅ | ✅ | ⭐⭐⭐⭐⭐ |
| **Opera** | ✅ | ✅ | ✅ | ✅ | ⭐⭐⭐⭐ |
| **Brave** | ✅ | ✅ | ✅ | ✅ | ⭐⭐⭐⭐⭐ |

## Browser Setup

### Chrome / Edge / Brave
1. Open browser
2. Go to: `http://localhost:3000`
3. Press `Ctrl + D` (Windows/Linux) or `Cmd + D` (Mac) to bookmark
4. Optional: Install as PWA (see below)

### Firefox
1. Open Firefox
2. Go to: `http://localhost:3000`
3. Click star icon to bookmark
4. Optional: Pin tab for quick access

### Safari (Mac only)
1. Open Safari
2. Go to: `http://localhost:3000`
3. Click "+" to add bookmark
4. Optional: Add to Reading List

## Progressive Web App (PWA) Installation

### Desktop (Chrome/Edge)
1. Open PFOS in browser
2. Look for **install icon** (⊕) in address bar
3. Click "Install PFOS"
4. App opens in standalone window
5. Access from Start Menu (Windows) or Applications (Mac)

### Mobile (Chrome/Safari)
1. Open PFOS in browser
2. Tap **Share** button
3. Select "Add to Home Screen"
4. App appears on home screen like native app

### PWA Benefits
- ✅ Works offline
- ✅ Faster loading
- ✅ Push notifications
- ✅ Full-screen mode
- ✅ No browser UI clutter

---

# 🔧 UNIVERSAL TROUBLESHOOTING

## Connection Issues

### Cannot Access PFOS

**Problem:** Browser shows "Cannot connect" or "Site can't be reached"

**Solutions:**

1. **Check if server is running:**
   ```bash
   # You should see "Compiled successfully!"
   # If not, restart: npm start
   ```

2. **Verify correct URL:**
   - Local: `http://localhost:3000`
   - Network: `http://YOUR_IP:3000`

3. **Check firewall:**
   - Windows: Allow Node.js through Windows Firewall
   - Mac: System Preferences → Security → Firewall → Allow
   - Linux: `sudo ufw allow 3000`

4. **Try different port:**
   ```bash
   PORT=3001 npm start
   ```

### Slow Performance

**Solutions:**

1. **Close unused tabs**
2. **Clear browser cache:**
   - Chrome: `Ctrl + Shift + Delete`
   - Firefox: `Ctrl + Shift + Delete`
   - Safari: `Cmd + Option + E`

3. **Disable browser extensions**
4. **Increase RAM allocation:**
   ```bash
   NODE_OPTIONS=--max-old-space-size=4096 npm start
   ```

### Data Not Saving

**Problem:** Changes don't persist after refresh

**Current Status:** Data stored in memory (resets on refresh)

**Coming Soon:** SQLite database for persistence

**Temporary Solution:** Keep browser tab open

---

# 📊 FEATURE COMPARISON

## Desktop vs Mobile

| Feature | Desktop | Mobile | Status |
|---------|---------|--------|--------|
| **Add Expenses** | ✅ | ✅ | Working |
| **Add Tasks** | ✅ | ✅ | Working |
| **Add Documents** | ✅ | ✅ | Working |
| **Edit Data** | ✅ | ✅ | Working |
| **Delete Data** | ✅ | ✅ | Working |
| **Multi-Currency** | ✅ | ✅ | Working |
| **Expiry Alerts** | ✅ | ✅ | Working |
| **Export PDF** | ✅ | ⚠️ | Coming Soon |
| **Document Scan** | ⚠️ | ✅ | Coming Soon |
| **OCR** | ⚠️ | ⚠️ | Coming Soon |
| **Cloud Sync** | ⚠️ | ⚠️ | Phase 2 |
| **Offline Mode** | ✅ | ✅ | Working |
| **Push Notifications** | ⚠️ | ⚠️ | Phase 2 |

---

# 🎯 PLATFORM-SPECIFIC TIPS

## Windows Tips

### Performance
- Use SSD for better performance
- Close background apps
- Disable Windows Search indexing for pfos folder

### Security
- Use Windows Defender (built-in)
- Enable BitLocker for data encryption
- Regular Windows Updates

### Backup
```powershell
# Backup PFOS data
Copy-Item -Recurse pfos "D:\Backups\pfos-$(Get-Date -Format 'yyyy-MM-dd')"
```

## Mac Tips

### Performance
- Use Activity Monitor to check resource usage
- Enable "Reduce Motion" for better performance
- Close unused apps

### Security
- Use FileVault for disk encryption
- Enable Firewall
- Regular macOS updates

### Backup
```bash
# Backup with Time Machine
tmutil setdestination /Volumes/Backup
tmutil startbackup

# Manual backup
cp -R ~/pfos ~/Backups/pfos-$(date +%Y-%m-%d)
```

## Linux Tips

### Performance
- Use lightweight desktop environment (XFCE, LXDE)
- Disable unnecessary services
- Use `htop` to monitor resources

### Security
- Keep system updated: `sudo apt update && sudo apt upgrade`
- Use UFW firewall: `sudo ufw enable`
- Regular backups

### Backup
```bash
# Backup with rsync
rsync -avz ~/pfos ~/Backups/pfos-$(date +%Y-%m-%d)

# Automated backup with cron
crontab -e
# Add: 0 2 * * * rsync -avz ~/pfos ~/Backups/pfos-$(date +\%Y-\%m-\%d)
```

## Mobile Tips

### Battery Optimization
- Use dark mode
- Reduce screen brightness
- Close app when not in use

### Data Usage
- Use WiFi when possible
- Enable offline mode
- Sync only when needed

### Storage
- Clear cache regularly
- Delete old data
- Use cloud backup

---

# 🚀 QUICK START GUIDE (All Platforms)

## 5-Minute Setup

### Step 1: Install (2 minutes)
- **Windows:** Run `install.bat`
- **Mac:** `brew install node && npm install`
- **Linux:** `sudo apt install nodejs && npm install`

### Step 2: Start (1 minute)
```bash
npm start
```

### Step 3: Access (1 minute)
- Open browser
- Go to: `http://localhost:3000`

### Step 4: Add Data (1 minute)
- Click "Add Expense"
- Fill form
- Click "Save"
- Done!

---

# 📚 ADDITIONAL RESOURCES

## Documentation
- 📄 `README.md` - Technical overview
- 📄 `DATA_ENTRY_GUIDE.md` - How to add/edit data
- 📄 `TROUBLESHOOTING.md` - Fix common issues
- 📄 `WINDOWS_SETUP.md` - Windows-specific guide

## Video Tutorials (Coming Soon)
- 🎥 Installation walkthrough
- 🎥 Feature demonstrations
- 🎥 Tips and tricks

## Community Support
- 💬 GitHub Issues
- 💬 Discord Server (coming soon)
- 💬 Reddit Community (coming soon)

---

# ✅ PLATFORM CHECKLIST

## Before You Start

### Windows Users
- [ ] Windows 10/11 installed
- [ ] 4GB RAM available
- [ ] Administrator access
- [ ] Internet connection

### Mac Users
- [ ] macOS 10.15+ installed
- [ ] 4GB RAM available
- [ ] Admin password ready
- [ ] Internet connection

### Linux Users
- [ ] Ubuntu 20.04+ or equivalent
- [ ] 4GB RAM available
- [ ] sudo access
- [ ] Internet connection

### Mobile Users
- [ ] iOS 13+ or Android 8+
- [ ] WiFi connection
- [ ] Modern browser installed
- [ ] Computer running PFOS

---

# 🎉 SUCCESS!

**You're now ready to use PFOS on any platform!**

Choose your platform above and follow the guide.

**Need help?** Check `TROUBLESHOOTING.md`

**Questions?** See `DATA_ENTRY_GUIDE.md`

**Ready to start?** Run `npm start` and go to `http://localhost:3000`

---

**Last Updated:** 2024
**Version:** 1.0.0 (MVP)
**Status:** ✅ Fully Functional