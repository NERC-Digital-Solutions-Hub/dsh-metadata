# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

## Overview
- A Countryside Survey dataset detailing soil physico-chemical properties collected in 1998/1999 across up to 256 1km squares in Great Britain.
- Properties include pH, loss on ignition (LOI), carbon concentration and stock, total nitrogen, and Olsen phosphorus.
- Data gathered from plots within each 1 km square and linked to land classification and geographic identifiers.

## Data structure and columns
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier (one of 5 plots per 1 km square) (text)
- YEAR: Year of survey (number)
- PH: Soil pH (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration from LOI (g/kg); uses 0.55 x LOI for %C calculation
- C_STOCK_LOI: Carbon stock from LOI (t/ha); uses 0.55 x LOI
- N_PERCENT: Total nitrogen percentage (number)
- PO4_OLSEN: Olsen Phosphorus (mg/kg) (number)
- LC07 (text): ITE Land Class 2007 description
- LC07_NUM: ITE Land Class 2007 numeric code
- COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
- COUNTY07: County/Region (Eng/Wal) or Council (Sco)
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Methods and conversions
- LOI methods
  - Samples from the top 15 cm of soil; up to 256 plots per survey
  - 10 g soil per LOI, dried at 375°C for 16 hours, then 1 g sub-sample combusted at 550°C for 3 hours
  - LOI (%) calculated from weight loss
  - Carbon concentration conversion: originally 0.5; updated to 0.55 for CS estimates
- Soil pH methods
  - pH measured in deionised water (ratio soil:water 1:2 by weight)
  - Procedure: shake, settle for 30 minutes, measure after an additional 30 seconds
- Total nitrogen
  - Up to 1280 samples analyzed at ITE Merlewood
  - Instrument: Elementar Vario-EL elemental analyzer; combustion with oxygen, detection by thermal conductivity
  - QA: two in-house reference materials per batch; calibration via certified standard
- Olsen phosphorus
  - Up to 1280 cores analyzed at ITE Merlewood
  - Extraction: 5 g of air-dried soil with 100 ml of 0.5 M NaHCO3 (pH 8.5)
  - Determination: colorimetric molybdenum blue at 880 nm with optional dialysis step
  - QA: two in-house reference materials per batch

## Data quality and provenance
- Data sourced from established Countryside Survey protocols and methodologies
- Acknowledgement and ownership: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all CS data use must be acknowledged
- Data outputs (reports/maps) typically stored and uploaded to appropriate data portals

## Usage notes for analysts
- Enables monitoring of soil health indicators and carbon storage across Great Britain for 1998/1999
- Allows standardised comparisons over time when integrated with LC07 land classifications and geographic metadata
- Suitable for linking soil physico-chemical properties with environmental zoning and policy assessments

## References and related materials
- Countryside Survey methodologies and outputs (web links and publications)
- Key publications on soil quality and land classification relevant to the dataset (e.g., MASQ, ITE Land Classification 2007)
- Additional methodological details and validation reports linked in the data documentation