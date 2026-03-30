# SC Med POS - Installers

This repository contains the official release builds of SC Med POS, a Point of Sale & Inventory Management System for pharmacies.

## 📥 Installation

### Windows
1. Download the latest `SC Med POS Setup [version].exe` file from the [Releases page](../../releases)
2. Run the installer
3. Follow the installation wizard
4. Launch "SC Med POS" from your desktop or Start menu

### macOS
1. Download the latest `SC Med POS-[version]-arm64.dmg` file from the [Releases page](../../releases)
2. Double-click the DMG file to mount it
3. Drag "SC Med POS" to your Applications folder
4. Launch from Applications folder (may need to right-click → Open on first run)

## 🔧 First Time Setup

On first launch, the app will show a **"Create Admin Account"** screen:
1. Enter admin details (name, username, password)
2. Click "Create Admin"
3. Login with your new admin credentials

The database and all necessary files are created automatically.

## 📱 Features

- 🛒 **Point of Sale** - Product search, cart management, split payments
- 👴♿ **Senior/PWD Discounts** - 20% discount on eligible items
- 📦 **Inventory Management** - Stock tracking, low-stock alerts
- 🚫 **Void & Returns** - Transaction management with stock restoration
- 📊 **Reports** - Daily/monthly/yearly sales analytics
- 🏁 **End of Day** - Cash counting, expense tracking, variance reports
- 👥 **User Management** - Admin and staff roles

## 🔄 Auto-Updates

This app automatically checks for updates:
- Updates are downloaded in the background
- You'll be prompted to restart when updates are ready
- No manual installation required

## 💾 Data Storage

Your data is stored locally on your computer:
- **Windows**: `%APPDATA%\SC Med POS\pos_inventory.db`
- **macOS**: `~/Library/Application Support/SC Med POS/pos_inventory.db`

## 🔐 Security

- All data is stored locally on your machine
- No cloud connectivity or data transmission
- Your business data never leaves your computer

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
- Apple Silicon (M1/M2) or Intel Mac

## 📋 User Roles

| Role | Access |
|---|---|
| **admin** | Full access - POS, Inventory, Reports, User Management |
| **staff** | POS, Inventory, Transactions, End of Day (no Reports/User Management) |

---

**Version**: [Latest release version](../../releases/latest)  
**License**: ISC  
**Developer**: SC Med Pharmacy

© 2026 SC Med Pharmacy. All rights reserved.
