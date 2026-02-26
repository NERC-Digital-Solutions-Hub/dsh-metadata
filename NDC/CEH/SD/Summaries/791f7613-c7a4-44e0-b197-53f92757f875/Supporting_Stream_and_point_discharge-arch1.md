# Supporting information

- Collected by Emma Gray for the project NEC05744.

## Data collected and instruments

- Blelham Tarn has four inflows; three are accessible.
- A water level logger (TROLL) at the outflow (Blelham Beck) recorded water level, depth, and water temperature every 15 minutes (BLEL_water_level_temp.csv).
- A logger on the bank of Wray Beck recorded air temperature and atmospheric pressure; used to adjust water level pressure at Blelham Beck.
- Data were downloaded and quality checked monthly.
- Detailed stream surveys were conducted at inflows and outflow to map stream shapes; depth at bank full recorded every 10 cm.
- A Sontek handheld Acoustic Doppler Velocimeter (ADV) measured flow velocity at 3–4 locations across each inflow/outflow; depth recorded; locations adjusted to avoid bedload obstructions.
- Bedload and location adjustments noted during surveys.

## Methods for discharge calculation

- Mean-Section Method used to compute segment discharges:
  - Qseg = 0.5(v1 + v2) × 0.5(d1 + d2) × b
  - v = velocity, d = depth, b = number of segments.
- Mean discharge (Q) for each stream (BLEL_Point_Discharge.csv) obtained by summing Qseg and dividing by the number of segments.
- A rating curve was plotted between outflow discharge and the closest-in-time inflow discharge; used to convert water level to daily discharge via a polynomial:
  - y = 2.9011 x^2 − 1.7618 x + 0.2899 (R^2 = 0.8162), where x is water level and y is discharge.
- Daily discharge for remaining inflows (BLEL_Stream_Discharge.csv) computed using relationships between outflow discharge and inflow discharges; R^2 values provided in Table 1.
- Alternatively, inflow discharges can be calculated as proportions of the outflow:
  - Wray Beck 26.35%, Fish Pond Beck 49.22%, Ford Wood Beck 24.43%.

## Data files and structure

- BLEL_Stream_Discharge.csv: Date (dd/mm/yyyy); discharges (m^3/s) for Blelham Beck, Wray Beck, Fish Pond Beck, Ford Wood Beck.
- BLEL_water_level_temp.csv: DateTime (dd/mm/yyyy hh:mm); water level pressure (kPa); temperature (°C); depth (cm); barometric pressure (kPa); stream (Blelham Beck-outflow or Wray Beck-inflow).
- BLEL_point_discharge.csv: Date (dd/mm/yyyy); Stream name; Discharge (m^3/s).

## Calculations and relationships

- Outflow–inflow discharge relationships (linear regressions) used to estimate inflows from outflow:
  - S1 & S2: y = 0.1746x + 0.0055; R^2 = 0.7294
  - S2 & S3: y = 0.3649x + 0.0023; R^2 = 0.7069
  - S2 & S4: y = 0.1375x + 0.0100; R^2 = 0.5187
- These relationships and their R^2 values are summarized in Table 1 of the document.

## Quality assurance and data processing

- Monthly quality checks and data quality assurance performed.
- Temperature and pressure data used to adjust water level measurements.
- Measurements adjusted to avoid bedload obstructions; measurement locations may be altered to maintain data quality.

## References

- Shaw, E. M., Beven, K. J., Chappell, N. A., and Lamb, R. (2011). Hydrology in Practice. Chapter 7: River Flow. Spon Press. Page 117.