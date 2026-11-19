# World Mortality — All-Cause Deaths

Monthly all-cause mortality, Jan 2015 – Dec 2024.

## Hierarchy

Total → Continent (6) → Country (76)

- Total: 1
- Continent: 6
- Country: 76
- Series: 83

## Mapping

### Africa — 8 countries

| Countries |
|---|
| Algeria, Botswana, Cabo Verde, Egypt, Mauritius, Namibia, Seychelles, Tunisia |

### Asia — 25 countries

| Countries |
|---|
| Azerbaijan, Bhutan, Brunei, Hong Kong, Japan, Jordan, Kazakhstan, Kuwait, Kyrgyzstan, Lebanon, Macao, Malaysia, Maldives, Mongolia, Oman, Palestine, Philippines, Qatar, Singapore, Taiwan, Tajikistan, Thailand, Turkey, United Arab Emirates, Uzbekistan |

### Europe — 18 countries

| Countries |
|---|
| Albania, Andorra, Armenia, Belarus, Bosnia, Faroe Islands, Georgia, Gibraltar, Kosovo, Liechtenstein, Moldova, Monaco, North Macedonia, Russia, San Marino, Serbia, Transnistria, Ukraine |

### North America — 16 countries

| Countries |
|---|
| Antigua and Barbuda, Aruba, Bahamas, Barbados, Belize, Bermuda, Costa Rica, Cuba, Dominican Republic, El Salvador, Greenland, Jamaica, Nicaragua, Panama, Saint Kitts and Nevis, Saint Vincent and the Grenadines |

### Oceania — 3 countries

| Countries |
|---|
| Fiji, French Polynesia, New Caledonia |

### South America — 6 countries

| Countries |
|---|
| Argentina, Bolivia, Brazil, Paraguay, Suriname, Uruguay |

## Files

`data.csv` — 120 × 83
- Rows: months, date index (YYYY-MM-DD), 2015-01-01 to 2024-12-01
- Columns: stringified paths, e.g. `['Japan', 'Asia']`, `['Asia']`, `['Total']`

`agg_mat.csv` — 83 × 76
- Rows = `data.csv` columns, same order
- Columns = 76 country series
- Total row: all ones; continent rows: 1 for member countries; identity block for countries
