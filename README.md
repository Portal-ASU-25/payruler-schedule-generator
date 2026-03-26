# 📅 EData Schedule Generator

A modern, offline-first web application for generating employee shift schedules in CSV format, specifically designed for EData and similar BPO companies.

## Commands
- `npm start` - Start the development server
- `npm run dist` - Build the production
## Build Instructions
- Clone the repository
- Run `npm install` to install dependencies
- Run `npm start` to launch the app in development mode
- Run `npm run dist` to create a production build (outputs to `dist/` folder)
- Make Sure You Run as Administrator on Powershell to avoid permission issues when running the dist version
- Open `dist/EData Schedule Generator.exe` to use the application

## ✨ Features

- **Fast Schedule Generation** – Create schedules for first half (1-15), second half (16-end), or custom date ranges
- **Shift Time Display** – Full shift names with time schedules (AM9, PM7, NS2, RD, etc.)
- **Auto Weekend Handling** – Automatically sets weekends as Rest Day (RD) with one click
- **Bulk Actions** – Set all days to AM9, PM7, NS2, or RD instantly
- **Editable Table** – Modify individual shifts, rest days, and onsite status
- **CSV Export** – Download ready-to-upload CSV files with proper formatting
- **Profile Management** – Save and quickly load employee profiles (ID No, Name, Prefix, Default Shift)
- **Save/Load Schedules** – Save generated schedules to IndexedDB and reload them anytime
- **Custom Cut-off Dates** – Support for special payroll periods
- **Fully Offline** – Works without internet after initial load
- **Modern UI** – Built with Material-UI (MUI) and React

## 🚀 How to Use

1. **Open the HTML file** in any modern browser (Chrome, Edge, Firefox recommended)
2. **Quick Load Profile** (optional) – Select a saved employee profile
3. **Fill in employee details**:
   - ID No
   - Full Name
   - Year and Month
   - Period (First Half / Second Half) or Custom Dates
4. **Configure options**:
   - CSV Prefix (usually Last Name)
   - Default Shift
   - Auto-set weekends as Rest Day
5. Click **"Generate Schedule Table"**
6. Edit shifts as needed using the dropdowns or bulk buttons
7. **Download CSV** or **Save Schedule** for future use

## 📁 File Structure
EData-Schedule-Generator/
├── EData-Schedule-Generator.html    ← Main application file (single file)
└── README.md


> **Note**: This is a single-file application. No installation or server required.

## 💾 Data Storage

- **Employee Profiles** – Saved using `idb-keyval` (IndexedDB)
- **Saved Schedules** – Saved using **Dexie.js** (IndexedDB)
- All data stays in your browser – completely private and offline

## 🎯 Supported Shifts

| Code   | Description                  |
|--------|------------------------------|
| RD     | Rest Day                     |
| AM9    | 06:00 AM - 02:00 PM          |
| PM7    | 02:00 PM - 10:00 PM          |
| NS2    | 10:00 PM - 06:00 AM          |
| ...    | (Full list available in app) |

## 🛠️ Technologies Used

- **React** 18 (via esm.sh)
- **Material-UI (MUI)** – Modern component library
- **Dexie.js** – IndexedDB wrapper
- **idb-keyval** – Simple key-value storage
- **React Router** – Client-side routing
- **TypeScript** (with `@ts-nocheck` for simplicity)

## 📝 CSV Output Format

The generated CSV includes:
- `idno`
- `name`
- `date` (MM/DD/YYYY)
- `shiftcode`
- `restday` (YES/NO)
- `onsite` (YES/NO)

Perfect for direct upload to most scheduling/payroll systems.

## 📌 Tips

- Use **Last Name** as CSV Prefix for easier file identification
- Save frequently used employees as **Profiles** for faster workflow
- Use **Save Schedule** feature when you need to make small adjustments later
- Works great on both desktop and tablet

## 🔧 Future Enhancements (Ideas)

- Dark mode support
- Import existing CSV
- Print-friendly schedule view
- Database integration

---

**Made with ❤️ for EData Team**

*Single HTML file – Just open and start generating schedules!*
