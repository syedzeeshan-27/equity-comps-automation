# Equity Research Tool: Automated Comps Puller

Built to automate equity research comps analysis and eliminate manual data entry.

## The Why

Manually pulling valuation metrics from Yahoo Finance for a sector comp set takes 1–2 hours. This tool replaces that workflow with a reusable 10-second Python automation tool.

## What This Tool Does

• Pulls live financial data using yfinance

• Extracts Market Cap, P/E Ratio, Revenue Growth (YoY %), Enterprise Value, and EBITDA

• Calculates EV/EBITDA

• Computes sector median valuation metrics

• Flags companies as 'Undervalued' if P/E is 20% below sector median

• Exports a clean, analyst-grade Excel file

## Key Features

✓ Automated EV/EBITDA calculation

✓ Dynamic sector median benchmarking

✓ Undervaluation screening logic

✓ Error handling for missing financial data

✓ Reusable function-based Python structure

Tech Stack:

- - Python
    - Pandas
    - yfinance
    - openpyxl

## How To Run:

1\. Install dependencies:

pip install yfinance pandas openpyxl

2\. Run the script:

 sector_comps_tool.py

3\. Output: SaaS_Comps_Function_Version.xlsx

## ⚠️ Limitations & Data Notes

- **Not a Primary Data Source:** Yahoo Finance aggregates financial data from exchanges and third-party providers. It is not an official filing source (e.g., SEC, SEDAR).
- **Potential Data Gaps:** Some companies — particularly non-U.S., small-cap, or recently listed firms — may have incomplete or delayed financial data (e.g., EBITDA or enterprise value may be missing).
- **Reporting Differences:** International companies may follow different accounting standards or reporting timelines.
- **Usage Terms:** Data is used for informational and educational purposes only and should not be redistributed or relied upon for investment decisions.
- **Technical Note:** This project uses the yfinance library, the most widely adopted Python interface for programmatic extraction of structured Yahoo Finance data.
