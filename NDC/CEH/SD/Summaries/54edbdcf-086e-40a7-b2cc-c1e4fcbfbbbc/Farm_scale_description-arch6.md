# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview
- Study site: Easter Bush Farm Estate, Midlothian, UK; collaboration between SRUC and University of Edinburgh.
- Timeframe: Measurements from autumn 2012 to summer 2013; four seasonal measurement periods.
- Data collected: 500+ N2O flux measurements and 457 concurrent soil measurements across 20 fields with varied management (arable fodder crops and grazing pastures).
- Purpose: quantify soil N2O fluxes using a high-precision dynamic chamber system and characterize associated soil properties to enable data exploration, analysis, and product creation.

## Data collection design and methods
- N2O flux measurements
  - Instrumentation: dynamic closed chamber system with a pump (SH-110) and a mobile quantum cascade laser (QCL) gas analyser inside a vehicle.
  - Chamber: circular, 39 cm diameter, 7 L chamber volume placed on stainless steel collars inserted 5 cm into soil.
  - Sampling: 3-minute measurement period with air circulated over 30 m radius from the vehicle.
  - Calculation: fluxes estimated by regression of gas concentration over time (dc/dt) using the HMR package for R; 95% confidence intervals derived from the regression, air density, and chamber volume.
  - Quality checks: CO2 response used to detect leaks; data with unstable signals discarded.
  - Data handling: outliers kept due to log-normal distribution; see related analyses in Cowan et al. (2017).
- Field and sampling context
  - 20 fields selected to represent management diversity and accessibility for flux measurements.
  - Fields used for arable fodder or grazing livestock.

- Soil measurements
  - Depth and timing: soil samples (5 cm) collected within flux measurement collars immediately after flux measurement.
  - Storage and analysis: samples frozen at -18°C, later analyzed for pH (in H2O) and inorganic nitrogen.
  - Soil chemistry and properties:
    - pH (soil solution)
    - NH4+ and NO3- via KCl extraction
    - Total carbon (Tot_C) and total nitrogen (Tot_N) via grinding and analysis
  - Physical properties:
    - Bulk density (BD_density) via cutting ring method; used to compute moisture content and soil porosity
    - Water-filled pore space (WFPS) and volumetric water content (BD_VWC)
    - Porosity (BD_Porosity)
  - Procedure notes: samples kept refrigerated until analysis; standard extraction and measurement protocols cited (Rowell, 1994).

## Data structure and dataset details
- File name: Farm_Flux_and_Soil
- Key fields (21 columns):
  - Date (dd/mm/yyyy)
  - Period (season and year)
  - Measurement_ID
  - Field
  - Plot type
  - Plot Description
  - GPS_E (BNG easting)
  - GPS_N (BNG northing)
  - Soil_T (°C)
  - SMAv (WFPS, %)
  - BD_density (g cm-3)
  - BD_Porosity (ratio)
  - BD_VWC (ratio)
  - BD_WFPS (WFPS %, calculated)
  - pH
  - NH4N (g NH4-N kg-1)
  - NO3N (g NO3-N kg-1)
  - Tot_C (g C kg-1)
  - Tot_N (g N kg-1)
  - Flux (µg N2O-N m-2 h-1)
  - Flux_Error (µg N2O-N m-2 h-1; 95% CI)
- Units and formats:
  - Date format: day/month/year
  - Temperature: °C
  - Flux values: N2O-N flux in µg N2O-N m-2 h-1
  - Concentration/water metrics: percentages or ratios as indicated

## Data processing, quality control, and uncertainty
- Flux calculation and modeling
  - Use of HMR package in R to compare multiple flux estimation methods and select the best fit per chamber set.
  - Regression-based flux estimates with integrated uncertainty (95% CI) accounting for gas concentration trend, air density, and chamber volume.
- Data quality
  - Visual inspection of regression fits to confirm CO2 response; data flagged if chamber leaks detected.
  - Outliers retained due to log-normal data characteristics; prior work discusses the distribution and justification (Cowan et al., 2017).
- Documentation and provenance
  - Data and methods align with cited methodological papers (Cowan et al. 2014, 2015, 2017; Levy et al. 2011; Pedersen et al. 2010; Rowell 1994).

## Potential data products and reuse
- Datasets enabling:
  - Spatial analysis and hotspot detection of N2O fluxes across fields with varying management.
  - Correlation studies between N2O fluxes and soil properties (pH, NH4+, NO3-, Tot_C, Tot_N, WFPS, bulk density, porosity).
  - Temporal analysis across seasonal measurement periods to identify seasonal flux patterns.
- End-user tools:
  - Self-serve dashboards or pivot-table style reports linking fluxes to soil and site metadata.
  - Prototyped outputs for broader data-sharing and re-use, with opportunities for data augmentation and re-analysis.

## References (key sources)
- Cowan, N.J. et al. (2014, 2015, 2017) on dynamic chamber measurements and spatial variability of N2O fluxes.
- Levy, P.E. et al. (2011) on quantifying uncertainty in trace gas fluxes with static chambers.
- Pedersen, A.R. et al. (2010) on comprehensive flux estimation approaches.
- Rowell, D.L. (1994) on soil science methods.