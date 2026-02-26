# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

- Purpose and context
  - Part of the UK Countryside Survey, a long-running national audit of natural resources designed to detect changes over time and inform policy on soil health, food security, public health, and climate understanding.
  - Adopted a rolling five-year sampling cycle since 2019 to monitor topsoil condition and changes, enabling comparisons with prior surveys (1978, 1998, 2007, and 2019+).
  - Covid-19 disruption in 2020 affected fieldwork; adjustments included reselecting 50 squares within England.

- Survey design and sampling framework
  - Rolling program: 500 1-km2 squares sampled per five-year cycle; 100 squares visited annually.
  - Stratified sampling based on Land Classification of Great Britain (ITE LC07) to ensure national/sub-national representativeness.
  - Exclusions: squares with >75% urban land or >90% sea were omitted.
  - Winter topsoil survey subset (2021) used a hierarchical selection to prioritize prior survey squares (1978, 1998, 2007) and to reflect environmental zones; 30 (+5 reserve) squares repeated in winter 2021.
  - Each selected square involves five sampling locations (PLOTs) where topsoil (0–15 cm) is collected for analysis.

- Sample collection and data collection methods
  - In each square, five randomly dispersed locations using vegetation X-Plots; soil collected with a 15 cm core at co-located vegetation survey points.
  - Historical sampling locations tracked via maps and permanent markers; 1990 markers placed adjacent to 1978 plots for relocation.
  - For 2021 winter, Broad Habitat was recorded; samples refrigerated and sent to UKCEH laboratories for processing and storage in the Soil Bank.
  - Data structure uses 1-km square IDs (SQUARE) and plot IDs (PLOT), with year (YEAR) specified for each soil sample.

- Measured metrics and laboratory protocols
  - Core suite of soil metrics (0–15 cm FE: fine earth) and derived metrics:
    - pH in deionised water (PH)
    - Loss-on-Ignition (LOI) as a measure of soil organic matter (LOI)
    - Soil carbon concentration from LOI (C_CONC_LOI)
    - Soil carbon stock per hectare (C_STOCK_LOI)
    - Soil bulk density (BULK_DENSITY)
    - Gravimetric water content/moisture (MOISTURE_DRY; MOISTURE)
    - Total nitrogen (N_PERCENT; N_STOCK)
    - Olsen phosphorus (PO4_OLSEN) not measured in 2021 winter survey; reported for compatibility with other data
  - LOI is converted to carbon concentration and stock using established equations (e.g., C_CONC_LOI = 0.55 × C_FE_LOI × 10; C_STOCK_LOI calculated with area and bulk density).
  - Soil carbon groups (SOIL_GROUP) categorized by LOI-derived levels.
  - Land Classification (LC07 / LC07_NUM) and Environmental Zones (EZ_DESC_07) included to contextualize results within environmental gradients.
  - Training data and QA ensure calibration and accuracy; internal QC standards and duplicates used for pH and LOI.

- Data quality assurance and governance
  - A robust, multi-step QA workflow:
    - Lab data QA: initial QA of lab data with checks for unexpected values, gaps, and consistency with measurement standards.
    - Analyst QA1: cross-check lab data against measurement records; document queries and changes.
    - Calculation of derived soil metrics via standardized R scripts (calculate_soil_derived_metrics_function.R and Derive soil data.R) to ensure reproducibility and auditability.
    - Analyst QA2: automated HTML QA reports to examine patterns, relationships, and outliers; cross-check with habitat/vegetation data.
  - All changes are logged against data records and QA steps to maintain transparency and auditability.
  - Data workflow integrates outputs with other survey components and supports data governance standards.

- Data structure and accessibility
  - The winter 2021 soil dataset comprises 18 columns and 576 rows; missing samples denoted by -9999.
  - Key fields include SQUARE, PLOT, YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, SOIL_GROUP, BULK_DENSITY, MOISTURE_DRY, MOISTURE, N_PERCENT, N_STOCK, PO4_OLSEN (not measured in 2021 winter), LC07, LC07_NUM, COUNTRY, EZ_DESC_07.
  - Data are organized to allow linkage with vegetation and habitat data, supporting integrated analyses of soil-vegetation interactions and multi-metric monitoring.
  - Related resources include the UKCEH Soil Bank and Countryside Survey methodological documents; datasets are designed for open sharing within governance constraints.

- Context and policy relevance
  - Aims to quantify directions and magnitudes of soil change across Great Britain and to understand interactions among pressures (deposition, land use, climate).
  - Focus on topsoil health indicators that influence soil function and ecosystem services, including carbon stock, nutrient status, pH, and moisture dynamics.
  - Enables generation of maps and indicators of stock and change in GB soils, supporting national-scale indicators for soil health and informing land management and policy decisions.

- Key limitations and considerations for monitoring framework authors
  - Some measurements (e.g., Olsen phosphorus) are not always collected in every sub-survey cycle, requiring careful handling in cross-cycle comparisons.
  - Data gaps and metadata completeness can pose challenges for rapid reuse; emphasis on robust metadata and open data governance is essential.
  - Seasonal and year-to-year sampling variability (e.g., winter sampling subset) requires explicit architectural design to maintain comparability across cycles.
  - Transformations and harmonization steps (e.g., LOI-to-C conversions, bulk density adjustments) must be transparently codified and auditable for policy-relevant reporting.

- Contact and access
  - Data and methodological details are maintained by UK Centre for Ecology & Hydrology (UKCEH); inquiries can be directed to enquires@ceh.ac.uk and related contact points through CEH catalogues and the Countryside Survey website.