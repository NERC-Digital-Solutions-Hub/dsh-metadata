# Supporting documentation - Ozone effects in high sugar grass pasture

## Overview
- Experimental study of ozone effects on high-sugar pasture comprising Lolium perenne (AberMagic) and Trifolium repens (Crusader) using mesocosms and solardomes near Bangor, North Wales, UK.
- Ozone exposure based on episodic profiles from a rural monitoring site, with a 16-week treatment period and regular biomass and physiological measurements.
- Aims to quantify how ozone influences biomass, nitrogen fixation, injury, forage quality, and canopy gas exchange, with data suitable for integration into spatial analyses and GIS-driven visualization.

## Experimental design and setting
- Species and sourcing: AberMagic perennial ryegrass; Crusader white clover; seeds sourced commercially.
- Setup: 24 pots per solardome, equal distribution of clover and grass, soil inoculated with a grassland soil slurry.
- Environment: 6 hemispherical solardomes (3 m diameter, 2.1 m high); randomised ozone treatments within domes; ambient conditions monitored (temperature, soil moisture, PAR, humidity).
- Timeline: 4-week establishment, then 16 weeks of ozone exposure (11/06/2013–01/10/2013).
- Sampling cadence: above-ground biomass assessed every 4 weeks; root biomass and nodules assessed at 16 weeks; injury scored prior to harvests.

## Measurements and datasets
- Acetylene Reduction Assay (ARA): nitrogenase activity measured every 4 weeks to estimate N-fixation; involves a 10% acetylene atmosphere and ethylene quantification.
- Biomass and quality: shoot and root biomass for both cultivars; injury assessment on clover; nutritive quality via near-infrared reflectance (NIR); relative feed value (RFV) and consumable forage value (CFV) calculations.
- Canopy gas exchange: whole-canopy measurements for net primary production (NPP), gross primary production (GPP), canopy respiration (Rtot), and dark canopy respiration; ozone flux estimated using the DO3SE model; stomatal flux thresholds applied (POD 6 for AberMagic; POD 1 for Crusader).
- Leaf-area and phenology: leaf area index (LAI) inferred from biomass; phenology function fixed due to frequent cuts.
- Data processing and analysis: values normalized to zero POD; regressions against accumulated POD values; ANOVA for canopy gas exchange; Tukey tests for treatment differences; all analyses performed in R (v3.1.1).

## Datasets and file structure
Data files (CSV) include:
- Acetylene reduction assays (4, 8, 12, 16 weeks): acetylene_reduction_assay4week.csv, acetylene_reduction_assay8week.csv, acetylene_reduction_assay12week.csv, acetylene_reduction_assay16week.csv
  - Columns include pot, size, harvest.level, ozone, time period, vial, time, ethylene area, and related metrics.
- Shoot biomass (week 4, 8, 12, 16): week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv
  - 27 columns covering pot, size, harvest.level, dome, mean.ozone, and masses for grass/clover (with and without bags), clover:grass ratios, total biomass, and related metrics.
- Root biomass (week 4, 8, 12, 16): week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv
  - 21 columns including root and nodule metrics, clover/grass masses, nodules, and related ratios.
- Injury data (week 4, 8, 12, 16): week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv
  - 8 columns detailing injury counts and percentages for T. repens.
- All measurements: allmeasurements.csv
  - 12 columns capturing date, time, pot, size, dome, mean.ozone, and key gs/abiotic variables.
- Gaseous-atmosphere and climate context: AOT40_and_climate_variables.csv
  - 32 columns including date, time, weekday, week, dome-specific >40ppb indicators, PAR, air temp, VPD, PAR>200, and related climate metrics.
- Spatial/experimental structure: dataset contains eight domes (Dome 1–8) with ozone >40 ppb markers per dome and calibration domes; FALSE indicators denote ozone concentrations <40 ppb.

Note: The AOT40 dataset links ozone exposure (above 40 ppb) to dome and cabinet measurements, enabling integration of exposure metrics with plant response data.

## GIS-ready opportunities and usage
- Spatial mapping of ozone exposure and plant responses:
  - Map mean ozone exposure by dome, and relate to biomass, injury, and N-fixation metrics at the pot level.
  - Visualize above- vs below-4 cm canopy biomass (shoot and root) and clover-grass composition across domes.
- Temporal GIS analyses:
  - Time-series mapping by 4-week intervals (weeks 4, 8, 12, 16) to track treatment effects on NPP, GPP, Rtot, and biomass changes.
- Environmental overlays:
  - Integrate AOT40 and climate variables (PAR, air temp, VPD) with biological responses to assess exposure-response patterns spatially and temporally.
- Data integration and provenance:
  - Join by pot, dome, and week to create GIS layers representing treatment, dome location, and sample dates.
- Potential map products:
  - Ozone exposure maps by dome with overlaid biomass or injury rasters.
  - Canopy productivity maps under different POD thresholds.
  - Clover-to-grass canopy composition maps across the experimental space.

## Data considerations for GIS use
- Spatial units: domes and pots provide a hierarchical spatial framework; ensure proper georeferencing when integrating with GIS (e.g., dome centroids, pot positions).
- Temporal alignment: harmonize weekly 4-week harvest data with hourly/daily AOT40 and climate records for accurate exposure-response modelling.
- Replication and design notes: ozone treatments were not replicated within solardomes, and parameterizations for ozone flux used cultivar-specific or default values; account for this in spatial analyses and uncertainty assessments.
- Data normalization: several response variables are expressed relative to POD values or as ratios; maintain clear metadata on normalization when creating maps or models.
- Data formats: all primary data are in CSV with well-defined column headers; ensure consistent linking keys (pot, dome, week) when joining datasets for GIS products.