# SC Med POS - Installers

This repository contains the official release builds of SC Med POS, a Point of Sale & Inventory Management System for pharmacies.

## 📥 Installation

### Stable Releases

#### Windows
1. Download the latest `SC Med POS Setup [version].exe` file from the [Releases page](../../releases)
2. Run the installer
3. Follow the installation wizard
4. Launch "SC Med POS" from your desktop or Start menu

#### macOS
1. Download the latest `SC Med POS-[version]-arm64.dmg` file from the [Releases page](../../releases)
2. Double-click the DMG file to mount it
3. Drag "SC Med POS" to your Applications folder
4. Launch from Applications folder (may need to right-click → Open on first run)

### Beta Releases

For testing new features and platform validation before stable release.

#### Windows
1. Go to the [Releases page](../../releases) and click the "**Pre-releases**" tab
2. Download the latest `SC Med POS Setup [beta-version].exe` file
3. Run the installer
4. Follow the installation wizard
5. Launch "SC Med POS" from your desktop or Start menu

#### macOS
1. Go to the [Releases page](../../releases) and click the "**Pre-releases**" tab
2. Download the latest `SC Med POS-[beta-version]-arm64.dmg` file
3. Double-click the DMG file to mount it
4. Drag "SC Med POS" to your Applications folder
5. Launch from Applications folder (may need to right-click → Open on first run)

**Note:** Beta versions include `-beta.x` in the version number (e.g. `0.4.0`).

## 🔧 First Time Setup

On first launch, the app will show a **"Create Admin Account"** screen:
1. Enter admin details (name, username, password)
2. Click "Create Admin"
3. Login with your new admin credentials

The database and all necessary files are created automatically.

## 📱 Features

- 🛒 **Point of Sale** — Product search, cart management, split cash/e-wallet payments (GCash or Maya with reference number)
- 👴♿ **Senior/PWD Discounts** — 20% discount on eligible items
- 📦 **Inventory Management** — Brand/generic names, batch and expiry tracking, suppliers, per-category low-stock alerts, CSV export
- 🚫 **Void & Returns** — Transaction management with stock restoration; split cash/e-wallet refunds and exchanges
- 💸 **Expenses** — Manual and EOD-sourced expense tracking with categories
- 📊 **Reports** — Daily/monthly/yearly sales analytics *(admin: full access; staff: today only)*
- 🏁 **End of Day** — Cash counting by denomination, GCash/Maya on hand, expense tracking, variance reports, automatic CSV export
- 💾 **Backup** — Automatic backup on EOD save, manual backup, optional Google Drive upload *(admin only)*
- 👥 **User Management** — Admin and staff roles *(admin only)*

## 🔄 Auto-Updates

This app automatically checks for updates about 10 seconds after launch:
- **Stable users** only receive stable release updates by default
- **Beta users** receive both beta and stable updates automatically
- **Beta preference persists** across version updates (beta → stable → beta)
- Updates are downloaded in the background
- You'll be prompted to restart when updates are ready
- No manual installation required for updates

### Beta Channel Management

There is no in-app settings toggle for the beta channel. Use the steps below to opt in or out.

#### Opt in to beta updates

1. Go to the [Releases page](../../releases) and open the **Pre-releases** tab
2. Download the latest beta installer for your platform (Windows `.exe` or macOS `.dmg`)
3. Run the installer and launch the app
4. Done — installing a beta build automatically opts you into beta updates

Your preference is saved and persists even after you update to a stable release.

#### Opt out of beta updates

> **Important:** While you are running a beta build (version contains `-beta`), the app re-creates the preference file on every launch. To fully opt out, use a **stable** release first, then remove the preference file.

1. **Install or update to a stable release** (version without `-beta` in the name)
2. **Close the app completely**
3. **Delete the beta preference file:**
   - **Windows:** Press `Win + R`, type `%APPDATA%\SC Med POS`, press Enter, then delete `beta-preference.json`
   - **macOS:** Open Finder → Go → Go to Folder (`Cmd + Shift + G`), enter `~/Library/Application Support/SC Med POS`, then delete `beta-preference.json`
4. **Restart the app**

After restart, you will only receive stable updates.

## 💾 Data Storage

Your data is stored locally on your computer:

| Data | Windows | macOS |
|---|---|---|
| **Database** | `%ProgramData%\SC Med POS\pos_inventory.db` | `/Users/Shared/SC Med POS/pos_inventory.db` |
| **Local backups** | `%ProgramData%\SC Med POS\backups\` | `/Users/Shared/SC Med POS/backups/` |
| **Beta preference** | `%APPDATA%\SC Med POS\beta-preference.json` | `~/Library/Application Support/SC Med POS/beta-preference.json` |

Backups are ZIP archives of the database, created automatically when you save an End of Day report or manually from the Backup tab.

## 🔐 Security & Privacy

- All business data (sales, inventory, users) is stored locally on your machine
- No cloud connectivity is required for normal operation
- **Optional:** Admins can configure Google Drive backup upload from the Backup settings
- **Auto-updates only:** The app checks GitHub releases for new installer versions — no business data is transmitted

## 📞 Support

For technical support or questions:
- Check the main [project repository](https://github.com/masutabato/pos-inventory-system)
- Review the [documentation](https://github.com/masutabato/pos-inventory-system/blob/main/README.md)

## 🖥️ System Requirements

### Windows
- Windows 10 or later
- 100MB free disk space
- Administrator access for installation

### macOS
- macOS 10.12 (Sierra) or later
- 100MB free disk space
- Apple Silicon (M1/M2/M3) or Intel Mac

## 📋 User Roles

| Role | Access |
|---|---|
| **admin** | Full access — POS, Inventory, Transactions, Returns, Expenses, Reports (daily/monthly/yearly + charts), End of Day, Backup, User Management |
| **staff** | POS, Inventory, Transactions, Returns, Expenses, End of Day, Reports (today only — no monthly/yearly views or charts) |

---

**Version**: [Latest release version](../../releases/latest)  
**License**: ISC  
**Developer**: SC Med Pharmacy

© 2026 SC Med Pharmacy. All rights reserved.
