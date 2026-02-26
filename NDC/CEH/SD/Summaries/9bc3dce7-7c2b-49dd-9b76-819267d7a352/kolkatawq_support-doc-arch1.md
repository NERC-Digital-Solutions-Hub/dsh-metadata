KolkataWQ Water Quality Dataset: Field Sensor, Laboratory Microbiological and Chemical Analysis of Urban Surface Water in Kolkata, India (June 2018, March 2019, December 2019)

## Overview
- A dataset of field sensor measurements, laboratory microbiological and chemical analyses of urban surface water samples from Kolkata, India.
- Collected across three surveys: June 2018, March 2019, and December 2019.
- Aimed to develop and test sensing/treatment technologies for monitoring water quality, with a focus on identifying waters with high bacterial load via Peak T fluorescence.
- Includes location coordinates, field and laboratory measurements, and details on sensors and protocols.

## What was collected
- Field sensor data: physicochemical and optical/fluorescence measurements using handheld meters and in-situ fluorimeters.
- Laboratory analyses: microbiological (E. coli, coliforms, total bacteria by flow cytometry) and chemical analyses (nutrients, anions, DOC, phosphorus fractions, etc.).
- A total of 40 samples across three field surveys, from urban Kolkata locations, plus reference samples (municipal water and deionised water).

## Field sampling design
- Sampling sites primarily within Kolkata city, West Bengal; sites categorized as:
  - Hooghly River (Ganga)
  - East Kolkata Wetlands
  - Open sewage canals
  - outside Kolkata: marine and groundwater examples (RS1_DHG, RS1_NLH)
- Some sites revisited to enable seasonal/diurnal comparisons.
- Sampling methods:
  - ~1 m from bank/boat side; 2 L bucket collection; triplicate handling with field logging of time, date, and GPS.
  - Subsamples collected for in-field measurements and laboratory analyses, with specific handling (filtration, storage at 4°C, darkness, etc.).
- Field sampling ensured by local knowledge and safe access considerations.

## In-field measurements and sensors
- Physicochemical parameters measured in the field:
  - Dissolved oxygen (DO), temperature, conductivity, pH; DO and temperature readings taken immediately after collection, with daily calibration.
  - Some surveys used different instrument sets (June 2018 & March 2019 vs December 2019) with different meters (e.g., Hach HQ10; Ultrameter 6Pfc).
- Fluorometric sensing:
  - 2018: three single-channel Chelsea sensors (precursor to multichannel sensor) measuring Peak C fluorescence, Peak T fluorescence, and turbidity.
  - 2019: VLux multichannel fluorimeter (5 channels) with internal corrections for absorbance, turbidity, and temperature; data averaged over 1 minute (n=60) and logged at 30 cm depth.
  - Data formats included per-site averages and standard deviations for 1 minute of data collection (where applicable).
- Depth and logging:
  - Depth of sensors up to 30 cm; 1-minute data averages; some 1-second or single readings in later fieldwork due to logging issues.

## Laboratory analyses
- Nutrients and related chemistry (Palintest photometer, CEH lab analyses):
  - Ammonia, ammonium, phosphate, nitrate, nitrite; soluble reactive phosphorus, total phosphorus, total dissolved phosphorus, dissolved ammonium, DOC (via thermal oxidation), major anions (fluoride, chloride, nitrite, nitrate, sulfate) by ion chromatography.
  - Quality controls using Aquacheck standards.
- Microbiology:
  - E. coli, total coliforms, and other coliforms (excluding E. coli) via membrane filtration and MLGA plates; incubated at 37°C for enumeration.
  - Total bacterial cells counted by flow cytometry after glutaraldehyde fixation and SYBR Green I staining; calibration with 1 µm beads.
- Data handling:
  - Lab analyses completed within stated windows after sample collection (often within 6–24 hours depending on parameter).

## Prototype fluorimeter data and data logging
- 2018 field data used Chelsea single-channel fluorimeters; 2019 field data used Chelsea VLux multi-channel sensor with five outputs.
- Output channels include chlorophyll-a fluorescence, tryptophan fluorescence, CDOM fluorescence, absorbance at 280 nm, turbidity, and several phosphorus/nutrient proxies.
- Data are reported as:
  - Average over 1 minute (n=60) for field measurements.
  - Standard deviations over the same interval where available.
- Data logging progressed from a Raspberry Pi data logger (Mar 2019) to a custom Hawk logger (Dec 2019); some single readings recorded due to logging issues.

## Data structure and files
- Three CSV files:
  - 1_KolkataWQ_Jun2018.csv (file 1) with 20 columns, including date, sample ID, location, EC, pH, DO, Temp, nutrient/chemistry lab results, E. coli, coliforms, total bacteria, and fluorescence data (Peak T, Peak C, CDOM, turbidity; SDs).
  - 2_KolkataWQ_Mar2019.csv (file 2) with 37 columns, including expanded time/sample fields and comprehensive field and lab measurements; additional fluorescence channel outputs and quality notes.
  - 3_KolkataWQ_Dec2019.csv (file 3) with 33 columns, including field and lab values; detailed sensor outputs; single-read measurements where applicable.
- Common data features:
  - Geographic coordinates for sample locations.
  - Field measurements (EC, pH, DO, Temp, etc.) and laboratory results (nutrients, DOC, ions, E. coli, coliforms, total bacteria).
  - In-situ fluorescence and related sensor outputs with averages and standard deviations where available.
- Data quality notes:
  - Aqualog excitation-emission matrices were discarded due to sample integrity concerns (age/storage/transport).
  - Some field logs contain NA where values were not collected or were recorded by hand.
  - Some field data logger issues led to single-value entries or missing SDs in certain files.

## Data quality, limitations, and context
- Sample integrity concerns led to removal of certain fluorescence data (Aqualog EEMs).
- Field equipment changes across surveys introduced some inconsistency in measurement techniques and instrumentation.
- Data include robust metadata (instrumentation, units, sampling approach, and analysis methods) to enable reproducibility and cross-study comparisons.
- Reference framework:
  - Bowes et al. 2020 provides methodological context for nutrient and microbial water quality in the upper Ganga River and related analyses.

## How analysts can use this dataset
- Identify correlations between in-field fluorescence signals (Peak T, Peak C, CDOM, chlorophyll-a, tryptophan) and lab-measured microbial loads (E. coli, total/other coliforms) to calibrate sensor-based screening.
- Model relationships between fluorescence signatures and nutrient/chemical parameters (ammonium, nitrate, phosphate, DOC, major ions) to infer pollution sources.
- Assess spatial variability across Kolkata water bodies (Hooghly River, East Kolkata Wetlands, sewage canals) and temporal changes (diurnal/seasonal) using repeated-site sampling data.
- Develop predictive models for bacterial contamination events using Peak T fluorescence and other sensor outputs.
- Compare field sensor data against lab analyses to evaluate the in-situ sensing technology's effectiveness for monitoring and early warning.

## References
- Bowes, M.J., Read, D.S., Joshi, H., Sinha, R., Ansari, A., Hazra, M., Simon, M., Vishwakarma, R., Armstrong, L.K., Nicholls, D.J.E., Wickham, H.D., Ward, J., Carvalho, L.R., Rees, H.G., 2020. Nutrient and microbial water quality of the upper Ganga River, India: identification of pollution sources. Environ. Monit. Assess. 192. https://doi.org/10.1007/s10661-020-08456-2