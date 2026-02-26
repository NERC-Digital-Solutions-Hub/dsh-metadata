# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

## Overview
- UKCEH Countryside Survey implements a rolling, national-scale soil and vegetation monitoring program in GB.
- Focus of this dataset: topsoil (0–15 cm) physico-chemical properties and derived carbon metrics to track change over time and across landscapes.
- Rolling design supports robust national and sub-national indicators while buffering against climate variability.

## Spatial design and sampling framework
- 1-km x 1-km squares across GB are sampled; 500 squares are visited over a five-year cycle, with 100 squares annually.
- Squares are stratified within Land Classification (LC07) across England, Scotland, and Wales.
- Exclusions: squares with >75% urban land or >90% sea are removed from selection.
- The design reuses historical CS squares (from 1978, 1998, 2007) to enable long-term change detection.

## Covid-19 disruption and adaptation
- Covid-19 disrupted 2020 fieldwork; sampling occurred mainly in July–August 2020 after reselecting 50 England-only squares.

## Sample collection and field workflow
- In each square, up to five pre-defined sampling locations are surveyed for vegetation and soils (X-Plots).
- Topsoil cores (15 cm long, from a 2x2 m vegetation quadrat area) are collected at randomly dispersed locations within the square.
- After collection, samples are refrigerated and sent to UKCEH laboratories; processed samples are stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Soil metrics are measured on either bulk soil or the fine-earth (FE) fraction; field core length is recorded for volume calculations.
- Key metrics and methods:
  - pH in deionized water (PH): standardized with internal pH standards and duplicates for QC.
  - Loss-on-Ignition (LOI) and derived carbon: LOI measured via LECO TGA701 (105°C hold, then 375°C), LOI used to derive soil organic matter and soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI) per hectare.
  - Soil carbon stocks: derived using FE LOI, bulk density, core depth, and area conversions.
  - Bulk density (BULK_DENSITY): calculated from core mass and volumes, accounting for stones.
  - Fine-earth moisture content (MOISTURE and MOISTURE_DRY): gravimetric water content for FE, expressed per wet or dry weight.
  - Olsen phosphorus (PO4_OLSEN): measured on arable/improved grassland samples; colorimetric molybdenum blue method with QC checks.
  - Total nitrogen (N_PERCENT): measured with elemental analyzer after ball milling and drying; N_STOCK calculated per hectare.
- Derived units and conversions:
  - C_STOCK_LOI in t C per ha; C_CONC_LOI in g C per kg soil; FE LOI used for carbon fraction.
  - Core depth assumed 0.15 m; 1 ha = 10,000 m2; stone corrections included in bulk density and carbon stock calculations.

## Data quality assurance (QA)
- Robust QA workflow implemented using R-based scripts and guidance documents.
- pH: internal standards and duplicates; batches flagged if deviations exceed tolerance.
- LOI: internal standards and calcite checks; repeated batches if QC criteria fail.
- Olsen-P and N measurements: included blanks, duplicates, and reference materials; instrument calibration validated with standards.

## Data structure and contents
- Dataset size: 18 columns, 465 rows.
- Key fields:
  - SQUARE: 1-km survey square identifier (text).
  - PLOT: Plot identifier within square (numeric).
  - YEAR: Year of soil sampling (numeric).
  - PH: Soil pH in deionized water (numeric).
  - LOI: LOI value and description (numeric; includes percentage and g LOI per 100 g soil).
  - C_CONC_LOI: Soil carbon concentration in FE (g C per kg soil; derived).
  - C_STOCK_LOI: Carbon stock in FE (t C per ha; derived).
  - SOIL_GROUP: Soil carbon group (categorical; LOI-based categories).
  - BULK_DENSITY: Dry bulk density of FE (g soil per cm3).
  - MOISTURE, MOISTURE_DRY: Gravimetric moisture contents (numeric).
  - N_PERCENT: Total soil nitrogen content (percent; numeric).
  - N_STOCK: Nitrogen stock per hectare (derived).
  - PO4_OLSEN: Olsen phosphorus (mg/kg; arable/improved grassland only).
  - LC07, LC07_NUM: ITE Land Classification (text and numeric).
  - COUNTRY: GB country (England/Scotland/Wales) (categorical).
  - EZ_DESC_07: Countryside Survey Environmental Zone description (text; derived from LC07).
- Quality and missing data:
  - Missing values encoded as -9999.

## Spatial classifications and derived groupings
- Land Classification (LC07) forms the basis for stratified analyses across GB habitats.
- Environmental Zones (EZ_DESC_07) aggregate LC07 classes into broader environmental zone categories (EZ1–EZ9, with EZ7 excluded for NI in this dataset).
- UKCEH-CS soil carbon groups (SOIL_GROUP) categorize soils by LOI-driven carbon content (Mineral, Humus mineral, Organo-mineral, Organic).

## Practical implications for GIS and map-based data products
- Spatially explicit topsoil properties (pH, LOI, carbon concentration and stock, bulk density, moisture, N, P) mapped at 1-km resolution with year-specific sampling.
- Ability to compare changes over time by square, land class, and environmental zone within the rolling 5-year cycle.
- Derived carbon stock maps (C_STOCK_LOI) enable quantification of soil carbon changes per hectare across landscapes.
- Data structure supports joining with vegetation data and environmental layers for integrated habitat analyses.

## References and data accessibility
- Methods and sampling protocols are anchored in the Countryside Survey Soils Manual and related CEH/CS technical reports.
- Data are managed within the UKCEH Soil Bank; contact and access details provided in project documentation.