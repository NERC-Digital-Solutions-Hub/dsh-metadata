# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain Version: 1: 02-6-2016 CS1978_SOIL_PHYSICOCHEM.csv file details:

## Overview
- Dataset of soil physico-chemical properties (pH and loss on ignition, LOI) from up to 256 1km squares across Great Britain, surveyed in 1978.
- Derived soil carbon metrics included: soil carbon concentration (C_CONC_LOI) and soil carbon stock (C_STOCK_LOI) calculated from LOI.

## Dataset structure and columns
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier within each 1km square (1 of 5) (number)
- YEAR: Year of survey (number)
- PH: Soil pH (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration from LOI (g/kg) using a conversion factor of 0.55xLOI
- C_STOCK_LOI: Carbon stock from LOI (t/ha) using a conversion factor of 0.55xLOI
- LC07: ITE Land Class 2007 (text)
- LC07_NUM: Land Class 2007 numeric code (number)
- COUNTRY: Country where the 1km square is located (England ENG, Scotland SCO, Wales WAL)
- COUNTY07: County (or Council in Scotland)
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Derived metrics and conversion notes
- C_CONC_LOI and C_STOCK_LOI are calculated with a bespoke conversion value of 0.55 (not the original 0.50) for soil carbon concentration and density, based on analyses from 1998 and 2007 data.
- LOI-to-C conversion is explicitly stated as 0.55x LOI for both concentration (g/kg) and stock (t/ha).

## Measurement methods
- Loss-on-ignition (LOI):
  - Samples: 1197 plots within 256 1km squares; top 15 cm of soil.
  - Procedure: 10 g soil, sieved to 2 mm; dried at 375°C for 16 hours; 1 g sub-sample combusted at 550°C for 3 hours; LOI (%) calculated from weight loss.
- Soil pH:
  - Method: pH in soil-water suspension.
  - Procedure: 10 g soil with 25 ml deionised water (1:2.5 soil:water by weight); mix, stand 30 minutes, measure after 30 seconds.

## Data usage, governance, and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” with Countryside Survey ©; Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Documentation includes methods, references, and links to methodological publications and data centre records.

## Provenance, references, and supporting materials
- LOI methods and conversion rationale described; baseline 0.5 factor used historically, updated to 0.55 based on later data.
- References and sources provided include:
  - Countryside Survey: Soils Report from 2007 (CS Technical Report No. 9/07)
  - ITE Merlewood Land Classification; ITE Land Classification of Great Britain 2007
  - Soil survey laboratory methods (Avery & Bascomb, 1974)
  - Carey et al. 2008 Countryside Survey: UK Results from 2007
- Links and DOIs are provided for key datasets and methodological documents within the accompanying notes.