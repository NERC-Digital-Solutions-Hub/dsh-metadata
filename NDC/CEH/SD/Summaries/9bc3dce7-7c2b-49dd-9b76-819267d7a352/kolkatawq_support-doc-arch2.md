# Kolkata water quality dataset

- Purpose and scope
  - A dataset of urban surface water quality in Kolkata, India, including field sensor physicochemical and optical/fluorescence measurements, plus laboratory microbiological and chemical analyses.
  - Collected across three field surveys: June 2018, March 2019, and December 2019.
  - Locations cover three urban watercourses/types: Hooghly River (Ganga), East Kolkata Wetlands, open sewage canals; some control samples from outside Kolkata (marine and groundwater) and municipal/deionised water.
  - Aims to test a prototype multichannel fluorimeter (Peak T fluorescence) for identifying waters with high bacterial load and contamination; data used to inform sensor development and adaptations for use in India.
  - Dataset comprises three CSV files (1_KolkataWQ_Jun2018.csv, 2_KolkataWQ_Mar2019.csv, 3_KolkataWQ_Dec2019.csv) with corresponding methodologies and parameters.

- Data collection and completeness
  - In-field measurements using handheld meters and a prototype fluorimeter; samples collected for laboratory analyses in parallel.
  - Fluorescence data: Averaged over 1 minute (n=60) for each sampling site; some data cropped; Peak T fluorescence (and related parameters) recorded as field averages.
  - Aqualog excitation-emission data (for fluorescence) discarded due to concerns about sample integrity (storage-age issues).
  - Some field logging issues resulted in single values without standard deviations (noted as such in the dataset).
  - Missing values are marked as NA.

- Sampling design and frequency
  - 40 samples across three field surveys over two years.
  - Field sites sampled once or revisited for seasonal/diurnal comparisons.
  - Sample collection distance: approximately 1 m from bank/boat side; GPS coordinates recorded; time/date logged.
  - Controls/reference samples included municipal tap water and deionised water.

- Parameters and analyses (overview by data type)
  - Physicochemical parameters (field)
    - June 2018 and March 2019: dissolved oxygen (DO), conductivity, temperature, pH (various meters; daily/calibration routines).
    - December 2019: DO, temperature, conductivity, total dissolved solids (TDS), oxidation-reduction potential (ORP), pH; Ultrameter 6Pfc used; weekly calibration.
  - Nutrient analyses (laboratory)
    - Ammonia, ammonium, phosphate, nitrate, nitrite measured by Palintest photometer.
    - Additional analyses at CEH (Wallingford) for total phosphorus, total dissolved phosphorus, soluble reactive phosphorus, dissolved ammonium, dissolved organic carbon (DOC) and major anions (fluoride, chloride, nitrite, nitrate, sulfate) via ion chromatography.
    - Aquacheck QC standards used; Bowes et al. 2020 methods referenced for certain analyses.
  - Microbiological analyses
    - E. coli and coliforms via membrane filtration on MLGA plates; incubation at 37°C for 24 h.
    - Total bacterial cells quantified by flow cytometry on glutaraldehyde-fixed samples with SYBR Green I staining.
  - In-situ fluorimetry sensor (prototype)
    - 2018: Three single-channel Chelsea Technologies sensors deployed (Peak C, Peak T, CDOM, turbidity-related readings).
    - 2019: Upgraded to VLux TPro five-channel fluorometer (chlorophyll-a, tryptophan, CDOM; absorbance; turbidity; additional channels for total fluorescence metrics). Data logged at 1 Hz depth (0–30 cm).
    - Data loggers: Raspberry Pi TR1 (2019), Hawk logger (2019); data averaged to 1-minute intervals (n=60) when possible; some single readings due to logging issues.
  - Data structure (files and columns)
    - File 1 (June 2018): 20 columns; fields include Date, Time, Sample_ID, Latitude, Longitude, EC, pH, DO_c, Temp, PO4, NO3, E_coli, Coliforms, TCs, plus fluorescence outputs (U_TRYP, U_TRYP_SD, U_CDOM, U_CDOM_SD, U_Turbidity, U_Turbidity_SD, V_Abs280, V_Abs280_SD, SRP, TP, NH4_N, F, Cl, NO2, NO3, etc.).
    - File 2 (Mar 2019): 37 columns; expanded metadata and parameters including NH4, PO4, NO2, NO3, E_coli, Coliforms, Total_bact_cells, V_Chl-a, V_TRYP, V_TRYP_SD, V_CDOM, V_CDOM_SD, V_Turbidity, V_Turbidity_SD, V_Abs280, SRP, TP, NH4_N, F, Cl, NO2, NO3, etc.
    - File 3 (Dec 2019): 33 columns; similar structure with depth-specific readings and single-reading field entries; includes DO, DO_s, Temp, NH4, PO4, NO2, NO3, E_coli, Coliforms, TCs, V_Chl-a, V_TRYP, V_CDOM, V_Turbidity, V_Abs280, SRP, TP, NH4_N, F, Cl, NO2, NO3, etc.
  - Instrumentation and data provenance
    - Field meters: HQ10 DO meter, Accumet conductivity meter, pH meters; in 2019 Ultrameter 6Pfc used with weekly calibration.
    - Laboratory analysis: Palintest photometer for nutrients; CEH laboratory analyses for phosphorus fractions, DOC, and major anions.
    - Microbiology: MLGA plates for E. coli and coliforms; flow cytometry for total bacterial cells.
    - Fluorimeters: Chelsea Technologies single-channel sensors (2018) and VLux 5-channel fluorometer (2019); data standardized to 1-minute averages; raw sensor data logged every second in the field.
  - Data quality and references
    - Completeness and QC procedures described; Bowes et al. (2020) referenced for methodological details on nutrient and microbial analyses.
    - Aqualog data discarded due to sample integrity concerns; some data gaps due to field logging issues or manual data entry.

- Relevance for environmental monitoring and analysis
  - Enables cross-comparison of urban freshwater quality across riverine, wetland, and sewage-impacted environments.
  - Provides multi-modal datasets suitable for environmental health monitoring, sensor validation, and integration of physico-chemical, microbial, and fluorescence-based indicators.
  - Supports assessment of the in-situ fluorimeter’s capability to flag high bacterial loads and contamination events via Peak T fluorescence.
  - Offers a rich, provenance-tracked data suite for method standardization, data cleaning, and long-term trend analysis across seasons and years.

- Limitations and caveats for analysts
  - Aqualog fluorescence data excluded from final analyses for sample integrity concerns.
  - Some measurements recorded as single values without variability estimates due to field logging constraints.
  - Three CSV files differ in column count and parameter coverage; careful alignment required for integrated analyses.
  - Spatial and temporal coverage limited to three discrete field campaigns; extrapolation beyond these periods should be approached with caution.

- Access and references
  - Data files: 1_KolkataWQ_Jun2018.csv, 2_KolkataWQ_Mar2019.csv, 3_KolkataWQ_Dec2019.csv.
  - Methods and context: Bowes et al. 2020, Nutrient and microbial water quality of the upper Ganga River; references for analytical methods and quality control.