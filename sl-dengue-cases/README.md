# Sri Lanka Dengue Cases (Weekly)

Weekly dengue cases by climatic zone, province, and district, 23 Dec 2006 – 13 Dec 2025.

Source: https://www.kaggle.com/datasets/tharinduheshan/dengue-research-2006-2026

## Hierarchy

Total → Climatic Zone (3) → Province (12) → District (25)

- Total: 1
- Climatic Zone: 3
- Province: 12
- District: 25
- Series: 41

## Mapping

### Wet Zone

| Province | Districts |
|---|---|
| Central (2) | Kandy, Nuwara Eliya |
| Sabaragamuwa (2) | Kegalle, Ratnapura |
| Southern (2) | Galle, Matara |
| Western (3) | Colombo, Gampaha, Kalutara |

### Dry Zone

| Province | Districts |
|---|---|
| Eastern (3) | Ampara, Batticaloa, Trincomalee |
| North Central (2) | Anuradhapura, Polonnaruwa |
| Northern (5) | Jaffna, Kilinochchi, Mannar, Mullaitivu, Vavuniya |
| Southern (1) | Hambantota |
| Uva (1) | Monaragala |

### Intermediate Zone

| Province | Districts |
|---|---|
| Central (1) | Matale |
| North Western (2) | Kurunegala, Puttalam |
| Uva (1) | Badulla |

## Data Processing & Imputation Notes

- **Monaragala Gap:** Aug 2019 – Dec 2020 reporting blackout filled via weekly seasonal median decomposition.
- **War-Era Lag (2006–2009):** Northern districts (Kilinochchi, Mullaitivu, Jaffna) backcast using post-war seasonal baseline.

## Files

`data.csv` — 991 × 41
- Rows: weeks, date index (`YYYY-MM-DD`), 2006-12-23 to 2025-12-13
- Columns: stringified paths, e.g. `['Colombo', 'Western', 'Wet Zone']`, `['Western', 'Wet Zone']`, `['Wet Zone']`, `['Total']`

`agg_mat.csv` — 41 × 25
- Rows = `data.csv` columns, same order
- Columns = 25 district series
- Total row: all ones; zone rows: 1 for member districts; province rows: 1 for member districts; identity block for districts
