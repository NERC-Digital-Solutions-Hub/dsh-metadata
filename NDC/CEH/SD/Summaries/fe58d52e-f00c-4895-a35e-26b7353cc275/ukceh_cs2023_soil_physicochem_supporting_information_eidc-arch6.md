# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

## Overview
- QA metadata and results for topsoil physico-chemical data collected under the UK Centre for Ecology & Hydrology (UKCEH) Countryside Survey (CS) in 2023.
- Focus on rolling CS design (soil and vegetation) with standardized sampling across GB to monitor change in soil condition and function.
- Data are generated from 1-km squares, with five topsoil sampling locations per square, co-located with vegetation plots; samples preserved and analyzed in UKCEH laboratories; data stored in UKCEH Soil Bank.

## Background
- Countryside Survey is a long-running national audit of UK countryside resources, conducted since 1978.
- The 2019 onwards program uses a rolling survey to repeatedly sample 500 squares over a five-year cycle, allowing detection of spatial and temporal changes in soil and vegetation.
- Aims include understanding how multiple pressures affect topsoil condition, carbon pools, pH, compaction, phosphorus availability, and vegetation feedbacks.
- The program is supported by NERC under UK-SCAPE to generate national-scale soil condition data and maps.

## Rolling program and design
- Five-year rolling cycle: 500 x 1-km squares in total; 100 squares are visited each year.
- Squares selected within strata defined by the Land Classification of Great Britain (LC07); urban (>75% urban) or sea (>90%) squares are excluded.
- The survey design enables robust national and sub-national indicators across GB and its countries.
- The 2020 Covid disruption affected fieldwork; 50 squares were resampled in England later in the year.

## Covid disruption (2020)
- Limited fieldwork May–June 2020; resumed in July–August 2020.
- Re-selection of survey squares with additional England-only sampling to maintain coverage.

## Sample collection methods
- In each 1-km square, five soil samples are taken at predetermined locations near vegetation X-Plots.
- Soil core: 15 cm long; sampling occurs at or near the 0–15 cm topsoil layer, co-incident with vegetation plots.
- Historical sampling locations evolved: 1978 (centre of 200 m2 plots); 1990 markers placed; 1998/2007 resampling adjustments; 2019 relocation to the western corner of the inner plot.
- After collection, cores are refrigerated and shipped to UKCEH labs, typically within a few days.

## Metrics, laboratory protocols and analytical methods
- Field and laboratory workflow described in the Soils Manual (Emmett et al., 2008) and related CS documentation.
- Five samples per square are analyzed; data organized in a structured laboratory system; samples stored in the UKCEH Soil Bank.
- Key measured metrics and methods:
  - Soil pH in deionised water (PH): field-moist bulk soil suspension; QC with internal pH standards and duplicates.
  - Loss-on-Ignition (LOI) and soil carbon (C_CONC_LOI, C_STOCK_LOI): LOI determined with LECO TGA701 across four heating steps; carbon concentration derived from LOI; carbon stock calculated per hectare with standard conversions; QA with internal standards.
  - Soil bulk density (BULK_DENSITY) and stone content; porosity derived from core measurements; moisture content (MOISTURE, MOISTURE_DRY) using gravimetric approaches.
  - Olsen phosphorus (PO4_OLSEN): measured on arable/improved grassland soils via Olsen extraction and colorimetric detection; QC with blanks and duplicates.
  - Total soil nitrogen (N_PERCENT, N_STOCK): measured with elemental analyzer after ball milling and drying; QA using in-house references and standard checks.
- Data quality controls throughout: internal standards, duplicates, blanks, and calibration checks integrated into each batch/run.

## Data quality assurance
- Dedicated QA workflow developed by UKCEH laboratory staff and data scientists using R scripts and guidance documents.
- Transition to rolling surveys necessitates robust, ongoing QA to ensure data integrity and comparability across years and sites.

## Details of data structure
- Dataset: 18 columns, 597 rows (topsoil data for 2023); missing samples denoted by -9999.
- Key fields include:
  - SQUARE: 1-km survey square identifier.
  - PLOT: soil sampling location within the square.
  - YEAR: year of sampling.
  - PH: soil pH (water, field-moist bulk soil).
  - LOI: soil organic matter content (g LOI per 100 g soil; %).
  - C_CONC_LOI: soil carbon concentration (g C per kg soil).
  - C_STOCK_LOI: carbon stock (t C per ha).
  - SOIL_GROUP: LOI-based soil grouping.
  - BULK_DENSITY: dry bulk density (g cm-3).
  - MOISTURE, MOISTURE_DRY: gravimetric water content measures.
  - N_PERCENT, N_STOCK: total soil nitrogen content and stock.
  - PO4_OLSEN: Olsen phosphorus concentration (arable/improved grassland only).
  - LC07, LC07_NUM: ITE Land Classification identifiers (2007).
  - COUNTRY: GB country (Eng, Sco, Wal).
  - EZ_DESC_07: Countryside Survey Environmental Zone description.
- Data are aligned to the field-log and laboratory system for traceability from square to measurement.

## References and further reading
- Foundational CS methods and QA practices are documented in:
  - Soils Manual (Emmett et al., 2008)
  - Countryside Survey: Soils Report from 2007 (Emmett et al., 2010)
  - ITE Land Classification of Great Britain (Bunce et al., 2007)
  - Various CS-related methodological and analytical publications listed in the document

## Contact and accessibility
- Enquiries: enquiries@ceh.ac.uk
- UKCEH locations and contact details provided, including Bangor, Edinburgh, Lancaster, and Wallingford offices.
- UKCEH Soil Bank and CS project resources are referenced for data access and methodology details.