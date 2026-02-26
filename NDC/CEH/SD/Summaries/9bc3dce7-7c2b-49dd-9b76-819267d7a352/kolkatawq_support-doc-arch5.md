# KolkataWQ Kolkata Water Quality Dataset

## Overview
- Urban surface water in Kolkata, India, with field sensor physicochemical and optical/fluorescence measurements and laboratory microbiological and chemical analyses.
- Three field surveys: June 2018, March 2019, December 2019.
- Aims linked to UK-India Water Quality project; evaluates a prototype multi-channel fluorimeter for detecting high bacterial loads via Peak T fluorescence and informs sensor development for Indian context.
- Data include GPS coordinates, field measurements, and laboratory analyses; some data have been discarded due to sample integrity concerns.

## Data structure and content
- Three CSV data files:
  - 1_KolkataWQ_Jun2018.csv (20 columns)
  - 2_KolkataWQ_Mar2019.csv (37 columns)
  - 3_KolkataWQ_Dec2019.csv (33 columns)
- Key content across files:
  - Location: sample_id, latitude, longitude
  - In-field physicochemical parameters: EC (µS/cm), pH, DO (mg/L), Temp (°C), etc.
  - Laboratory analyses (within 24 hours): ammonia, ammonium, phosphate, nitrate, nitrite
  - Microbiology: E. coli, coliforms, total bac/TCs (cfu/100 mL)
  - Fluorescence and optical measurements: Peak T fluorescence (tryptophan), Peak C fluorescence (CDOM), chlorophyll-a (Chl-a), absorbance at 280 nm, turbidity
  - Flow cytometry data: total bacterial cells (cells/mL)
  - Data quality fields: SD (standard deviation) for 1-minute averages; NA values for missing data
- Measurements include a mix of field-derived sensors, laboratory chemistry, and microscopy-based microbial assays.
- Data for in-field fluorimetry and turbidity were averaged over 1 minute (n = 60) where applicable.

## Sampling regimes and sites
- Locations: predominantly within Kolkata urban area; three site types:
  - Hooghly River (Ganga)
  - East Kolkata Wetlands
  - Open sewage canals
- Additional samples outside Kolkata: RS1_DHG (marine) and RS1_NLH (groundwater) as references/controls
- 40 samples in total across the three surveys; some sites revisited for seasonal/diurnal comparisons
- Sampling method: ~1 m from water body edge, using a 2 L bucket; GPS and time/date recorded; field and lab workflows documented

## Collection, handling, and instrumentation
- Water sampling:
  - Field collection documented; aliquots prepared for lab analyses
  - Filtration and sterile handling for chemical/nutrient analyses
  - Flow cytometry aliquots fixed with glutaraldehyde for bacterial counts
- In-field physicochemical measurements:
  - June 2018 & March 2019: DO meter, conductivity, temperature, pH (calibrated daily)
  - December 2019: DO, temperature, conductivity, TDS, ORP, pH (Ultrameter calibrated weekly)
- Nutrient and chemistry analyses:
  - Palintest photometer for ammonia, ammonium, phosphate, nitrate, nitrite (lab within 24 h)
  - CEH Wallingford handled additional chemical analyses (total phosphorus, dissolved phosphorus fractions, dissolved organic carbon, major anions by ion chromatography)
  - Aquacheck QC standards used for quality control
- Microbiological analyses:
  - Filtration onto MLGA plates for E. coli and coliforms (incubation 24 h at 37°C)
  - Flow cytometry for total bacteria, with SYBR Green I staining and calibrations
- Prototype fluorimeter measurements:
  - 2018: three Chelsea Technologies single-channel sensors (Peak C, Peak T, turbidity)
  - 2019: VLux multi-channel fluorimeter with five outputs (Chl-a, Tryptophan, CDOM, absorbance at 280, turbidity)
  - Data collection:
    - 2018: 1-minute averages (n = 60) during field deployment; depth up to 30 cm
    - 2019: Raspberry Pi data logger (Mar) and Hawk data logger (Dec); 1-minute averages; some single readings due to logging issues

## Data quality, provenance, and limitations
- Data processing and QA:
  - 1-minute averages calculated from sensor data; some data logged as individual values due to field issues
  - Missing values marked as NA
  - Aqualog CDOM data discarded due to sample age/storage/transport concerns
  - Laboratory analyses performed within specified timeframes after collection
- Instrumentation variability:
  - Different field meters across surveys (DO meters, conductivity meters, pH meters, Ultrameter in later survey)
  - Different fluorimeters across surveys (Chelsea single-channel in 2018; VLux multi-channel in 2019)
- Data completeness:
  - 40 samples across two years; some parameters may have incomplete coverage due to logistical constraints
- Methods and references:
  - Nutrient and microbial methods aligned with Bowes et al. 2020
  - Detailed column mappings provided for each file, including instrument models and data collection notes

## Metadata, provenance, and usage notes for Data Stewards
- Provenance:
  - Part of UK-India Water Quality project; data collected by field teams and analyzed by collaborating laboratories
  - Post-collection interpretation led by researchers, with explicit documentation of methods
- Metadata considerations for reuse:
  - Ensure clear data lineage: field collection → in-field measurements → laboratory analyses → QA steps
  - Preserve both raw and processed data (e.g., 1-minute averages, SD, and any single-field readings)
  - Record instrument models, calibration schedules, units, and detection limits
  - Note data caveats: discarded Aqualog data, logger-related single readings, site revisits for temporal analysis
  - Align with Bowes et al. (2020) methods where applicable to ensure comparability
- Governance recommendations:
  - Include comprehensive metadata with method references, calibration details, and QA steps
  - Maintain versioning and provenance links to the three CSV files
  - Provide guidance on how to handle NA values and any data imputation strategies
  - Clarify licensing/access rights if sharing beyond the original project

## References
- Bowes, M.J., Read, D.S., Joshi, H., Sinha, R., Ansari, A., Hazra, M., Simon, M., Vishwakarma, R., Armstrong, L.K., Nicholls, D.J.E., Wickham, H.D., Ward, J., Carvalho, L.R., Rees, H.G., 2020. Nutrient and microbial water quality of the upper Ganga River, India: identification of pollution sources. Environ. Monit. Assess. 192. https://doi.org/10.1007/s10661-020-08456-2