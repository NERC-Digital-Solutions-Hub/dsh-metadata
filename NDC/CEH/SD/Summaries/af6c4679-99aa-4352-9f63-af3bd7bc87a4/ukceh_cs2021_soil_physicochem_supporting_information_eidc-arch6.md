# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

## Overview
- National-scale Countryside Survey (since 1978) now operates as a rolling program (since 2019) to monitor soil condition and function across Great Britain.
- Focuses on topsoil health and associated vegetation, enabling comparisons over time and space.
- This dataset presents topsoil physico-chemical data (0–15 cm) collected in 2021, with QA metadata and analytical methods.

## Survey design and rolling program
- Rolling survey: 500 x 1-km squares over a five-year cycle; 100 squares visited annually, to balance spatial coverage and temporal monitoring.
- Stratified sampling using Land Classification of Great Britain (ITE LC07) to robustly estimate national and sub-national indicators.
- Exclusions: squares with >75% urban land or >90% sea removed from sampling.
- 2020 Covid disruption: May–June restrictions; sampling resumed later in the year; 50 England-only squares added due to disruptions.

## Sampling methods
- Within each 1-km x 1-km square, topsoil samples collected from up to five pre-defined random locations within vegetation X-Plots.
- Soil cores: 15 cm long, collected from 0–15 cm depth at co-located vegetation plots (2 m x 2 m).
- In 1998/2007, relocation accuracy supported by maps/markers; from 2019 plots relocated to the western corner with GPS/photo verification.
- After collection, cores are refrigerated and sent to UKCEH laboratories for processing and storage in the UKCEH Soil Bank.

## Metrics and laboratory protocols
- General methods described in the Soils Manual; five soil samples per square, processed and stored as needed.
- Key measured and derived metrics:
  - pH (PH): measured in deionised water on field-moist bulk soil.
  - Loss-on-Ignition (LOI): determined with a LECO TGA701 to estimate soil organic matter and carbon; used to derive C_CONC_LOI and C_STOCK_LOI.
  - Soil carbon and nitrogen stocks: C_STOCK_LOI and N_STOCK derived per hectare; N_PERCENT reported from ball-milled samples.
  - Olsen phosphorus (PO4_OLSEN): measured on arable/improved grassland samples using Olsen’s extraction and colorimetric detection.
  - Bulk density (BULK_DENSITY): calculated from core mass and core volume, accounting for stones.
  - Moisture content: gravimetric water content (MOISTURE and MOISTURE_DRY) calculated from field-moist and oven-dry conditions.
- Units and conversions: depth 0.15 m core; 1 ha = 10,000 m2; stone volume estimated; conversion factors provided for C and N stocks.
- Quality control: internal pH standards and duplicates; LOI standards and blanks; two-point nitrogen standards; Olsen-P calibration checks; routine instrument QC.

## Quality assurance
- Data collection and processing underwent rigorous QA as part of the rolling program shift.
- Data workflow developed by UKCEH laboratory staff and data scientists using R-based scripts and guidance documents to ensure high data quality.
- Regular QA procedures include batch-level internal standards, duplicates, calibration checks, and cross-validation with reference materials.

## Data structure and metadata
- Dataset characteristics: 18 columns and 496 rows; missing samples denoted by -9999.
- Primary columns and meanings:
  - SQUARE: 1-km survey square identifier
  - PLOT: soil sampling location within the square
  - YEAR: year of soil sampling
  - PH: soil pH (water, field-moist bulk soil)
  - LOI: percent soil organic matter by LOI
  - C_CONC_LOI: g C per kg oven-dry soil (fine earth)
  - C_STOCK_LOI: t C per ha
  - N_PERCENT: g N per 100 g oven-dry soil
  - N_STOCK: t N per ha
  - PO4_OLSEN: mg P per kg oven-dry soil (arable/improved grassland only)
  - BULK_DENSITY: g soil per cm3
  - MOISTURE: gravimetric water content (wet)
  - MOISTURE_DRY: gravimetric water content (oven dry)
  - LC07 and LC07_NUM: ITE Land Classification (2007)
  - COUNTRY: GB country (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone descriptor
  - SOIL_GROUP: soil carbon group classification (LOI-based)
- Structure supports stratified analysis by country, land class, and environmental zones; data linked to Soil Bank and broader Countryside Survey outputs.

## Data workflow, handling, and accessibility
- Data are part of UKCEH Soil Bank and Countryside Survey data products; QA workflow ensures consistency across years and sites.
- Metadata and methodology sections provide traceability for data provenance, sampling locations, and lab protocols.
- The dataset supports monitoring of soil carbon pools, pH dynamics, nitrogen and phosphorus status, moisture, and bulk density across habitat types and environmental zones.
- References and further reading supplied to situate methods within the broader Countryside Survey framework.

## References and further reading
- Key methodological and background documents from the Countryside Survey program (Soils Manual, 2007; 2010–2020 reports; land classification guides; environment zones analyses).
- Related publications on soil carbon, nitrogen, and land-use change within the Countryside Survey series.