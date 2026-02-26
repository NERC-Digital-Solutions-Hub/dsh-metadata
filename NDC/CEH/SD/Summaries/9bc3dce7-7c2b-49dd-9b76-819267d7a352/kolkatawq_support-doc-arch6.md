# KolkataWQ Kolkata Water Quality Dataset

## Overview
- Urban surface water quality dataset from Kolkata, India, collected as part of a UK-India Water Quality project.
- Three field surveys: June 2018, March 2019, and December 2019.
- Data types include field sensor physicochemical and optical/fluorescence measurements, plus laboratory microbiological and chemical analyses.
- Location data (latitude/longitude) provided for all sample sites.
- Purpose: evaluate sensing technologies (prototype multichannel fluorimeter) for detecting high bacterial load and contamination events via Peak T fluorescence; inform sensor development for Indian contexts.

## Data Completeness and Processing Notes
- Full excitation-emission matrix data (Aqualog) collected but discarded due to sample integrity concerns (age, storage, transport).
- Prototype sensor data cropped to 1-minute averages (60 readings) per sampling site; where logging failed in the field (file 3), single values are provided.
- Missing values denoted as NA.
- Field sensor data averaged over 1 minute (n = 60) in most files; some instances use single readings.
- Outputs are organized in three CSV files: 1_KolkataWQ_Jun2018.csv, 2_KolkataWQ_Mar2019.csv, 3_KolkataWQ_Dec2019.csv.

## Sampling Regime and Study Sites
- Three Kolkata urban-water contexts: Hooghly River, East Kolkata Wetlands, open sewage canals.
- Additional controls: RS1_DHG (marine outside Kolkata) and RS1_NLH (groundwater outside Kolkata).
- Total of 40 samples across the three surveys, enabling diurnal/seasonal comparisons where locations were revisited.

## Data Collection and Laboratory Workflows

- A. Water sample collection
  - Collected ~1 m from bank/boat side using a 2 L bucket; GPS and date/time recorded.
  - In-field physicochemical parameters logged; subsamples sent for laboratory analysis.
  - Subsamples filtered (0.45 µm) for chemical/nutrient analyses; aliquots fixed (glutaraldehyde) for flow cytometry in duplicates.

- B. In-field physicochemical parameters
  - June 2018 and March 2019: DO (with daily calibration), conductivity, temperature, pH (field meters).
  - December 2019: DO, temperature, TDS, ORP, pH measured with Ultrameter 6Pfc (weekly calibration).

- C. Nutrient analysis
  - Palintest photometer used in the laboratory within 24 hours for ammonia, ammonium, phosphate, nitrate, nitrite.
  - CEH (Wallingford) conducted additional analyses on 60 mL filtered samples for total phosphorus, total dissolved phosphorus, soluble reactive phosphorus, dissolved ammonium, DOC, and major dissolved anions (F, Cl, NO2, NO3, SO4); quality controlled with Aquacheck standards.

- D. Microbiological analysis
  - In-lab analyses within 6 hours of collection.
  - Coliforms and E. coli enumerated via membrane filtration on MLGA plates after serial dilution.
  - Flow cytometry: fixed samples stained with SYBR Green I; counted bacterial cells with calibration beads on a Gallios cytometer.

- E. Prototype in-situ Fluorimeter
  - June 2018: three single-channel Chelsea sensors (Peak C, Peak T, turbidity).
  - 2019: five-channel VLux fluorimeter (Chlorophyll fluorescence, Tryptophan, CDOM fluorescence, Absorbance at 280, Turbidity) with internal corrections for absorbance, turbidity, and temperature.
  - Depth: sensors deployed at 30 cm; data logged per second in 2019; averaged to 1 minute (n=60).
  - Data loggers: Raspberry Pi TR1 (Mar 2019) and Hawk logger (Dec 2019); some December readings were single values due to logging issues.

