# Supporting information

- Data files and provenance
  - BLEL_Stream_Discharge.csv, BLEL_water_level_temp.csv and BLEL_point_discharge.csv
  - Collected by Emma Gray for the project NEC05744

- Study site and instrumentation
  - Blelham Tarn with four inflows; three accessible
  - Inflow/outflow water level logger installed at Blelham Beck (outflow) recording water level, depth, and water temperature every 15 minutes (BLEL_water_level_temp.csv)
  - Logger on Wray Beck bank recorded air temperature and atmospheric pressure to adjust Blelham Beck water level pressure
  - Data downloaded and quality checked monthly
  - Detailed stream surveys at inflows/outflow to map stream shapes; depth at bank-full level recorded every 10 cm
  - Sontek handheld Acoustic Doppler Velocimeter (ADV) used for flow speed at 3–4 evenly spaced locations per inflow/outflow; depth recorded; measurement locations adjusted to avoid bedload obstructions

- Data collection procedures
  - Stream discharge estimated with the Mean-Section Method: Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b
  - Mean discharge for each stream (BLEL_Point_Discharge.csv) computed by summing Qseg values and dividing by the number of Qseg
  - A rating curve (Fig. 2) relates discharge to water level at the closest sampling time at the outflow; polynomial relationship: y = 2.9011 x^2 − 1.7618 x + 0.2899 (R^2 = 0.8162)
  - Daily discharge for remaining inflows calculated using relationships with the outflow; regression details in Table 1
  - Alternative discharge estimate method: inflows as a proportion of the outflow
    - Wray Beck: 26.35%
    - Fish Pond Beck: 49.22%
    - Ford Wood Beck: 24.43%

- Data structure and fields
  - BLEL_Stream_Discharge.csv: Date (dd/mm/yyyy), discharge (m3/s) for Blelham Beck, Wray Beck, Fish Pond Beck, Ford Wood Beck
  - BLEL_water_level_temp.csv: DateTime (dd/mm/yyyy hh:mm), water level pressure (kPa), temperature (°C), depth (cm), barometric pressure (kPa), stream (Blelham Beck outflow or Wray Beck inflow)
  - BLEL_point_discharge.csv: Date (dd/mm/yyyy), Stream name, Discharge (m3/s)
  - Instruments: In-Situ Level TROLL data logger (outflow) and SonTek ADV hand-held flow meter

- Modelling relationships and key equations
  - Rating curve: y = 2.9011 x^2 − 1.7618 x + 0.2899 (R^2 = 0.8162)
  - Outflow–inflow linear relationships (Table 1):
    - S1 & S2: y = 0.1746 x + 0.0055 (R^2 = 0.7294)
    - S2 & S3: y = 0.3649 x + 0.0023 (R^2 = 0.7069)
    - S2 & S4: y = 0.1375 x + 0.01 (R^2 = 0.5187)

- Data quality, governance, and notes
  - Monthly quality checks of logger data
  - Adjustments to measurement locations to avoid bedload obstructions
  - Data synthesis relies on proximity in time between water level and discharge measurements (closest sampling time)

- Visuals and references
  - Fig.1: Map of Blelham Tarn and inflows/outflow
  - Fig.2: Rating curve
  - Table 1: Regression equations between outflow and inflow discharges
  - Reference: Shaw, E. M., Beven, K. J., Chappell, N. A. and Lamb, R. (2011). Hydrology in Practice. Chapter 7: River Flow, Page 117