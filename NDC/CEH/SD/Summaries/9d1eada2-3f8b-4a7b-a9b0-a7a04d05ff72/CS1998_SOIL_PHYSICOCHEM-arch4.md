# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey 1998/1999 covering up to 256 1km squares across Great Britain.
- Measured soil properties: pH, loss on ignition (LOI), carbon concentration (C_CONC_LOI), carbon stock (C_STOCK_LOI), total nitrogen (N_PERCENT), and Olsen phosphorus (PO4_OLSEN).
- Samples taken from the top 15 cm of soil.
- Includes land classification and location metadata (ITE Land Class 2007, country, county, environmental zone).
- Version 1, dated 02-06-2016; data owned by NERC - Centre for Ecology & Hydrology; requires acknowledgement in all uses.

## Data content and structure
- File: CS1998_SOIL_PHYSICOCHEM.csv
- Key columns:
  - SQUARE: 1km square site code
  - PLOT: plot within each square
  - YEAR: survey year (1998)
  - PH: soil pH
  - LOI: loss on ignition (%)
  - C_CONC_LOI: carbon concentration (g/kg), calculated as 0.55 × LOI
  - C_STOCK_LOI: carbon stock (t/ha), calculated as 0.55 × LOI
  - N_PERCENT: total nitrogen (%)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07 / LC07_NUM: ITE Land Class 2007 (description and code)
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: county or council
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Sample scope: up to 1280 samples for total N and Olsen P measurements.
- Notes: All use of Countryside Survey data must be acknowledged.

## Methods and quality
- LOI methods:
  - Samples from up to 256 squares; top 15 cm soil
  - 10 g soil (sieved to 2 mm) dried at 375°C for 16 h; 1 g sub-sample combusted at 550°C for 3 h
  - LOI% used to derive soil carbon metrics
  - Conversion factor updated from 0.50 to 0.55 for C concentration/stock
- Soil pH method:
  - pH in a suspension of de-ionised water (ratio 1 part soil to 2 parts water by weight)
  - Measurement procedure described (overnight suspension, measurement after 30 seconds)
- Total nitrogen:
  - Measured with Elementar Vario-EL elemental analyser
  - Automated oxidative combustion with calibration via certified standard; QC with in-house references
- Olsen phosphorus:
  - Extraction with 0.5 M NaHCO3 (pH 8.5), 100 ml extract
  - Colorimetric determination using molybdenum blue; dialysis step to mitigate reagent effects
  - QC with in-house reference materials
- Overall quality controls include use of reference materials across batches and documented analytical procedures.

## Provenance, references and licensing
- Data source: Countryside Survey (Great Britain), © NERC - Centre for Ecology & Hydrology
- Acknowledgement and copyright:
  - Acknowledgement: Countryside Survey data owned by NERC - CEH
  - Countryside Survey ©; Database Right/Copyright NERC-CEH. All rights reserved.
- Relevant publications and references accompany the dataset (e.g., Bunce et al. on land classification; Allen 1989 on chemical analysis; Carey et al. 2008 UK Results; MASQ and related methodology).

## Access and usage considerations for Data Leaders
- Documentation provides detailed methodological context, enabling data-driven planning and integration with other Countryside Survey years.
- Data discoverability relies on metadata links to the Countryside Survey resources and related datasets (land classification, environmental zones).
- Governance considerations include ensuring proper acknowledgment in all publications and outputs.