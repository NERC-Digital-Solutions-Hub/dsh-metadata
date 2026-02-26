# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

## Overview and aim
- National, long-running audit of UK countryside resources; allows comparison of 2019+ results with previous surveys.
- Focus on topsoil condition and function (0–15 cm) with co-located vegetation data; supports understanding of soil status, change, and responses to pressures.
- Rolling program initiated in 2019 to monitor change at national and sub-national scales, with outputs to inform policy and science.

## Survey design, rolling programme and disruption
- Rolling survey: 500 x 1-km squares over a five-year cycle; 100 squares visited per year.
- Sampling strata defined by Land Classification of Great Britain to ensure robust national and sub-national indicators.
- 2020 Covid disruption caused late-year fieldwork; 50 squares were reselected from England to compensate.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded.

## Sample collection methods
- In each 1-km square, five topsoil samples collected from predefined randomly dispersed locations (X-Plots) at ~15 cm depth.
- Consistent with historic methodologies (since 1978); relocation markers and maps used for future visits; method refined in 1990, 1998, 2007, and 2019.
- Samples refrigerated and sent to UKCEH laboratories; stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Core measurements (0–15 cm) across up to five locations per square; processing/storage handled at UKCEH sites.
- Land Classification (LC07) used to stratify results; Environmental Zones (EZ_DESC_07) aggregate LC07 classes for interpretation.
- Soil groups (SOIL_GROUP) based on Loss-on-Ignition (LOI) and carbon content; include Mineral, Humus Mineral, Organo-mineral, Organic categories.
- Key measured metrics and derived values:
  - pH in deionised water (PH) with QA checks.
  - Loss-on-Ignition (LOI) and derived Soil Carbon Concentration (C_CONC_LOI) and Stock (C_STOCK_LOI).
  - Bulk density (BULK_DENSITY) and stone content to derive fine-earth porosity.
  - Gravimetric moisture (MOISTURE) and moisture on oven-dry basis (MOISTURE_DRY).
  - Olsen-phosphorus (PO4_OLSEN) for arable/improved grassland soils only.
  - Total nitrogen (N_PERCENT) and nitrogen stock (N_STOCK).
- QA controls include internal standards, duplicates, blanks, calibration checks, and batch-level quality control.

## Data quality assurance (QA)
- Implemented robust QA workflow with R-based data processing and guidance documents.
- Regular QA as part of the shift to rolling surveys to ensure high data standards across continuous collection and processing.

## Data structure and metadata
- Dataset: 18 columns, 496 rows; missing samples marked as -9999.
- Key columns:
  - SQUARE: 1-km survey square ID (text)
  - PLOT: plot number for soil sampling location (numeric)
  - YEAR: survey year (numeric)
  - PH: soil pH (field-moist bulk soil, water)
  - LOI: soil organic matter content by LOI (g LOI per 100 g soil; %)
  - C_CONC_LOI: soil carbon concentration (g C per kg soil)
  - C_STOCK_LOI: carbon stock (t C per ha)
  - SOIL_GROUP: carbon grouping based on LOI (categories)
  - BULK_DENSITY: bulk density of fine earth (g cm-3)
  - MOISTURE, MOISTURE_DRY: gravimetric moisture metrics
  - N_PERCENT: total soil nitrogen (%)
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus (mg kg-1) for applicable soils
  - LC07 and LC07_NUM: ITE Land Classification (2007)
  - COUNTRY: GB country (England/Scotland/Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data products are designed to support national and sub-national trend analysis, cross-ecosystem interpretation, and integration with vegetation data.

## Environmental zones and soil carbon context
- Environmental Zones (EZ_DESC_07) provide regionally contextualized groupings derived from multivariate analysis of environmental data across squares.
- Soil carbon groups (SOIL_GROUP) enable consistent categorization of soil organic matter and carbon stocks across sites and years.

## How the data support aims and use
- Enables monitoring of soil condition and function over time, including interactions among land-use, climate, and management practices.
- Facilitates stock-change analysis for carbon and nitrogen, soil health indicators, and nutrient status.
- Supports data sharing and transparency through standardized QA, clear metadata, and alignment with Countryside Survey outputs (soil and vegetation).

## References and further reading
- Methodologies and background aligned with UKCEH Countryside Survey manuals and reports (Soils Manual and related CS outputs), including 2007, 2008, 2010–2020 literature and data centre resources.