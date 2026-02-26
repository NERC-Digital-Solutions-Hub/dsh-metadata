# Topsoil physico-chemical data 2020

- Purpose and context
  - UK Countryside Survey uses a rolling monitoring program to assess soil condition and function across Great Britain, enabling comparison over time and understanding interactions of multiple pressures.
  - The 2020 dataset marks part of the rolling program (first cycle started in 2019) supported by NERC under UK-SCAPE; aims to quantify direction and magnitude of topsoil change and related soil properties, including carbon pools and nutrient status.

- Survey design and sampling framework
  - Rolling five-year cycle: 500 x 1-km squares sampled per cycle, with 100 squares visited annually.
  - Squares are stratified by Land Classification (ITE LC07) to capture environmental gradients; urban or marine-dominated squares are excluded.
  - Covid disruption in 2020: first-half fieldwork limited; 50 squares reselected from England; distribution map adjusted for confidentiality.
  - Within each square: up to five sampling locations (PLOT) corresponding to vegetation X-Plots; topsoil (0–15 cm) cores collected from five randomly dispersed points.
  - Relocation controls introduced (maps, markers, GPS) to ensure accurate plot re-sampling over time.

- Sample collection and handling
  - Topsoil cores (15 cm long, black plastic core) collected at five locations per square, co-located with vegetation sampling.
  - Samples refrigerated, shipped within days to UKCEH laboratories, stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analytical methods
  - Core measurements and derived metrics
    - pH (in deionised water) measured on field-moist bulk soil.
    - LOI (loss on ignition) by Thermogravimetric Analysis (TGA701) to estimate soil organic matter and carbon content.
    - C_CONC_LOI (g C per kg soil) and C_STOCK_LOI (t C per ha) derived from LOI and soil mass/density.
    - N_PERCENT (total soil nitrogen) and N_STOCK (t N per ha) via standard combustion analysis (Elementar VarioEL).
    - PO4_OLSEN (Olsen phosphorus) measured on arable/improved grassland soils using Olsen’s method and colorimetric detection.
    - BULK_DENSITY, MOISTURE, MOISTURE_DRY (gravimetric water contents) and stone content for volume corrections.
  - Land classification and zone context
    - LC07 (ITE Land Classification 2007) used for stratification; LC07_NUM numerical codes accompany LC07.
    - EZ_DESC_07 (Environmental Zones) derived from multivariate analysis of ITE Land Classes; zones reflect combinations of environmental characteristics.
  - Data quality control and QA practices
    - Internal standards and duplicates included in batches (pH QC, LOI QC with internal references).
    - Calibration checks and blanks used for Olsen-P and nitrogen measurements; standards (e.g., Acetanilide) used to monitor instrument performance; QA ensured at defined frequencies.
  - Data integration and storage
    - Processed and/or frozen samples stored in the UKCEH Soil Bank; data managed with workflow scripts (R-based) and guidance documents to ensure high data quality.

- Data structure and dataset details
  - Dataset characteristics
    - 18 columns and 194 rows (topsoil 2020 data subset); missing samples coded as -9999.
  - Key fields and meanings
    - SQUARE: 1-km survey square identifier (text)
    - PLOT: soil sampling location within square (numeric)
    - YEAR: year of sampling (numeric)
    - PH: soil pH in water (numeric)
    - LOI: soil organic matter via LOI (% and g per 100 g)
    - C_CONC_LOI: soil carbon concentration (g C per kg soil)
    - C_STOCK_LOI: soil carbon stock (t C per ha)
    - N_PERCENT: total soil nitrogen (%)
    - N_STOCK: total soil nitrogen stock (t N per ha)
    - PO4_OLSEN: Olsen phosphorus (mg kg-1)
    - BULK_DENSITY: bulk density (g cm-3)
    - MOISTURE / MOISTURE_DRY: gravimetric water content (field moist and oven dry)
    - LC07 / LC07_NUM: ITE Land Classification (text and numeric)
    - COUNTRY: country location
    - EZ_DESC_07: Environmental Zone description
    - SOIL_GROUP: carbon group category based on LOI
  - Notes
    - Data are aligned to long-standing Countryside Survey conventions and LAB methods; units and conversions are specified (e.g., 0.15 m core depth, ha = 10,000 m2).

- Environmental interpretation and application
  - Environmental Zones (EZ) and Land Classification (LC07) enable stratified analysis of soil condition by environmental context and landscape position.
  - LOI-based soil carbon groups (SOIL_GROUP) allow assessment of carbon stock distribution across soils with different organic matter contents.
  - The dataset supports analyses of soil carbon pool dynamics, nutrient status (N, P), pH trends, soil texture-related density and porosity implications, and potential correlations with vegetation changes and land use.

- Practical implications for analysts
  - Standardised, QA‑driven data collection enables robust temporal comparisons (2019+ rolling program vs prior surveys).
  - Rolling design increases spatial coverage and resilience to annual climate variability, improving detection of change signals.
  - Data pipelines (QA workflows, R scripts) support ongoing quality assurance, data cleaning, and integration with other environmental datasets.
  - The accessibility goal is reinforced by clear data structure and metadata, enabling broader reuse and facilitating cross-project data fusion while maintaining traceability to sample locations and years.

- References and further reading
  - Full references and methodological sources are listed in the document, including Countryside Survey reports, soils manuals, land classification frameworks, and QA QC standards.