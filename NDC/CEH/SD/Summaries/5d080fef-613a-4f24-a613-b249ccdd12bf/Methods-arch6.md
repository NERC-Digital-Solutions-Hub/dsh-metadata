# Methods

- Hydrological and meteorological data were collected for three 50 x 50 m plots near Andasibe village in the Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
- Plot classifications:
  - SMF: semi-mature forest
  - ReforestedTF (YSF): reforested tree fallow or young secondary forest
  - Degradedland: degraded grassland
- Data organization:
  - File names indicate data type and plot:
    - Forest*: SMF data
    - ReforestedTF*: YSF data
    - Degradedland*: grassland data
  - Each dataset has raw and processed versions (e.g., Forest_Rainfall_raw.csv, Forest_Rainfall_processed.csv).
- Timeframe:
  - Processing scripts indicate data coverage around 2014–2015 (e.g., rainfall from 2014-10-01 to 2015-10-01 in MATLAB examples).

- Data types and measurement methods (summary by category):

  - Rainfall
    - Raw: tipping bucket rain gauges with event logging (Forest_Rainfall_raw.csv; ReforestedTF_Rainfall_raw.csv; Degradedland_Rainfall_raw.csv)
    - Processed: 5-minute rainfall data produced from raw using MATLAB scripts
    - Headers: Date and Time (DD/MM/YYYY hh:mm), Rainfall (mm), Missing Data (NA)

  - Micrometeorology
    - Forest (SMF): air temperature, relative humidity, windspeed measured on a 10 m mast at 10-minute intervals (Forest_micrometeorology.csv)
    - Degradedland: similar measurements at 5-minute intervals on a 3 m mast (Degradedland_micrometeorology.csv)
    - Headers: Date and Time, Air Temperature (°C), Relative Humidity (%), Windspeed (m/s); Missing Data (NA)

  - Throughfall
    - Automatic: three V-shaped gutters with tipping buckets per plot; data recorded as mm of throughfall per gutter (Forest_Throughfall_automatic.csv; ReforestedTF_Throughfall_automatic.csv)
    - Manual: 66 funnel gauges placed on subplots; measurements read daily; throughfall converted to mm (Forest_Throughfall_manual.csv; ReforestedTF_Throughfall_manual.csv)
    - Headers: Date and Time, Gutter-1/2/3 or Throughfall (mm), Missing Data (NA)

  - Stemflow
    - Forest and ReforestedTF: stemflow measured on a number of trees using spiral collars connected to 20 L collectors; daily measurements (Forest_Stemflow_raw.csv; ReforestedTF_Stemflow_raw.csv)
    - Processed: plot-scale stemflow by scaling per-tree volumes by tree counts and dividing by plot area (Forest_Stemflow_processed.csv; ReforestedTF_Stemflow_processed.csv)
    - Headers: Date (DD/MM/YYYY hh:mm), Stemflow (ml) per tree; Species, DBH, Height information included in raw; Missing Data (NA)

  - Sapflow
    - Forest and ReforestedTF: Thermal Dissipation Probes (TDP) used to estimate sap flux density (Js) and sapflow; temperature difference measured every 30 s, 5-minute averages saved (Forest_Sapflow_raw.csv; ReforestedTF_Sapflow_raw.csv)
    - Processed: Js calculated via Granier et al. method; Qt calculated from Js and sapwood area; outputs per monitored tree (Forest_Sapflow_processed.csv; ReforestedTF_Sapflow_processed.csv)
    - Included MATLAB scripts to perform the calculations (script details provided in the files)
    - Headers: Date and Time, A1…G3 (Sapflux Density and Sapflow for each tree); Missing Data (NA)

  - Soil Moisture
    - Raw: measured at multiple depths (5, 15, 40, 75, 110, 160 cm) using TDR sensors; intervals include 30-min and 5-min periods depending on dataset (Forest_Soilmoisture_raw.csv; ReforestedTF_Soilmoisture_raw.csv; Degradedland_Soilmoisture_raw.csv)
    - Processed: actual soil moisture values using manufacturer equation (0.4667 + 0.0283 * raw); depth-specific columns (5 cm, 15 cm, 40 cm, 75 cm, 110 cm, 160 cm)
    - Headers: Date and Time, 5 cm, 15 cm, 40 cm, 75 cm, 110 cm, 160 cm; Missing Data (NA)

  - Runoff / Overlandflow
    - Overland runoff measured on bounded plots using gutters and 200 L collectors; daily measurements with corrections for direct rainfall; runoff expressed in mm (Forest_Overlandflow.csv; Degradedland_Overlandflow.csv)
    - Includes plot-specific slope, drum calibration, gutter area, correction areas, and plot area in metadata
    - Headers: Date, Height (cm), Volume (L), Corrected Volume (L), Runoff (mm), Effective rainfall (mm), Average runoff (mm); Missing Data (NA)

  - Soil Heat Flux
    - Measured at 5, 15, 40, 75 cm using HFP01 sensors; data every 30 s with 5-minute averages (Forest_Soil_Heat_Flux.csv; Degradedland_Soil_Heat_flux.csv)
    - Headers: Date and Time, 5 cm, 15 cm, 40 cm, 75 cm; Missing Data (NA)

- Data quality and metadata conventions:
  - Missing data are consistently indicated as "NA" across all files.
  - Date formats are standardized as DD/MM/YYYY hh:mm.
  - Column headers clearly label measurement type, depth (for soil moisture), or tree/plot identifiers (e.g., A1…G3 for sapflow; Gutter-1…3 for throughfall).
  - Plot-level data products are created by scaling per-tree or per-gauge measurements to the corresponding plot area (with slope corrections where applicable).

- Data processing and usage notes:
  - Rainfall processing is performed with MATLAB scripts to aggregate raw event data into 5-minute intervals.
  - Sap flux calculations follow the Granier method, with explicit scripts provided to compute Js and Qt.
  - Soil moisture uses a manufacturer-provided calibration equation to convert raw to actual volumetric moisture.
  - Throughfall data include both automatic gutter measurements and systematic manual gauging, enabling cross-validation.
  - Overlandflow and runoff data incorporate corrections for direct rainfall and area-based normalization.
  - Metadata and tables include device specifics, calibration details, plot areas, slopes, and gauge/drum dimensions to support reproducibility and re-use.

- Practical implications for data support work:
  - The dataset enables cross-plot hydro-ecological analyses across forest, regrowth, and degraded landscapes.
  - Rich time-series coverage across rainfall, micrometeorology, soil moisture, transpiration-related fluxes (sapflow), and water fluxes (throughfall, stemflow, runoff) supports integrated hydrological modeling and ecosystem water-use studies.
  - The presence of both raw and processed files, plus processing scripts, facilitates quality assurance, reprocessing with updated parameters, and creation of consistent data products for end users.