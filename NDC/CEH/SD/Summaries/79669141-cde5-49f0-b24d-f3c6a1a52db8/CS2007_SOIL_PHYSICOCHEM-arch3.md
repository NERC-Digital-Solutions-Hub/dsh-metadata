# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain
Version: 1: 02-6-2016

- A Countryside Survey 2007 dataset describing soil physico-chemical properties collected across Great Britain (up to 591 1km squares).
- Data owned by NERC - Centre for Ecology & Hydrology; CS2007_SOIL_PHYSICOCHEM.csv details the measurements and metadata.
- Focus: pH, loss on ignition (LOI), carbon and nitrogen stocks, moisture, bulk density, Olsen phosphorus, land class, and geographic context.

## Data coverage and structure

- Sampling scope: soils from up to 591 1km squares across Great Britain (England, Scotland, Wales) surveyed in 2007.
- Key columns (example definitions):
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Year of survey
  - PH: Fresh soil pH in water
  - LOI: Loss on ignition (%)
  - C_CONC_LOI: Carbon concentration (g/kg) calculated as 0.55 × LOI
  - C_STOCK_LOI: Carbon stock (t/ha) calculated as 0.55 × LOI
  - BULK_DENSITY: Bulk density (g/cm3)
  - MOISTURE: Moisture content (%)
  - N_PERCENT: Nitrogen percentage
  - N_STOCK: Nitrogen stock (0–15 cm) (t/ha)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07, LC07_NUM: ITE Land Class descriptions and codes
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County/ council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data provenance and use: Acknowledgement required; CS data publicly documented and available through CS publications and portals.

## Measurements and laboratory protocols

- pH measurements
  - Two measurements per sample: pH in deionised water and in 0.01 M CaCl2
  - Fresh soil pH in water: 10 g soil with 25 ml deionised water; read after stabilization
  - Calibration and QA: batch checks with pH 4 and pH 7 buffers; standard soil and certified references included
  - Quality assurance aligned with Defra/NERC/BBSRC Joint Codes of Practice
- Loss on Ignition (LOI)
  - Up to 3145 black cores analyzed; LOI on 10 g air-dried sub-sample
  - Procedure: 105°C drying for 16 h, then 375°C combustion for 16 h
  - QA: standard material and duplicates per batch; cross-checks with alternative methods (CS2000 vs CS2007)
  - Rationale: 1978 LOI method retained for consistency with CS2000 and 1978 datasets
- Bulk Density (BD)
  - Core-based determination using LOI material relationship; account for core removals when calculating BD
  - QC: limited control soil; cross-checks against expected values and cross-era comparisons (CS2000 vs CS2007)
- Olsen Phosphorus (PO4_OLSEN)
  - Extraction with 0.5 M NaHCO3, pH 8.5; colorimetric molybdenum blue detection
  - QA: replicate plus standard and certified reference soil per batch of 25 samples
  - Considerations: drying effects, extraction temperature, soil:solution ratio, organic matter influence
- Total Nitrogen (N)
  - Analysis by CEH Lancaster UKAS-accredited method SOP3102
  - Instrument: Elementar Vario-EL elemental analyzer
  - QA: in-house reference materials; calibration using certified standards
- Data governance and QA
  - QA and QA: Joint Codes of Practice followed; cross-laboratory cross-checks and re-analyses where needed
  - Documentation: Soils Manual (CS Technical Report No. 3/07, 180 pages) with sampling, processing, QC, archiving, and data manipulation details

## Sampling strategy and study design

- Stratified national design based on Land Classes and environmental gradients
- Sample framework:
  - 591 sample squares (1 km × 1 km)
  - England: 289 squares; Wales: 107; Scotland: 195
  - 0–15 cm topsoil sampled; variations in corner sampling positions over time (compared to 1978 CS)
- Power analysis
  - Ensured sufficient sample size for reporting major measurements (e.g., pH, LOI) with required confidence
  - Some analytes (e.g., metals) permitted reduced sample sizes to meet funder requirements
- Field and laboratory processing
  - Standard field sampling protocol provided to surveyors
  - Consistent processing of cores, logging, chemical analyses, and archiving
- Cross-comparisons and consistency
  - CS2007 LOI method aligned with 1978 method for comparability
  - Cross-comparisons with CS2000 performed to ensure reliability

## Documentation, references, and data accessibility

- Core technical references and manuals:
  - Countryside Survey: Soils Manual (Emmett et al., 2008)
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - CS2007 Soils Manual details sampling, QC, archiving, data manipulation
- Data acknowledgement and licensing
  - Acknowledgement: Countryside Survey data owned by NERC-CEH
  - Data usage governed by CS documentation and publication references
- Availability
  - Data and methods are documented in CS technical reports and related publications; accessible via CS website and ethical data portals (NERC/NORA references)

## Implications for monitoring frameworks and policy assessment

- Provides a comprehensive, standardized set of soil health indicators across Great Britain for 2007
- Enables national and country-level monitoring of soil pH, organic matter (via LOI and carbon proxies), nutrient stocks (N, P), and bulk density
- Demonstrates rigorous QA/QC, metadata richness, and governance aligned with joint codes of practice
- Supports trend analysis and policy evaluation by enabling comparisons with CS2000 and CS1978 datasets and by offering transparent methodological documentation
- Highlights data stewardship considerations relevant to monitoring frameworks, such as data accessibility, metadata completeness, and data provenance across time and laboratories