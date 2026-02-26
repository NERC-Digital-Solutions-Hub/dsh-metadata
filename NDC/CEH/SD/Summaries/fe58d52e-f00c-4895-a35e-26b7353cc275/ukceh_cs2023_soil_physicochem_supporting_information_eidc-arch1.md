# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

- The Countryside Survey is a long-running national audit of UK soils and natural resources, conducted since 1978 and transitioning to a rolling program in 2019 to monitor soil condition and function over time.
- Focuses on topsoil (0–15 cm) condition and co-located vegetation, with five soil samples per 1-km square collected alongside vegetation plots.
- Aims to quantify direction and magnitude of soil change and how multiple pressures interact, including soil carbon stocks, pH, nutrient status, and physical properties.

## Study design and rolling program

- Rolling survey adopted: repeats every five years or after 500 squares completed; 100 squares visited annually.
- Sampling frame: 500 x 1-km2 squares randomly sampled within Land Classification (LC07) strata to represent national and sub-national scales.
- Exclusions: squares with >75% urban land or >90% sea excluded.
- Covid-19 disruption in 2020 led to partial year work and reallocation of 50 English squares.

## Sample collection methods

- In each 1-km square, up to five sampling locations (PLOTs) are selected, with soil cores collected from 0–15 cm at co-located vegetation X-Plots.
- Historical relocation markers established since 1978; plots re-located using maps, photos, and GPS data to ensure accuracy.
- Samples are refrigerated, shipped to UKCEH laboratories, and stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods

- Core measurements and derived metrics are collected for each square/plot/year, including:
  - pH in deionised water (PH)
  - Loss-on-Ignition (LOI) and derived soil carbon content (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Soil organic matter (LOI) and related carbon stocks per hectare
  - Bulk density (BULK_DENSITY)
  - Gravimetric and volumetric moisture (MOISTURE, MOISTURE_DRY)
  - Total nitrogen (N_PERCENT) and nitrogen stock (N_STOCK)
  - Olsen phosphorus for arable/improved grassland (PO4_OLSEN)
  - Land Classification (LC07) and country (COUNTRY)
  - Environmental Zone description (EZ_DESC_07)
  - Soil carbon group (SOIL_GROUP) based on LOI
- Lab methods and quality control:
  - LOI measured with ThermoGravimetric Analyser (LECO TGA701) across defined heating steps
  - LOI% converted to soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI) with specified conversions
  - pH measured on field-moist bulk soil in deionised water; internal standards and duplications used for QA
  - Olsen-P measured via molybdate blue colorimetric method; QA includes duplicates and blanks
  - Total N measured with Elementar VarioEL after ball milling; QA includes in-house standards and calibration checks
- QA practices:
  - Regular QA workflow with R-based data processing scripts
  - Internal standards, duplicates, blanks, and calibration checks used to ensure data quality
  - Data and metadata documented to support traceability and reproducibility

## Data structure and dataset details

- Dataset contains 18 columns and 597 rows; missing samples denoted by -9999.
- Key columns:
  - SQUARE: 1-km survey square identifier
  - PLOT: plot number for soil sampling locations
  - YEAR: year of sampling
  - PH: soil pH (water)
  - LOI: soil organic matter content (g LOI per 100 g dry soil)
  - C_CONC_LOI: soil carbon concentration (g C per kg dry soil)
  - C_STOCK_LOI: carbon stock (t C per ha)
  - SOIL_GROUP: LOI-based soil carbon group
  - BULK_DENSITY: bulk density (g soil per cm3)
  - MOISTURE / MOISTURE_DRY: moisture contents (gravimetric and dry-weight bases)
  - N_PERCENT / N_STOCK: total soil nitrogen concentration and stock
  - PO4_OLSEN: Olsen phosphorus concentration (arable/improved grassland only)
  - LC07 / LC07_NUM: ITE Land Classification (GB 2007)
  - COUNTRY: GB country (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data are organized to support multi-scale analysis, including cross-walks to vegetation data and environmental classifications.

## Covid disruption and temporal context

- 2020 Covid-19 disrupted fieldwork; some squares were relocated or reselected, with additional England-only sampling to mitigate gaps.
- First rolling cycle began in 2019, enabling year-to-year monitoring and cross-year comparisons across GB.

## References and metadata provenance

- Data and methodology are anchored in UKCEH Countryside Survey documentation, including the Soils Manual and related technical reports.
- Notable sources include descriptions of the LC07 land classification, Environmental Zones, and prior Countryside Survey soil change findings.