## Data Files and Column Details
- 1_KolkataWQ_Jun2018.csv
  - 20 columns: time, sample ID, latitude, longitude, EC, pH, DO_c, Temp, PO4, NO3, E_coli, Coliforms, TCs, U_TRYP (Peak T fluorescence), U_TRYP_SD, U_CDOM (Peak C fluorescence), U_CDOM_SD, U_Turbidity, U_Turbidity_SD, U_Abs280, U_Abs280_SD, SRP/TP/NH4 etc. 
  - Field vs lab-derived measurements aligned with the June 2018 protocol.

- 2_KolkataWQ_Mar2019.csv
  - 37 columns: includes Date/Time, Sample_ID, Latitude, Longitude, EC, pH, DO_c, Temp, NH4, PO4, NO2, NO3, E_coli, Coliforms, TCs, Total_bact_cells (flow cytometry), Chlorophyll-a (V_Chl-a) and its SD, Peak T (V_TRYP) and SD, Peak C (V_CDOM) and SD, Turbidity (V_Turbidity) and SD, Absorbance at 280 (V_Abs280) and SD, SRP, TP, NH4_N, F, Cl, NO2, NO3, SO4 and other dissolved species; includes numerous field-averaged and SD columns for 60-second data.

- 3_KolkataWQ_Dec2019.csv
  - 33 columns: Date/Time, Sample_ID, Latitude, Longitude, EC, TDS, ORP, pH, DO_c, DO_s, Temp, NH4, PO4, NO2, NO3, E_coli, Coliforms, TCs, Chlorophyll-a (V_Chl-a) and its SD, Peak T (V_TRYP) and SD, Peak C (V_CDOM) and SD, Turbidity (V_Turbidity) and SD, Absorbance at 280 (V_Abs280) and SD, SRP, TP, NH4_N, F, Cl, NO2, NO3, SO4, etc.; includes field-averaged readings and standard deviations where applicable.

- Data provenance and references
  - Bowes et al. 2020: Nutrient and microbial water quality of the upper Ganga River; methodology referenced for nutrient analyses.

## Data Quality and Reuse Considerations
- Aqualog EM data excluded due to sample integrity concerns; consider omitting or flagging if re-use requires fluorescence matrices.
- Field logging gaps in December 2019 resulted in some single-value measurements; treat as single observations rather than time-averaged.
- Units vary across files (e.g., µS/cm, mg/L, µg/L, cfu/100 mL, FNU); ensure consistent unit normalization if combining across files.
- Spatial coverage covers three urban water contexts, with nearby controls; useful for site-based dashboards and comparative analyses.
- Data supports linking sensor-derived fluorescence signals (Peak T, Peak C, V_Chl-a, etc.) with microbiological indicators (E. coli, total coliforms) and nutrient status (NH4, NO3, TP, SRP, DOC).

## Potential Data Products and Use for Data Support
- Self-serve dashboards by site and survey, showing:
  - Temporal trends in physicochemical parameters (DO, pH, EC, TDS, ORP, Turbidity).
  - Relationship between fluorescence signals (Peak T, Peak C, Chlorophyll-a, CDOM) and microbial indicators (E. coli, coliforms, total bacteria).
  - Nutrient dynamics (ammonium, nitrate/nitrite, phosphate, SRP, TP, DOC) across sites and times.
- Data integration workflows:
  - Join in-situ sensor outputs with lab-based nutrient and microbiological results using Sample_ID, time, and location.
  - Harmonize units and time-averaging (1-minute means) across files; flag or impute NA values where needed.
- Analytical opportunities:
  - Multivariate analyses linking fluorescence-derived features to contamination events.
  - Seasonal/diurnal comparisons and site-type contrasts (river vs wetlands vs canals).
  - Evaluation of fluorimeter-based rapid screening against laboratory microbial counts.

## Alignment with Data Support Archetype
- The dataset exemplifies a data support workflow: understanding the ask (sensor vs lab data to monitor urban water quality), data discovery and verification (field and lab data across three surveys, with location and instrumentation details), quality assurance and transformation (clear documentation of methods, missing data handling, and data exclusions), data analysis and product creation (potential dashboards and reports for end-users), and output promotion/feedback (data companions for further sensor development and policy-relevant insights).