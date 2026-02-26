# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Objective and scope
  - Multidisciplinary NERC project to understand carbon flow from land to the ocean.
  - Aimed to characterise diurnal greenhouse gas emissions from inland water bodies and how these vary with water body type and season.
  - Approach: 24-hour measurements using floating chambers placed on selected waterbodies; gas samples compared between start and end of the period.

- Sampling locations and design
  - Sampling conducted across the UK at ponds, streams, lochs, dykes, broads, and wetlands.
  - Timeframe: July 2021 to March 2022.
  - Site selection emphasized geographical and land-type variation.
  - Details of sampling sites provided in Table 1 and Figure 1.

- In-field collection and measurements
  - Water chemistry samples for DOC/TdN, TP, and SRP collected with 60 ml syringes; filtration steps described for SRP and DOC analyses.
  - Physicochemical parameters measured on-site: pH, conductivity, dissolved oxygen (DO), and temperature using calibrated instruments.
  - Floating chambers: inverted basins with floats, sealed with three-way taps; used in duplicate or triplicate; chambers covered to limit temperature fluctuations; gas accumulation over 24 hours.
  - Gas sampling: headspace sampling at the start; post-24-hour gas retrieval from chambers into pre-evacuated vials.
  - Field sampling completed by named researchers.

- Sample storage and handling
  - TP, SRP, and filtered SRP/DOC samples stored at -18°C for later analysis.
  - DOC/TdN and UV/Vis samples stored at 4°C and analyzed within a week.
  - Greenhouse gas samples stored at room temperature until batch analysis.

- Laboratory analysis and methods
  - DOC/TdN: Shimadzu TOC-LCPH with TNM L unit; 680°C combustion method with sparging; NPOC taken as DOC; rigorous QA with standards, blanks, and replicate measurements.
  - UV/Vis SUVA: absorbance scan from 230 to 800 nm; SUVA254 calculated to indicate DOC aromaticity.
  - Total phosphorus: SEAL AQ2 with potassium persulfate digestion; acid molybdenum blue colorimetric detection; calibration with multiple standards; blanks used throughout.
  - Soluble reactive phosphorus: SRP analyzed by the same colorimetric method on filtered samples.
  - Greenhouse gases: dissolved GHGs analyzed by GC (Agilent 7890B) with μECD for N2O and FID for CH4/CO2; concentrations calibrated against mixed standards; results reported as ppmv and converted to µg/L via Henry’s law.

- Data structure, units, and recording
  - MERLIN 2022-2023 dataset structure described:
    - Columns for sampling information (Site_name, Site_type, Date, Latitude, Longitude, Time).
    - Field measurements (conductivity, conductivity temperature, pH, DO, various temps, presence of chambers).
    - Lab results (DOC, TdN, C/N, UV absorbance metrics, TP, SRP, CH4_C, CO2_C, N2O_N).
    - Chamber concentrations at time 0 and 24 hours for CH4, CO2, N2O.
  - Units and decimal places specified for each parameter to ensure data consistency.

- Data quality, completeness, and transparency
  - Dataset completeness and data curation are documented (exclusions and reasons) in Table 4.
  - Exclusions include issues such as missing time, missing DO temperature, sample contamination, and missing pH or related measurements.
  - The documentation reflects careful data quality management and transparent handling of incomplete or problematic data.

- Data governance and considerations for monitoring frameworks
  - Emphasizes robust QA/QC, standardized protocols, and detailed metadata to support scrutiny, evaluation, and policy informing.
  - Clear description of measurement protocols, sampling design, and data handling supports reproducibility and potential integration into monitoring frameworks.
  - Public data sharing policy is not explicitly stated; however, the comprehensive metadata, unit definitions, and exclusion records enhance transparency and potential data reuse within governance structures.

- Acknowledgements and references
  - Acknowledges permissions and collaboration from multiple trusts and water companies.
  - References methodological sources related to DOC SUVA and dissolved inorganic carbon dynamics.