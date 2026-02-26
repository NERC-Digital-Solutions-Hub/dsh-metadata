# Supporting information

- Study site and purpose
  - Focus on Blelham Tarn with four inflows and one outflow (Blelham Beck); data collected to estimate stream discharges and related water level, temperature, and atmospheric conditions.
  - Map and figures referenced: Fig. 1 (map of inflows/outflow) and Fig. 2 (rating curve).

- Datasets and file structure
  - BLEL_Stream_Discharge.csv: Date (dd/mm/yyyy); discharge (m3/s) for Blelham Beck (outflow) and three inflows (Wray Beck, Fish Pond Beck, Ford Wood Beck).
  - BLEL_water_level_temp.csv: Date and Time (dd/mm/yyyy hh:mm); water level pressure (kPa), temperature (°C), depth (cm), barometric pressure (kPa); stream identifier (Blelham Beck outflow or Wray Beck inflow).
  - BLEL_point_discharge.csv: Date (dd/mm/yyyy); Stream name; Discharge (m3/s) for individual streams (points).
  - Instruments: In-Situ Level TROLL at Blelham Beck outflow; SonTek handheld Acoustic Doppler Velocimeter (ADV) for flow velocity.

- Data collection procedures
  - Hydrometric setup: Level logger installed at Blelham Beck outflow capturing water level, depth, and temperature every 15 minutes; air temperature and atmospheric pressure recorded at Wray Beck bank.
  - Stream surveying: Detailed cross-sections at inflows/outflow; depth at bank-full recorded every 10 cm using measuring stick and tape.
  - Flow velocity: ADV measurements at 3–4 evenly spaced locations across each inflow/outflow; depths recorded; sampling locations adjusted to avoid bedload obstructions.

- Discharge calculation methods
  - Mean-Section Method (for each segment):
    - Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b
      - v = flow velocity; d = depth; b = number of segments.
  - Mean discharge for each stream (BLEL_Point_Discharge.csv) calculated by summing segment discharges and dividing by the number of segments.
  - Rating curve: discharge vs. water level at the closest sampling time; used a polynomial relationship to convert remaining water level values to daily discharge for the outflow.
    - Polynomial equation (example): y = 2.9011 x^2 − 1.7618 x + 0.2899; R² = 0.8162.
  - Outflow–inflow relationships: daily discharge for inflows estimated from outflow using linear relationships; linear regressions with R² values provided in Table 1.
    - S1 & S2: y = 0.1746x + 0.0055; R² = 0.7294
    - S2 & S3: y = 0.3649x + 0.0023; R² = 0.7069
    - S2 & S4: y = 0.1375x + 0.01; R² = 0.5187
  - Alternative approach: inflow discharge as a proportion of outflow with fixed percentages:
    - Wray Beck 26.35%
    - Fish Pond Beck 49.22%
    - Ford Wood Beck 24.43%

- Data processing and quality assurance
  - Monthly quality checks of logger data and field measurements.
  - Data merged across datasets to produce daily discharge values for all streams.
  - Relationships and rating curves validated statistically (R² values reported).

- Data usage and GIS relevance
  - Enables creation of map-based hydro network datasets (inflows/outflow, discharge by stream, time series).
  - Supports spatial analysis of flow partitioning among inflows and temporal changes in discharge.
  - Useful for integrating water level, depth, and temperature with discharge for hydro-geomorphic studies.
  - Highlights data availability issues (multiple data sources, varying resolutions) and the need for consistent data standards in GIS workflows.