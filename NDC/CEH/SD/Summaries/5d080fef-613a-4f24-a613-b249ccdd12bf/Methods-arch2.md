# Methods

- Overview
  - Describes data collection and data structure for hydrological and micrometeorological measurements across three plots near Andasibe village in eastern Madagascar (Corridor Ankeniheny-Zahamena, CAZ).
  - Three plot types: semi-mature forest (SMF), reforested tree fallow/YSA (YSF), and degraded grassland (DL). File names indicate the site (Forest, ReforestedTF, Degradedland) and data type (raw vs processed).
  - Aims align with standardized environmental monitoring: collect, verify, clean, transform, and present data in clear formats (CSV) for monitoring and cross-site comparisons.

- Study sites and plot setup
  - Plots are each 50 x 50 meters.
  - Data cover rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, runoff/overlandflow, and soil heat flux.

- Data files and naming conventions
  - Forest_Rainfall_raw.csv and Forest_Rainfall_processed.csv
  - Forest_micrometeorology.csv
  - Forest_Throughfall_automatic.csv and Forest_Throughfall_manual.csv
  - Forest_Stemflow_raw.csv and Forest_Stemflow_processed.csv
  - Forest_Sapflow_raw.csv and Forest_Sapflow_processed.csv
  - Forest_Soilmoisture_raw.csv and Forest_Soilmoisture_processed.csv
  - Forest_Overlandflow.csv
  - ReforestedTF_Rainfall_raw.csv and ReforestedTF_Rainfall_processed.csv
  - ReforestedTF_micrometeorology.csv
  - ReforestedTF_Throughfall_automatic.csv and ReforestedTF_Throughfall_manual.csv
  - ReforestedTF_Stemflow_raw.csv and ReforestedTF_Stemflow_processed.csv
  - ReforestedTF_Sapflow_raw.csv and ReforestedTF_Sapflow_processed.csv
  - ReforestedTF_Soilmoisture_raw.csv and ReforestedTF_Soilmoisture_processed.csv
  - ReforestedTF_Overlandflow.csv
  - Degradedland_Rainfall_raw.csv and Degradedland_Rainfall_processed.csv
  - Degradedland_micrometeorology.csv
  - Degradedland_Soilmoisture_raw.csv and Degradedland_Soilmoisture_processed.csv
  - Degradedland_Overlandflow.csv
  - Degradedland_Soil_Heat_flux.csv
  - Each dataset includes explicit column headers, units, and NA handling for missing data.

- Variables and measurement approaches (high-level)
  - Rainfall
    - Event-based tipping-bucket gauges; 0.20–0.21 mm per tip depending on site.
    - Raw data: Forest_Rainfall_raw.csv; processed to 5-minute intervals in Forest_Rainfall_processed.csv (Matlab-based aggregation).
  - Micrometeorology
    - Air temperature, relative humidity, wind speed; measured at 10-minute (Forest) or 10-minute (ReforestedTF) intervals on mast(s) near the plots.
    - Data files: Forest_micrometeorology.csv, ReforestedTF_micrometeorology.csv, and Degradedland_micrometeorology.csv.
  - Throughfall
    - Automatic gutters (three per plot) for direct measurement; manual throughfall gauges in subplots (66 gauges per plot) to ensure even spatial coverage.
    - Data files: Forest_Throughfall_automatic.csv, Forest_Throughfall_manual.csv; ReforestedTF_Throughfall_automatic.csv, ReforestedTF_Throughfall_manual.csv.
  - Stemflow
    - Measured on trees using spiral collars and 20 L collectors; separate counts per tree; daily readings.
    - Data files: Forest_Stemflow_raw.csv and Forest_Stemflow_processed.csv; ReforestedTF_Stemflow_raw.csv and ReforestedTF_Stemflow_processed.csv.
  - Sapflow
    - Thermal Dissipation Probes (Granier method) to estimate sap flux density; data per monitored tree; sapwood area and basal area provided per tree for plot-scale calculations.
    - Data files: Forest_Sapflow_raw.csv and Forest_Sapflow_processed.csv; ReforestedTF_Sapflow_raw.csv and ReforestedTF_Sapflow_processed.csv.
  - Soil moisture
    - Time-series at multiple depths (5, 15, 40, 75, 110, 160 cm, depending on site) using TDR sensors; recorded at 30-minute intervals (earlier) and 5-minute intervals (later).
    - Raw and processed data: Forest_Soilmoisture_raw.csv / Forest_Soilmoisture_processed.csv; ReforestedTF_Soilmoisture_raw.csv / ReforestedTF_Soilmoisture_processed.csv; Degradedland_Soilmoisture_raw.csv / Degradedland_Soilmoisture_processed.csv.
    - Processing uses manufacturer-provided equations to convert raw readings to actual soil moisture.
  - Overlandflow/Runoff
    - Runoff measured on bounded plots using gutter/drum systems; corrections applied for direct rainfall input; runoff reported as mm per plot and per area.
    - Data files: Forest_Overlandflow.csv; ReforestedTF_Overlandflow.csv; Degradedland_Overlandflow.csv.
  - Soil heat flux
    - Measured at 5, 15, 40 and 75 cm with HFP01 sensors; data captured every 30 seconds, 5-minute averages.
    - Data file: Degradedland_Soil_Heat_flux.csv (and related site-specific equivalents).

- Data processing and transformations (highlights)
  - Rainfall processing
    - Raw event data converted to 5-minute rainfall sums using Matlab scripts; resulting in 5-minute rainfall columns with NA for missing data.
  - Sapflow processing
    - Sap flux density calculated from temperature differences using Granier-based equations; Matlab code provided to compute Js (sap flux density) per monitored tree, then aggregated to sapflow (Q t) using sapwood area.
  - Soil moisture processing
    - Converted raw moisture readings to actual volumetric moisture using manufacturer-provided equation (e.g., 0.4667 + 0.0283 * raw).
  - Throughfall and stemflow
    - Manual throughfall volumes converted to depth using orifice area; automatic throughfall converted by gutter area; stemflow scaled to plot level using tree counts and plot area (slope-corrected as needed).
  - Overlandflow and groundwater-related metrics
    - Runoff volumes corrected for direct rainfall and normalized by plot area to yield runoff in mm; projected and corrected areas provided for each plot.
  - Data accessibility and format
    - All datasets organized with explicit column headers and units; missing data consistently marked as NA; documentation references measurement intervals and instrument types.

- Data quality, consistency, and access considerations
  - Data come from standardized yet site-specific gear and protocols, enabling cross-site comparisons while acknowledging site differences (SMF, ReforestedTF, Degradedland).
  NA values indicate instrument failure or missing measurements.
  Datasets include both raw and processed forms, along with explicit methods and Matlab scripts to reproduce processing steps.
  - The structure supports reuse and combination with other environmental data to enhance dataset value and facilitate broader analyses and policy-relevant monitoring.