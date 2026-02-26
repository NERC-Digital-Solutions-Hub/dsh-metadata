# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

- Purpose and scope
  - Presents QA metadata and analyses for 2020 topsoil (0–15 cm) physico-chemical data from the UK Countryside Survey (CS), part of a rolling, national soil monitoring program.
  - Context: CS monitors soil condition and function across GB to detect changes over time and under multiple pressures; supports policy-relevant insights for soil health, carbon, nutrients, and soil-vegetation interactions.
  - Rolling program began in 2019 to repeatedly sample 500 1-km squares per five-year cycle (100 squares annually) within stratified Land Classes.

- Study design and sampling framework
  - 1-km x 1-km squares selected within stratified Land Classification (ITE LC07) across GB; aims for national/sub-national indicators.
  - In 2020, Covid disruption shortened field windows; 50 squares were resampled from England only to maintain continuity.
  - Within each square: up to five sampling locations (PLOTS) co-located with vegetation X-Plots; five topsoil cores (0–15 cm) collected per square where possible.

- Sample collection and processing
  - Topsoil cores collected at five randomly dispersed locations per square using a 15 cm long core (co-incident with vegetation plots); cores refrigerated and shipped to UKCEH laboratories.
  - Plot relocation accuracy checked via maps, photos, GPS; 2019 plotting moved to western corner of inner plots for relocation accuracy.

- Metrics, laboratory protocols and analytical methods
  - Core suite per sampling location processed and stored in UKCEH Soil Bank; soils analyzed at UKCEH laboratories.
  - Key soil metrics measured (for fine earth or bulk soil where applicable):
    - pH in deionised water (PH)
    - Loss on ignition (LOI) and derived soil carbon (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
    - Total nitrogen (N_PERCENT) and N stock (N_STOCK)
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland only
    - Bulk density (BULK_DENSITY)
    - Gravimetric water content (MOISTURE, MOISTURE_DRY)
  - Derived calculations and conversions include soil core volume, carbon stocks per hectare, and conversion factors for LOI to organic matter and carbon.

- Quality control and assurance (QA)
  - Rigorous QA with internal standards and replicates:
    - pH measured with internal standards; acceptance within ±2 SD of batch mean.
    - LOI with internal standards and calcite blanks; batch-level QC implemented.
    - Olsen-P and N analyses include blanks, duplicates, and reference materials; instrument calibration checked with standards.
  - Laboratory workflows implemented in R-based data processing to ensure consistent QA across fields and samples.
  - Ongoing data QA supports the transition from intensive annual surveys to the rolling program.

- Data structure and metadata
  - The topsoil dataset (2020) comprises 18 columns and 194 rows; missing samples denoted by -9999.
  - Key fields:
    - SQUARE: 1-km survey square ID
    - PLOT: soil sampling location within square
    - YEAR: year of sampling
    - PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY
    - LOI (soil organic matter by LOI), C_CONC_LOI (g C/kg oven-dry soil), C_STOCK_LOI (t C/ha)
    - SOIL_GROUP: soil carbon grouping based on LOI
    - LC07: ITE Land Classification (2007)
    - COUNTRY: GB country
    - EZ_DESC_07: Countryside Survey Environmental Zone description
  - Dataset is linked to broader frameworks: Environmental Zones (EZ), Land Classification, and Soil Carbon Groupings used in CS.

- Environmental zones and soil carbon context
  - Environmental Zones (EZ_DESC_07) aggregate ITE Land Classes into zonal groupings to reflect multi-attribute environmental contexts.
  - SOIL_GROUP categories reflect LOI-based soil carbon classes (Mineral, Humus Mineral, Organo-mineral, Organic) for comparative carbon assessments.

- Data provenance and references
  - Aligns with CS methodological manuals and prior CS soils reports; includes links to Soil Manual (2007) and subsequent CS soil-focused literature.
  - Data and methods build on long-term soil monitoring from CS (1978–present) with harmonized QA and rolling sampling to enable trend detection.

- Practical relevance for data users
  - Provides a well-documented, QA-anchored 2020 topsoil data slice suitable for dashboards, trend analyses, and integration with vegetation and environmental zone data.
  - Facilitates cross-year comparisons (rolling program) of topsoil properties, carbon pools, nutrient status, and soil moisture/physical properties at national scale.
  - Supports exploration of how land use, climate, and management pressures relate to soil condition and carbon/nutrient stocks across GB.