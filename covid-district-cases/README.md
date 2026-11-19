# COVID-19 Cases — Sri Lanka

Daily cumulative confirmed COVID-19 cases by district, 1 Apr 2020 – 18 May 2021.

Source: https://www.kaggle.com/datasets/asheniranga/sri-lanka-covid19-dataset

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

`data.csv` — 412 × 35
- Rows: days, unnamed index, `YYYY-MM-DD`
- Columns: stringified paths, e.g. `['Colombo', 'Western Province']`, `['Total']`

`agg_mat.csv` — 35 × 25
- Rows = `data.csv` columns, same order
- Columns = 25 districts
- Total row, one row per province, then identity block
