# Methods

- Study context and design
  - Hydrological and meteorological data were collected on three 50 x 50 m plots near Andasibe village in the Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
  - The three plots represent different land covers: semi-mature forest (SMF), reforested tree fallow (also called young secondary forest, YSF), and degraded grassland (DL).
  - Data cover a range of water-cycle components including rainfall, throughfall, stemflow, sapflow, soil moisture, micrometeorology, runoff/overlandflow, and soil heat flux.
  - Data were collected to support monitoring, evaluation of policies, and informing future decisions regarding environmental health and ecosystem processes.

- Data files and structure
  - Data are organized by data type and site, with raw and processed versions where applicable.
  - File naming conventions indicate site and data type:
    - Forest_* correspond to the SMF plot.
    - ReforestedTF_* correspond to the YSF (reforested tree fallow) plot.
    - Degradedland_* correspond to the DL plot.
  - All datasets follow a consistent date-time format (Date and Time: DD/MM/YYYY hh:mm) and indicate missing data with "NA".
  - Processing steps are described for converting raw measurements to processed data, including explicit equations, software (e.g., Matlab), and slope/area corrections where relevant.
  - Several datasets include MATLAB code for replicating processing steps (e.g., sap flux, rainfall aggregation).

- Key data collection methods and processing approaches (high-level)
  - Rainfall
    - Event-based tipping bucket gauges; raw data at fine temporal resolution; processed into 5-minute rainfall data.
    - Example: Forest_Rainfall_raw.csv (0.20 mm per tip); Forest_Rainfall_processed.csv contains 5-minute rainfall.
  - Micrometeorology
    - Air temperature, relative humidity, and windspeed measured on tall masts; spacing and instrumentation described; data at 10-minute intervals (Forest_micrometeorology.csv and ReforestedTF_micrometeorology.csv).
  - Throughfall
    - Automatic via three gutters per plot and manual via 66 funnel gauges (5 L collectors) arranged systematically.
    - Data include gutter throughfall or funnel-based throughfall (in mm), with daily readings for manual measurements.
  - Stemflow
    - Measured on multiple trees using spiral collars feeding into 20 L collectors; daily measurements; plot-level stemflow derived by scaling by species counts and dividing by plot area (Forest_Stemflow_raw.csv and Forest_Stemflow_processed.csv).
  - Sapflow
    - Thermal Dissipation Probes (Granier method) used to estimate sap flux density; measurements across multiple trees with species metadata; 5-minute sap flux density (Js) and sapflow (Qt) calculated; MATLAB code provided for Forest_Sapflow_raw.csv and ReforestedTF_Sapflow_raw.csv, with corresponding processed files.
  - Soil moisture
    - Time-lagged TDR sensors at depths of 5, 15, 40, 75, 110, and 160 cm; data at 30-minute and 5-minute intervals; raw and processed versions; conversion using manufacturer equation (Forest_Soilmoisture_raw.csv and Forest_Soilmoisture_processed.csv; similarly for Degradedland and ReforestedTF versions).
  - Overland flow / Runoff
    - Runoff measured on bounded plots using gutters and 200 L collectors; daily readings; corrected for direct rainfall input and converted to runoff in mm; plot-area normalization (Forest_Overlandflow.csv and Degradedland_Overlandflow.csv).
  - Soil heat flux
    - Measured at multiple depths (5, 15, 40, 75 cm) with HFP01 sensors; data collected every 30 s and summarized to 5-minute averages (Degradedland_Soil_Heat_flux.csv).

- Data quality, metadata and governance considerations (relevant to monitoring framework authors)
  - Data are accompanied by explicit metadata within each file (methods, unit definitions, column headers, missing data conventions).
  - Data processing steps (including scale-up to plot level, area corrections, and depth-to-volume conversions) are documented, with explicit equations and sometimes site-specific parameters (e.g., slope corrections, gutter areas, orifice areas, plot areas).
  - Some data require sharing of underlying datasets to ensure transparency and reproducibility, which can pose barriers if metadata or provenance are incomplete or if datasets are siloed.
  - The documentation demonstrates attention to data governance through clear data-handling rules (e.g., missing data indicators, transformation procedures, and the public sharing of used data where applicable).