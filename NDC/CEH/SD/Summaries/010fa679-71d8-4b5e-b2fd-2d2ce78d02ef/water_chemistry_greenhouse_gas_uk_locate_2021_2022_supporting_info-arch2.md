# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Aim and scope
  - LOCATE is a multidisciplinary project to improve understanding of carbon flow from land into the ocean.
  - Field campaign focused on characterising diurnal greenhouse gas emissions from inland water bodies and how emissions vary by water body type and season (summer vs winter).
  - Method: floating chambers deployed for 24 hours to measure water-atmosphere gas exchange.

- Project and sampling design
  - Collaboration across UK institutions (NERC-supported) including CEH, NOC, BGS, Plymouth Marine Laboratory, and others.
  - Sampling conducted across the UK from July 2021 to March 2022.
  - Sites chosen to capture geographical and land-type variation (ponds, streams, lochs, dykes, broads, wetlands).
  - Detailed site information provided in Table 1 and Figure 1 of the dataset.

- Field sampling and measurements
  - In-field collection for:
    - Dissolved organic carbon/total dissolved nitrogen (DOC/TdN)
    - Total phosphorus (TP)
    - Soluble reactive phosphorus (SRP)
  - Water samples collected with syringes and filtered (SRP and DOC) through 0.45 µm filters; TP collected in sterile bottles for freezing.
  - Physicochemical parameters measured in situ: pH, conductivity, dissolved oxygen (DO), temperature using a multi-parameter meter; calibration procedures described.
  - Floating chambers prepared to enclose air above water surface; 24-hour incubations with sampling via three-way taps.
  - Dissolved GHGs measured at start (0 hours) using headspace method; gases accumulated in chambers were sampled after 24 hours.

- Sample storage and handling
  - TP, SRP, and spare filtered DOC samples stored at -18°C until batch analysis.
  - DOC/TdN/UV-Vis samples stored at 4°C and analysed within a week.
  - GHG samples stored at room temperature until batch analysis.

- Laboratory analyses
  - DOC and TdN: Shimadzu TOC-LCPH with TNM L unit; uses 680°C combustion, acidification, sparging; NPOC treated as DOC; quality control with standards and blanks; duplicate measurements with outlier rejection.
  - UV/Vis and SUVA: Absorbance from 230–800 nm; SUVA at 254 nm for DOC aromaticity; blank-corrected.
  - Total Phosphorus: SEAL AQ2 discrete analyzer after digestion with potassium persulfate; acid molybdenum blue colorimetric method; calibration with multiple standards; blanks used.
  - Soluble Reactive Phosphorus: SRP measured by SEAL AQ2 via same colorimetric method on filtered samples.
  - Greenhouse gases: Dissolved GHGs analysed by Agilent 7890B GC with μECD for N2O and FID for CH4/CO2; concentrations calibrated against mixed standards; results in ppmv converted to µg/L via Henry’s law; averages of duplicates used.

- Data structure, units, and recorded values
  - Dataset structure described for the MERLIN 2022-2023 dataset:
    - Columns A–F: sampling information (Site_name, Site_type, Date, Latitude, Longitude, Time)
    - Columns G–M: field physicochemical data (Conductivity, Conductivity_temp, pH, pH_temp, DO, DO_temp, Temp_av)
    - Columns O–AD: laboratory results (DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, plus chamber-specific gas concentrations over time)
  - Units and descriptions provided in Table 3 (e.g., Conductivity in µS/cm, DO in mg/L, CH4_C in µg/L, etc.).

- Dataset completeness and exclusions
  - Table 4 documents exclusions and reasons for missing or invalid data.
  - Exclusions include: missing time/recording details, DO_temp not recorded, sample contamination, pH or CH4_C data missing, missing samples for certain gas measurements, and other determinant-specific gaps.
  - Reasons include “Not recorded,” “Sample contamination,” “Missing sample,” or “Time/Determinants” not recorded for specific site-date entries.

- Outputs and accessibility
  - The study emphasises standardised data collection, quality assurance, and transformation for downstream analysis.
  - Datasets are prepared for storage in appropriate data portals and are suitable for cross-site comparisons and policy-relevant environmental monitoring.

- Acknowledgements and references
  - Acknowledges site access and sampling permissions from various organisations.
  - References include methodological sources for SUVA and downstream GHG concepts.