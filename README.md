# Semantic-Spreadsheet-Search-Engine
Search engine for spreadsheet 1.Using Gemini AI 2. Without using AI

1.Using Gemini AI

📊 Semantic Spreadsheet Search Engine (Gemini-powered)

A Google Sheets + Gemini AI powered search engine that allows you to query spreadsheets using business-friendly semantic queries instead of raw keywords.
Example:

“Find all profitability metrics” → Gross Margin, Net Profit, EBITDA

“Show lookup formulas” → VLOOKUP, INDEX/MATCH, XLOOKUP

“Budget vs actual analysis” → Variance calculations, comparison ratios

🚀 Features

🔍 Semantic Search – Ask natural-language business queries.

🧮 Formula Awareness – Detects AVERAGE, SUMIF, VLOOKUP, etc.

📈 Business Domain Mapping – Handles profitability, growth rates, efficiency ratios, etc.

📂 Multi-Sheet Support – Load multiple Google Sheets simultaneously.

🎨 User-Friendly Output – Results displayed with clear formatting + emojis.

⚠️ Robust Handling – Deals with duplicate/blank headers and parsing errors.

📦 Installation

Run inside Google Colab or local Python environment:

pip install gspread google-auth google-auth-oauthlib google-generativeai pandas

🔑 Authentication

Google Account – Required for accessing Google Sheets.

from google.colab import auth
auth.authenticate_user()


Gemini API Key – Get one from Google AI Studio
 and configure:

import google.generativeai as genai
genai.configure(api_key="YOUR_API_KEY")

🏗️ Project Structure
├── SpreadsheetLoader      # Loads and cleans Google Sheets
├── SemanticSearchEngine   # Handles query processing & semantic matching
├── DemoInterface          # CLI for interactive querying
├── main()                 # Entry point

⚙️ Usage
# Run main program
main()


Interactive mode starts:

🎉 Semantic Spreadsheet Search Engine (Gemini-powered)!
📥 Loading <spreadsheet-url> ...
✅ Loaded 3 sheets

🔍 Enter your query (or 'exit' to quit):


Example Query:

🔍 Enter your query: Find efficiency ratios

✨ === RESULTS === ✨
ROI
├──📍 Location: Finance!Col_C12
├── 🔢 Value/Formula: NetIncome / TotalAssets
└──💡 Relevance: Measures return generated per unit of assets.

💡 Supported Query Types

Business Metrics: Profitability, Growth rates, Efficiency ratios

Formulas: AVERAGE, SUMIF, IF, VLOOKUP, INDEX/MATCH

Comparisons: Budget vs Actual, Benchmarking, Time Series

⚡ Performance Considerations

Limits context to 300 rows per query for speed & token efficiency.

Uses Gemini 1.5 Flash for fast responses (low-latency).

Can be extended with caching for repeated queries.

🛠️ Known Challenges

Large spreadsheets may be truncated.

Some formulas may appear simplified.

Requires Gemini API availability.

📚 Example Queries
"Find all profitability metrics"
"Show cost calculations"
"Where are my growth rates?"
"Find efficiency ratios"
"Show percentage calculations"
"Budget vs actual analysis"

2.Without AI
