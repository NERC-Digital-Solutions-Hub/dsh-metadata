# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

## Overview and purpose
- Long-running national study of the UK countryside (since 1978) with a rolling 5-year monitoring programme since 2019.
- Aims to track changes in topsoil condition and function, respond to multiple pressures, and provide data/maps of stock and change in GB soils.
- Focuses on soil and vegetation change with data intended for national and sub-national indicators; supported by NERC under UK-SCAPE.

## Data governance, scope, and programme design
- Rolling survey: 500 x 1-km squares per cycle (5-year cycle), with 100 squares visited annually.
- Stratified by Land Classification (ITE LC07) to capture environmental gradients; excludes squares that are >75% urban or >90% sea.
- Environmental Zones defined by aggregation of ITE Land Classes; zones describe broad environmental context for analysis.
- 2020 Covid disruption caused partial year work; 50 England-only squares reselected to maintain coverage.
- Data are intended to support comparisons across years (e.g., 2019+).

## Sampling and data collection methods
- In each 1-km square, five topsoil sampling locations (X-Plots) within vegetation plots.
- Topsoil (0–15 cm) sampled with a 15 cm core at co-located vegetation survey points.
- Historical plot relocation documented to ensure repeatability (maps, markers, GPS).
- Soil cores refrigerated and shipped to UKCEH laboratories (Bangor) for processing and storage in the UKCEH Soil Bank.

## Metrics, laboratory protocols, and analytical methods
- Field metadata and sampling framework:
  - SQUARE (1-km square ID), PLOT (soil sampling location), YEAR (sampling year).
  - LC07 and LC07_NUM: Land Classification used for stratification (ITE 2007).
  - COUNTRY and EZ_DESC_07: Geographic and Environmental Zone descriptors.
- Key measured and derived soil metrics (0–15 cm FE = fine earth):
  - pH in deionized water (PH).
  - Loss-on-Ignition (LOI) for soil organic matter and carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI).
  - Soil carbon groups based on LOI (SOIL_GROUP).
  - Bulk density (BULK_DENSITY), moisture content (MOISTURE, MOISTURE_DRY).
  - Olsen-P (PO4_OLSEN) for arable/improved grassland soils.
  - Total nitrogen (N_PERCENT) and N stock (N_STOCK).
- Derived calculations:
  - Soil core volume and FE volume accounting for stones.
  - Conversions to carbon stock and nitrogen stock per hectare using standard depth and area factors.
- Quality control specifics:
  - pH: internal standards and duplicates (target within ±2 SD).
  - LOI: internal standards, calcite checks, batch duplication checks.
  - Olsen-P: blanks, duplicates, calibration with moisture correction.
  - Total nitrogen: UKAS-like standard checks, instrument calibration with acetanilide standard.
- Lab and QA reference materials, replication strategies, and documentation linkages are maintained to ensure comparability over time.

## Data quality assurance and workflow
- Transition to rolling surveys necessitated robust QA/QA procedures.
- Data workflow implemented by UKCEH lab staff and data scientists using R scripts and guidance documents.
- Ongoing data quality assurance to maintain high standards across continuous data collection and processing.

## Data structure and metadata
- Dataset characteristics for Topsoil data 2022:
  - 18 columns and 465 rows.
  - Missing values denoted by -9999.
- Key columns (summary):
  - SQUARE (text): 1-km square identifier.
  - PLOT (number): soil sampling location within square.
  - YEAR (number): sampling year.
  - PH (number): soil pH in field-moist bulk soil.
  - LOI (number): LOI (% or g per 100 g) and related carbon metrics (C_CONC_LOI in g C per kg soil; C_STOCK_LOI in t C per ha).
  - SOIL_GROUP (category): LOI-based carbon grouping.
  - BULK_DENSITY (number): dry bulk density of fine earth.
  - MOISTURE, MOISTURE_DRY (numbers): gravimetric water content (wet and oven-dry basis).
  - N_PERCENT (number): total soil nitrogen percentage.
  - N_STOCK (derived number): total soil nitrogen stock per ha.
  - PO4_OLSEN (number): Olsen phosphorus (arable/improved grassland only).
  - LC07, LC07_NUM (text/number): ITE Land Classification.
  - COUNTRY (category): GB country.
  - EZ_DESC_07 (category): Countryside Survey Environmental Zone description.
- Data provenance and structure documented to support discoverability and re-use.

## Data sharing, storage, and discoverability
- Data stored in the UKCEH Soil Bank and associated data management systems.
- Metadata and QA processes support data discoverability, traceability, and reproducibility for end-users and auditors.
- Contact and access pathways provided (enquiries@ceh.ac.uk; CEH information channels; Soil Bank catalogUE links referenced in the report).

## Practical considerations for Data Stewards
- Alignment with user needs: dataset design supports national/sub-national soil indicators and trend analysis; metadata supports usability and interoperability.
- Standards and interoperability: consistent use of Land Classification (LC07), Environmental Zones, and standardized QA procedures across years.
- Update and governance: rolling program requires ongoing data QA, documentation, and delta-updates to reflect new squares, relocated plots, and methodological refinements.
- Challenges to anticipate:
  - Incomplete understanding of user priorities for long-term soil indicators.
  - Timely data acquisition from field teams and standardization across diverse systems.
  - Handling large, multi-year, multi-system datasets with varying formats.
  - Maintaining compatibility with legacy datasets and ensuring smooth data updates and embargo handling where applicable.

## References and further reading (highlights)
- Soils Manual and prior Countryside Survey methodologies.
- Land Classification and Environmental Zone framework documentation.
- QA and data-management workflows and related CEH/NERC publications.
- Data availability and contact points for access requests.