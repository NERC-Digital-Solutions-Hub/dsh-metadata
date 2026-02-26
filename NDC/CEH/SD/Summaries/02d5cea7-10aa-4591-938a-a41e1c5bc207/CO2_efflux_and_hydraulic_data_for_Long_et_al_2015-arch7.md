# CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13

## Overview
- Dataset of CO2 efflux and hydraulic parameters from six field sites (two in Scotland: River Kelvin, Drumtee Water; four in the Amazon: Main Trail, New Colpita, La Torre river, Tambopata river).
- Sites span different locations, catchment sizes, land use, and seasons, with measurements taken across multiple years to capture varying flow conditions.
- Data suitable for GIS-based visualization and spatial analysis of CO2 flux in fluvial systems.

## Site characteristics
- Scotland
  - River Kelvin (RK): 335 km2 catchment, semi-urban 23%, agriculture 70%, max elevation 510 m, coordinates 55°52'06"N 4°17'16"W. Sampling within a 30 m reach, near Clyde Estuary; bankfull width 15–20 m; bed with large pebbles and bedrock patches.
  - Drumtee Water (DW): 9.6 km2 peat-dominated catchment, rough grazing, max elevation 260 m, coordinates 55°41'16"N 4°23'37"W. Sampling in a 19 m reach; channel 4–5 m wide.
- Amazon
  - Main Trail (MT): ~5 km2 catchment; active during rainy season; channel 4–7 m wide at sampling point.
  - New Colpita (NC): ~7 km2 catchment; perennial small stream; channel 4–7 m wide.
  - La Torre river (LT): ~2000 km2 catchment; sampling near confluence with Tambopata; channel 40–80 m wide.
  - Tambopata river (TP): ~14,000 km2 catchment; sampling point ~200 m wide; rainforest-dominated with small-scale agriculture and gold mining nearby.

## Sampling regime and data coverage
- Periodicity
  - RK and DW: weekly to every three weeks, June 2012–December 2013 (covering all four seasons and a wide range of flow conditions).
  - MT, NC, LT, TP: field campaigns Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012 (wet and dry seasons).
- Sample counts (per site, representative parameters)
  - RK: CO2 efflux 83; Flow 87; Water depth 87; pCO2 58; [DIC] 58; pH 87; Water temp 86.
  - DW: CO2 efflux 79; Flow 75; Water depth 77; pCO2 57; [DIC] 57; pH 79; Water temp 79.
  - MT: CO2 efflux 42; Flow 41; Water depth 42; pCO2 42; [DIC] 42; pH 42; Water temp 42.
  - NC: CO2 efflux 46; Flow 46; Water depth 45; pCO2 46; [DIC] 37; pH 46; Water temp 46.
  - LT: CO2 efflux 37; Flow 37; Water depth 34; pCO2 36; [DIC] 36; pH 37; Water temp 37.
  - TP: CO2 efflux 26; Flow 26; Water depth 26; pCO2 26; [DIC] 26; pH 26; Water temp 26.

## CO2 flux measurement
- Method: floating chamber (volume 0.0029 m3) with LICOR LI-840A CO2/H2O analyzer; closed-loop circulation with Schego pump (0.3–1.0 L/min); CO2 accumulation measured over four minutes, three repeats.
- Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)), where δCO2/δt is the slope (μatm s−1), V is chamber volume, T is air temperature (K), S is chamber surface area; R is the gas constant.
- Auxiliary observations: qualitative water surface state recorded at UK sites (smooth, medium, rough); wind speed not directly measured.

## Hydraulic parameters
- In UK rivers (RK, DW): depth-averaged velocity measured with Valeport flow meter at 60 s averaging, at 20% and 80% of depth, plus at least three additional heights to identify outliers.
- Parameters derived: mean velocity (ū, m s−1), Froude number (Fr = ū / sqrt(gH)), Reynolds number (Re = ūH/ν).
- Note: For the Amazon sites, information to calculate Re and Fr was not available.

## Water chemistry and related variables
- pH, conductivity, and temperature
  - DW: continuous pH logging at 30 min resolution using In-Situ Troll Troll 9000; other sites used Troll 9500 or spot measurements.
  - RK: pH measured directly but later deemed unreliable; pH estimated from a discharge–pH relationship using upstream monitoring data (no significant tributaries between sites).
  - MT, NC: pH, conductivity, temperature logged at 15 min resolution (Troll 9500).
  - LT, TP: spot measurements at flux deployment (pH, conductivity, temperature) with Troll 9500; deployed >20 minutes to equilibrate.
- Dissolved inorganic carbon
  - [DIC] measured from water samples collected within 15 minutes of flux measurement; triplicate samples preserved and analyzed within 6 months using GasBench/Delta V Plus.
  - pCO2 calculated from [DIC], pH, and temperature.
- Troll calibration
  - Troll 9000: calibration roughly every 5 weeks (pH4 and pH7), field cleaning after calibration.
  - Troll 9500: calibration roughly monthly (pH4 and pH7), field cleaning weekly; electrolyte top-up if needed.

## Data structure and quality control
- Data file: 11-column dataset in an Excel/CSV file titled CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13.
- Columns included: Date, Region, Site, Mean CO2 efflux, SD of mean CO2 efflux, Flow, Water depth, pCO2, [DIC], pH, Water temperature.
- Missing data: indicated as NA; gaps due to equipment failure, high flows preventing access, or seasonal drying (e.g., MT dried during dry season).
- Quality notes: DIC and pCO2 data availability varies by site and period; RK pH represented by discharge-based estimate due to instrument failure; traceability and calibration steps detailed in methods.

## Practical implications for GIS and data use
- Spatial coverage across Scotland and the Amazon enables comparative mapping of CO2 efflux against catchment characteristics, flow conditions, and water chemistry.
- Data can be joined with geospatial layers (site coordinates, region, catchment attributes) to create map-based visuals of CO2 flux, hydraulic regime, and chemical drivers.
- The dataset provides a transparent metadata trail: measurement methods, instrumentation, calibration, sampling cadence, and data quality notes essential for GIS data provenance and reproducibility.