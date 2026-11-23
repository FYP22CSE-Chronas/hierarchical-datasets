# H&M Fashion Product Taxonomy Sales

Daily garment sales volume across H&M's multi-level fashion product taxonomy, covering 4.47 million real-world transactions.

Source: H&M Group / Kaggle Personalized Fashion Recommendations Dataset

## Hierarchy

Total Fashion Sales → Collection / Index Group (5) → Product Category (38)

- Total: 1
- Collection / Index Group: 5
- Product Category (Leaves): 38
- Total Series: 44
- Bottom Series: 38

## Mapping

| Collection / Index Group | Active Product Categories |
|---|---|
| Ladieswear | Accessories, Garment Full body, Garment Lower body, Garment Upper body, Shoes, Socks & Tights, Swimwear, Underwear |
| Menswear | Accessories, Garment Full body, Garment Lower body, Garment Upper body, Shoes, Socks & Tights, Swimwear, Underwear |
| Divided (Youth / Casual) | Accessories, Garment Full body, Garment Lower body, Garment Upper body, Shoes, Socks & Tights, Swimwear, Underwear |
| Baby/Children | Accessories, Garment Full body, Garment Lower body, Garment Upper body, Shoes, Socks & Tights, Swimwear, Underwear |
| Sport | Accessories, Garment Lower body, Garment Upper body, Underwear, Swimwear, Socks & Tights |

## Key Events & Data Notes

- **Pure Product Taxonomy:** Hierarchy is defined strictly by retail catalog semantics (collections down to apparel garment types) with zero geographic attributes.
- **Fast-Fashion Intermittency:** Reflects rapid seasonal product turnover, apparel drops, and distinct shopping patterns between kids, womenswear, and sport collections.
- **Exact Additive Coherence:** Aggregate collections are the exact arithmetic sums of member apparel groups; total fashion sales equals the sum of all collections. Zero missing values, zero NaNs.

## Files

`data.csv` — 107 × 44
- Rows: days, date index (`YYYY-MM-DD`)
- Columns: stringified paths, e.g. `['Garment Upper body', 'Ladieswear']`, `['Ladieswear']`, `['Total Fashion Sales']`

`agg_mat.csv` — 44 × 38
- Rows = `data.csv` columns, same order
- Columns = 38 product category bottom series
- Total row: all ones; collection rows: 1 for member garment groups; bottom 38 rows: 38 × 38 identity block
