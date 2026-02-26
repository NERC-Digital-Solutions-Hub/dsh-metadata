# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

## Purpose and scope
- Documents QA metadata and analytical methods for topsoil 0–15 cm in the UK Countryside Survey (CS) 2020, part of a rolling GB-wide soil monitoring program.
- Supports tracking soil condition and change across time, integrating with vegetation data and environmental classifications.

## Study design and program context
- Countryside Survey is a long-running national audit (since 1978) with a rolling five-year sampling cycle to detect change, optimize site coverage, and buffer against climate variability.
- 2019 marked the start of the rolling program; first cycle for 2019–2023 aims to sample 500 1-km squares per cycle, with 100 squares visited annually.
- Sample selection stratified by Land Classification (ITE LC07) and Environmental Zones (EZ_DESC_07) to ensure national and sub-national representativeness.
- 2020 Covid disruption: fieldwork suspended part of the year; 50 England-only squares were added later to complete sampling.

## Sample collection methods
- Within each 1-km square: up to five sampling points (locations) co-located with vegetation surveys (X-Plots).
- Topsoil cores collected to 15 cm depth using a 15 cm long core; sampling positions fixed at pre-defined locations for re-location.
- Field relocation accuracy assessed via maps, photos, GPS data; 1990 markers used historically to aid relocation.
- After collection, cores are refrigerated and sent to UKCEH laboratories for processing (stored in the UKCEH Soil Bank).

## Metrics, laboratory protocols and analytical methods
- Five soil cores per square (up to five locations) analyzed for a suite of soil properties; key metrics include:
  - pH (in deionised water) and quality control via internal standards and duplicates.
  - Loss-on-Ignition (LOI) to estimate soil organic matter and derive soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI).
  - Bulk density (BULK_DENSITY) and stone/porosity calculations for fine earth (FE).
  - Moisture content (MOISTURE and MOISTURE_DRY) for gravimetric water content.
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils.
  - Total nitrogen (N_PERCENT) and stock (N_STOCK) using elemental analysis.
- Derived calculations cover carbon and nitrogen stocks per hectare, converting percentages to stocks using bulk density and core volume.
- Units and conversions clearly defined (e.g., core depth 0.15 m; 1 ha = 10000 m2; 1 g cm-3 = 1000 kg m-3).

## Data quality assurance and quality control
- Robust QA workflow implemented by UKCEH laboratory staff and data scientists; uses R-based scripts and documentation.
- QC procedures include:
  - pH: internal standards and duplicates to ensure readings within ±2 SD of batch mean.
  - LOI: internal standards and calcite checks; repeat runs if QC criteria fail.
  - PO4_OLSEN: blanks, duplicates, and reference samples (every 25 samples) to ensure accuracy; moisture-corrected results.
  - N_PERCENT: in-house references and standard checks (Acetanilide) with recurring calibration checks.
- Data are processed and stored in the UKCEH Soil Bank; a traceable data flow from field collection to laboratory processing and data warehousing.

## Data structure and accessibility
- Dataset characteristics:
  - 18 columns, 194 rows in the topsoil 2020 dataset.
  - Missing data denoted by -9999.
- Key columns include: SQUARE (GB 1-km square ID), PLOT (soil sampling location within square), YEAR (sampling year), PH, LOI, C_CONC_LOI, C_STOCK_LOI, SOIL_GROUP, BULK_DENSITY, MOISTURE, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN, LC07, LC07_NUM, COUNTRY, EZ_DESC_07.
- Land Classification (LC07 and LC07_NUM) and Environmental Zone (EZ_DESC_07) provide context for stratified analyses and cross-comparisons.
- Data are curated to support long-term trend analyses and cross-study comparisons; data and metadata are linked to soil banks and CS documentation.
- Documentation and data references available through UKCEH channels and Countryside Survey resources; contact and portal information provided for data access.

## Data governance, stewardship and publication notes
- This dataset supports the Data Steward aim: ensuring standards, metadata clarity, and interoperability across large, multi-source datasets.
- Data are generated under a rolling program to facilitate timely, repeatable, and scalable updates; clear provenance from field collection to QA-enabled data products.
- Metadata and QA processes are designed to improve discoverability, reuse, and transparency of methods, QC, and derived metrics.
- Potential limitations acknowledged (e.g., 2020 Covid disruptions altering square selection and sampling in England) that Data Stewards would document for downstream users.

## Challenges and considerations for data users
- Completeness of user-needs alignment: dataset focuses on soil metrics with a specific sampling design; users should align questions with the 0–15 cm topsoil scope and LS data availability.
- Timeliness and consistency: rolling design mitigates some temporal gaps but users should account for Covid-era disruptions when interpreting year-to-year changes.
- Interoperability: reliance on Land Classification and Environmental Zones requires careful cross-walking when integrating with other datasets or classifications.
- Large and multi-system workflow: data flow from field to Soil Bank involves multiple steps and QC checks; users should consider data provenance when combining with external datasets.

## References and further reading
- Core methodological documents and related Countryside Survey publications (Soils Manual, 2007-2010 series, and later CS reports) as well as UKCEH Environmental Zone documentation and Land Classification references.
- Contact information and access points provided (enquiries@ceh.ac.uk; CEH and CS websites).