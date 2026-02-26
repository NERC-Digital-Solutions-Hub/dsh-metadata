# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

## Overview
- Describes background, design, sampling, analytical methods, QA, and data structure for topsoil physico-chemical data collected in 2023 as part of the UKCEH Countryside Survey (CS).
- CS is a long-running national audit of the UK countryside (since 1978) with a rolling program since 2019 to monitor soil health, carbon, nutrients and responses to multiple pressures.
- Aims include understanding direction and magnitude of soil change, interactions of pressures, and implications for soil function and ecosystem services.
- The 2019 rolling program involves a five-year cycle with 500 1-km2 squares, of which 100 are visited annually, stratified by Land Classification; urban/sea exclusions apply.
- Data are prepared for QA, stored in the UKCEH Soil Bank, and designed for integration with vegetation data and wider datasets.

## Survey Design and Rolling Program
- Rolling survey: repeats every five years or after 500 squares completed; captures change over the interval and buffers against extreme years.
- Sampling frame: 1-km x 1-km squares across Great Britain; 500 squares selected within strata defined by Land Classification (LC07) with 100 squares visited per year.
- Historical continuity: 1978, 1998, and 2007 squares are included; some resampling and relocation practices exist for older plots.
- Covid disruption (2020): restrictions caused partial year; 50 squares were reselected from England to complete the year's sampling.
- Exclusions: squares with >75% urban land or >90% sea are excluded from selection.

## Sample Collection and Location
- Within each square, five sampling points (locations) are selected, co-located with vegetation X-Plots, using a 15 cm deep soil core (0–15 cm) per location.
- Sampling framework evolved from 1978 (center of 2x2 m plots) to modern routines with relocation checks, photos, maps, and GPS data to ensure accurate re-sampling.
- After collection, topsoil cores are refrigerated and shipped to UKCEH laboratories or stored in the UKCEH Soil Bank.

## Metrics, Laboratory Protocols and Analytical Methods
- Core metrics (for FE = fine earth or bulk soil as applicable):
  - pH (in deionised water) with internal standards and duplicates for QA.
  - Loss-on-Ignition (LOI) by ThermoGravimetric Analyser to derive soil organic matter and carbon content; LOI is converted to C concentration and stock using defined equations.
  - Soil bulk density (dry) and stone content to determine porosity and to convert %C to C stocks per area.
  - Moisture content: gravimetric water content (both per dry weight and per wet weight).
  - Olsen-P for arable/improved grassland only, measured colorimetrically after extraction.
  - Total nitrogen (N) via elemental analysis (oxidative combustion, thermal conductivity detection); stocks calculated per hectare.
- Lab methods and QA:
  - LOI measured with a defined heating schedule; internal LOI standards and calcite checks; QC thresholds (≤2 standard deviations) applied.
  - pH measured with internal standards; QC with duplicates and consistency checks.
  - Olsen-P with calibration curves and blanks; QC includes duplicates and blanks every ~25 samples.
  - Total N measured with UKAS-accredited SOP; calibration checks with standard materials; routine QA with in-house references.
- Data interpretation:
  - LOI used to classify soils into UKCEH-Countryside Survey carbon groups (Soil_GROUP) and to derive carbon stocks (C_STOCK_LOI).
  - Derived units and conversions specified (e.g., C stocks per hectare, field vs fine-earth fractions, area of 1 ha, etc.).
- Laboratory and QA governance emphasize traceability, standardization, and reproducibility across rolling survey cycles.

## Data Quality Assurance
- A formal QA workflow was developed by UKCEH laboratory staff and data scientists using R scripts and guidance documents.
- QA covers data collection, processing, and metadata alignment to ensure high data standards across rolling surveys.
- QC procedures are embedded within each metric (pH, LOI, Olsen-P, N, etc.) with internal standards, duplicates, blanks, and calibration checks.

## Data Structure and Accessibility
- Dataset characteristics:
  - Table consists of 18 columns and 597 rows (as of 2023); missing values denoted by -9999.
  - Core fields include:
    - SQUARE: 1-km survey square identifier (text)
    - PLOT: soil sampling location within square (numeric)
    - YEAR: survey year (numeric)
    - PH: soil pH (numeric)
    - LOI: soil organic matter content (g LOI per 100 g of oven-dry soil; percentage) 
    - C_CONC_LOI: soil carbon concentration (g C per kg soil)
    - C_STOCK_LOI: carbon stock (t C per ha)
    - SOIL_GROUP: LOI-based soil carbon category
    - BULK_DENSITY: soil bulk density (g/cm3)
    - MOISTURE, MOISTURE_DRY: gravimetric water content (various definitions)
    - N_PERCENT, N_STOCK: total soil nitrogen content and stock
    - PO4_OLSEN: Olsen phosphorus (arable/improved land)
    - LC07, LC07_NUM: ITE Land Classification (numerical and textual)
    - COUNTRY: GB country (ENG, SCO, WAL)
    - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data provenance and access:
  - Data are linked to the UKCEH Soil Bank and Countryside Survey repositories.
  - References and methodological documents are listed for methodological transparency.
  - Contact points for inquiries and further access are provided (enquiries@ceh.ac.uk; UKCEH websites).

## Practical Implications for Data Leaders
- The report documents a robust, QA-driven, rolling national soil data program with clearly defined sampling design, measurement protocols, and metadata standards suitable for long-term trend analysis and cross-cycle comparability.
- It demonstrates rigorous data governance, including standardized lab methods, QC protocols, and detailed data field definitions, enabling reproducibility and cross-study integration.
- The dataset supports policy-relevant inquiries into soil carbon dynamics, nutrient status, soil health indicators, and the influence of land class and environmental zones on topsoil properties.
- The data structure and documentation facilitate discoverability, data integration with vegetation and environmental datasets, and future updates within the rolling survey framework.