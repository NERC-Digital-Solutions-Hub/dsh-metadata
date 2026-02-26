# Methods

- Overview
  - Hydrological and meteorological data collected from three 50 x 50 m plots near Andasibe village in the Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
  - Plots represent different land covers: semi-mature forest (SMF), reforested tree fallow (also called young secondary forest, YSF), and degraded grassland (DL/Degradedland).
  - Data are organized into multiple CSV files (raw and processed) with naming conventions by plot type: Forest*, ReforestedTF*, and Degradedland*.

- Study sites and plot descriptors
  - SMF: semi-mature forest plot
  - ReforestedTF: reforested/tree-fallow plot (YSF)
  - Degradedland: degraded grassland plot
  - Data cover rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, runoff/overlandflow, and soil heat flux.

- Data files and structure (examples)
  - Rainfall
    - Forest_Rainfall_raw.csv: event-based rainfall measurements from a tipping bucket gauge; columns: Date and Time, Rainfall (mm), with NA indicating missing data.
    - Forest_Rainfall_processed.csv: 5-minute rainfall data generated from raw data using MATLAB code.
    - ReforestedTF_Rainfall_raw.csv and Degradedland_Rainfall_raw.csv: similar event-based rainfall data for other plots; corresponding processed files convert to 5-minute resolutions.
  - Micrometeorology
    - Forest_micrometeorology.csv and ReforestedTF_micrometeorology.csv: air temperature, relative humidity, and windspeed measured at 10-minute intervals (masts in nearby clearing); NA used for missing data.
    - Degradedland_micrometeorology.csv: weather conditions measured at 5-minute intervals (Vaisala WXT520 transmitter, additional radiation measurements).
  - Throughfall
    - Forest_Throughfall_automatic.csv: three gutter-based throughfall gauges per plot (diagonal across 50 x 50 m), with 50 mL tipping buckets; data in mm; NA for missing.
    - Forest_Throughfall_manual.csv: manual throughfall using 66 funnel gauges (5 L collectors) read daily; throughfall converted to depth (mm) via orifice area; NA for missing.
    - ReforestedTF_Throughfall_automatic.csv and ReforestedTF_Throughfall_manual.csv: same structure for the reforested plot.
  - Stemflow
    - Forest_Stemflow_raw.csv and ReforestedTF_Stemflow_raw.csv: stemflow measured on 10 or 5 trees respectively using spiral collars; daily readings; NA for missing.
    - Forest_Stemflow_processed.csv and ReforestedTF_Stemflow_processed.csv: plot-scale stemflow calculated by scaling per-tree volumes by species counts and dividing by adjusted plot area.
  - Sapflow
    - Forest_Sapflow_raw.csv and ReforestedTF_Sapflow_raw.csv: Thermal Dissipation Probe (Granier) data; 5-minute averages; tree metadata includes species, DBH, sapwood area, basal area; NA where data missing.
    - Forest_Sapflow_processed.csv and ReforestedTF_Sapflow_processed.csv: sap flux density (Js) and sapflow (Qt) computed; includes 5-minute results; MATLAB code provided for calculation.
  - Soil moisture
    - Forest_Soilmoisture_raw.csv and ReforestedTF_Soilmoisture_raw.csv and Degradedland_Soilmoisture_raw.csv: measurements at multiple depths (e.g., 5, 15, 40, 75, 110, 160 cm) with 30-minute and 5-minute intervals; NA for missing.
    - Forest_Soilmoisture_processed.csv, ReforestedTF_Soilmoisture_processed.csv, Degradedland_Soilmoisture_processed.csv: conversion to actual soil moisture using manufacturer equations (e.g., 0.4667 + 0.0283 * raw).
  - Runoff and overland flow
    - Forest_Overlandflow.csv, Degradedland_Overlandflow.csv: runoff measured with gutter/collectors, corrected for direct rainfall, converted to mm; includes plot-area corrections and slope adjustments in metadata.
    - Degradedland_Overlandflow.csv includes multiple plots with runoff data, rainfall inputs, and plot-specific geometries.
  - Soil heat flux
    - Degradedland_Soil_Heat_flux.csv: soil heat flux measured at 5, 15, 40, and 75 cm depth every 30 s with 5-minute averages; NA for missing data.

- Data processing and transformations
  - Rainfall processing
    - Raw event-based rainfall (Forest_Rainfall_raw.csv, etc.) converted to 5-minute rainfall (Forest_Rainfall_processed.csv, etc.) via MATLAB scripts that aggregate rainfall over 5-minute windows.
  - Soil moisture
    - Processed soil moisture uses manufacturer-provided equation to convert raw TDR readings to actual volumetric moisture values (e.g., 0.4667 + 0.0283 * raw).
  - Sapflow
    - Sap flux density (Js) calculated from temperature differences using Granier’s method; 5-minute averages produced; sapflow (Qt) computed as Js multiplied by sapwood area.
    - MATLAB code excerpts are provided for converting raw sapflow temperature difference data to Js and exporting to Excel.
  - Stemflow
    - Plot-level stemflow (mm per unit ground area) derived by scaling average per-tree stemflow by tree counts in the plot, then dividing by plot area corrected for slope.
  - Throughfall and runoff
    - Throughfall: automatic gutters convert water volume to depth using gutter area and inclination corrections; manual throughfall uses 5 L funnels read daily and converted to depth via orifice area.
    - Runoff: daily water levels converted to volume using calibration, corrected for direct rainfall, and normalized by projected plot area.

- Metadata, formats, and data quality
  - Date and time format: DD/MM/YYYY hh:mm across all files.
  - Missing data: indicated by NA in all datasets.
  - Slope, area, and calibration details are embedded in file headers or accompanying notes to enable proper normalization (e.g., plot areas, gutter areas, drum areas, and calibration constants).
  - Data are organized to support cross-dataset analyses (e.g., linking rainfall to soil moisture, evapotranspiration proxies from sapflow, and runoff responses).

- Analytical potential and usage
  - Enables cross-site comparisons of hydrological processes under different land covers (forest, reforested, degraded land).
  - Supports analyses of rainfall–runoff, evapotranspiration proxies (sapflow, sap flux, soil moisture dynamics), and soil–atmosphere exchanges (soil heat flux, micrometeorology).
  - Facilitates scaling from tree- or subplot-level measurements to plot- or watershed-scale estimates, with explicit area and slope corrections.
  - Provides a reproducible framework (MATLAB code snippets and detailed method descriptions) for processing and harmonizing multi-parameter hydrological data.

- Key considerations for analysts
  - Data gaps are present (NA entries); account for missing data in analyses and possibly interpolate or use models robust to gaps.
  - Local scale measurements (beds of gutters, collars, sapflow probes) require careful upscaling to plot-level metrics using the documented scaling rules.
  - Consistent units and formats are critical when merging datasets (e.g., rainfall in mm per 5 minutes vs. mm per day; sapflow in Js and Qt; soil moisture in calibrated volumetric values).
  - The three plots provide a gradient of land cover, allowing assessment of how hydrological responses differ with vegetation structure and land management.

- Accessibility and reproducibility
  - Data are accompanied by explicit processing steps (e.g., MATLAB scripts and processed CSVs) to reproduce 5-minute rainfall series and sapflow calculations.
  - File naming conventions and detailed column headers aid discoverability and reuse across studies focused on hydrology and ecosystem water fluxes.