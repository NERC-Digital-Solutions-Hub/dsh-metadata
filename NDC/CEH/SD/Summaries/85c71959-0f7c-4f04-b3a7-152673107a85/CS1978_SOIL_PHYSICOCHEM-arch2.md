# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain Version: 1: 02-6-2016 Countryside Survey data © NERC - Centre for Ecology & Hydrology CS1978_SOIL_PHYSICOCHEM.csv file details:

## Overview
- Provides soil physico-chemical properties (pH and loss on ignition, LOI) from up to 256 1km squares across Great Britain surveyed in 1978.
- LOI is used to estimate soil organic matter and soil organic carbon concentration (C concentration) and carbon stock.
- Sampling focused on the top 15 cm of soil; LOI values were derived from 10 g soil samples (after sieving to 2 mm).
- Data include derived fields: C_CONC_LOI (g/kg) and C_STOCK_LOI (t/ha) using a CS-specific conversion factor of 0.55 for %C calculation.
- Dataset comprises 1197 plots within 256 1km squares, with columns describing location, year, and classifications.

## Data content and structure (columns)
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier (one of 5 plots per 1 km square) (number)
- YEAR: Year of survey (number)
- PH: Soil pH (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration from LOI (g/kg) using 0.55xLOI
- C_STOCK_LOI: Carbon stock from LOI (t/ha) using 0.55xLOI
- LC07 (text): ITE Land Class 2007
- LC07_NUM (number): ITE Land Class 2007 numeric code
- COUNTRY (text): Country (England ENG, Scotland SCO, Wales WAL)
- COUNTY07 (text): County or Council
- EZ_DESC_07 (text): Countryside Survey Environmental Zone description

## Methods and conversion factors
- Loss-on-ignition (LOI) methods:
  - LOI determined for 1197 plots within 256 1km squares in 1978.
  - Samples taken from the top 15 cm of soil; 10 g soil per sample after sieving to 2 mm.
  - Drying: 375°C for 16 hours; 1 g sub-sample combusted at 550°C for 3 hours.
  - LOI (%) calculated from weight loss after cooling.
  - Conversion to soil carbon concentration used a factor of 0.5 initially (Carey et al., 2008); analysis of later data (1998 and 2007) indicated 0.55, which is now used for all Countryside Survey soil C concentration and carbon density estimates.
- Soil pH methods:
  - pH measured in a suspension of de-ionised water.
  - Procedure: 10 g field-moist soil + 25 ml deionised water (soil:water ratio 1:2.5 by weight).
  - Suspension stirred, stood for 30 minutes, pH reading taken after a further 30 seconds.
  - Conducted at ITE Bangor using a method modified from Soil Survey of England and Wales (Avery and Bascomb, 1974).

## Data provenance and usage notes
- All Countryside Survey data must be acknowledged when used.
- Acknowledgement text: "Countryside Survey data owned by NERC - Centre for Ecology and Hydrology" and copyright notice applicable.
- Data are stored and uploaded to appropriate portals; outputs are presented in clear formats (tables, maps, charts) as part of standardised analyses.
- LOI and pH methods follow established CS documentation and cited sources; data are intended for consistent environmental monitoring and policy evaluation over time.

## Relevance for environmental monitoring and analysis
- Fits the Analysts Monitoring the Environment archetype by providing standardized, quality-assured soil health data suitable for time-series monitoring and cross-dataset comparisons.
- Facilitates integration with other environmental datasets through standard classifications (LC07, COUNTRY, COUNTY07, EZ_DESC_07) and derived carbon metrics (C_CONC_LOI, C_STOCK_LOI).
- Encourages data sharing and access by documenting methods, converting LOI to carbon metrics, and storing data in accessible portals, addressing challenges of dataset value enhancement and underlying data accessibility.

## References and publications
- Countryside Survey: Soils Report from 2007 (Emmett et al., 2010) — UK results and methods.
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996; Bunce et al., 1981) — Land classification context for LC07.
- Soil survey laboratory methods (Avery and Bascomb, 1974).
- Carey et al. (2008) Countryside Survey: UK Results from 2007.
- Additional links and DOIs provided for the ITE Land Classification dataset and related CS documentation.