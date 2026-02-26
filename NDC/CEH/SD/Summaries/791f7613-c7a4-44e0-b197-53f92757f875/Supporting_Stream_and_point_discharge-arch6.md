# Supporting information

- Overview
  - Project collects and processes hydrological data for Blelham Tarn inflows and outflow to derive daily discharge for each stream.
  - Data are organized into three CSV files and supported by field measurements, quality checks, and derived discharge relationships.

- Data collected and collection methods
  - Inflows and outflow
    - Four inflows; three accessible. Outflow monitored at Blelham Beck.
  - Instruments
    - Water level logger (TROLL) at the outflow: records water level, depth, and water temperature every 15 minutes (BLEL_water_level_temp.csv).
    - Logger on the bank of Wray Beck: records air temperature and atmospheric pressure (used to adjust water level pressure).
    - SonTek handheld Acoustic Doppler Velocimeter (ADV) used to measure flow speed at 3–4 locations across each inflow/outflow; records water depth and position relative to the detailed survey.
  - Quality control
    - Data downloaded and quality checked monthly.

- Site surveys and hydraulic calculations
  - Detailed stream surveys at inflows and outflow to determine stream shapes; depth at bank-full level recorded every 10 cm.
  - Mean-Section Method (Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b) used to compute segment discharges.
  - Daily discharge per stream (BLEL_Point_Discharge.csv) obtained by summing Qseg values and dividing by the number of segments (Q).

- Rating curve and discharge derivation
  - A rating curve links outflow discharge to water level near sampling times (Fig. 2).
  - Polynomial discharge–water level relation (R^2 = 0.8162) used to convert remaining water level values to daily discharge.
  - Example equation (approximate): y ≈ 2.9011 x^2 − 1.7618 x + 0.2899 (x = water level; y = discharge).

- Discharge for inflows (rest of the streams)
  - Daily discharge for inflows calculated using relationships to the outflow discharge, with R^2 values shown in Table 1.
  - Alternatively, inflow discharges can be estimated as a proportion of the outflow:
    - Wray Beck: 26.35%
    - Fish Pond Beck: 49.22%
    - Ford Wood Beck: 24.43%

- Data structure and contents
  - BLEL_Stream_Discharge.csv: Date; discharge (m3/s) for Blelham Beck (outflow), Wray Beck, Fish Pond Beck, Ford Wood Beck.
  - BLEL_water_level_temp.csv: Date and Time; water level pressure (kPa); temperature (°C); Depth (cm); Barometric pressure (kPa); stream (Blelham Beck – outflow or Wray Beck – inflow).
  - BLEL_point_discharge.csv: Date; Stream name; Discharge (m3/s).

- Additional materials and references
  - In-field figures: Fig.1 map of Blelham Tarn and inflows/outflow; Fig.2 rating curve.
  - Table 1: Linear regression equations between outflow and inflow discharges (S1–S4) with corresponding R^2 values (e.g., S1&S2: y = 0.1746x + 0.0055, R^2 = 0.7294; S2&S3: y = 0.3649x + 0.0023, R^2 = 0.7069; S2&S4: y = 0.1375x + 0.01, R^2 = 0.5187).
  - References: Shaw, E. M., Beven, K. J., Chappell, N. A. and Lamb, R. (2011). Hydrology in Practice. Chapter 7: River Flow.

- Practical outcomes for data use
  - Produces self-serve time series of daily discharges for each stream.
  - Enables cross-system comparisons via regression relationships between inflows and outflow.
  - Supports transparency and reuse by providing raw measurements, processed discharges, and the rating curve-derived daily discharges.