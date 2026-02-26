# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC

- Purpose and scope
  - QA metadata and analysis report for the UKCEH Countryside Survey topsoil physico-chemical data for 2021.
  - Part of a broader Countryside Survey program that assesses soil condition and function to inform policy and management.

- Context and aims
  - Countryside Survey is a long-running national audit of the UK countryside, now operating as a rolling program since 2019 to detect change over time.
  - Aims include understanding how multiple pressures affect topsoil and vegetation, tracking soil carbon changes, pH shifts, potential compaction, nutrient changes, and feedbacks between vegetation and soil.
  - Data support policy-relevant questions about the direction and magnitude of soil change and interactions with environmental pressures.

- Survey design and rolling program
  - Rolling survey with a five-year cycle; 500 1-km squares sampled per cycle, with 100 squares visited annually.
  - Stratified sampling within Land Classification (ITE Land Classes) to ensure national and sub-national representativeness.
  - Exclusions: squares with >75% urban land or >90% sea excluded; Covid-19 disruption in 2020 led to resampling and adjustments (England-only subset).

- Sample collection methods
  - In each 1-km square, five sampling locations (PLOTs) chosen co-incident with vegetation surveys (X-Plots).
  - Topsoil core depth: approximately 0–15 cm, using a 15 cm long core, collected at five locations per square.
  - Relocation and mapping procedures refined across survey years (e.g., 1978 baseline plots, GPS/photos for accuracy in 2019–2021).
  - Cores refrigerated and shipped to UKCEH laboratories for processing; soil samples stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analytical methods
  - Core suite includes:
    - Soil pH in deionised water (PH)
    - Loss on ignition (LOI) and derived soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI)
    - Bulk density (BULK_DENSITY) and stone content to derive fine-earth porosity
    - Gravimetric moisture content (MOISTURE, MOISTURE_DRY)
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland areas
    - Total soil nitrogen (N_PERCENT, N_STOCK)
  - LOI methodology uses Thermogravimetric Analysis (TGA701) with four heating steps to estimate organic matter and convert LOI to soil carbon metrics.
  - Olsen-P measured via colorimetric/flow-injection techniques with quality controls.
  - Units and conversions provided (e.g., C_STOCK_LOI expressed in t C/ha; bulk density and volume calculations for soil core).
  - Quality control procedures include internal standards, duplicates, blanks, and calibration checks for each batch.

- Data quality assurance (QA)
  - Dedicated data workflow and QA processes developed by UKCEH laboratory staff and data scientists (R-based pipelines and guidance).
  - Regular QA checks across the rolling data collection to maintain high data standards and consistency with prior years.

- Data structure and metadata
  - The 2021 topsoil dataset comprises 18 columns and 496 rows; missing samples denoted by -9999.
  - Key fields include:
    - SQUARE: 1-km survey square identifier
    - PLOT: soil sampling location within square (X-Plot)
    - YEAR: year of soil sampling
    - PH: soil pH (water, field-moist bulk soil)
    - LOI, C_CONC_LOI, C_STOCK_LOI: LOI and derived carbon metrics
    - SOIL_GROUP: carbon grouping based on LOI
    - BULK_DENSITY: dry bulk density of fine earth
    - MOISTURE, MOISTURE_DRY: gravimetric water contents
    - N_PERCENT, N_STOCK: total soil nitrogen and stock
    - PO4_OLSEN: Olsen phosphorus (arable/improved land)
    - LC07, LC07_NUM: ITE Land Classification at 2007 basis
    - COUNTRY: GB country (England, Scotland, Wales)
    - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data governance, sharing and accessibility
  - Data are processed under a formal QA framework and stored in the UKCEH Soil Bank.
  - Data handling supports transparency and reproducibility, though access policies and data sharing considerations are noted as part of the overarching monitoring framework challenges (e.g., data sharing barriers discussed in the archetype).

- Implications for monitoring framework authors
  - Demonstrates a robust, policy-relevant monitoring framework with rolling design, stratification by environment, and multi-metric integration.
  - Highlights important data governance practices: standardized sampling, rigorous QA, transparent metadata, and clear data structures to enable comparability over time.
  - Shows practical responses to disruptions (e.g., Covid-19) to maintain continuity of long-term monitoring.
  - Emphasizes stakeholder- and data-driven decision-making through consistent reporting on soil health metrics and their relation to environmental pressures.
  - Addresses common challenges for monitoring frameworks: data gaps, access and sharing barriers, metadata adequacy, data transformation needs, and governance to ensure data are up-to-date and usable.