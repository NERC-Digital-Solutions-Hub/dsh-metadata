# Methods

- Context and purpose
  - Hydrological and meteorological data were collected on three plots (each 50 x 50 m) near Andasibe village in Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
  - Plots cover different land covers: semi-mature forest (SMF), reforested tree fallow (also called young secondary forest, YSF), and degraded grassland. Data are organized into file prefixes Forest, ReforestedTF, and Degradedland.

- Dataset families and structure
  - Forest, ReforestedTF, and Degradedland datasets include both raw and processed data files, named to reflect site type and measurement type (e.g., Forest_Rainfall_raw.csv, ReforestedTF_Rainfall_raw.csv, Degradedland_Soilmoisture_raw.csv).
  - Each file has a corresponding processed version (e.g., Forest_Rainfall_processed.csv) with transformations described in the Methods sections.
  - For most datasets, each file contains:
    - Methods: a narrative description of the measurement setup and instruments.
    - Column Headers: clearly labeled variables (dates, depth, height, etc.).
    - Missing Data: indicated with NA.
  - Units and formats are specified within the Column Headers sections (e.g., Date and Time in DD/MM/YYYY hh:mm format; rainfall in mm; temperature in °C; wind speed in m s-1).

- Variables and measurement types
  - Rainfall
    - Forest_Rainfall_raw.csv and ReforestedTF_Rainfall_raw.csv and Degradedland_Rainfall_raw.csv use tipping-bucket gauges with data logged automatically; processed files convert raw readings to 5-minute rainfall data.
  - Micrometeorology
    - Forest_micrometeorology.csv and ReforestedTF_micrometeorology.csv describe air temperature, relative humidity, windspeed, and (where applicable) radiation, measured at 10-minute intervals.
    - Degradedland_micrometeorology.csv lists temperature, humidity, wind speed, wind direction, and incoming/outgoing short-wave radiation at 5-minute intervals.
  - Throughfall
    - Automatic: Forest_Throughfall_automatic.csv and ReforestedTF_Throughfall_automatic.csv with three gutters per plot (water depth in mm per gutter).
    - Manual: Forest_Throughfall_manual.csv and ReforestedTF_Throughfall_manual.csv use funnel gauges (66 per plot) read daily; values converted to depth (mm).
  - Stemflow
    - Forest_Stemflow_raw.csv and ReforestedTF_Stemflow_raw.csv record stemflow on a set of trees using spiral collars; processed versions scale to plot area.
  - Sapflow
    - Forest_Sapflow_raw.csv and ReforestedTF_Sapflow_raw.csv use Thermal Dissipation Probes; processed files convert to sap flux density and compute sapflow per tree.
  - Soil moisture
    - Forest_Soilmoisture_raw.csv and ReforestedTF_Soilmoisture_raw.csv (5, 15, 40, 75, 110, 160 cm depths) with 30-min and 5-min intervals; processed files apply manufacturer conversion to obtain actual soil moisture values.
  - Runoff / Overlandflow
    - Forest_Overlandflow.csv, Degradedland_Overlandflow.csv describe runoff collected from bounded plots with gutters and 200-L collectors; data include corrected runoff (mm) and effective rainfall, plus plot-area corrections.
    - Degradedland_Overlandflow.csv includes multiple plots with detailed plot and instrument calibration parameters.
  - Soil heat flux
    - Degradedland_Soil_Heat_flux.csv documents soil heat flux at 5, 15, 40, and 75 cm depths.

- Data processing and provenance
  - Rainfall processing
    - Matlab code converts raw rainfall to 5-minute intervals for several sites (Forest_Rainfall_processed.csv, ReforestedTF_Rainfall_processed.csv, Degradedland_Rainfall_processed.csv).
  - Sapflow processing
    - Matlab scripts compute sap flux density (Js) from temperature differences following Granier (1985) and derive sapflow by multiplying Js by sapwood area; produced as sapflow density per tree and aggregated to files like Forest_Sapflow_processed.csv and ReforestedTF_Sapflow_processed.csv.
  - Soil moisture processing
    - Processed values are calculated from raw sensors using manufacturer equations (e.g., 0.4667 + 0.0283 * raw).
  - Stemflow and runoff processing
    - Stemflow and runoff data are scaled to plot-level volumes using tree counts, plot areas, slope corrections, and calibrated relationships for drum or gutter systems.
  - Metadata standardization
    - Each dataset documents measurement intervals, depth/area parameters, calibration values, and plate-specific notes (e.g., slope, drum opening diameter, gutter area) to enable reproducibility and cross-site comparability.

- Measurement specifics and site details
  - Plots and environments
    - SMF (semi-mature forest) plot, ReforestedTF/YSF plot, and Degradedland (grassland) plot, each with distinct instrumentation setups and data collection intervals.
  - Instrumentation and setup
    - Rain gauges, tipping buckets, HOBO loggers; micrometeorology masts of varying heights; gutters for throughfall; spiral collars for stemflow; TDP sapflux probes; TDR soil moisture sensors; HFP/B sensors for soil heat flux.
  - Calibration and corrections
    - Runoff and stemflow data include plot-area corrections and slope gradient corrections; throughfall calculations adjust for gutter inclination; multiple instrument calibration parameters are provided in the file metadata.

- Data quality and governance considerations for Data Stewards
  - Data completeness and consistency
    - Missing data are indicated with NA across all files; several datasets rely on continuous instrumentation with potential gaps due to instrument malfunction or data loss.
  - Interoperability and formats
    - Data are stored as CSV files with explicit column headers and standard date-time formats; prefixes differentiate site types (Forest, ReforestedTF, Degradedland) and data types (raw vs processed).
  - Documentation and reproducibility
    - The Methods sections provide detailed descriptions of instrumentation, placement, measurement intervals, and processing steps; embedded Matlab code examples illustrate reproducible data transformations.
  - Governance and change management
    - Recommend maintaining versioning of processed files, documenting any updates to calibration constants or processing scripts, and ensuring metadata remains synchronized across raw and processed datasets.

- Key challenges and considerations highlighted
  - Incomplete or evolving user needs for pastoral data governance and metadata standards.
  - Timely access to data from multiple plots and systems; ensuring data creators meet metadata and standardization requirements.
  - Handling diverse systems and formats across forest and degraded land sites; large data volumes from high-frequency measurements.
  - Ensuring up-to-date data and transparent documentation of data handling, processing, and quality checks.