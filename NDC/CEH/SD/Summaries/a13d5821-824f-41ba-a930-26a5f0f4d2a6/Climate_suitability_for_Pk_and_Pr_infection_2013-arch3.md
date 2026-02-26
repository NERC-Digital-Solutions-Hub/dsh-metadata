# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

- Objectives
  - Refine climate suitability models for Phytophthora infection by incorporating updated epidemiological data and literature.
  - Develop separate models for Pr and Pk to reflect species-specific temperature and humidity responses.
  - Improve spatial resolution to reduce data gaps, particularly around coastal regions.
  - Validate model outputs against field data on onward transmission to assess whether climatically suitable areas are associated with spread; extend Scotland-based models to the UK.

- Modelling approach
  - Use 48-hour (two-day) windows in a 4 km grid to reflect infection process continuity (up to ~32 hours at 2°C).
  - Invert lab-derived infection time curves to derive hourly infection rates for each pathogen and apply to hourly temperature series.
  - Infection is considered successful over a 48-hour period if hourly rates sum to one, applying pathogen-specific temperature and humidity rules.
  - Lower/upper temperature thresholds and relative humidity rules differ by pathogen:
    - Pr: infection between 2°C and 29°C; 85% RH for 10+ hours on both days.
    - Pk: infection between 3°C and 27°C; 85% RH for 10+ hours on both days; below 2°C, no further completion for 16+ hours makes the 48-hour period fail.
  - Spatial and temporal data
    - Climate inputs: hourly relative humidity and temperature, 2007–2011, 4 km grid across the UK (23246 land squares); provided by Met Office.
    - Output: for each grid cell and year, the predicted number of days suitable for infection; reprojected to OSGB 5.5 grid for overlay with risk factors.
    - Modelling implemented in R; outputs expressed as average annual days suitable per square.

- Pathogen-specific rules and data inputs
  - Lower thresholds: Pr and Pk not possible to complete infection below 2°C; for Pk, 16+ hours below 2°C yields a fail in the 48-hour period.
  - Upper thresholds: Pr up to 29°C (with 1/3 success probability between 28–29°C); Pk up to 27°C.
  - Humidity: 85% RH for at least 10 hours on both days required for infection success for both pathogens.

- Outputs and interpretation
  - Spatial measures: maps of expected days per year with suitable climate for Pr and Pk infection; UK-wide and Scotland-focused results.
  - Temporal patterns: Pr infection predicted to peak in November–February; Pk infection peaks June–August.
  - Geographical patterns: Scotland predicted to have higher suitability for Pr than for Pk; west and south coasts, central belt, and parts of the highlands show higher average suitability for Pr; Pk suitability is generally lower but relatively higher in Argyll & Bute, Ayrshire, Dumfries & Galloway, central highlands, Perthshire, and north Highlands including Orkney/Skye.
  - Variability: year-to-year variation in suitable days can be substantial, particularly in southern Scotland; Pr shows broader geographic and seasonal distribution than Pk due to faster and more reliable infection at low temperatures.

- Model validation with field data
  - Datasets and approach
    - (i) Wild plantings and established plantings in England and Wales (2002–2009), with 240 positives out of 1981 squares, using species-level infection status.
    - (ii) Scottish non-trade premises (2007–2012), 93 positives out of 795 squares, using combined infection status for Pr/Pk.
    - (iii) Larch fragments across Scotland (Forestry Commission and others), 229 positives out of 25791 fragments, modeled for Pr.
  - Analysis: binary logistic regression to test whether infection status is predicted by climate-suitability values; AUC values indicate discrimination ability.
  - Key results
    - All three datasets show climate-suitability values as significant predictors of infection status.
    - England/Wales (i): Pr squares had ~20 more suitable days/year; Pk squares had ~7 more suitable days/year; AUCs: Pr ~0.63, Pk ~0.72.
    - Scottish non-trade premises (ii): positives had ~20 more suitable days/year; AUC ~0.65.
    - Larch plantations (iii): Pr-positive squares had ~40 more suitable days/year; AUC ~0.81.
  - Interpretations
    - The Pr model often performs better at predicting presence of Pr in Scotland and broader distribution due to its wider suitability across seasons.
    - In England/Wales, the Pk model occasionally provides stronger discrimination due to the species’ more defined environmental requirements.
    - Overall, climate-suitability outputs are strong predictors of observed infection presence, supporting use in risk-based monitoring and decision-making.

- Key findings and implications for monitoring and policy
  - The UK-wide extension of Scotland-grounded models provides a spatially explicit tool for assessing climate-driven infection risk.
  - The metric of interest is the average annual number of days with suitable climate for infection per grid cell, enabling prioritisation of surveillance and management in high-risk areas and periods.
  - Seasonality and regional patterns inform targeted monitoring windows (Pr broadly year-round with winter emphasis; Pk mainly April–October).
  - Model validation supports their use to complement field surveillance, aiding data-driven decisions on resource allocation and intervention timing.

- Data, transparency, and reproducibility considerations
  - The modelling relies on publicly available climate data (Met Office) and is implemented in R; outputs are suitable for integration with other risk factors.
  - Data gaps and resolution differences exist (4 km input grid vs 5.5 grid for overlays); results are presented as relative suitability rather than absolute risk.
  - The approach emphasizes clear documentation, data provenance, and the potential for ongoing updates as new epidemiological data become available.