# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

- Overview and purpose
  - UKCEH Countryside Survey tracks long-term soil condition and function across Britain using a rolling program starting in 2019.
  - Aims to quantify direction and magnitude of soil change and interactions with multiple pressures, supporting policy and understanding of soil health.
  - This dataset reports topsoil (0-15 cm) physicochemical properties from the 2021 winter survey, with data preparation, QA, and derived metrics for map-ready use.

- Survey design and rolling program
  - Rolling survey cycle: repeats every five years or after 500 squares completed; 100 squares surveyed per year.
  - Sampling units: 1-km x 1-km squares, selected to provide national/sub-national indicator estimates; exclusion of squares with >75% urban land or >90% sea.
  - Land classification and environmental context: stratified by ITE Land Class (2007) to enable regional comparisons; environmental zones (EZ) derived from multivariate analysis of Land Classes.
  - Covid-19 disruption (2020): partial year; surveyors operated only in late 2020, with England-only resampling of 50 squares.
  - Winter survey square selection (2021): hierarchical selection prioritizing 1978/1998/2007 survey squares; subset of 30 (+5 reserve) squares repeated in winter 2021 to reflect environmental zones.

- Sampling methods and field procedures
  - Per square: up to five sampling locations (PLOTs) within randomly dispersed X-Plots; topsoil cores collected from 0-15 cm using a 15 cm long core at five locations per square.
  - Plot relocation and mapping: historical markers used (since 1990); locations re-located using graphical aids; for 2019 plots moved to a specific inner plot corner.
  - Sample handling: cores refrigerated and shipped to UKCEH laboratories for processing; soils stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols, and analytical methods
  - General framework: field methods described in the Soils Manual; five cores per square analyzed for multiple metrics; samples banked after analysis.
  - Key measured and derived soil metrics
    - pH (PH): measured in deionised water on field-moist bulk soil; QA includes internal pH standards and duplicates.
    - Loss-on-Ignition (LOI) and soil carbon
      - LOI measured by ThermoGravimetric Analysis (LECO TGA701) from 105°C to 375°C; LOI expressed as g LOI per 100 g soil and %.
      - Derived soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI) calculated from LOI and soil parameters.
    - Soil carbon stocks
      - C_STOCK_LOI computed using core volume, bulk density, and LOI-derived carbon concentration.
    - Bulk density and porosity
      - BULK_DENSITY (dry bulk density) derived from core mass, core volume, and stone content; used to convert %C to C per unit volume.
      - Stones and porosity inferred from stone mass and core volume.
    - Moisture
      - MOISTURE_DRY: gravimetric water content (g water per g oven-dry soil); MOISTURE: gravimetric water content per wet weight.
    - Total nitrogen
      - N_PERCENT and N_STOCK derived from elemental analysis (Vario EL) on ball-milled samples; nitrogen stocks calculated similarly to carbon stocks.
    - Olsen phosphorus
      - PO4_OLSEN not measured in the 2021 winter survey (noted for completeness and cross-dataset compatibility).
  - Data structure for lab and derived calculations
    - Derived metrics are produced via dedicated R scripts to ensure reproducibility: calculate_soil_derived_metrics_function.R and Derive_soil_data.R.
  - Quality control
    - Lab QA pipeline flags unexpected values and trends; automated QA reports (QA2) compare to prior data and identify outliers; changes documented for auditability.

- Data quality assurance and workflow
  - Multi-stage QA process
    - Lab data QA: labs QA raw data and flag issues; stability of measurement standards checked.
    - Analyst QA1: cross-check lab data with lab records; document queries and changes.
    - Derivation stage: compute derived metrics via standardized scripts; join with vegetation data for integrated QA.
    - Analyst QA2: automated HTML QA reports highlighting patterns, relationships, and consistency with historical data.
  - Transparent audit trail: all data modifications linked to QA steps; full data lineage preserved.

- Data structure and accessibility
  - Dataset characteristics
    - 18 columns and 576 rows; missing samples indicated by -9999.
    - Year: 2022 (survey year in metadata); dataset represents 2021 winter survey results.
  - Core fields (selected)
    - SQUARE (1-km grid identifier), PLOT (sampling location within square), YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, SOIL_GROUP (LOI-based carbon groups), BULK_DENSITY, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN (not measured in 2021 winter), LC07, LC07_NUM (ITE Land Classification 2007), COUNTRY, EZ_DESC_07 (Environmental Zone description).
  - Data structure details
    - LC07/LAND CLASS used for stratification; environmental zones (EZ_DESC_07) derived from environmental analyses.
    - LOI-based soil carbon groupings (SOIL_GROUP) reflect carbon content categories used across Countryside Survey datasets.
  - Depth and mapping scope
    - Topsoil focus: 0-15 cm across up to five sampling points per 1-km square; results map to 1-km grid across Great Britain (England, Scotland, Wales).

- Practical implications for GIS and map-based products
  - Enables creation of national and sub-national maps of topsoil properties (pH, carbon stock, LOI-based carbon groups, bulk density, moisture, nitrogen) across GB.
  - Supports visualization by environmental zones and land classifications to analyze spatial patterns and drivers of soil change.
  - Provides a framework for comparing 2021 winter results with previous survey cycles (rolling program) to detect trends and interactions among pressures.
  - The dataset is designed for integration with vegetation data and other Countryside Survey components to produce ecosystem- and soil-health-focused map products.

- Limitations and notes
  - Olsen phosphorus (PO4_OLSEN) not measured in the 2021 winter survey; included for compatibility but flagged as NA for this specific dataset.
  - Covid-related disruption affected 2020 data collection and square selection; winter 2021 sample may reflect subset selection strategies.
  - Data represent topsoil condition at time of survey and are subject to spatial and temporal variability; built for long-term trend analysis via rolling surveys.

- References and further reading
  - See the Countryside Survey and Soils Manual documentation, along with methodological papers and the UKCEH Soil Bank for additional data standards, QA processes, and data accessibility.