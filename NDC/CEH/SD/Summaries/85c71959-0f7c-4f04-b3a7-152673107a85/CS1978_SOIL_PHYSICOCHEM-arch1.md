# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain

## Overview
- Dataset of soil physico-chemical properties (pH and loss on ignition) from up to 256 1km squares across Great Britain, surveyed in 1978.
- LOI and pH data collected from top 15 cm of soil.
- Coverage includes multiple plots per square (PLOT within each SQUARE) and links to Land Classification and location metadata.

## Dataset contents and fields
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier within each 1 km square (number)
- YEAR: Year of survey (number; 1978)
- PH: Soil pH value (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration calculated from LOI (g/kg) using 0.55 x LOI
- C_STOCK_LOI: Carbon stock calculated from LOI (t/ha) using 0.55 x LOI
- LC07: ITE Land Classification 2007 (text)
- LC07_NUM: Land Classification numeric code
- COUNTRY: Country in which the 1km square is located (England ENG, Scotland SCO, Wales WAL)
- COUNTY07: County (or Council) in which the square is located
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Measurement methods
- Loss-on-ignition (LOI)
  - 1197 plots within 256 1km squares; samples from top 15 cm soil
  - 10 g soil per sample, sieved to 2 mm
  - Dry at 375°C for 16 h; 1 g sub-sample combusted at 550°C for 3 h
  - LOI (%) calculated from weight loss
  - Conversion to soil carbon concentration uses a factor: initially 0.5 ( Carey et al., 2008); updated to 0.55 based on 1998 and 2007 data
  - LOI-to-carbon conversions inform C_CONC_LOI and C_STOCK_LOI
- Soil pH
  - pH in water measured with de-ionised water
  - Procedure: 10 g soil in 50 ml beaker, add 25 ml water (soil:water ratio 1:2.5 by weight), stir, stand 30 min, read pH after 30 s

## Data provenance, rights, and usage notes
- Data owned by NERC - Centre for Ecology & Hydrology (CEH)
- All Countryside Survey data requires acknowledgement
- Acknowledgement text: Countryside Survey data owned by NERC - CEH; Countryside Survey © CEH. All rights reserved.
- References to methodologies and related publications provided for context and reproducibility

## Key references and links
- Countryside Survey methodologies and soils report (UK Results from 2007)
- ITE Merlewood Land Classification and related documents (Bunce et al.)
- Soil survey laboratory methods (Avery & Bascomb, 1974)

## Practical considerations for analysts
- Data scale and coverage: 256 1km squares, 1197 LOI measurements; 1978 snapshot, limited to topsoil (0–15 cm)
- LOI conversion factor sensitivity: carbon estimates depend on the chosen LOI-to-C factor (0.55 for this dataset’s conversions)
- Linkages: LC07/LC07_NUM and COUNTY07/EZ_DESC_07 enable spatial aggregation and regional analyses
- Data access and attribution: ensure proper acknowledgement when using in reports, datasets, or visualisations
- Potential limitations: historical dataset; differences in sampling density across squares; classification and boundary definitions may have evolved since 1978