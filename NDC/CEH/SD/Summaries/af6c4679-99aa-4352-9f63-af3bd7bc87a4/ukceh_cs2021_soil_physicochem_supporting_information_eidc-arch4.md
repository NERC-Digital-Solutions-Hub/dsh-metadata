# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

## Overview
- Long-running UK countryside survey (since 1978) now operating a rolling program from 2019 to monitor soil condition and function across Great Britain.
- Primary aim: detect direction and magnitude of soil change, and how multiple pressures interact with topsoil condition and vegetation.
- Data support policy-relevant insights on soil carbon, nitrogen, pH, compaction, phosphorus, and the interactions between vegetation change and soil condition.
- Rolling program: 500 1-km squares per five-year cycle; 100 squares visited annually; design stratified by Land Classification to ensure national and sub-national representativeness.

## Design and rolling program
- Sample framework: 1-km x 1-km squares within strata defined by Land Classification (ITE LC07), with 500 squares per cycle; 100 squares visited each year.
- Exclusions: squares with >75% urban land or >90% sea excluded.
- Covid disruption in 2020: fieldwork delayed; 50 England-only squares resampled later in the year.

## Covid disruption
- 2020: partial fieldwork due to COVID-19; adjustments included reselection and reallocation of some survey squares to maintain coverage.

## Sample collection methods
- Within each selected square, five soil samples are taken from randomly dispersed locations aligned with vegetation X-Plots.
- Topsoil core: 15 cm depth, using a black plastic core, co-located with vegetation surveys.
- Historical note: sampling locations and plots have been relocated and tracked across survey years (1998, 2007, 2019 onward) to ensure comparability.
- Samples are refrigerated and transported to UKCEH laboratories for processing; stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- General field methods described in the Soils Manual; five samples per square analyzed for soils; processed samples stored in the Soil Bank.
- Key metrics:
  - pH (in deionised water) on field-moist bulk soil.
  - Loss-on-Ignition (LOI) to estimate soil organic matter and derive soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI).
  - Bulk density (BULK_DENSITY) and stone content for porosity and carbon stock calculations.
  - Moisture content (MOISTURE and MOISTURE_DRY) for gravimetric water assessments.
  - Olsen-P (PO4_OLSEN) in arable/improved grassland soils.
  - Total soil nitrogen (N_PERCENT; N_STOCK) using an Elementar VarioEL analyzer.
- Lab quality control:
  - pH: internal standards and duplicates; acceptance within ±2 standard deviations.
  - LOI: internal standards and calcite checks; duplicates/ blanks for QC; repeated runs if standards deviate.
  - Nitrogen and phosphorus: duplicates and blanks every set number of samples; moisture corrections applied.
- Calculations:
  - LOI-based soil carbon and nitrogen stocks converted to t/ha; conversions rely on soil depth (0-15 cm), bulk density, and area units.
  - Volume and stone adjustments applied to derive fine-earth metrics.

## Data quality assurance
- A robust QA workflow developed with UKCEH staff and data scientists using R scripts and guidance documents.
- Rolling program requires continuous QA and validation to maintain consistency across years and sites.

## Details of data structure
- Dataset configuration: 18 columns, 496 rows; missing samples coded as -9999.
- Key fields:
  - SQUARE: 1-km survey square identifier (text).
  - PLOT: soil sampling location within the square (numeric).
  - YEAR: year of survey (numeric).
  - PH: soil pH (numeric).
  - LOI: LOI value (g per 100 g or % depending on context).
  - C_CONC_LOI: soil carbon concentration (g C per kg soil).
  - C_STOCK_LOI: carbon stock (t C per ha).
  - SOIL_GROUP: LOI-based soil carbon group category.
  - BULK_DENSITY: bulk density (g per cm3).
  - MOISTURE, MOISTURE_DRY: water content metrics (g water per g soil; per g dry soil).
  - N_PERCENT, N_STOCK: total nitrogen content and stock (g N per 100 g; t N per ha).
  - PO4_OLSEN: Olsen phosphorus (mg/kg).
  - LC07, LC07_NUM: ITE Land Classification (2007) and numeric code.
  - COUNTRY: GB country (England, Scotland, Wales).
  - EZ_DESC_07: Countryside Survey Environmental Zone description.
- Data lineage and references tied to Land Classification and Environmental Zones for contextual interpretation.

## Data management and storage
- Samples and derived metrics are processed at UKCEH laboratories; raw and processed samples stored in the UKCEH Soil Bank.
- Data linked to the broader Countryside Survey design, including environmental zones (EZ) and land classifications (LC07).

## Relevance and potential uses for data leaders
- Enables tracking of long-term soil change and regional variation through a standardized, repeatable sampling framework.
- Supports analyses of interactions between vegetation change and soil condition, soil carbon dynamics, pH changes, nitrogen deposition effects, and phosphorus status under different land classifications and environmental zones.
- Provides a well-documented QA and data structure suitable for governance, metadata completeness, and future data discoverability.
- Demonstrates robust data workflows (collection, processing, QA, storage) that can inform data governance and cross-institution collaborations.

## Access and contact
- For data questions or access inquiries: enquiries@ceh.ac.uk
- Additional project context and documentation available via UKCEH Countryside Survey resources.