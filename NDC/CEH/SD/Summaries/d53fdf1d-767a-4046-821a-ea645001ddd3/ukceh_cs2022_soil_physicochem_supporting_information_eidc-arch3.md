# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

- The Countryside Survey is a long-running audit of the UK countryside, now operating as a rolling program since 2019 to monitor soil health and related vegetation changes. It supports policy and decision-making on soil condition, carbon dynamics, and interactions of multiple pressures. The 2022 topsoil dataset focuses on physico-chemical properties of the 0–15 cm layer and is part of the UK-SCAPE-enabled rolling monitoring.

## 1. Purpose and policy-relevant aims
- Provide measures of topsoil condition and function to assess change over time and under multiple pressures (soil carbon, pH, nutrients, etc.).
- Generate data and maps for national and sub-national indicators to inform policy and land-management decisions.
- Ensure data are collected, processed, QA’d, and openly shared to support transparent governance and future analyses.

## 2. Survey design and rolling program
- Rolling survey: 500 x 1-km squares across GB per 5-year cycle; 100 squares visited annually.
- Sampling strata based on Land Classification (LC07) to capture environmental gradients (climate, relief, geology).
- Environmental zones (EZ) derived from ITE land classes to enable habitat- and zone-based reporting.
- Exclusions: squares with >75% urban land or >90% sea; Covid disruption in 2020 led to partial resampling (50 England-only squares).
- Alignment with vegetation data and a snapshot approach to capture multi-scale change while buffering against climate year-to-year variation.

## 3. Sample collection and locations
- Within each square, up to five topsoil sampling locations co-located with vegetation X-Plots; soil cores collected at 15 cm depth.
- Sampling locations originally fixed in 1978; relocation maps and GPS/photo validation used to ensure accurate re-sampling.
- Soil cores stored cold and transported to UKCEH laboratories for processing; samples stored in the UKCEH Soil Bank.

## 4. Metrics, laboratory protocols and analytical methods
- 4.1 Location identifiers: 1-km squares (SQUARE), planted plots (PLOT), country (England, Scotland, Wales).
- 4.2 Land Class: LC07 used for stratification; LC07_NUM provides numeric codes; descriptions reflect major environmental gradients.
- 4.3 Environmental Zones: EZ_DESC_07 categorizes zones (e.g., Easterly/Westerly Lowlands, Uplands, etc.).
- 4.4 Soil carbon groups: LOI-based categories (Mineral, Humus mineral, Organo-mineral, Organic) for soil organic matter.
- 4.5 Measured and derived soil metrics: five cores per square/plot; calculations include soil volume, fines fraction, and carbon stocks.
- 4.6 Soil pH: measured in deionised water on field-moist bulk soil; QA includes internal standards and duplicates.
- 4.7 LOI and derived carbon: LOI measured by ThermoGravimetric Analyzer (LECO) with four-step heating; carbon concentration derived from LOI; carbon stock calculated per hectare using core depth and bulk density; QA includes internal standards and calcite checks.
- 4.8 Bulk density: derived from core mass, stone fraction, and core volume; important for converting %C to C per unit volume.
- 4.9 Moisture content: gravimetric water content for fine earth (MOISTURE and MOISTURE_DRY); quality control via standardized sampling sleeves and operator training.
- 4.10 Olsen phosphorus: measured for arable/improved grassland soils; colorimetric molybdenum blue method with calibration and blanks; QA includes duplicates and blanks.
- 4.11 Total nitrogen: measured by elemental analyzer after prep (ball-milled, oven-dried samples); QA includes in-house references and regular calibration checks.

## 5. Data quality assurance and workflow
- Transition to rolling surveys requires robust QA systems; data processed with R-based workflows and guidance documents.
- QA controls include internal standards, duplicate samples, blanks, and cross-checks against historical references to ensure consistency over time.
- Data stored and managed to high standards (Canada “Soil Bank”/UKCEH system) with documentation to support reuse and auditability.

## 6. Data structure and accessibility
- Dataset for topsoil 2022 comprises 18 columns and 465 rows; missing samples marked with -9999.
- Key fields include SQUARE, PLOT, YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, LOI-based soil groups, BULK_DENSITY, MOISTURE, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN, LC07, COUNTRY, EZ_DESC_07.
- Clear metadata supports traceability from field sampling through to derived metrics and stock estimates.
- Soil samples are stored in the UKCEH Soil Bank; data and methods align with Soils Manual (2008) and related CS documentation.

## 7. Data governance, sharing and documentation
- Outputs designed for open dissemination to inform policy and research; underlying data governed under UKCEH/Countryside Survey frameworks.
- Methodology and QA references provided for reproducibility; contact details available for data access and further information.

## 8. End-user relevance and implications for monitoring frameworks
- Demonstrates a robust, policy-relevant monitoring design: rolling, stratified sampling by environmental gradients, multi-metric soil health assessment, and transparent QA.
- The combination of soil chemistry (pH, LOI, C stocks, P, N) with physical properties (bulk density, moisture) enables estimation of carbon stocks and nutrient status across habitats and zones.
- The structure supports national and sub-national reporting, trend analysis, and scenario testing for soil health under multiple pressures.
- Highlights practical governance considerations for monitoring frameworks: scalable rolling designs, metadata completeness, data transformation needs, and the balance between public data sharing and metadata/data sensitivity.