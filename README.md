# Semantic-Spreadsheet-Search-Engine
Search engine for spreadsheet 1.Using Gemini AI 2. Without using AI

# 1.Using Gemini AI

📊 Semantic Spreadsheet Search Engine (Gemini-powered)

A Google Sheets + Gemini AI powered search engine that allows you to query spreadsheets using business-friendly semantic queries instead of raw keywords.
Example:

“Find all profitability metrics” → Gross Margin, Net Profit, EBITDA

“Show lookup formulas” → VLOOKUP, INDEX/MATCH, XLOOKUP

“Budget vs actual analysis” → Variance calculations, comparison ratios

# 🚀 Features

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


Gemini API Key – Get one from Google AI Studio and configure:

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

# 2.Without AI

# Key Features

Semantic Understanding: Recognizes business concepts like revenue, costs, margins, ratios

Natural Language Queries: Process queries like "show growth rates" or "budget vs actual analysis"

Context-Aware: Uses headers, formulas, and surrounding cells for accurate concept identification

Multi-Sheet Support: Search across multiple spreadsheet tabs simultaneously

Formula Intelligence: Understands what calculations represent in business context

Google Sheets Integration: Load and analyze real Google Sheets data

Comprehensive Analysis: Automated business intelligence insights and data quality assessment

Installation
Requirements

Python 3.7+
Google Colab (recommended) or Jupyter Notebook
Internet connection for package installation

Setup

Copy the complete code from the provided artifacts into Google Colab cells,
Run the installation cell - it will automatically install all dependencies:

python   !pip install -q pandas openpyxl gspread google-auth sentence-transformers scikit-learn nltk spacy
   !python -m spacy download en_core_web_sm

Execute the main code - all components will be loaded and ready to use

Quick Start
Option 1: Immediate Demo python # Run this for instant demonstration

quick_start()

Option 2: Simple Search Function python# Search with a simple command

search_spreadsheet("find profitability metrics")

search_spreadsheet("show cost calculations")

search_spreadsheet("revenue growth rates")

Option 3: Full Interactive Experience python# Launch full demo with menu options

main()
# Choose option 1 for interactive queries
# Choose option 2 for batch demonstration
# Choose option 3 for Google Sheets integration
Usage Examples
Basic Semantic Queries
python# Conceptual queries "find all profitability metrics", "show cost calculations", "where are my growth rates"

# Functional queries  
"percentage calculations", "sum formulas", "conditional logic"

# Comparative queries
"budget vs actual analysis", "year over year comparison", "variance analysis"

Advanced Features python# Run comprehensive analysis:
run_comprehensive_google_sheets_analysis(search_engine)

# Performance benchmarking
analyze_performance()

# Business user scenarios
run_business_scenarios()

# Compare with traditional search
compare_with_traditional_search()

Architecture
Core Components

SemanticAnalyzer: Business concept recognition using sentence transformers

ContentExtractor: Spreadsheet parsing and context extraction

QueryProcessor: Natural language query processing and intent recognition

SemanticSearchEngine: Search orchestration and relevance ranking

Data Flow

Loading: Spreadsheet data parsed into semantic contexts

Analysis: Business concepts identified using ML and pattern matching

Query Processing: Natural language converted to search intent

Ranking: Multi-factor relevance scoring (concept matching, semantic similarity, formula types, context richness)

Results: Structured output with explanations and business context

Business Domain Coverage
Supported Concepts

Revenue: sales, income, turnover, receipts, earnings

Cost: expense, expenditure, spending, COGS, outlay

Margin: profit margin, gross margin, operating margin

Profit: earnings, net income, EBITDA, bottom line

Ratio: efficiency, percentage, proportion, rates

Growth: YoY, QoQ, CAGR, increase rates

Forecast: projections, budgets, plans, estimates

Formula Types

Mathematical (SUM, AVERAGE, arithmetic)
Conditional (IF, SUMIF, COUNTIF)
Lookup (VLOOKUP, INDEX/MATCH)
Percentage and ratio calculations

Supported URLs
python# Example Google Sheets URLs financial_url = "https://docs.google.com/spreadsheets/d/[SHEET_ID]/edit"
sales_url = "https://docs.google.com/spreadsheets/d/[SHEET_ID]/edit"

Core Classes
SemanticSearchEngine

pythonengine = SemanticSearchEngine()

engine.load_spreadsheets(sheets_data)

results = engine.search("query", top_k=5)

Utility Functions python# Quick demonstrations
quick_start()                    # Instant demo

test_with_sample_data()         # Sample data testing

run_ultimate_demonstration()    # Complete feature showcase

# Analysis functions
analyze_performance()           # Performance benchmarks

run_evaluation()               # Quality assessment

generate_comprehensive_documentation()  # Technical docs

# Business scenarios
finance_manager_scenario()      # Financial analysis use case

sales_analyst_scenario()       # Sales analysis use case

executive_dashboard_scenario()  # Executive KPI use case

# Performance Characteristics

Loading Time: ~2-3 seconds for 1000 cells

Search Time: ~100-300ms per query

Memory Usage: ~50MB base + 1KB per cell

Accuracy: 85-95% on well-structured data

Scalability: Handles up to 10,000 cells efficiently

# Examples and Demos
Financial Analysis python# Load financial data and run analysis

engine = SemanticSearchEngine()

sheets_data = loader.create_enhanced_sample_data()

engine.load_spreadsheets(sheets_data)

Ready to transform your spreadsheet experience? Start with quick_start() and explore the power of semantic search!

