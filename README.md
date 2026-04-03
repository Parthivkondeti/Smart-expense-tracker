# Smart Expense Tracker

A personal finance dashboard built with pure HTML, CSS, and JavaScript — no frameworks, no backend, no database.

## 🔗 Live Demo
**[View Live →](https://parthivkondeti.github.io/Smart-expense-tracker/)**

---

## About the Project

SmartTrack is a fully client-side expense tracking dashboard that helps users monitor their income, expenses, and savings in real time. Built as a portfolio project to demonstrate skills in DOM manipulation, data visualisation, localStorage persistence, and UI/UX design.

---

## Features

- **📊 Interactive Charts** — 6-month bar chart, category donut chart, and 30-day balance trend line chart using Chart.js
- **💰 Live Stats** — Real-time balance, income, expense, and savings rate cards
- **🔍 Smart Search** — Instantly filter transactions by description or category
- **🗓 Month Navigator** — Browse any previous month's data
- **🎯 Budget Tracker** — Set a monthly spending limit with a warning at 80% and alert at 100%
- **🔁 Recurring Transactions** — Mark transactions to auto-repeat every month
- **📥 Excel Export** — Export transactions and monthly summary to a real `.xlsx` file
- **💡 Smart Insights** — Auto-generated observations comparing spending month-over-month
- **🌓 Dark / Light Mode** — Toggle between themes
- **📱 Responsive** — Works on mobile and desktop
- **💾 Persistent Storage** — All data saved locally using localStorage (no login needed)

---

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and form inputs |
| CSS3 | Styling, glass morphism, dark/light themes, responsive grid |
| JavaScript (Vanilla) | All logic — data handling, filtering, rendering, localStorage |
| [Chart.js](https://www.chartjs.org/) | Bar, Donut, and Line chart rendering |
| [SheetJS (xlsx)](https://sheetjs.com/) | Excel file generation in the browser |

---

## Project Structure

```
Smart-expense-tracker/
│
├── index.html        # Complete app — HTML + CSS + JS in one file
└── README.md         # Project documentation
```

---

## How to Run

**Option 1 — Live Demo (recommended)**
Click the Live Demo link above.

**Option 2 — Run locally**
```bash
# Clone the repo
git clone https://github.com/Parthivkondeti/Smart-expense-tracker.git

# Open the file in your browser
cd Smart-expense-tracker
open index.html
```
No installation. No npm. No server. Just open the file.

---

## How It Works

### Data Flow
```
User fills form → addTx() validates input → saves to localStorage
                                          → refreshAll() updates all sections
```

### Key Functions

| Function | What it does |
|---|---|
| `addTx()` | Reads form, validates, builds transaction object, saves |
| `delTx(id)` | Removes transaction by ID using array filter |
| `renderTxList()` | Filters by month + type + search, builds HTML list |
| `updateStats()` | Calculates income / expense / savings, updates cards |
| `renderBarChart()` | Prepares 6-month data arrays, draws Chart.js bar chart |
| `exportExcel()` | Builds 2D arrays, converts to .xlsx via SheetJS |

### Data Persistence
All transactions are stored in the browser's `localStorage` under the key `st2_txs`. No server, no database, no account needed. Data persists across sessions as long as the user doesn't clear their browser storage.

---

## 📸 Screenshots

<img width="1876" height="976" alt="image" src="https://github.com/user-attachments/assets/bb846ba2-43fb-4304-85f0-4fb1415f3ca1" />
<img width="1885" height="986" alt="image" src="https://github.com/user-attachments/assets/82b0dbe8-8264-45bf-a4f6-8bfacb6fd20f" />


---

## Future Improvements

- [ ] Cloud sync (Firebase)
- [ ] Multiple account support
- [ ] CSV import from bank statements
- [ ] Annual report view
- [ ] Spending predictions using trend analysis

---

## Author

**Parthiv Kondeti**
- GitHub: [@Parthivkondeti](https://github.com/Parthivkondeti)
- LinkedIn: [linkedin.com/in/parthiv-kondeti](https://linkedin.com/in/parthiv-kondeti)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
