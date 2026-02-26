# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

## Executive summary
- Describes the 2023 topsoil physico-chemical dataset from UKCEH Countryside Survey (CS) with QA metadata and analysis methods.
- Soil samples (0–15 cm) collected across a rolling five-year cycle from 500 1-km squares (100 per year) stratified by Land Classification (LC07) to monitor soil condition and change across Great Britain.
- Provides detailed laboratory methods, QA procedures, data structure, and storage in the UKCEH Soil Bank, enabling robust national-scale analysis of soil carbon, nutrients, texture proxies, and related properties.

## Data scope, design and program
- Rolling survey design: repeats every five years or after 500 squares completed; first cycle started in 2019.
- Sampling framework: 1-km x 1-km squares randomly selected within stratified Land Classification zones; 100 squares visited annually.
- Exclusions and disruptions: squares with >75% urban land or >90% sea excluded; 2020 Covid disrupted fieldwork with partial resampling in England.
- Environmental context: data linked to ITE Land Classification and Countryside Survey Environmental Zones to enable stratified analysis of soil indicators by environment.

## Sampling methods and collection details
- In each square, up to five sampling locations co-located with vegetation X-Plots (5 cores per location, 15 cm depth) are collected.
- Historical relocation notes: plot positions have shifted across survey years (e.g., 1998, 2007 re-sampling; 2019 relocations) with methods to verify accuracy (maps, GPS, photos).
- Sample handling: topsoil cores refrigerated, stored, and shipped to UKCEH laboratories; processed and stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Core metrics (0–15 cm FE where applicable): pH (in deionised water), LOI (loss on ignition) to estimate soil organic matter and carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI), bulk density (BULK_DENSITY), moisture content (MOISTURE, MOISTURE_DRY), total nitrogen (N_PERCENT, N_STOCK), Olsen-P (PO4_OLSEN) for arable/improved grassland, plus derived carbon stock calculations.
- LOI methodology: ThermoGravimetric Analysis (LECO TGA701), heating to 105°C and 375°C to determine organic matter; carbon concentration derived from LOI with a factor (approx. 0.55) and used to calculate stocks per hectare.
- Measurements and units: detailed definitions for each field (e.g., C_STOCK_LOI in t C/ha; N_STOCK in t N/ha).
- Data recording: 18-column schema capturing square, plot, year, and all analyzed metrics; sample IDs denoted with specific field codes.

## Quality assurance and quality control
- QA workflow developed by UKCEH lab staff and data scientists; implemented via R-based scripts and guidance documents.
- Laboratory QC: internal pH standards, duplicates (~10% of repeats); LOI QC with internal standards and calcite checks; Olsen-P QC with duplicates and blanks every 25 samples; nitrogen analysis with in-house reference materials and calibration checks.
- Data integrity: explicit handling of units, conversions, and batch-level QC to ensure consistency across samples and years.

## Data structure and metadata
- Dataset structure: Table 5 with 18 columns and 597 rows; missing samples coded as -9999.
- Key fields:
  - SQUARE: 1-km square identifier
  - PLOT: plot number within square
  - YEAR: sampling year
  - PH, LOI, C_CONC_LOI, C_STOCK_LOI
  - SOIL_GROUP, BULK_DENSITY, MOISTURE, MOISTURE_DRY
  - N_PERCENT, N_STOCK
  - PO4_OLSEN
  - LC07, LC07_NUM, COUNTRY
  - EZ_DESC_07
- Data provenance: samples processed and stored at UKCEH laboratories; linked to long-term CS data and environmental zone classifications.

## Data availability, storage and governance
- Data stored in the UKCEH Soil Bank and available for reuse by researchers via UKCEH channels and CS documentation.
- Publication context: 2023 QA metadata and analysis report for topsoil data; references provided for methodologies and historical CS work.
- Contact and access: inquiries via ceh.ac.uk channels and CS project documentation; guidance documents accompany the data.

## Practical considerations for data reuse
- Longitudinal comparability: rolling program supports temporal trends, but plot relocations and cycle-based sampling may introduce nuance when comparing across years.
- Data limitations: some squares excluded due to urban/sea coverage; 2020 Covid disruptions may affect year-to-year continuity in certain areas.
- Derived metrics: carbon stocks and nutrient concentrations depend on LOI-based transformations and bulk density adjustments; QC procedures must be accounted for in analyses.
- Documentation and references: extensive methodological references are provided to support replication and understanding of laboratory and analytical workflows.