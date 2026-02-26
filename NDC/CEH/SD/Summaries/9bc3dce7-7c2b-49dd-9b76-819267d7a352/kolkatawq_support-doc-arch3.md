Kolkata Water Quality Dataset (KolkataWQ_Jun2018, KolkataWQ_Mar2019, KolkataWQ_Dec2019)

Overview and objectives
- Dataset from UK-India Water Quality project focusing on sensing and treatment technologies to monitor and improve water quality in India.
- Case study of three urban surface water types in Kolkata, intended to evaluate a prototype multichannel fluorimeter and its ability to identify high bacterial load and contamination via Peak T fluorescence.
- Three field surveys (June 2018, March 2019, December 2019) used to inform sensor development and identify adaptations needed for applicability in India.
- Data include field sensor measurements, laboratory analyses, and microbiological assessments, with the goal of informing environmental health monitoring and policy decisions.

Data types and measures
- Physicochemical: Electrical conductivity, pH, dissolved oxygen, temperature, total dissolved solids, oxidation-reduction potential, turbidity, absorbance at 280 nm.
- Nutrients: Ammonia, ammonium, nitrate, nitrite, phosphate, soluble reactive phosphorus, total phosphorus, dissolved organic carbon.
- Microbiological: Escherichia coli, total coliforms, coliforms (excluding presumptive E. coli), total bacteria cells (flow cytometry).
- Fluorescence and related sensors: Peak T fluorescence (tryptophan), Peak C fluorescence (CDOM), chlorophyll-a fluorescence, turbidity, absorbance, with data standardized on 1-minute averages.
- Additional metrics: Total bacterial cells (flow cytometry), chlorophyll-a measurements, and various data quality indicators (standard deviations, QSU units, CFU/100 mL, etc.).

Sampling design and field methods
- Locations: Urban Kolkata sampling sites within Hooghly River (Ganga), East Kolkata Wetlands, open sewage canals; two additional samples (RS1_DHG, RS1_NLH) outside urban area as marine and groundwater references.
- Sampling of 40 sites across three surveys over two years; some sites revisited for seasonal/diurnal comparisons; controls included municipal water and deionised water samples.
- Field collection: ~1 m from bank/boat side, 2 L buckets, with GPS coordinates and date/time recorded; duplicates prepared for flow cytometry.
- In-field measurements largely conducted with handheld meters and in-situ fluorimeters; samples sent for laboratory analyses within defined time frames.

In-field and laboratory methods
- Field instrumentation (varying by survey): optical dissolved oxygen meters, conductivity meters, pH meters, temperature sensors, and multiple fluorimeters (Chelsea Technologies and VLux prototypes) deployed at 30 cm depth.
- 2018: three single-channel Chelsea sensors; 2019: VLux multi-channel fluorimeter with one-minute data averaging and absorbance/turbidity corrections.
- Data logging: 2019 used a Raspberry Pi data logger with Python GUI; 2020 used a Chelsea Hawk data logger; some 3rd survey values recorded as single readings due to logging issues.
- Nutrient analyses (Palintest photometer) conducted within 24 hours of collection at Bose Institute; CEH performed additional chemical analyses (phosphorus species, major ions, DOC, etc.) using standard methods.
- Microbiological analyses: filtration method for E. coli and coliforms; flow cytometry for total bacterial cells with fixed samples stained with SYBR Green I.
- Data quality controls: blanks, Aquacheck standards, and method descriptions referenced (Bowes et al., 2020).

Data structure, availability, and quality
- Three CSV files corresponding to field campaigns:
  - 1_KolkataWQ_Jun2018.csv (20 columns)
  - 2_KolkataWQ_Mar2019.csv (37 columns)
  - 3_KolkataWQ_Dec2019.csv (33 columns)
- Column details map to sampling metadata (date, time, Sample_ID, Latitude, Longitude), field measurements (EC/µS/cm, pH, DO, Temp, etc.), laboratory results (NH4, PO4, NO2, NO3, E. coli, Coliforms, Total bacteria), and in-field sensor outputs (Peak T, Peak C, CDOM, Chl-a, Turbidity, Absorbance, associated SDs).
- Data processing: values averaged over 1 minute of data collection (n = 60) for most sensors; where logging issues occurred, single values provided with no SD.
- Data completeness and integrity: some Aqualog fluorescence data discarded due to sample age/storage concerns; missing values marked as NA; some field data represented as averages post-collection.
- Data provenance: detailed method notes and instrumentations per file; references Bowes et al. (2020) for nutrient and microbial analyses; three datasets together provide a longitudinal view across two years.

Data quality, gaps, and governance considerations
- Completeness gaps: occasional missing or single readings due to logging issues; some datasets partially field-logged or cropped (1-minute averages); Aqualog data discarded due to sample integrity concerns.
- Metadata and standardization: comprehensive column mappings and instrument details enable cross-site comparability; variability in equipment across surveys highlights the need for standardized metadata and calibration records for monitoring frameworks.
- Data sharing and openness: dataset structured for public sharing with explicit metadata and methods; recognition of data governance considerations in sharing sensor-derived and laboratory-analytical data.
- Implications for policy and monitoring frameworks: demonstrates feasibility of integrating in-situ sensing with laboratory analyses to monitor urban water quality, detect contamination events, and identify pollution sources; highlights the importance of metadata richness, data quality controls, and transparent reporting to support evidence-based decisions.

Relevance for monitoring frameworks and decision-making
- Provides a practical example of combining field sensor networks with laboratory analyses to monitor environmental health in an urban setting.
- Useful for policymakers and program managers to:
  - Define a suite of environmental health metrics (physicochemical, nutrient, microbial, and fluorescence-based indicators) for policy scrutiny.
  - Assess data quality, provenance, and governance requirements for monitoring datasets.
  - Identify data gaps and data management needs (metadata completeness, data standardization, sharing protocols) to support transparent decision-making.
  - Inform sensor development and deployment strategies by analyzing how in-situ fluorescence and related measurements correlate with microbial contamination events.
- Underlines challenges common to monitoring frameworks: data access, metadata quality, data transformation needs, data governance, and ensuring datasets remain up-to-date and usable for policy evaluation.