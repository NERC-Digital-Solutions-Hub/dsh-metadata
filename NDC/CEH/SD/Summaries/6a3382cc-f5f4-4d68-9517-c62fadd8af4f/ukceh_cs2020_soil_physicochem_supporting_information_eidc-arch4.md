# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

- Overview
  - UKCEH Countryside Survey topsoil physico-chemical data for 2020 (0–15 cm depth) as part of the rolling Countryside Survey program.
  - Aimed at tracking soil condition and change across Great Britain, enabling comparisons with past surveys and monitoring trends under multiple pressures.
  - Supports national-scale soil health understanding for food security, public health, and climate system insights.

- Data scope and structure
  - Dataset type: Topsoil metrics (0–15 cm) from 1-km x 1-km squares, collected at up to five sampling locations per square aligned with vegetation X-Plots.
  - Columns (18 total) include: SQUARE (1-km square ID), PLOT (plot number), YEAR, PH (soil pH in deionized water), LOI (loss-on-ignition; g LOI per 100 g soil or %), C_CONC_LOI (g C per kg soil), C_STOCK_LOI (t C per ha), SOIL_GROUP (LOI-based carbon group), BULK_DENSITY (g cm-3), MOISTURE (gravimetric water content), MOISTURE_DRY (g water per g oven-dry soil), N_PERCENT (N content), N_STOCK (t N per ha), PO4_OLSEN (mg/kg; Olsen phosphorus for arable/improved grassland), LC07 and LC07_NUM (ITE Land Classification 2007), COUNTRY, EZ_DESC_07 (Environmental Zone description).
  - Data quality flag: Missing values denoted by -9999.
  - Sample count: 194 rows in this dataset.

- Sampling design and rollout
  - Rolling survey: 500 squares sampled over a five-year cycle; 100 squares visited annually.
  - Stratification: Based on ITE Land Classification (LC07) across GB to ensure national and sub-national representativeness.
  - 2020 disruption: Covid-19 affected fieldwork; recruitment shifted with 50 squares sampled in England only in the latter part of the year.
  - Sampling depth and location: Topsoil cores collected from five fixed pre-defined points within each square, co-located with vegetation plots; cores are 15 cm long.

- Methods and analytical protocols
  - Field and lab workflow: Five soil cores per square sent to UKCEH labs; soils banked for processing.
  - Key measurements and methods:
    - pH: Soil pH in deionized water (field-moist bulk soil).
    - LOI: LOI by ThermoGravimetric Analyser (LECO TGA701) from 25°C to 1000°C with specified steps to estimate soil organic matter and derive C_CONC_LOI.
    - Carbon stocks: C_STOCK_LOI derived from LOI, soil depth, and bulk density parameters.
    - Bulk density: Calculated from core mass, core volume, and stone content.
    - Moisture: Gravimetric water content (MOISTURE and MOISTURE_DRY) from field-moist and oven-dried soil respectively.
    - Olsen phosphorus: Measured on arable/improved grassland soils via Olsen’s method and analyzed with a segmented flow analyzer.
    - Nitrogen: Total soil nitrogen (N_PERCENT) measured by elemental analyzer after ball milling and drying; N_STOCK computed per hectare.
  - Data processing: Processing and storage in UKCEH laboratories; QA QA workflow supported by R-based pipelines and guidance documents.

- Data quality assurance and governance
  - QA framework: Regular data QA/assurance with internal standards, duplicates, blanks, and batch-level checks for pH, LOI, Olsen-P, and nitrogen analyses.
  - Standards and calibration: Use of reference materials, duplicates (~10%), and instrument calibration checks (e.g., acetanilide standard) to ensure accuracy and traceability.
  - Provenance and reproducibility: Documented laboratory workflows and data workflows in R; data curated for QA and consistency before inclusion in the Soil Bank.

- Data structure and storage
  - Data model: Each row represents a soil sampling event within a square-year, with fields for square ID, plot, year, measured metrics, classifications, and zone descriptors.
  - Data format: 18 columns with units specified (e.g., LOI in g/100 g or %; C_CONC_LOI in g C/kg; N_STOCK in t N/ha; PO4_OLSEN in mg/kg).
  - Access and hosting: Processed data stored in UKCEH Soil Bank; associated materials and methodologies referenced in the Countryside Survey documentation and CEH data portals.

- Contextual classifications and environmental context
  - Land Classification: LC07 (2007) used for stratification and interpretation across environmental gradients (climate, relief, geology).
  - Environmental Zones: EZ_DESC_07 provides zone descriptions derived from analysis of environmental characteristics across squares, enabling cross-zone comparisons.

- Implications for data leaders
  - Data governance: Demonstrates a robust QA-driven workflow for a long-running national soil monitoring program, with clear metadata, classification schemes, and provenance.
  - Data interoperability: Uses standardized classifications (LC07, EZ_DESC_07) and consistent measurement protocols to enable integration with other Countryside Survey datasets (e.g., vegetation data) and across time.
  - Analytic potential: Enables analysis of soil carbon, nitrogen, phosphorus dynamics, pH trends, bulk density, moisture, and organic matter changes in relation to land use and environmental zones; suitable for trend analysis and policy-relevant reporting.
  - Data accessibility and stewardship: Clarifies data bank storage (Soil Bank) and QA processes, highlighting the importance of ongoing data quality, documentation, and version control for long-term datasets.

- References and further reading
  - Countryside Survey methodology and prior soil reports (e.g., 2007 soils report; Soils Manual; related CEH/NERC references) for context and methodological alignment.
  - UKCEH Environmental Zones and ITE Land Classification documentation for interpretation and cross-dataset analysis.