# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain

## Overview
- Data from Countryside Survey 1978 detailing soil physico-chemical properties (pH and loss on ignition, LOI) for up to 256 1km squares across Great Britain.
- Includes derived soil carbon concentration (C_CONC_LOI, g/kg) and carbon stock (C_STOCK_LOI, t/ha) using a conversion factor of 0.55 from LOI.
- Attributes cover land classification (ITE Land Class 2007), country, county, and environmental zone description.
- Samples taken from the top 15 cm of soil.

## Spatial scope and dataset composition
- Region: Great Britain (England ENG, Scotland SCO, Wales WAL).
- Scale: 1 km square grid; up to 256 squares with 1197 plots overall.
- Key identifiers: SQUARE (1km square code), PLOT (within-square plot), YEAR (survey year, 1978).

## Variables / fields
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier (within each 1km square) (number)
- YEAR: Year of survey (number)
- PH: Soil pH (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration from LOI (g/kg) using conversion factor 0.55
- C_STOCK_LOI: Carbon stock from LOI (t/ha) using conversion factor 0.55
- LC07: ITE Land Class 2007 (text)
- LC07_NUM: ITE Land Class 2007 numeric code
- COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
- COUNTY07: County or Council area
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Methods and data provenance
- Loss-on-ignition (LOI) method: 10 g soil, sieved to 2 mm; dried at 375°C for 16 hours; 1 g sub-sample combusted at 550°C for 3 hours; LOI (%) calculated from weight loss.
- LOI to soil carbon concentration: initial use of conversion factor 0.5; subsequently 0.55 adopted (as per later Countryside Survey analyses) for all soil C concentration and carbon density estimates.
- Soil pH method: pH in water measured on a suspension of de-ionised water with a 1:2.5 soil-to-water ratio, after 30 minutes mixing.
- Data sources and references include CEH Countryside Survey reports and ITE Land Classification documentation.

## Data rights and acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC-Centre for Ecology & Hydrology. All rights reserved.

## GIS usage and considerations
- Suitable for map-based analyses of soil properties and carbon: create thematic maps of pH, LOI, C_CONC_LOI, and C_STOCK_LOI.
- Can be integrated with land classification (LC07) and environmental zones (EZ_DESC_07) for habitat and land-use planning.
- Allows calculation of spatially explicit soil carbon density, and cross-plot comparisons within and across 1km squares.
- Caution with temporal scope: data reflect conditions from 1978; suitability for historical comparison or long-term trend analyses should consider changes since then.
- Data resolution is 1km; LOI conversion factor history (0.5 → 0.55) may influence carbon estimates if comparing across periods.

## Practical notes
- Data is provided as a CSV with explicit site, plot, and derived carbon variables suitable for joins in GIS workflows.
- Ensure proper attribution in any published maps or reports and comply with the stated acknowledgement requirement.