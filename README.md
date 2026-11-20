# Explainable Stock Analyzer

A privacy-friendly static HTML app for technical analysis using imported daily OHLCV CSV data. It calculates EMA20, SMA50, SMA200, RSI(14), relative volume, gaps, and clustered swing support/resistance zones.

## Deploy on GitHub Pages
1. Create a new public or private GitHub repository.
2. Upload `index.html` and this `README.md` to the repository root.
3. Open **Settings > Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then click **Save**.
6. Open the Pages URL after deployment finishes.

## Use
- Click **Load demo** to test the interface. Demo prices are synthetic and are not MSFT market data.
- Export daily price history from a legitimate market-data provider or brokerage as CSV.
- Required headers: `Date,Open,High,Low,Close,Volume`.
- Import at least 30 rows; 200+ daily rows are recommended for the SMA200.

## Important limitations
This version intentionally does not embed a market-data API key in browser code because keys committed to GitHub can be stolen. For live data, use a serverless proxy such as a GitHub-hosted frontend plus Cloudflare Worker, Netlify Function, or Vercel Function, with the provider key stored as a secret. Do not scrape Fidelity.

The output is educational and descriptive, not financial advice or an automated trading system. Support and resistance are zones inferred from historical pivots and may fail, especially around earnings and news.
