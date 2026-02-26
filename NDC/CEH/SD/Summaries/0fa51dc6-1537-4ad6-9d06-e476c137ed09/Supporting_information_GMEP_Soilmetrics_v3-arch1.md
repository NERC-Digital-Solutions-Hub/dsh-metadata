# Glastir Monitoring & Evaluation Programme (GMEP) – Soil Monitoring Methods (2013-2016)

- Purpose and scope
  - Welsh Government program to monitor Glastir interventions’ effects on soil quality and to quantify status and trends related to soil, climate change, biodiversity, water quality, and woodland expansion.
  - Aims to identify drivers of change (land use, climate, pollution) beyond Glastir actions and to support evidence-based decision-making.
  - Uses a 4-year rolling survey cycle (2013–2016 for the first cycle) with an ecosystem-based approach and multi-scale data collection.

- Survey design and sampling framework
  - Two components: Wider Wales (baseline estimation and national trends) and Targeted (Glastir priority areas).
  - Common spatial unit: 1 km square; total of 300 squares sampled over the cycle.
  - 1km squares selected via the Countryside Survey methodology to enable future data integration.
  - Exclusion criteria: any square with >75% urban land or >90% sea excluded.
  - Sampling within each square: 5 pre-determined randomly dispersed locations for soil sampling; vegetation surveys conducted at sampling locations.
  - Soil cores: 15 cm long black C-core collected at each location; cores refrigerated and sent to labs within a few days.

- Laboratory analyses and soil metrics
  - Soil organic matter and carbon measurements
    - Loss-on-ignition (LOI) on 10 g sub-sample; LOI used to derive soil organic carbon concentration (C_FE_CARBO_CONC_GPERKG) via C_FE_LOI (%) × 5.5.
    - Total soil carbon (SOC) and total nitrogen (N) after inorganic carbon removal; measured with an Elementar Vario-EL analyser.
  - Nutrients and related metrics
    - Total phosphorus (P) by acid digestion and colorimetric measurement.
    - Olsen-phosphorus (Olsen-P) for arable/improved grassland habitats using 0.5 M NaHCO3 extraction and spectrophotometric detection.
  - Soil properties
    - pH in deionised water and in CaCl2, with quality control checks.
    - Electrical conductivity (EC) of soil slurry.
    - Bulk density of fine earth and volumetric water content derived from core measurements.
    - Soil water repellency (WDPT) measured on air-dried surface soils; median WDPT time derived from 6 drops per sample; video-recorded for accuracy.
  - Data logging
    - Data structured in GMEP_SOIL_METRICS_2013_16.csv with fields for square ID, plot type, year, measurements (CTOTAL, C_LOI, NTOTAL, PTOTAL, POLSEN, pH, EC, bulk density, VWC, SWR), and derived units.
  - Quality control
    - Internal soil standards used in each batch; repeated if LOI deviates by more than 2 standard deviations.
    - Two in-house reference materials per batch; duplicates and blanks included for P measurements; moisture-corrected and calibrated results.

- Data handling and provenance
  - Data collected, processed, and QA/QC’d by CEH (Centre for Ecology & Hydrology) and Bangor University staff; includes lab analysis, data management, and scripting for derived units.
  - Dataset designed to be compatible with legacy surveys for integration (e.g., Countryside Survey data) and to support future joint analyses.

- Outputs and implications for analysis
  - Enables national and sub-national indicators of soil quality and trends, linked to drivers of change and Glastir interventions.
  - Supports cross-survey integration and meta-analyses to assess policy impact on soil health, carbon stocks, nutrient status, and soil physical properties.
  - Highlights potential data challenges for analysts: gaps at local scales, data accessibility, standardization across sources, and the need for robust QA to ensure comparability.