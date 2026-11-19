# Dengue Cases — Sri Lanka

Monthly dengue cases, Jan 2010 – Dec 2020.

Source: https://www.kaggle.com/datasets/nsadaa/sri-lanka-dengue-cases-2010-2020

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

## Files

`data.csv` — 132 × 35
- Rows: months, unnamed index
- Columns: stringified paths, e.g. `['Colombo', 'Western Province']`, `['Total']`

`agg_mat.csv` — 35 × 25
- Rows = `data.csv` columns, same order
- Columns = 25 districts
- Total row, one row per province, then identity block
