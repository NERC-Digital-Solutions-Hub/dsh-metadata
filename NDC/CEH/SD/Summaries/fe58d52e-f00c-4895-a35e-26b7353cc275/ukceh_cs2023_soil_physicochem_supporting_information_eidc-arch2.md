# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

## Overview and aim
- Presents background, methods, QA, and data structure for topsoil physico-chemical data (0–15 cm) collected under the Countryside Survey rolling programme.
- Primary purpose: monitor soil condition and function across Great Britain, detect changes over time, and understand interactions between multiple pressures to inform policy and soil health assessments.

## Monitoring design and rolling programme
- Rolling survey adopted in 2019: repeats on a five-year cycle or after 500 squares completed; aims to capture change cost-effectively and buffer against year-to-year climate variation.
- Sampling frame: 1-km × 1-km squares, with 500 squares across GB per cycle; 100 squares visited annually.
- Stratified sampling using Land Classification of Great Britain (LC07) to ensure robust national and sub-national indicators; excludes squares with >75% urban land or >90% sea.
- Covid disruption in 2020 led to partial fieldwork and re-selection; 50 English-only squares added to compensate.

## Sample collection and sites
- In each square, up to five sampling locations (PLOTs) co-located with vegetation X-Plots (5 core samples per square).
- Topsoil (0–15 cm) collected using 15 cm cores at predetermined locations; relocation accuracy checked with maps, photos, and GPS.
- Samples refrigerated and shipped to UKCEH laboratories; stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analysis
- Core soil metrics analyzed or derived from laboratory processing:
  - pH in deionised water (PH)
  - Loss-on-Ignition (LOI) for organic matter and carbon stock (C_CONC_LOI; C_STOCK_LOI)
  - Soil bulk density (BULK_DENSITY) and related stone content for fine earth volume
  - Moisture content: MOISTURE (gravimetric, wet weight basis) and MOISTURE_DRY (gravimetric, dry weight basis)
  - Olsen-phosphorus (PO4_OLSEN) for arable/improved grassland soils
  - Total nitrogen (N_PERCENT; N_STOCK)
- Derived calculations include carbon stock per hectare and conversions from LOI to carbon content.
- Lab frameworks reference established manuals and methods; LOI and other measures include internal QC checks using standards and blanks.

## Data quality assurance and controls
- Transition to rolling programme requires robust QA workflows; implemented with R-based data processing and guidance.
- QA measures include internal standards, duplicates, and batch-level checks for pH and LOI.
- LOI quality control uses internal standards and calcite as reference; pH QA uses standard checks within batches; Olsen-P QA includes blanks and duplicates every ~25 samples; nitrogen analysis uses instrument calibration with reference materials and standard compounds.
- Data processing emphasizes data provenance, traceability, and reproducibility; aims to ensure high-quality, comparable national dataset.

## Data structure and metadata
- Dataset for topsoil 2023 contains 18 columns and 597 rows; missing values denoted by -9999.
- Key fields include:
  - SQUARE (1-km square identifier)
  - PLOT (soil sampling location within square)
  - YEAR (sampling year)
  - PH (soil pH)
  - LOI (soil organic matter by LOI; g LOI per 100 g soil)
  - C_CONC_LOI (g C per kg oven-dry soil)
  - C_STOCK_LOI (t C per ha)
  - SOIL_GROUP (LOI-based soil carbon group)
  - BULK_DENSITY (g soil per cm3)
  - MOISTURE (gravimetric moisture)
  - MOISTURE_DRY (gravimetric moisture on oven-dry basis)
  - N_PERCENT (total soil nitrogen %)
  - N_STOCK (t N per ha)
  - PO4_OLSEN (mg/kg, Olsen-P)
  - LC07, LC07_NUM (ITE Land Classification)
  - COUNTRY (GB country)
  - EZ_DESC_07 (Countryside Survey Environmental Zone description)
- Data are organized to support national and sub-national analyses by land class and environmental zones.

## Environmental context and classifications
- Environmental Zones (EZ_DESC_07) aggregate ITE Land Classes into zones reflecting combined environmental characteristics, enabling multi-parameter analyses beyond single variables.
- LC07 land classifications underpin stratification and interpretation across GB landscapes.

## Outputs, usage and accessibility
- Data are intended to enable long-term monitoring of soil condition and carbon/nutrient dynamics, supporting comparisons with previous surveys and across habitats.
- Results and data are managed within the UKCEH Soil Bank, with contact information provided for access and inquiries.
- The report references extensive methods, background literature, and further reading to support transparent, reproducible use and interpretation.

## Relevance to analysts monitoring the environment
- Demonstrates standardized data collection, QA, and metadata practices essential for consistent environmental monitoring.
- Provides a structured, multi-metric dataset suitable for tracking soil condition, carbon stocks, nutrient status, and their responses to multiple pressures over time.
- Emphasizes the importance of combining datasets (e.g., soil metrics with vegetation or deposition data) and ensuring data accessibility for broader analyses and policy evaluation.