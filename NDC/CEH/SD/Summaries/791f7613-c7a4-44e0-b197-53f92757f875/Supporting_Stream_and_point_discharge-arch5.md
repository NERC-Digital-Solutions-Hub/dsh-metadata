# Supporting information

## Overview
- Dataset collected for the NEC05744 project by Emma Gray, comprising BLEL_Stream_Discharge.csv, BLEL_water_level_temp.csv, and BLEL_point_discharge.csv.
- Purpose: quantify inflows and outflow at Blelham Tarn, including water level, depth, temperature, and discharge; enable derivation of daily discharge and assessment of relationships between inflow and outflow.

## Data collection and processing
- Blelham Tarn has four inflows; three are accessible. A water level logger (TROLL) at the outflow (Blelham Beck) records water level, depth, and water temperature every 15 minutes. A log at the Wray Beck bank records air temperature and atmospheric pressure to adjust water level pressure.
- Data are downloaded and quality checked monthly.
- Detailed stream surveys measure stream geometry and depth at bank-full level (every 10 cm).
- Flow velocity measured with a SonTek ADV at 3–4 locations per inflow/outflow, recording depth and location. Adjustments made for bedload obstructions.
- Discharge calculations use the Mean-Section Method: Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b; mean discharge Q for each stream is the sum of Qseg divided by the number of segments.
- A rating curve relates outflow discharge to the closest-time inflow/outflow water level; the polynomial relationship is:
  y = 2.9011 x^2 − 1.7618 x + 0.2899, with R^2 = 0.8162.
- Daily discharge for remaining inflows is calculated via regression relationships between outflow and inflow discharges (Table 1). Alternatively, inflow discharges can be estimated as proportions of the outflow: Wray Beck 26.35%, Fish Pond Beck 49.22%, Ford Wood Beck 24.43%.

## Data structure and contents
- BLEL_Stream_Discharge.csv: Date (dd/mm/yyyy); columns for discharge (m3/s) at Blelham Beck (outflow), Wray Beck, Fish Pond Beck, Ford Wood Beck.
- BLEL_water_level_temp.csv: Date Time (dd/mm/yyyy hh:mm); water level pressure (kPa); temperature (°C); depth (cm); barometric pressure (kPa); stream identifier (Blelham Beck-outflow or Wray Beck-inflow).
- BLEL_point_discharge.csv: Date (dd/mm/yyyy); Stream name; Discharge (m3/s).
- Instruments: Level TROLL data logger at the outflow; SonTek ADV handheld flow meter.

## Methods and standards
- Mean-Section Method used for segment discharges; rating curve applied to convert water level to discharge.
- Documented linear regression relationships between outflow and inflow discharges (S1–S4) with corresponding equations and R^2 values.
- Units, time stamps, and instrument details are recorded to support traceability and reproducibility.

## Provenance, quality, and governance
- Data collected and processed by a named researcher; monthly QA ensures data quality and consistency.
- Metadata includes instrument types, sampling intervals, measurement units, and data processing steps.
- Data are structured to support discovery, reuse, and integration with related datasets; suitable for sharing under standard data governance practices.

## References
- Shaw, E. M., Beven, K. J., Chappell, N. A., and Lamb, R. (2011). Hydrology in Practice. Abingdon [UK], Spon Press. Chapter 7: River Flow.