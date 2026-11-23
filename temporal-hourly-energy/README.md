# Temporal Hierarchy — Intra-Day Electricity Generation

Temporal hierarchical decomposition of daily electric grid load into multi-scale time intervals (Hours → 4-Hour Shifts → Semi-Diurnal Day/Night → Daily Total), 2026-01-01 – 2026-11-04.

Source: National Energy System Operator (NESO) / UK National Grid

## Hierarchy

Daily Total (1) → Semi-Diurnal Phase (2) → 4-Hour Operational Period (6) → Hourly Interval (24)

- Daily Total: 1
- Semi-Diurnal Phase: 2 (Daytime Peak, Nighttime Off-Peak)
- Operational Block: 6 (4-hour intervals)
- Hourly Interval: 24 (H00 to H23)
- Total Series: 33
- Bottom Series: 24

## Mapping

| Semi-Diurnal Phase | 4-Hour Operational Block | Hourly Bottom Series | Hours Spanned |
|---|---|---|---|
| Nighttime (20:00-07:59) | Night Deep (00-03) | H00, H01, H02, H03 | 00:00 – 03:59 |
| Nighttime (20:00-07:59) | Morning Ramp (04-07) | H04, H05, H06, H07 | 04:00 – 07:59 |
| Daytime (08:00-19:59) | Day Morning (08-11) | H08, H09, H10, H11 | 08:00 – 11:59 |
| Daytime (08:00-19:59) | Day Afternoon (12-15) | H12, H13, H14, H15 | 12:00 – 15:59 |
| Daytime (08:00-19:59) | Evening Peak (16-19) | H16, H17, H18, H19 | 16:00 – 19:59 |
| Nighttime (20:00-07:59) | Night Winding (20-23) | H20, H21, H22, H23 | 20:00 – 23:59 |

## Key Events & Data Notes

- **Pure Temporal Hierarchy:** Every level represents a mathematical time aggregation operator (Hour $\rightarrow$ 4-Hour $\rightarrow$ 12-Hour $\rightarrow$ 24-Hour). Zero spatial, geographic, or product classifications.
- **Diurnal Load Dynamics:** Captures the early morning load surge, afternoon plateau, evening cooking/heating peak, and overnight baseload trough.
- **Exact Additive Coherence:** Each operational block equals the exact sum of its 4 member hours; semi-diurnal blocks equal the sum of their 12 member hours; daily total equals the sum of all 24 hours. Zero missing days, zero NaNs.

## Files

`data.csv` — 308 × 33
- Rows: calendar days, date index (`YYYY-MM-DD`), 2026-01-01 to 2026-11-04
- Columns: stringified paths, e.g. `['H18', 'Evening Peak (16-19)']`, `['Evening Peak (16-19)', 'Daytime (08:00-19:59)']`, `['Daily Total Generation']`

`agg_mat.csv` — 33 × 24
- Rows = `data.csv` columns, same order
- Columns = 24 bottom hourly series
- Row 0: all ones; intermediate block rows: 1 for member hours; bottom 24 rows: 24 × 24 identity block
