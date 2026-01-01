# PFOS - Personal & Family Operating System

A unified, deterministic, offline-first life management platform that solves real, recurring problems without AI hype or unnecessary complexity.

## 🎯 Core Features

- **One app, one login, multi-domain control**
- **Offline-first**: All data lives locally first; sync optional
- **Zero-knowledge**: User owns keys; no backdoors
- **Rule-driven, not AI-driven**: Predictable automation
- **Universal utility**: Works for students, migrants, parents, freelancers, small businesses

## 🚀 Quick Start (Windows & Web)

### Prerequisites
- Node.js 16+ installed
- npm or yarn package manager

### Installation

1. Navigate to the project directory:
```bash
cd pfos
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

4. Open your browser to `http://localhost:3000`

## 📊 Dashboard Features

### ✅ Implemented Features

1. **Summary Cards**
   - Total Expenses tracking
   - Pending Tasks counter
   - Expiring Documents alerts
   - Vault Items count

2. **Filters & Reports**
   - Date range filtering (Today, Week, Month, Year, Custom)
   - Category filtering (All, Documents, Finance, Tasks, Vault)
   - Export to PDF, Excel, CSV

3. **Custom Dashboard**
   - Toggle widgets on/off
   - Available widgets:
     - Upcoming Expiries
     - Pending Tasks
     - Recent Expenses
     - Summary Cards
     - Analytics Charts

4. **Upcoming Expiries**
   - Color-coded alerts (Critical, Warning, Info)
   - Days remaining counter
   - Quick renew action

5. **Pending Tasks**
   - Priority levels (High, Medium, Low)
   - Due date tracking
   - Quick complete action

6. **Recent Expenses**
   - Multi-currency support (USD, SCU, PKR, etc.)
   - Category tagging
   - Date tracking
   - Detailed view option

## 🗄️ Database Schema

The application uses SQLite with the following core tables:

- **users** - User identity and emergency contacts
- **devices** - Device trust management
- **documents** - Scanned documents with expiry tracking
- **currency_units** - Custom currency definitions
- **expenses** - Multi-currency expense tracking
- **tasks** - Tasks and appointments
- **vault_items** - Encrypted password storage
- **emergency_records** - Digital will and emergency data
- **rules** - Automation rules engine

## 🎨 Customization

### Custom Currency Units

The system supports custom currency units for:
- Site-specific currencies (e.g., "Site Cash Units")
- Family tokens
- Barter systems
- Asset tracking

### Dashboard Widgets

Users can customize their dashboard by:
1. Clicking "Customize Dashboard" button
2. Selecting/deselecting widgets
3. Widgets automatically rearrange

## 📱 Platform Support

- ✅ **Web Browser** (Chrome, Firefox, Edge, Safari)
- ✅ **Windows Desktop** (via browser or Electron build)
- 🔄 **Mobile** (React Native - Coming in Phase 2)
- 🔄 **Linux/Mac** (via browser or Tauri build)

## 🔐 Security Features

- Local-first data storage
- Encrypted vault for passwords
- Device trust levels
- Emergency access controls
- Zero-knowledge architecture

## 📈 Roadmap

### Phase 1 (Current - 8 weeks)
- ✅ Local SQLite DB
- ✅ Dashboard UI
- ✅ Custom Currency support
- 🔄 Document Scan + OCR
- 🔄 Expiry Tracker
- 🔄 Basic Rules

### Phase 2 (6 weeks)
- Family sharing
- Cloud sync (encrypted)
- Backup/Export
- Mobile app

### Phase 3 (4 weeks)
- Password Vault
- Digital Will
- Advanced Rules
- Queue estimation

## 💰 Monetization

| Tier | Features | Price |
|------|----------|-------|
| **Free** | Single user, local-only, 5 custom units, basic rules | $0 |
| **Family** | Family sharing (5 users), cloud backup, 20 custom units, expiry alerts | $0/month |
| **Pro** | Unlimited rules, audit logs, export to Excel/PDF, queue API integrations | $0/month |

## 🛠️ Technology Stack

- **Frontend**: React 18
- **State Management**: Zustand
- **Database**: SQLite (better-sqlite3)
- **Styling**: CSS3 with modern gradients
- **Build Tool**: Create React App
- **Future**: Tauri for desktop, React Native for mobile

## 📝 Development

### Project Structure
```
pfos/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   └── dashboard/
│   │       ├── DashboardScreen.js
│   │       └── Dashboard.css
│   ├── database/
│   │   └── schema.sql
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   └── index.css
└── package.json
```

### Build for Production
```bash
npm run build
```

This creates an optimized production build in the `build/` folder.

## 🤝 Contributing

This is a personal project blueprint. Feel free to fork and customize for your needs.

## 📄 License

MIT License - Use freely for personal or commercial projects.

## 🎯 Why PFOS Wins

- **Solves fragmentation**: One place for docs, money, tasks, IDs, passwords
- **Works offline**: Critical for global users (migrants, rural, travelers)
- **Custom Currency**: Enables informal economies (construction, family budgets, barter)
- **No AI dependency**: No hallucinations, no subscriptions to LLMs
- **Emergency-ready**: Digital will unlocks only when needed
- **Family-first**: Not just personal productivity—**family resilience**

---

**Built with ❤️ for real-world utility**
