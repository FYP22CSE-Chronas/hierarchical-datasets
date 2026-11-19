# Dengue Cases — Sri Lanka (Weekly)

Weekly dengue cases, 2025 W01 – 2026 W45.

Source: https://www.epid.gov.lk/weekly-epidemiological-report/weekly-epidemiological-report

## Hierarchy

Total → Province (9) → District (25)

- Total: 1
- Province: 9
- District: 25
- Series: 35

## Mapping

| Province | Districts |
|---|---|
| Western Province | Colombo, Gampaha, Kalutara |
| Central Province | Kandy, Matale, Nuwara Eliya |
| Southern Province | Galle, Matara, Hambantota |
| Northern Province | Jaffna, Kilinochchi, Mannar, Vavuniya, Mullaitivu |
| Eastern Province | Trincomalee, Batticaloa, Ampara |
| North Western Province | Kurunegala, Puttalam |
| North Central Province | Anuradhapura, Polonnaruwa |
| Uva Province | Badulla, Monaragala |
| Sabaragamuwa Province | Ratnapura, Kegalle |

## Key Events & Data Notes

- **Monsoon Cycles:** Biannual transmission peaks during Southwest (May–Aug) and Northeast (Oct–Jan) monsoon rains.
- **Dry-Season Zeros:** Intermittent zero-case weeks occur naturally in small, dry, or high-altitude districts.

## Files

`data.csv` — 90 × 35
- Rows: weeks, unnamed index, dated to week-start Monday
- Columns: stringified paths, e.g. `['Colombo', 'Western Province']`, `['Total']`

`agg_mat.csv` — 35 × 25
- Rows = `data.csv` columns, same order
- Columns = 25 districts
- Total row, one row per province, then identity block
