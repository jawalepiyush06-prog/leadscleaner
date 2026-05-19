# Leads Cleaner — Google Maps Scrape Formatter

A free, offline web app to clean and format Google Maps scraped CSV leads into
professional Excel files. No server, no API, no tokens. Runs entirely in your browser.

## How to Run

### Option 1 — Double-click (simplest)
Just open `index.html` directly in Chrome or Edge. No setup needed.

### Option 2 — Localhost (recommended for bulk files)
If your browser blocks local file access, run a quick local server:

**Python (recommended):**
```bash
cd leads_processor
python -m http.server 8080
```
Then open: http://localhost:8080

**Node.js:**
```bash
npx serve .
```
Then open the URL it shows.

## How to Use

1. Open the app in your browser
2. Drag & drop your CSV files (one or many at once)
3. See a live preview of the cleaned data
4. Click **Process & Download ZIP**
5. Extract the ZIP — each CSV gets its own cleaned `.xlsx` file
   plus a `_COMBINED_ALL_LEADS.xlsx` merging everything

## Output Excel Structure (per file)

| Sheet | Contents |
|---|---|
| All Leads | All records, formatted |
| Has Website | Only leads WITH a website |
| No Website | Only leads WITHOUT a website |
| Summary | Quick count dashboard |

## Columns in Output

- `#` — Serial number
- `Clinic / Doctor Name` — Cleaned name
- `Mobile Number` — Normalized 10-digit format
- `Address` — Extracted from 7 scattered raw columns
- `Google Maps Link` — Direct Maps URL
- `Website` — Website URL (blank if none)
- `Has Website` — Yes / No
- `Rating` — Google star rating
- `No. of Reviews` — Review count
- `Category` — Pediatrician, Hospital, etc.

## Requirements

- Any modern browser (Chrome, Edge, Firefox)
- CSV files must be from the same Google Maps scraper format

## Cost

Zero. No internet required after first load (fonts load from Google Fonts on first open only).
