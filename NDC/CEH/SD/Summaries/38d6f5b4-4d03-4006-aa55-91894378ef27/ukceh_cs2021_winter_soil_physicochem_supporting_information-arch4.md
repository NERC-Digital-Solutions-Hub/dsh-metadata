# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

## Overview and aims
- Countryside Survey (CS) is a long-running national audit of UK countryside resources, with rolling monitoring from 2019 to track soil condition, carbon stocks, and ecosystem function.
- Rolling program: 500 1-km2 squares sampled across GB per five-year cycle; 100 squares visited each year; designed to detect spatial and temporal change while buffering against climate year effects.
- Primary questions focus on how multiple pressures affect topsoil condition and function, including carbon stock changes, carbon to nitrogen ratios, soil pH shifts, compaction, phosphorus availability, and vegetation-soil feedbacks.
- Data support comparisons with previous CS surveys (1978, 1998, 2007, 2019) and are intended for national and sub-national indicators, with potential cross-use in soil health benchmarking and policy-relevant analyses.

## Design and sampling program
- Selection framework: 500 x 1-km2 squares within strata defined by Land Classification (ITE LC07), ensuring robust national and sub-national indicators; 100 squares visited annually.
- Exclusions: urban >75% or sea >90% (per LCM2007 and census data).
- 2020 disruption: COVID-19 affected fieldwork; partial resampling occurred with England-only replanning.
- Winter topsoil subset: a hierarchical square selection prioritising squares from 1978/1998/2007 and reflective environmental zones; 30 (+5 reserve) squares chosen for winter 2021 follow-up.

## Sample collection and field methods
- Per square: five pre-determined sampling locations (PLOTs) aligned with vegetation X-Plots; 15 cm soil cores collected at co-located locations with vegetation surveys.
- Depth and sampling: topsoil 0–15 cm; five cores per square; soil cores stored cold and shipped to UKCEH laboratories.
- Data captured in field: broad habitat recorded for winter survey; sampling locations tracked over time with plots relocated using long-term markers.

## Metrics, laboratory protocols and analytical methods
- Core metrics measured on fine earth (FE) and/or bulk soil:
  - pH (in deionised water, field-moist soil)
  - Loss-on-Ignition (LOI) to estimate soil organic matter and carbon content
  - Soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Soil bulk density (BULK_DENSITY)
  - Moisture content (MOISTURE and MOISTURE_DRY)
  - Total soil nitrogen (N_PERCENT and N_STOCK)
  - Olsen phosphorus (PO4_OLSEN) not measured in 2021 winter survey; recorded for compatibility with other CS datasets
- Lab processes: five cores per square; samples logged, stored in UKCEH Soil Bank; LOI measured with ThermoGravimetric Analyser (TGA701); N analyzed via elemental analyzer after ball milling; pH validated with internal standards and replicates.
- Data handling: derived metrics calculated with standardized R scripts to ensure reproducibility and auditability; quality controls applied at multiple steps.

## Data quality assurance and workflow
- QA workflow includes:
  - Lab data QA: visual QA and flagging of outliers and standard stability
  - Analyst data QA1: cross-check lab data against measurement records; document queries and changes
  - Derivation of soil metrics: use of two dedicated R scripts to define and apply calculations, with version-controlled processes
  - Analyst data QA2: automated HTML QA reports comparing patterns, validating against past data, and identifying outliers
- All data changes are recorded against data records and QA steps to ensure auditability.

## Data structure and accessibility
- Dataset structure: 18 columns, 576 rows; missing values denoted by -9999
- Key fields include:
  - SQUARE: 1-km square identifier
  - PLOT: plot number within square
  - YEAR: survey year (winter 2021 noted as 2022 in metadata)
  - PH: soil pH (in water)
  - LOI: loss-on-ignition (g LOI per 100 g soil; %)
  - C_CONC_LOI: soil carbon concentration (g C per kg soil)
  - C_STOCK_LOI: carbon stock (t C per ha)
  - SOIL_GROUP: UKCEH-Countryside Survey carbon groups by LOI
  - BULK_DENSITY: bulk density (g soil per cm3)
  - MOISTURE_DRY: gravimetric water content (g water per g oven-dry soil)
  - N_PERCENT: total nitrogen concentration (g N per 100 g soil)
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus (not measured in 2021 winter)
  - LC07, LC07_NUM: Land Classification 2007 codes
  - COUNTRY: GB country (England, Scotland, Wales)
  - EZ_DESC_07: Environmental Zone description
- Data are prepared for integration with other CS components (habitat/vegetation data) and potentially the UK soil health and policy-relevant analyses.

## Data governance, updates and usage notes
- Data are produced under UKCEH Countryside Survey protocols with rolling monitoring initiated in 2019; designed for longitudinal analyses of soil condition and pressures across GB.
- 2021 winter survey data intentionally exclude Olsen-P measurement, but include other core metrics and are designed to be compatible with broader CS datasets.
- Quality assurance emphasizes reproducibility and transparency, enabling robust derivation of soil health indicators and facilitating cross-study comparisons and benchmarking.

## References and further reading (selected)
- Foundational CS methodologies and prior surveys (1998, 2007, 2019) and soils manuals
- Related work on soil carbon, nitrogen, and health benchmarks in managed and semi-natural landscapes
- UKCEH and CS documentation on environmental zones, land classification, and soil data bank practices

## Practical implications for data leadership
- Demonstrates a robust, auditable data pipeline from field collection through lab analysis to derived metrics, with explicit QA stages and reproducible scripting.
- Provides long-term, standardized soil data suitable for monitoring trends, benchmarking, and policy-relevant analyses of soil health and carbon dynamics.
- Highlights the importance of harmonized metadata (SQUARE, PLOT, YEAR, LC07, COUNTRY, EZ_DESC_07) for discoverability and cross-project integration, as well as the need to note any deviations (e.g., 2020 COVID disruption, Olsen-P not measured in 2021 winter survey).