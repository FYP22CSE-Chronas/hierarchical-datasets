# S&P 500 Volume by GICS Sector

Daily trading share volume across the 11 Global Industry Classification Standard (GICS) sectors, 2022-01-03 – 2024-12-31.

Source: Yahoo Finance / S&P Dow Jones Indices GICS Classification

## Hierarchy

Total Market Volume → Sector (11) → Stock (33)

- Total: 1
- Sector: 11
- Stock: 33
- Series: 45
- Bottom Series: 33

## Mapping

| Sector | Constituent Stocks (Top Liquid Large-Caps) |
|---|---|
| Information Technology | AAPL (Apple), MSFT (Microsoft), NVDA (Nvidia) |
| Financials | JPM (JPMorgan Chase), BAC (Bank of America), V (Visa) |
| Health Care | UNH (UnitedHealth Group), JNJ (Johnson & Johnson), LLY (Eli Lilly) |
| Consumer Discretionary | AMZN (Amazon), TSLA (Tesla), HD (Home Depot) |
| Communication Services | GOOGL (Alphabet), META (Meta Platforms), NFLX (Netflix) |
| Industrials | CAT (Caterpillar), GE (GE Aerospace), UNP (Union Pacific) |
| Consumer Staples | WMT (Walmart), PG (Procter & Gamble), KO (Coca-Cola) |
| Energy | XOM (ExxonMobil), CVX (Chevron), COP (ConocoPhillips) |
| Utilities | NEE (NextEra Energy), SO (Southern Company), DUK (Duke Energy) |
| Real Estate | PLD (Prologis), AMT (American Tower), EQIX (Equinix) |
| Materials | APD (Air Products and Chemicals), SHW (Sherwin-Williams), FCX (Freeport-McMoRan) |

## Key Events & Data Notes

- **Tech Volume Dominance:** Driven by the AI market rally and megacap tech liquidity (NVDA, MSFT, AAPL).
- **Rate Cycle Volatility:** High cross-sector rotation between Energy (2022 inflation surge) and Tech/Growth (2023-2024 easing).
- **Exact Additive Coherence:** Sector volume is the exact sum of member equities; total market volume is the sum of all sectors. Zero missing values, zero NaNs.

## Files

`data.csv` — 753 × 45
- Rows: trading days, date index (`YYYY-MM-DD`), 2022-01-03 to 2024-12-31
- Columns: stringified paths, e.g. `['AAPL', 'Information Technology']`, `['Information Technology']`, `['Total']`

`agg_mat.csv` — 45 × 33
- Rows = `data.csv` columns, same order
- Columns = 33 stock series
- Total row: all ones; sector rows: 1 for member equities; bottom 33 rows: 33 × 33 identity block
