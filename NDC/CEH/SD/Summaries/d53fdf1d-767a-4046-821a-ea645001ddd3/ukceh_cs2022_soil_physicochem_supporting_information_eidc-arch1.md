# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC

## Overview and purpose
- Benchmark and monitor soil condition and function across the UK countryside using a rolling, long-term survey (since 2019) supported by NERC UK-SCAPE.
- Aims include assessing how multiple pressures interact to affect topsoil condition, carbon, nitrogen, pH, and nutrient availability; producing data and maps for national and sub-national change at GB scale.
- Focuses on topsoil (0–15 cm) and co-located vegetation assessments to understand ecosystem change and inform policy and management.

## Design and rolling program
- Rolling survey: 500 x 1-km2 squares sampled over a five-year cycle; 100 squares visited per year.
- Squares selected within strata defined by Land Classification (ITE LC07) to robustly estimate indicators nationally and regionally.
- Exclusions: squares with >75% urban land or >90% sea.
- Covid disruption (2020): restricted field work in May–June; 50 squares reselected from England only for the year.

## Sample collection methods
- In each 1-km square, up to five topsoil locations are sampled using five randomly dispersed points within the square’s X-Plots.
- Soil cores: 15 cm long, collected at 0–15 cm depth, co-located with vegetation surveys.
- Post-collection: cores refrigerated, shipped to UKCEH laboratories, and stored in the UKCEH Soil Bank.
- Relocation accuracy is checked via field maps, photos, and GPS data; plots re-located where feasible.

## Metrics, laboratory protocols and analytical methods

### 4.1 Soil sampling locations and general information
- Data organized by SQUARE (1-km square ID), PLOT (soil sampling location within square), COUNTRY (ENG/SCO/WAL), and YEAR.

### 4.2 Land Class
- LC07: ITE Land Classification (2007) used for stratification; supports interpretation across 45 vegetation classes within land classes.
- numeric LC07_NUM provides the code; descriptions reflect major environmental gradients.

### 4.3 Countryside Survey Environmental Zones
- EZ descriptions group ITE Land Classes into zones (e.g., Easterly/Westerly Lowlands, Uplands, Lowlands, Intermed. Uplands/Isles, True Uplands) to enable zone-based analyses.

### 4.4 UKCEH-CS soil carbon groups
- Soil groups based on Loss-on-Ignition (LOI) ranges:
  - Mineral (0–8% LOI)
  - Humus mineral (8–30% LOI)
  - Organo-mineral (30–60% LOI)
  - Organic (60–100% LOI)

### 4.5 Measured and derived soil metrics
- Five soil cores per square/location; measurements include bulk soil and fine earth (FE) fractions.
- Calculations derive soil volumes, FE volumes, and related metrics used for carbon and nutrient stocks.

### 4.6 Soil pH in deionized water
- pH measured on field-moist bulk soil suspensions in deionised water.
- Quality control uses internal pH standards and duplicates (≈10% of samples).

### 4.7 Loss-on-Ignition (LOI) and derived carbon concentration
- LOI measured with LECO TGA from ~25–1000°C with staged heating; 105°C hold then 375°C hold to derive soil organic matter.
- Derived soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI) calculated from LOI and FE characteristics.
- Units: LOI as g per 100 g or percent; C_CONC_LOI in g C per kg soil; C_STOCK_LOI in t C per ha.
- Quality control includes internal standards and calcite checks.

### 4.8 Bulk density
- Dry bulk density derived from 15 cm core, adjusting for stone volume and FE volume to obtain density (g cm-3).
- Critical for converting %C to carbon stocks and for estimating pore space.

### 4.9 Fine earth volumetric and gravimetric water content
- Gravimetric moisture content measured as moisture per oven-dry FE and per field-moist weight.
- Quality control emphasizes standardized sampling sleeves and operator training.

### 4.10 Olsen-P
- Olsen phosphorus measured on soils from arable and improved grassland only (mg/kg).
- Colorimetric molybdenum blue method with calibration and QC checks (blanks, duplicates) and moisture correction.

### 4.11 Total soil nitrogen
- Total N (% and stock) measured with a Vario EL elemental analyser after ball milling and 105°C drying.
- Stocks calculated per hectare like carbon stocks; QA uses in-house references and calibration standards.

## Data quality assurance
- Robust QA framework supporting rolling surveys, with data workflows and validation in R.
- Ongoing QA across collection, processing, and laboratory analysis to ensure high data quality and traceability.
- Metadata-driven practices aim to make datasets discoverable and usable, with clear documentation and versioning.

## Details of data structure
- Dataset characteristics: 18 columns, 465 rows; missing values coded as -9999.
- Core columns include:
  - SQUARE (1-km code), PLOT (soil sampling location), YEAR
  - PH (pH in water)
  - LOI (soil organic matter proxy)
  - C_CONC_LOI (g C per kg soil)
  - C_STOCK_LOI (t C per ha)
  - SOIL_GROUP (LOI-based carbon group)
  - BULK_DENSITY (g soil per cm3)
  - MOISTURE (g water per g wet soil)
  - MOISTURE_DRY (g water per g oven-dry soil)
  - N_PERCENT (total nitrogen, %)
  - N_STOCK (t N per ha)
  - PO4_OLSEN (mg/kg; arable/improved grassland)
  - LC07, LC07_NUM (ITE Land Classification)
  - COUNTRY (GB country)
  - EZ_DESC_07 (Environmental Zone description)
- Data history and structure support cross-year comparisons and regional analyses.

## References and usage
- The document references foundational methods and prior Countryside Survey outputs, with links to related manuals, land classifications, and environmental zones.
- Data are intended for integration with broader Countryside Survey results and for informing assessments of soil change over time across GB, including comparisons with habitat types and environmental zones.