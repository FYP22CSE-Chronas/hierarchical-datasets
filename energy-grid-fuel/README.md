# Energy Grid Generation by Fuel Mix

Hourly electricity generation (in Megawatts, MW) across generation technologies and fuel sources, 2026-01-01 – 2026-11-04.

Source: National Energy System Operator (NESO) / UK National Grid Historic Generation Mix Data Portal

## Hierarchy

Total Generation → Generation Family (4) → Fuel Technology (11)

- Total: 1
- Generation Family: 4
- Fuel Technology: 11
- Series: 16
- Bottom Series: 11

## Mapping

| Generation Family | Fuel / Generation Technology | Description |
|---|---|---|
| Clean & Renewable | Wind (Transmission) | High-voltage grid-connected offshore and onshore wind turbines |
| Clean & Renewable | Wind (Embedded) | Localized distribution-connected small wind farms |
| Clean & Renewable | Solar PV | Photovoltaic solar generation |
| Clean & Renewable | Hydroelectric | Run-of-river and conventional hydro dams |
| Clean & Renewable | Biomass | Sustainable forestry and bioenergy combustion plants |
| Nuclear Generation | Nuclear | Continuous zero-carbon baseload atomic fission |
| Fossil Fuels | Natural Gas | Combined-cycle (CCGT) and open-cycle gas turbines |
| Fossil Fuels | Coal | Legacy coal-fired thermal generation |
| Balancing & Storage | Interconnector Imports | Subsea high-voltage DC electricity transfers from European grids |
| Balancing & Storage | Pumped Storage | Hydroelectric pumped-storage peak balancing units |
| Balancing & Storage | Other Flex | Battery energy storage systems and miscellaneous rapid flex |

## Key Events & Data Notes

- **Intra-Day Solar & Wind Peaks:** Sharp diurnal solar cycle coupled with weather-driven wind intermittency.
- **Dispatchable Gas Balancing:** Natural gas ramping inversely with renewable wind surges to balance grid frequency.
- **Exact Coherence:** Hourly total generation equals the exact sum of all 11 constituent generation technologies. Zero missing timestamps, zero NaNs.

## Files

`data.csv` — 7,392 × 16
- Rows: hours, timestamp index (`YYYY-MM-DD HH:MM:SS`), 2026-01-01 00:00:00 to 2026-11-04 23:00:00
- Columns: stringified paths, e.g. `['Solar PV', 'Clean & Renewable']`, `['Clean & Renewable']`, `['Total Generation']`

`agg_mat.csv` — 16 × 11
- Rows = `data.csv` columns, same order
- Columns = 11 bottom fuel series
- Total row: all ones; category rows: 1 for member fuel sources; bottom 11 rows: 11 × 11 identity block
