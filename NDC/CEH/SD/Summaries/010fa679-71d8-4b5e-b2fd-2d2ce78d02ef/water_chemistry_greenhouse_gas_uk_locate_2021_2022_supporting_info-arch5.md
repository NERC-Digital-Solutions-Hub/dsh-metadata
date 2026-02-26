# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Objective and scope
  - LOCATE is a multidisciplinary NERC project aimed at understanding carbon flow from land to the ocean, focusing on diurnal greenhouse gas emissions from inland water bodies across the UK.
  - Field method: use floating chambers to measure 24-hour gas emissions and compare start vs. end samples to quantify emissions.

- Study design and sampling locations
  - Sampling conducted July 2021 to March 2022 across diverse UK water bodies (ponds, streams, lochs, dykes, wetlands) to capture geographical and land-type variation.
  - Site details and coordinates are provided in Table 1 and Figure 1, with extensive site naming (e.g., Wroxham Broad, Upton Broad, etc.).

- In-field collection and handling
  - Water samples collected for DOC/TdN, TP, and SRP using 60 mL syringes; filtration and bottle preparation described for each parameter.
  - Physicochemical measurements included pH, conductivity, dissolved oxygen, and temperature using calibrated multi-parameter equipment.
  - Floating chambers enabled gas concentration accumulation; gases sampled at start and after 24 hours and stored in pre-evacuated Exetainer vials.
  - Dissolved gas samples collected using headspace method with duplicates.

- Sample storage and laboratory analysis
  - Storage: TP/SRP/filtered samples frozen at -18°C; DOC/TdN/UV-Vis samples stored at 4°C and analyzed promptly; GHG samples stored at room temperature until batch analysis.
  - DOC/TdN: analysed by Shimadzu TOC-LCPH with NPOC method; QA included blanks, standards, calibration checks, and replicate processing with CV-based exclusions.
  - UV/Vis SUVA: absorbance measured from 230–800 nm; SUVA254 calculated to indicate DOC aromaticity.
  - Total phosphorus (TP) and soluble reactive phosphorus (SRP): analysed with SEAL AQ2 Discrete analyser; digestion and colorimetric steps described; calibration and blanks used for QA.
  - Greenhouse gases: CH4, CO2, and N2O analysed by GC (μECD for CH4/N2O; FID for CO2) with calibration against mixed standards; results converted to appropriate units.

- Data structure, columns, and units
  - Dataset structure (MERLIN 2022-2023) includes:
    - Site and sampling information (Site_name, Site_type, Date, Latitude, Longitude, Time, Chambers).
    - Field physicochemical data (Conductivity, Conductivity_temp, pH, pH_temp, DO, DO_temp, Temp_av).
    - Laboratory measurements (DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N).
    - Chamber-specific concentrations (Chamber_CH4_C_time_0, Chamber_CH4_C_time_24, Chamber_CO2_C_time_0, Chamber_CO2_C_time_24, Chamber_N2O_N_time_0, Chamber_N2O_N_time_24).
  - Each parameter includes specified decimal places and units (e.g., µS/cm, °C, mg/L, mg/L for TP/SRP, µg/L for CH4_C, etc.).
  - The dataset documents the column descriptions and units in Table 3.

- Data quality, completeness, and exclusions
  - Table 4 lists data exclusions with reasons (e.g., missing time data, DO_temp missing, sample contamination, missing pH/pH_temp data, not recorded measurements for various determinants).
  - Exclusions cover a wide range of sites and determinants (e.g., Auchencorth Pond, Hoveton Broad, St Margaret’s Loch, Loch Lucy Pool variants, etc.) and reflect issues such as recording gaps, contamination, or missing samples.
  - The document outlines how exclusions were determined and which determinants/sites were affected, illustrating an emphasis on traceable data quality and auditability.

- Governance, provenance, and acknowledgements
  - Data collection involved multiple collaborating institutions and field teams; site access and permissions acknowledged.
  - Supporting information details the methods, QA processes, and dataset structure to support data discoverability, reuse, and governance.
  - References provided for methodological context (e.g., SUVA calculation, downstream CO2 measurements).

- Practical implications for data stewards
  - Detailed, auditable metadata enabling reproducibility (site, date, time, coordinates, chamber usage, measurement methods, QA steps).
  - Clear data model and units enable interoperability and integration into larger data portals or catalogs.
  - Documented data quality controls (replicates, blanks, calibration checks, CV thresholds) and explicit reasons for data exclusion support robust governance and data quality assurance.
  - Comprehensive documentation of sampling and analysis workflows facilitates data lineage tracking and any future updates or re-analyses.