# US Deaths

Monthly deaths by sex and age group, Jan 2005 – Dec 2015.

## Hierarchy

Total → Sex (2) → Age Group (11)

- Total: 1
- Sex: 2
- Age Group: 22
- Series: 25

## Mapping

| Sex | Age Groups |
|---|---|
| Male | Under 1 year, 1 - 4 years, 5 - 14 years, 15 - 24 years, 25 - 34 years, 35 - 44 years, 45 - 54 years, 55 - 64 years, 65 - 74 years, 75 - 84 years, 85 years and over |
| Female | Under 1 year, 1 - 4 years, 5 - 14 years, 15 - 24 years, 25 - 34 years, 35 - 44 years, 45 - 54 years, 55 - 64 years, 65 - 74 years, 75 - 84 years, 85 years and over |

## Files

`data.csv` — 132 × 25
- Rows: months, date index (`YYYY-MM-DD`), 2005-01-01 to 2015-12-01
- Columns: stringified paths, e.g. `['Under 1 year', 'Male']`, `['Male']`, `['Total']`

`agg_mat.csv` — 25 × 22
- Rows = `data.csv` columns, same order
- Columns = 22 age group series
- Total row: all ones; sex rows: 1 for member age groups; identity block for age groups
