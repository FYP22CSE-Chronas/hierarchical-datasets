# Weighted Commodity Price Index

Daily price indices (base 100 on 2022-01-03) across 9 benchmark commodity futures, aggregated via non-integer economic expenditure weights, 2022-01-03 – 2024-12-31.

Source: CME / ICE / NYMEX via Yahoo Finance

## Hierarchy

Total Weighted Commodity Index → Commodity Sector (3) → Individual Commodity (9)

- Total: 1
- Commodity Sector: 3 (Energy, Metals, Agriculture)
- Commodity Series: 9 (Crude Oil, Brent, Gas, Gold, Silver, Copper, Corn, Wheat, Soybeans)
- Total Series: 13
- Bottom Series: 9

## Mapping & Weights

Unlike standard hierarchical time series where parents are unweighted arithmetic sums ($S_{ij} \in \{0, 1\}$), this dataset uses an explicit **weighted aggregation matrix** where row elements represent portfolio/economic index weights ($\sum w_i = 1.0$):

| Sector | Sector Weight | Commodity | Ticker | Intra-Sector Weight | Global Index Weight |
|---|:---:|---|:---:|:---:|:---:|
| **Energy** | **0.45** | Crude Oil (WTI) | `CL=F` | 0.50 | **0.225** |
| **Energy** | **0.45** | Brent Crude | `BZ=F` | 0.30 | **0.135** |
| **Energy** | **0.45** | Natural Gas (Henry Hub) | `NG=F` | 0.20 | **0.090** |
| **Metals** | **0.35** | Gold | `GC=F` | 0.50 | **0.175** |
| **Metals** | **0.35** | Silver | `SI=F` | 0.20 | **0.070** |
| **Metals** | **0.35** | Copper | `HG=F` | 0.30 | **0.105** |
| **Agriculture** | **0.20** | Corn | `ZC=F` | 0.40 | **0.080** |
| **Agriculture** | **0.20** | Wheat | `ZW=F` | 0.35 | **0.070** |
| **Agriculture** | **0.20** | Soybeans | `ZS=F` | 0.25 | **0.050** |

*Check:* $\sum_{\text{all}} w_i = 0.225 + 0.135 + 0.090 + 0.175 + 0.070 + 0.105 + 0.080 + 0.070 + 0.050 = 1.000$.

## Key Events & Data Notes

- **Non-Binary Summing Matrix:** Proves and evaluates reconciliation on non-binary aggregation operators $S \in \mathbb{R}^{13 \times 9}$ where weights are continuous fractions rather than integers.
- **Geopolitical Energy Shocks (2022):** Extreme price spike in crude oil and natural gas following European supply disruptions.
- **Inflation Hedge Rotations:** Gold price appreciation during 2023–2024 monetary tightening.
- **Exact Coherence:** Reconstructed directly via $y = S \cdot b$. Maximum absolute difference equals 0.0.

## Files

`data.csv` — 754 × 13
- Rows: trading days, date index (`YYYY-MM-DD`), 2022-01-03 to 2024-12-31
- Columns: stringified paths, e.g. `['Crude Oil', 'Energy']`, `['Energy']`, `['Global Commodity Index']`

`agg_mat.csv` — 13 × 9
- Rows = `data.csv` columns, same order
- Columns = 9 commodity series
- Top row: continuous global weights summing to 1.0; sector rows: continuous intra-sector weights; bottom 9 rows: 9 × 9 identity block
