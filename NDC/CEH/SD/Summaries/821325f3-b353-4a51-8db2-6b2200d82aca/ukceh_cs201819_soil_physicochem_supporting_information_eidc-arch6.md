# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC Topsoil physico-chemical data 2018/2019

- A national rolling survey (first cycle 2019) to monitor topsoil condition and function across Great Britain, enabling detection of spatial and temporal change and interactions with multiple pressures.
- Supported by UK-CEH and NERC, focusing on soil and vegetation change with potential co-located vegetation assessments; rolling program designed to buffer against climate variability and maximize site coverage.

## Survey design and sampling

- 1-km x 1-km squares sampled on a rolling five-year cycle; 500 squares selected per cycle, with 100 squares visited annually.
- Squares stratified by the Land Classification of Great Britain (ITE LC07); urban (>75%) and sea (>90%) areas excluded.
- Sampling within each square: up to five random locations (X-Plots) for soils and vegetation; topsoil (0-15 cm) cores collected at 15 cm depth from co-located plots.
- Movement and relocation of plots tracked using field maps, GPS, photos; annual resampling within the rolling framework to detect change.

## Sample collection and laboratory processing

- In each square, five soil samples collected per year from pre-defined points relative to a 2x2 m vegetation quadrat.
- Samples refrigerated and shipped to UKCEH laboratories; stored in the UKCEH Soil Bank.
- Field methods and sample handling align with the Soils Manual (Emmett et al. 2008).

## Metrics, laboratory protocols and analytical methods

- Core measurements include:
  - Soil pH in deionised water (B field-moist soil suspension) with internal pH standards and duplicates for QA.
  - Loss-on-Ignition (LOI) to estimate soil organic matter; LOI-derived carbon concentrations (C_CONC_LOI) and stocks (C_STOCK_LOI) using a 0.55 factor to convert LOI to carbon.
  - Bulk density (BULK_DENSITY) and porosity calculations from 15 cm cores; accounts for stones.
  - Gravimetric moisture contents: MOISTURE (wet) and MOISTURE_DRY (dry).
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils only; analyzed via molybdenum blue method with QA checks.
  - Total soil nitrogen (N_PERCENT) and N stocks (N_STOCK) using elemental analysis (VarioEL) after ashing/drying; QA via in-house references and standard corrections.
- Derived calculations:
  - Fine earth volume (with stone adjustment) and carbon stocks per hectare using bulk density and soil depth assumptions.
  - Units and conversions clearly defined (e.g., 0.15 m sampling depth, 1 ha = 10,000 m2).
- Land classification and environmental zoning:
  - LC07 (ITE Land Classification 2007) and country codes; Environmental Zones EZ (EZ_DESC_07) derived from combinations of LC07 classes.
- Data products include soil-carbon groupings (SOIL_GROUP) based on LOI levels (Mineral, Humus mineral, Organo-mineral, Organic).

## Data quality assurance and QA workflow

- Comprehensive QA across the data lifecycle; transition to rolling survey required robust QA pipelines.
- QA described via UKCEH staff and data scientists using R-based workflows and guidance documents.
- Quality controls in laboratories:
  - Internal pH standards and duplicated samples (about 10%).
  - LOI QA with internal standards and calcite checks; acceptance criteria tied to standard deviations.
  - Olsen-P QA with blanks and reference samples; moisture-corrected final results.
  - Nitrogen analysis validated against in-house references and standard materials.
- Data management:
  - Metadata and dataset structure documented; dataset uses -9999 to denote missing samples.

## Data structure and content

- The topsoil dataset contains 18 columns across 562 rows.
- Key fields:
  - SQUARE: 1-km survey square identifier.
  - PLOT: Plot number within the square (X-Plot).
  - YEAR: Year of soil sampling.
  - PH: Soil pH (water, field-moist bulk soil).
  - LOI: LOI (%) and related carbon concentration (C_CONC_LOI in g C/kg) and stock (C_STOCK_LOI in t C/ha).
  - SOIL_GROUP: LOI-based soil carbon group category.
  - BULK_DENSITY: Dry bulk density (g/cm3).
  - MOISTURE and MOISTURE_DRY: Gravimetric water contents (wet and oven-dry).
  - N_PERCENT and N_STOCK: Total soil nitrogen (%) and stock (t N/ha).
  - PO4_OLSEN: Olsen phosphorus (mg/kg) for applicable soils.
  - LC07 and LC07_NUM: Land Classification (2007) codes.
  - COUNTRY: GB country (England, Scotland, Wales).
  - EZ_DESC_07: Environmental Zone description code.
- Data are structured to enable linking soil metrics with vegetation, land-class, and environmental context.
- The dataset notes missing values as -9999.

## Outputs, data products and accessibility

- Data are stored and made available via the UKCEH Soil Bank and associated Countryside Survey data repositories.
- Outputs support analysis of soil condition trends, carbon stocks, nutrient status, and potential drivers across habitats and environmental zones.
- The rolling data framework facilitates policy-relevant insights into soil change (e.g., carbon pools, pH shifts, nutrient availability) and interactions with land-use pressures.

## Context, aims, and implications

- The Countryside Survey provides a long-term, standardized framework to assess soil health and ecosystem function at national scales, informing policy and scientific understanding of soil change since 1978.
- The 2019-onward rolling program aims to quantify direction and magnitude of soil change, interactions among pressures, and soil-vegetation feedbacks.
- The report documents methods, QA procedures, data structure, and the initial 2018/2019 topsoil dataset, including its carbon and nutrient indicators, environmental zoning, and land classification context.
- Covid-19 disruption is noted as a factor in the 2020 period, with implications for field operations and sampling continuity.

## References and additional notes

- Methodology and QA references align with Countryside Survey documentation (CS Soils Manual, Emmett et al.; LC07 land classification; soil analysis standards; and related CEH/NERC publications).
- Contact and further information channels are provided by UKCEH for data inquiries and access.