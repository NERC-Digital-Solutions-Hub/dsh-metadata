# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC

- Purpose and context
  - Countryside Survey is a long-running national audit of the UK countryside, enabling comparison over time and across regions.
  - The 2019-onward rolling program focuses on topsoil condition and vegetation to assess direction and magnitude of soil change and interactions with multiple pressures.
  - The program supports policy-relevant questions about soil carbon, acidity, nitrogen, nutrient status, compaction, and vegetation feedbacks.

- Monitoring framework and design
  - Rolling survey: repeats on a five-year cycle or after 500 squares completed to capture change and buffer against climate year variability.
  - Spatial design: 500 1-km x 1-km squares sampled per cycle, selected within strata defined by Land Classification to provide national and sub-national indicators.
  - Annual sub-sampling: 100 squares visited each year; urban or water-dominated squares excluded.
  - Data integration: multi-metric, ecosystem-scale approach with data collection aligned across vegetation and soils where possible.
  - Covid disruption (2020): partial year survey; reselected squares (50 in England) to maintain coverage and continuity.

- Sampling methods and field procedures
  - Within each 1-km square, topsoil samples are taken from five randomly dispersed locations aligned with vegetation X-Plots.
  - Core depth: 0–15 cm; sampling location linked to 2x2 m vegetation quadrats.
  - Long-term plotting: 1978 baseline with relocations and marker-based re-locations to maintain site continuity; sample relocation accuracy verified with photos, maps, and GPS.
  - Sample handling: cores refrigerated and sent to UKCEH laboratories or Soil Bank for processing/storage.

- Metrics, laboratory protocols and analytical methods
  - Core measurements: up to five samples per square for soil metrics; volumes calculated for bulk density and carbon stock estimates.
  - Key soil metrics:
    - Soil pH in deionized water (field-moist bulk soil)
    - Loss-on-Ignition (LOI) to determine soil organic matter and carbon content
    - Soil carbon concentration (g C per kg soil) and carbon stock (t C per ha)
    - Soil bulk density and stones/porosity calculations
    - Gravimetric moisture (MOISTURE) and moisture under oven-dry conditions (MOISTURE_DRY)
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils
    - Total nitrogen (N_PERCENT) and nitrogen stock (N_STOCK)
  - Derived measures:
    - LOI-based carbon concentration and carbon stock
    - LOI-derived soil carbon stocks per hectare
  - Laboratory QA:
    - pH batches include internal standards and duplicates; acceptance window within ±2 SD of batch mean
    - LOI QC with internal standards and calcite checks; rejection if standards deviate >2 SD
    - Olsen-P QC with duplications and blanks every 25 samples
    - Nitrogen analyses with in-house reference materials and calibration checks using acetanilide
  - Data quality assurance: robust QA workflow developed by UKCEH lab staff and data scientists using R scripts and guidance documents

- Data structure and metadata
  - Dataset characteristics: 18 columns and 597 rows; missing samples coded as -9999
  - Core fields include:
    - SQUARE: 1-km survey square ID
    - PLOT: soil sampling location within square
    - YEAR: year of sampling
    - PH, LOI, C_CONC_LOI, C_STOCK_LOI
    - SOIL_GROUP (carbon/LOI-based grouping)
    - BULK_DENSITY, MOISTURE, MOISTURE_DRY
    - N_PERCENT, N_STOCK
    - PO4_OLSEN
    - LC07, LC07_NUM (ITE Land Classification)
    - COUNTRY (ENG, SCO, WAL)
    - EZ_DESC_07 (Environmental Zone description)
  - Environmental framing:
    - ITE Land Classification (LC07) and Land Classification 2007 for stratification
    - Countryside Survey Environmental Zones (EZ_DESC_07) derived from multivariate environmental data
  - Data storage and access:
    - Samples and associated data stored in UKCEH laboratory systems and the UKCEH Soil Bank
    - Documentation and metadata accompany the dataset to support reuse and interpretation

- Data governance, openness and challenges
  - Emphasizes data quality assurance and standardized processing to support trustworthy, policy-relevant insights.
  - Data management procedures are designed to support transparency while ensuring data integrity and traceability from field collection to analysis.
  - The report references extensive methodological documentation and prior Countryside Survey outputs to enable cross-year comparability.
  - Potential broader data-access considerations include sharing underlying datasets and ensuring metadata completeness to facilitate verification and reuse.

- Implications for policy, monitoring and future decisions
  - The rolling design and standardized soil metrics enable detection of temporal changes and interactions between vegetation, land use, and soil properties across GB.
  - Metrics support assessment of soil carbon dynamics (LOI-derived carbon stocks), nutrient status (N and Olsen P), acidity (pH), moisture regime, bulk density, and carbon/nitrogen balance.
  - Spatial stratification by land class and environmental zones allows policy-relevant reporting at national and sub-national scales.
  - The structured data framework (Table 5 schema) provides a reproducible basis for trend analysis, benchmarking, and integration with other environmental indicators.

- References and contact
  - Extensive references and further reading are included within the document.
  - For inquiries: enquiries@ceh.ac.uk; UKCEH contact points across Bangor, Edinburgh, Lancaster, and Wallingford.