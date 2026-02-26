# Supporting information File: BLEL_Chlorophyll_chem.csv

- Goal and scope
  - Chemical analysis dataset intended as an indicator of phytoplankton biomass (chlorophyll a) for Blelham Tarn.
  - Collected in 2016 and 2017 to support aquatic ecosystem assessments; includes lake and inflow/outflow samples.

- Data content
  - Chlorophyll a concentration in micrograms per liter (µg/L).
  - Columns: Date (dd/mm/yyyy), Depth (m), Chlorophyll a (µg/L).
  - Depth convention: Depth values are negative to denote distance from the surface, ranging from -1 (surface) to -10 (deepest measurement).

- Sampling and methods
  - Water collected from the lake (500 mL) and streams (1000 mL) at metre intervals from the surface down to 10 m in 2016; 0.5 m then 1 m to 9 m in 2017; plus samples from three inflows and the outflow.
  - Immediate filtration on GF/C filter paper (5.5 cm diameter); filters frozen and samples analyzed within a month.
  - Chlorophyll a extraction with methanol; color measured with a spectrophotometer.
  - Spectrophotometer setup: A750 for background turbidity; A665 for chlorophyll a maximum.
  - Concentration calculation: Chlorophyll a = (13.9 × A_corr665 × 1/d) × (v/V), where
    - A_corr665 = A665 − A750 (corrected absorbance),
    - d = cuvette path-length (cm),
    - V = volume of sample filtered (mL),
    - v = volume of extract (mL).

- Spatial and sampling context
  - Location: Blelham Tarn, Lake District, NW England.
  - Monitoring buoy located at the lake’s deepest point (approximately 14.5 m).
  - Figure reference: includes map of the lake with buoy location.
  - Sampling also includes inflows and the outflow, enabling assessment of chlorophyll a inputs/throughput.

- Data structure and units
  - Date format: day/month/year (dd/mm/yyyy).
  - Depth: negative meters from surface (-1 to -10).
  - Chlorophyll a: micrograms per liter (µg/L).

- Temporal coverage
  - Data collected across 2016 and 2017, with differing depth interval schemes between years as described above.
  - Dates are present in the dataset for each measurement.

- Quality and provenance references
  - Methodological basis: standard spectrophotometric procedures for measuring photosynthetic pigments.
  - References:
    - Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association.
    - Talling J.F. (1974) Photosynthetic pigments. In: Manual on Methods for Measuring Primary Productivity in Aquatic Environments.
  - Metadata implies data were collected and processed following these established procedures.