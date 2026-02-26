# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2014 to 2018. Feuchtmayr, H., Carter, H.T., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P.O., Mackay, E.B., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

- Purpose and scope
  - Ongoing, fortnightly monitoring dataset for South Basin of Windermere (Cumbria, England) covering 2014–2018.
  - Variables include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
  - Data enable map-based analyses of physical, chemical, and biological conditions over time.

- Sampling regime and collection methods
  - Measurements taken fortnightly from a boat at a marked location (buoy) at the deepest part of the lake.
  - Water samples integrated from 0 to 7 m depth.
  - Reported variables and units:
    - TEMP: surface temperature, °C
    - OXYG: surface oxygen saturation, % air-saturation
    - SECC: Secchi depth, m
    - ALKA: alkalinity, µg CaCO3 per L
    - pH: pH
    - NH4N: ammonium, µg N per L
    - NO3N: nitrate, µg N per L
    - PO4P: soluble reactive phosphate, µg P per L
    - TOTP: total phosphorus, µg P per L
    - SIO2: dissolved reactive silicon, µg per L
    - TOCA: phytoplankton chlorophyll a, µg per L
  - Sign (if<LOD) column indicates values below detection limit with a < symbol.

- Data structure and access
  - Data delivered as comma-separated values (CSV).
  - Columns:
    - Date: measurement date
    - Variable, Description: variable name and description (as listed above)
    - Value, Description: measured value for each variable
    - Sign (if<LOD), Description: indicator for below detection limit
  - GIS use: straightforward for time-series layering and spatial visualization when combined with location data (buoy position at deepest part of South Basin).

- Quality control and data quality
  - Raw data presented; not yet quality controlled and calibrated.
  - Data have been double entered and visually checked.
  - Missing data attributed to weather conditions or staff shortages.

- Temporal and spatial coverage
  - Temporal: January 2014 – end of 2018 (fortnightly sampling).
  - Spatial: South Basin of Windermere, Cumbria, England.
    - Spatial reference is tied to measurements from buoy at the deepest part of the lake; precise coordinates not specified in the metadata.

- Data provenance and funding
  - Collection supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE program delivering National Capability.

- Example usage and supporting materials
  - Dataset has been used in multiple recent publications and reports, illustrating applications in climate analysis, storm impacts on lakes, fish environmental DNA distribution, and broader lake ecology studies (examples cited in the document).

- Considerations for GIS workflows
  - Treat the dataset as raw time-series data requiring standard GIS preprocessing (QC, calibration if needed) before map-based visualization.
  - Merge with complementary spatial layers (bathymetry, land use, meteorology) for enriched spatial analyses.
  - Be mindful of below-LOD values in analyses; interpret or impute appropriately.
  - Use the 0–7 m integrated sampling depth to align with other lake datasets that may have different depth stratifications.