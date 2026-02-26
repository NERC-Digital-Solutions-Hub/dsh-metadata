# Data Structure

## Overview
- Diffuse agricultural pollution to rivers in Scotland data stored as CSV files.
- Used to map pollution loads to Water Framework Directive (WFD) catchments in Scotland and support environmental monitoring and policy assessment.
- Intended to be linked to WFD catchment polygons; WFD catchments are not yet published by SEPA but planned for addition to the Environmental data page.

## File Names and Format
- AgLoadsInland_Scotland.csv (inland catchments)
- AgLoadsCoastal_Scotland.csv (coastal catchments)
- Format: comma-separated values (CSV)

## Key Fields and Their Meaning
- INLAND_ID: SEPA ID for inland catchments (inland file)
- COASTAL_ID: SEPA ID for coastal catchments (coastal file)
- CATCH_ID: Unique WFD catchment identifier
- Arable_Are: Total arable area (ha)
- Grass_area: Total improved grass area (ha)
- Rough_Area: Total rough grazing area (ha)
- Arable_x: Total pollutant load from arable land (per pollutant)
- Grass_x: Total pollutant load from improved grassland (per pollutant)
- Rough_x: Total pollutant load from rough grazing land (per pollutant)
- Other_x: Total pollutant load from other areas (e.g., steadings, tracks, manure storage) (per pollutant)

## Pollutants and Units
- _P: kg total P per year
- _N: kg NO3-N per year
- _S: kg suspended solids per year
- _F: 10^6 cfu per year
- _N2O: kg N2O per year
- _CH4: kg CH4 per year
- cfu = colony forming units

## GIS Mapping
- Datasets can be joined to WFD catchment polygons using INLAND_ID (inland file) or COASTAL_ID (coastal file).
- WFD catchments themselves are not yet published by SEPA; planned inclusion on SEPA’s Environmental data page.

## Data Provenance and Publication Status
- Based on approaches in Gooday et al. (2016) for mitigating rural diffuse pollution (SNIFFER Project DP1).
- Identifies land-use derived pollutant loads by catchment and year.
- Publication status: WFD catchment dataset not published yet by SEPA; expected to be added to the Environmental data page.

## Practical Use for Monitoring
- Provides standardized metrics of land-use–driven pollution loads to Scottish rivers.
- Facilitates categorisation and comparison of pollution contributions by land type across catchments.
- Supports data quality assurance, transformation, and storage for ongoing monitoring and policy evaluation.

## Data Management Considerations
- Aim to verify, quality-assure, clean, and transform data prior to analysis (consistent with the Analysts Monitoring the Environment approach).
- Ensure datasets are stored properly and uploaded to relevant portals for broad accessibility.