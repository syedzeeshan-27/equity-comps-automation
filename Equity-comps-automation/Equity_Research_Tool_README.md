# 📊 Equity Research Tool: Automated SaaS Comps Puller

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

Built to automate equity research comps analysis and eliminate manual data entry.

---

## 💡 The Why

Manually pulling valuation metrics from Yahoo Finance for a sector comp set takes
1–2 hours. This tool replaces that workflow with a reusable, 10-second Python automation.

---

## ⚙️ What This Tool Does

- Pulls **live financial data** using `yfinance`
- Extracts **Market Cap, P/E Ratio, Revenue Growth (YoY %), EV, and EBITDA**
- Calculates **EV/EBITDA** automatically
- Computes **sector median** valuation metrics across the comp set
- Flags companies with a **"Low P/E vs. Peers"** screening flag if P/E is 20% below sector median
- Exports a clean, **analyst-grade Excel file** with institutional formatting

---

## ✅ Key Features

| Feature | Details |
|---|---|
| EV/EBITDA Calculation | Computed automatically from live data |
| Sector Median Benchmarking | Dynamic — updates with whatever tickers you pass in |
| P/E Screening Flag | Flags names trading at a discount to peer median |
| Error Handling | Skips tickers with missing data, logs the error |
| Function-Based Structure | `get_sector_comps()` is fully reusable and importable |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `yfinance` | Live financial data extraction |
| `pandas` | Data manipulation and median calculations |
| `openpyxl` | Excel file creation and formatting |

---

## 🚀 How To Run

**1. Clone the repo**
```bash
git clone https://github.com/YOUR_USERNAME/equity-comps-automation.git
cd equity-comps-automation
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the script**
```bash
python sector_comps.py
```

**4. Output**

Opens `SaaS_Comps_Function_Version.xlsx` in your project folder —
formatted and ready for use.

---

## 📁 Project Structure
```
equity-comps-automation/
├── sector_comps.py                  # Main script + get_sector_comps() function
├── SaaS_Comps_Function_Version.xlsx # Sample output
├── requirements.txt                 # Pinned dependencies
└── README.md
```

---

## ⚠️ Limitations & Data Notes

> **Not a Primary Data Source:** Yahoo Finance aggregates data from exchanges and
> third-party providers — it is not an official filing source (e.g., SEC, SEDAR).

- **Potential Data Gaps:** Non-U.S., small-cap, or recently listed firms may have
  incomplete or delayed data (e.g., missing EBITDA or enterprise value)
- **Reporting Differences:** International companies may follow different accounting
  standards or reporting timelines
- **Usage Terms:** For informational and educational purposes only — not to be
  relied upon for investment decisions

  ## 📸 Sample Output

> The script pulls live data and auto-generates this formatted Excel file in under 10 seconds.

![Sample Output]([assets/output_preview.png](https://github.com/syedzeeshan-27/equity-comps-automation/blob/5899fca143460b6d9b4b613293de3b94717a3014/Screenshot%202026-03-01%20143936.png)
