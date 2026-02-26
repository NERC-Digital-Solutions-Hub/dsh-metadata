# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

## Purpose and scope
- UK Countryside Survey (CS) provides a national audit of UK countryside soil resources, enabling monitoring of changes since 1978 with a rolling program since 2019.
- Focus of this dataset: topsoil (0-15 cm) physico-chemical metrics across GB, supporting understanding of soil condition, carbon dynamics, and responses to multiple pressures.
- Rolling program: 5-year survey cycle, sampling 500 1-km squares per cycle (100 squares surveyed annually) to robustly estimate national and sub-national indicators.
- Key questions addressed: how multiple pressures affect topsoil condition and function; changes in soil carbon pools, carbon-to-nitrogen ratios, pH trends, compaction, phosphorus, and feedbacks with vegetation.

## Study design and rolling program
- Monitoring uses an ecosystem-based, multi-metric approach with data collected across scales in a single visit where possible.
- 2019 marked the start of the rolling program; cycle length is five years, with re-sampling to capture change over time and to buffer against climate variability.
- Sample selection: 500 1-km squares within Land Classification strata; 100 squares visited each year.
- Exclusions: urban (>75%) or sea-dominated (>90%) squares excluded.

## Covid disruption (2020)
- Survey disrupted in 2020; partial year activity (May–June) and resumed later in the year (July–August).
- Re-selection resulted in 50 England-only squares being added to the sample.

## Sample collection methods
- Within each square, five topsoil samples are taken from pre-determined locations that align with vegetation X-Plots.
- Soil cores: 15 cm length, collected at co-located vegetation survey points.
- Historical sampling locations are preserved when possible; plots relocated using maps, photos, and GPS to ensure consistency.
- Samples are refrigerated, stored, and sent to UKCEH laboratories for processing and storage in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Field methods follow the Soils Manual; five cores per square sent to UKCEH labs; soils stored in the Soil Bank.
- Data structure and metrics differentiate between bulk soil and fine earth (FE) fractions; volumes and densities are calculated with explicit formulas.
- Key measured metrics (topsoil 0-15 cm):
  - pH in deionized water (PH)
  - Loss on Ignition (LOI) and derived soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Soil carbon groups (SOIL_GROUP) based on LOI
  - Bulk density (BULK_DENSITY)
  - Gravimetric moisture content (MOISTURE) and moisture in oven-dry soil (MOISTURE_DRY)
  - Olsen-P (PO4_OLSEN) for arable/improved grassland soils
  - Total soil nitrogen (N_PERCENT) and nitrogen stock (N_STOCK)

## Data quality assurance
- Implementation of QA workflow with R-based data processing and guidance documents to maintain high data standards.
- Laboratory QA includes internal standards, duplicates, blanks, and calibration checks (especially for pH, LOI, Olsen-P, and N analyses).
- QA controls aim to ensure consistency across large-scale, rolling field surveys and to maintain data reliability for national indicators.

## Data structure and metadata
- Dataset characteristics: 18 columns, 465 rows (topsoil 2022).
- Typical fields and meanings:
  - SQUARE: 1-km survey square identifier
  - PLOT: soil sampling location within the square
  - YEAR: year of sampling
  - PH: soil pH in water
  - LOI: LOI (% and g per 100 g of oven-dry soil)
  - C_CONC_LOI: soil carbon concentration in FE (g C/kg soil)
  - C_STOCK_LOI: carbon stock in FE (t C/ha)
  - SOIL_GROUP: LOI-based carbon group
  - BULK_DENSITY: dry bulk density (g/cm^3) for FE
  - MOISTURE / MOISTURE_DRY: gravimetric water content (wet and dry weights)
  - N_PERCENT: total soil nitrogen (%)
  - N_STOCK: nitrogen stock (t N/ha)
  - PO4_OLSEN: Olsen-P (mg/kg) for applicable soils
  - LC07 / LC07_NUM: ITE Land Classification identifiers (GB-wide)
  - COUNTRY: GB country (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Missing data are coded as -9999.
- Supporting classifications: Land Classification (LC07) and Environmental Zones (EZ_DESC_07) link samples to environmental context for stratified analysis.

## Data provenance, access and usage
- Data collected under UKCEH Countryside Survey protocols with explicit documentation and references (Soils Manual and associated reports).
- Data curated through UKCEH QA processes; stored in the UKCEH Soil Bank.
- Contact and access: enquiries@ceh.ac.uk; CEH network and website for data discovery and documentation.
- Dataset supports national and sub-national assessments of soil carbon, nutrient status, pH shifts, moisture regime, density/porosity, and potential soil health trends within the rolling survey framework.