# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

## Overview
- Long-running audit of the UK's countryside, with a rolling monitoring programme since 2019 to track soil condition and function at national scale.
- Focuses on topsoil (0–15 cm) health and its relation to vegetation and multiple pressures; supports policy-relevant understanding of change over time.
- Data are collected, quality assured, and transformed into standardized outputs (including maps and reports) for monitoring progress.

## Survey Design and rolling programme
- Rolling survey: 500 one-kilometre squares across Great Britain per five-year cycle; 100 squares visited each year.
- Squares stratified by Land Classification (LC07) to capture environmental gradients; urban or sea-dominated squares excluded.
- Aims to provide robust national and sub-national indicators of soil change; allows year-on-year comparison within a practical field program.
- Covid disruption in 2020: restricted fieldwork in May–June; reselected 50 squares from England for later sampling.

## Sample collection methods
- In each 1-km square, five topsoil locations sampled randomly (aligned with vegetation X-Plots) using 15 cm long cores at ~0–15 cm depth.
- Sampling locations within squares tracked via historic plots; relocation aided by maps, field maps, and GPS data; consistent relocation over time is a priority.
- Samples refrigerated and shipped within days to UKCEH laboratories; soils processed and stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Field and lab methods are described in the Soils Manual; five cores per square are processed.
- Key data components (4.4–4.11):
  - 4.1 Soil sampling locations and general information: SQUARE, PLOT, COUNTRY, YEAR.
  - 4.2 Land Class (LC07) used to stratify sampling; 2007 ITE Land Classification.
  - 4.3 Countryside Survey Environmental Zones (EZ) derived from ITE classes.
  - 4.4 UKCEH-CS soil carbon groups based on Loss-on-Ignition (LOI).
  - 4.5 Measured and derived soil metrics: core length, volumes, and fraction calculations (including stones).
  - 4.6 Soil pH in deionized water with internal QC standards and duplicates.
  - 4.7 LOI and derived soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI) with calculation methods.
  - 4.8 Bulk density (dry) and stone corrections for fine earth volume; core-based calculation.
  - 4.9 Fine earth volumetric and gravimetric water content (MOISTURE and MOISTURE_DRY).
  - 4.10 Olsen-P for arable/improved grassland soils; colorimetric analysis with QC checks.
  - 4.11 Total soil nitrogen (N_PERCENT) with automated elemental analysis; N_STOCK derived for stocks.
- Units and conversion details provided (e.g., depth 0.15 m, 1 ha = 10,000 m2, bulk density in g cm-3, g C to t C conversions).

## Data quality assurance (QA)
- Transition to rolling surveys necessitates robust QA and data processing workflows.
- QA implemented via standardized pipelines, R-based workflows, and guidance documents.
- Laboratory and data staff perform continuous QA to maintain high data standards.

## Data structure and contents
- Dataset: 18 columns, 465 rows for topsoil data 2022.
- Missing data encoded as -9999.
- Key columns (examples):
  - SQUARE (text), PLOT (number), YEAR (number)
  - PH (soil pH in water)
  - LOI (g LOI per 100 g soil; percentage)
  - C_CONC_LOI (g C per kg soil in fine earth)
  - C_STOCK_LOI (t C per ha)
  - SOIL_GROUP (LOI-based soil carbon group)
  - BULK_DENSITY (g cm-3)
  - MOISTURE (gravimetric water content wet soil)
  - MOISTURE_DRY (gravimetric water content on oven-dry soil)
  - N_PERCENT (total soil nitrogen in %)
  - N_STOCK (t N per ha)
  - PO4_OLSEN (mg P per kg soil)
  - LC07 (ITE Land Classification number)
  - LC07_NUM (numeric LC07 code)
  - COUNTRY (GB country)
  - EZ_DESC_07 (Environmental Zone description)

## Outputs and usage
- Data designed to support monitoring of soil condition and stock/change, enabling assessment of pressures and their interactions across habitats and environmental zones.
- Outputs feed into national-scale analyses, maps, and policy-relevant indicators for soil health, carbon pools, nutrients, and pH dynamics.

## Accessibility and references
- Data and QA methodologies linked to UKCEH Countryside Survey and Soil Bank resources.
- Contact and further reading available through CEH/Countryside Survey channels and associated references.