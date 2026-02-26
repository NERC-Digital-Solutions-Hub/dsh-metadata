# Supporting information

- Study by Emma Gray for project NEC05744; dataFiles: BLEL_Stream_Discharge.csv, BLEL_water_level_temp.csv, BLEL_point_discharge.csv.
- Location: Blelham Tarn with four inflows (three accessible) and one outflow (Blelham Beck).

## Data collection and instruments

- Outflow monitoring: water level logger (TROLL) at Blelham Beck recording water level, depth, and water temperature every 15 minutes.
- Atmospheric adjustment: logger on the bank of Wray Beck recorded air temperature and atmospheric pressure to adjust water level pressure at Blelham Beck.
- Data quality: data downloaded and quality checked monthly.
- Channel surveys: detailed stream surveys to determine stream shape; depth at bank-full level recorded every 10 cm.
- Flow measurements: SonTek handheld Acoustic Doppler Velocimeter (ADV) used to measure flow velocity at 3–4 evenly spaced locations across each inflow/outflow; adjustments made to locations to avoid bedload obstructions.

## Discharge calculation methods

- Mean-Section Method: Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b (v = velocity, d = depth, b = number of segments).
- Mean discharge for each stream (BLEL_Point_Discharge.csv) obtained by summing Qseg and dividing by the number of Qseg.
- Rating curve: discharge at outflow vs. water level; used to convert water level to daily discharge with polynomial relation.
  - y = 2.9011 x^2 − 1.7618 x + 0.2899, R^2 = 0.8162 (x = water level, y = discharge).
- Daily discharge for inflows: derived from relationships between outflow discharge and inflow discharges (shown in Table 1) with corresponding R^2 values.
- Alternative inflow discharge method: inflows as proportions of outflow:
  - Wray Beck 26.35%, Fish Pond Beck 49.22%, Ford Wood Beck 24.43%.

## Data structure and contents

- BLEL_Stream_Discharge.csv: Date (dd/mm/yyyy); discharge (m3/s) for Blelham Beck (outflow) and inflows (Wray Beck, Fish Pond Beck, Ford Wood Beck).
- BLEL_water_level_temp.csv: Date and Time (dd/mm/yyyy hh:mm); water level pressure (kPa); temperature (°C); depth (cm); barometric pressure (kPa); stream label (Blelham Beck outflow or Wray Beck inflow).
- BLEL_point_discharge.csv: Date (dd/mm/yyyy); Stream name; Discharge (m3/s).
- Instruments: Level TROLL data logger at outflow; SonTek ADV handheld flow meter.

## Figures, tables and references

- Fig.1: Map of Blelham Tarn and inflows/outflow.
- Fig.2: Rating curve for Blelham Beck.
- Table 1: Linear regression equations linking outflow to inflow discharges (S1–S4) with R² values:
  - S1 & S2: y = 0.1746x + 0.0055, R² = 0.7294
  - S2 & S3: y = 0.3649x + 0.0023, R² = 0.7069
  - S2 & S4: y = 0.1375x + 0.01, R² = 0.5187
- References: Shaw, Beven, Chappell, and Lamb (2011), Hydrology in Practice, Chapter 7: River Flow. Page 117.

## Data quality, storage and accessibility

- Monthly quality assurance of loggers and measurements.
- Data reliability supported by cross-checks between outflow/inflow relationships and rating curves.
- Aimed at standardised, transparent outputs (discharge by stream) suitable for storage and sharing via appropriate data portals, promoting broader access to underlying data.