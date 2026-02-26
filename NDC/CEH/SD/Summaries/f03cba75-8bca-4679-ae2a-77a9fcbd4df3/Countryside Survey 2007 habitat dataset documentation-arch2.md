# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 2007, derived using the 2007 ITE Land Classification.
- Units are total area in thousands of hectares (000s ha) per Land Class, with lower and upper 95% confidence intervals.
- Freshwater habitats were analyzed using a different statistical model than other habitats.

## Data Components
- CS007_Broad_Habitat_Stock.csv
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total Area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
  - Note: MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.

## Spatial Data: Raster Estimates
- CS2007_Stock.tif
  - In each 1 km pixel, a mean percentage estimate of habitat is provided for the corresponding Broad Habitat class within each Land Class stratum.
  - Bands correspond to Broad Habitat classes as follows:
    - Broad Habitat 1/2: Coniferous Woodland (Band 2) and Broadleaved Mixed and Yew Woodland (Band 3)
    - Broad Habitat 3/1: Boundary and Linear Features (Band 3) and Broadleaved Mixed and Yew Woodland (Band 4)
    - Broad Habitat 4/1: Arable/Horticulture (Band 4) and Broadleaved Mixed and Yew Woodland (Band 5)
    - Broad Habitat 5/1: Improved Grassland (Band 5) and Broadleaved Mixed and Yew Woodland (Band 6)
    - Broad Habitat 6/1: Neutral Grassland (Band 6) and Broadleaved Mixed and Yew Woodland (Band 7)
    - Broad Habitat 7/1: Calcareous Grassland (Band 7) and Broadleaved Mixed and Yew Woodland (Band 8)
    - Broad Habitat 8/1: Acid Grassland (Band 8) and Broadleaved Mixed and Yew Woodland (Band 9)
    - Broad Habitat 9/1: Bracken (Band 9) and Broadleaved Mixed and Yew Woodland (Band 10)
    - Broad Habitat 10/1: Dwarf Shrub Heath (Band 10) and Broadleaved Mixed and Yew Woodland (Band 11)
    - Broad Habitat 11/1: Fen, Marsh, Swamp (Band 11) and Broadleaved Mixed and Yew Woodland (Band 12)
    - Broad Habitat 12/1: Bog (Band 12) and Broadleaved Mixed and Yew Woodland (Band 13)
    - Broad Habitat 13/1: Standing Open Waters/Canals (Band 13) and Broadleaved Mixed and Yew Woodland (Band 14)
    - Broad Habitat 14/1: Rivers/Streams (Band 14) and Broadleaved Mixed and Yew Woodland (Band 15)
    - Broad Habitat 15/1: Montane (Band 15) and Broadleaved Mixed and Yew Woodland (Band 16)
    - Broad Habitat 16/1: Inland Rock (Band 16) and Broadleaved Mixed and Yew Woodland (Band 17)
    - Broad Habitat 17/1: Urban (Band 17) (Broadleaved Mixed and Yew Woodland mapping also listed)

## Spatial Reference and File Information
- Pixel size: 1 km (1000 meters)
- Coordinate system: British National Grid (OSGB1936), Transverse Mercator projection
- Extent: Great Britain
- Data use and copyright: Acknowledgement required; Countryside Survey data owned by NERC-Centre for Ecology & Hydrology

## Data Usage and Access
- Acknowledgement: Countryside Survey data owned by NERC-CEH; Countryside Survey © CEH; All rights reserved
- Data outputs are provided for monitoring environmental health and policy performance, with standardized formats suitable for reports, maps, and charts
- Guidance and methodologies referenced in linked publications and reports

## Relevance for Environmental Monitoring
- Provides standardized, time-stamped estimates of Broad Habitat extent by Land Class for national-scale environmental monitoring
- Enables comparison over time and integration with other environmental datasets
- Includes uncertainty (confidence intervals) and notes potential negative mean estimates due to statistical modeling
- Supports storage, data management, and dissemination through established Countryside Survey channels and publications

## References and Publications
- Countryside Survey project overview and methodologies (CS Website)
- Carey et al. 2008: Countryside Survey UK Results from 2007 (CS UK 2007 TR)
- Scott 2007: CS Technical Report No.4/07 (Statistical report on national estimates)
- Bunce et al. 1996/1981: ITE Merlewood Land Classification and descriptions
- Jackson 2000: Guidance on Biodiversity Broad Habitat Classification interpretations
- Countryside Survey Field Mapping Handbook (CS Technical Report No.1/07)