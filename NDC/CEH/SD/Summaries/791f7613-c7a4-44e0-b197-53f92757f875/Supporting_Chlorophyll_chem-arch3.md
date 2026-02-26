# BLEL_Chlorophyll_chem.csv

- Purpose: Chemical analysis for chlorophyll a to indicate phytoplankton biomass in Blelham Tarn; data collected to support monitoring of aquatic health across lake and inflow/outflow points.

- Sampling design and data collection:
  - Samples collected in 2016 (500 mL) and 2017 (1000 mL) at metre intervals from 1 m to 10 m (and 0.5 m then 1 m to 9 m in 2017) in the lake, plus samples at three inflows and the outflow.
  - Depth measurements are recorded as Depth (m) with -1 as the first measurement from the surface down to -10 deepest measurement.
  - Water samples were filtered immediately after collection using GF/C filter paper (5.5 cm diameter) and then frozen; analyses performed within a month of collection.

- Analytical method:
  - Chlorophyll a extraction with methanol; color measured using a spectrophotometer.
  - Wavelengths: 750 nm for background turbidity (A750) and 665 nm for chlorophyll a maximum (A665).
  - Corrected absorbance: Acorr665 = A665 − A750.
  - Chlorophyll a concentration calculation: Chlorophyll a = (13.9 × Acorr665 × 1/d) × (v/V), where
    - d = path-length of cuvette (cm),
    - V = volume of sample filtered (mL),
    - v = volume of extract (mL).
  - Includes methodological references (Talling 1974) for spectrophotometric procedures.

- Data structure and variables:
  - Columns include Date (dd/mm/yyyy), Depth (m) (ranging from -1 to -10), and Chlorophyll a (µg/L).
  - Data reflect a depth-profile approach to capture phytoplankton biomass across the water column.

- Study site context:
  - Blelham Tarn located in the Lake District, North West England.
  - Monitoring buoy located at the deepest point (approximately 14.5 m) for in-lake sampling context.

- Timeline and references:
  - Data collected during 2016 and 2017.
  - Site and methods referenced: Ramsbottom (1976) depth charts; Talling (1974) methods for photosynthetic pigments and spectrophotometric procedures.