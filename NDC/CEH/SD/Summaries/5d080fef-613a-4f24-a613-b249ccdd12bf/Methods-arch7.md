# Methods

- Hydrological and meteorological data were collected for three plots (each 50 x 50 m) near Andasibe village, Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
- Three plots represent land-use/forest stages:
  - SMF: semi-mature forest
  - YSF: reforested tree fallow (also called young secondary forest)
  - DL: degraded grassland
- Data are organized into multiple CSV files with naming conventions that reflect the plot type (Forest for SMF, ReforestedTF for YSF, Degradedland for DL) and measurement type (Rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, runoff/overlandflow, soil heat flux).

- Data types and main measurements
  - Rainfall
    - Forest_Rainfall_raw.csv: Event-based rainfall from tipping bucket gauge; date/time in DD/MM/YYYY hh:mm; rainfall in mm; NA for missing data.
    - Forest_Rainfall_processed.csv: Converted to 5-minute rainfall data using a Matlab script; columns include Date and Time and Rainfall (mm) for 5-minute intervals; NA for missing data.
  - Micrometeorology
    - Forest_micrometeorology.csv: Air temperature (°C), relative humidity (%), wind speed (m/s) measured at 10-minute intervals from a 10 m mast; date/time in DD/MM/YYYY hh:mm; NA for missing data.
  - Throughfall
    - Forest_Throughfall_automatic.csv: Three V-shaped gutters across the plot (50 m x 50 m); throughfall per gutter (mm) with date/time; corrected to water depth (mm) via gutter area; NA for missing data.
    - Forest_Throughfall_manual.csv: Manual sampling with 66 funnel gauges at 5 m x 10 m subplots; date, water amount (ml), and throughfall depth (mm); NA for missing data.
  - Stemflow
    - Forest_Stemflow_raw.csv: Stemflow measured on ten trees with spiral collars; daily readings; date/time and stemflow (ml); tree-species, DBH, height provided in the raw description; NA for missing data.
    - Forest_Stemflow_processed.csv: Plot-scale stemflow derived by scaling per-tree volumes by species counts and dividing by corrected plot area; Date and Time and SF (mm); NA for missing data.
  - Sapflow
    - Forest_Sapflow_raw.csv: Thermal Dissipation Probes (TDP) sap flow temperature differences A1…G3 per monitored tree; date/time; NA for missing data.
    - Forest_Sapflow_processed.csv: Sapflux density (Js, cm3 cm-2 h-1) and sapflow (cm3 h-1) per monitored tree; Matlab code provided to compute Js; NA for missing data.
  - Soil moisture
    - Forest_Soilmoisture_raw.csv: Soil moisture at depths 5, 15, 40, 75, 110, and 160 cm; 30-min and 5-min recording periods; date/time; NA for missing data.
    - Forest_Soilmoisture_processed.csv: Actual soil moisture calculated from raw using manufacturer equation (0.4667 + 0.0283 * raw); date/time and depth columns; NA for missing data.
  - Runoff/Overlandflow
    - Forest_Overlandflow.csv: Runoff measured for two bounded runoff plots (3 x 10 m); runoff in mm after corrections; includes date, heights, volumes, corrected volumes, and effective rainfall; plot areas and correction factors documented; NA for missing data.
    - Degradedland_Overlandflow.csv: Similar runoff measurements for three bounded plots with corrections and plot-area normalization; includes slope, drum calibration, areas, and corrected runoff; NA for missing data.
  - Rainfall and micrometeorology for degraded land
    - Degradedland_Rainfall_raw.csv and Degradedland_Rainfall_processed.csv: Event-based to 5-minute rainfall conversion; date/time and rainfall (mm); NA for missing data.
    - Degradedland_micrometeorology.csv: Weather measurements at 3 m height (T, RH, wind speed, wind direction) plus radiation components; date/time; NA for missing data.
  - Degraded land soil moisture
    - Degradedland_Soilmoisture_raw.csv and Degradedland_Soilmoisture_processed.csv: 5 cm, 15 cm, 40 cm, 75 cm soil depths; conversion to actual moisture using manufacturer equation; date/time; NA for missing data.
  - Degraded land soil heat flux
    - Degradedland_Soil_Heat_flux.csv: Soil heat flux at 5, 15, 40, 75 cm; measurements at 30 s intervals with 5-minute averages; date/time; NA for missing data.

- Data structure and formats
  - Date formats: DD/MM/YYYY hh:mm across all datasets.
  - Units:
    - Rainfall: millimeters (mm); rainfall data often aggregated to 5-minute intervals.
    - Micrometeorology: temperature in °C, RH in %, wind speed in m/s, wind direction in degrees, radiation in W/m².
    - Throughfall/Stemflow/Sapflow: depth/volume in mm or cm³; sap flux density in cm³ cm⁻² h⁻¹; sapflow in cm³ h⁻¹.
    - Soil moisture: volumetric moisture in percent (actual %).
    - Runoff/Overlandflow: runoff in mm; corrected for direct rainfall; effective rainfall provided.
  - Spatial context: measurements collected within three 50 x 50 m plots representing SMF, YSF, and DL; data structured to support plot-level and tree-level aggregation for GIS analyses.

- Data processing and notes
  - Matlab scripts are provided for converting raw rainfall to 5-minute data (Forest_Rainfall_processed.csv and ReforestedTF_Rainfall_processed.csv, Degradedland_Rainfall_processed.csv) using date alignment and summation over intervals.
  - Sapflow processing uses Granier (1985) methodology to derive sap flux density from temperature differences; output includes per-tree Js and resulting sapflow; dedicated Matlab scripts are included for ReforestedTF_Sapflow_raw.csv and Forest_Sapflow_raw.csv.
  - Soil moisture datasets are derived from raw readings using manufacturer-specific transformation equations (0.4667 + 0.0283 * raw).
  - Stemflow and runoff data are scaled from per-tree or per-gutter measurements to plot-level fluxes by applying species counts, plot areas, and slope corrections where specified.

- Data quality and accessibility
  - Missing data are indicated with NA across all files.
  - The datasets combine automated measurements and manual measurements (throughfall gauges, funnel gauges) to provide cross-validation opportunities.
  - The data cover multiple temporal resolutions (5-minute to 30-minute intervals) and multiple depths/locations within the plots, enabling detailed GIS-based temporal-spatial analyses.

- GIS-relevant guidance
  - Use plot-level aggregates (per 50 x 50 m plots) to map spatial variation in hydrological fluxes across land-use types (SMF, YSF, DL).
  - Integrate time-series data (rainfall, rainfall-derived runoff, soil moisture, sapflow, stemflow, throughfall) with ancillary GIS layers (elevation, slope, aspect, vegetation type) to model hydrological processes.
  - Leverage the dataset’s multiple measurement modalities (automatic vs. manual throughfall, sapflow vs. sapwood area, soil moisture at multiple depths) for cross-validation and to derive water balance components in mapped space and time.
  - The naming conventions and documented processing steps facilitate programmatic data ingestion for GIS workflows and reproducible analysis.