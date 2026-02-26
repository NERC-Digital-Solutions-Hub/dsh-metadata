# Spatial mapping of surficial (top 10cm) soil OC storage and stocks across Great British saltmarshes

## Overview
- GIS-based data product mapping organic carbon (OC) storage density (kg OC m^-2) and OC stocks (tonnes OC) in surficial soils (top 10 cm) across 438 Great British saltmarshes.
- Integrates saltmarsh extents from England, Scotland, and Wales with surficial soil data and vegetation maps to produce bespoke GIS layers.
- Covers 451.65 km² of Great British saltmarshes and provides per-marsh stock estimates.

## Data Product
- Spatial maps of OC density and OC stock across GB saltmarshes, with:
  - Sample location data (latitude/longitude and X/Y)
  - Marsh area (km²)
  - OC storage for top 10 cm (kg OC m^-2)
  - OC stock (tonnes OC) by marsh and vegetation/naming classes
- Layers are designed for GIS use and can be linked to existing saltmarsh maps.

## Spatial Coverage and Coordinate Information
- Geographic scope: Great Britain (Scotland, England, Wales)
- Coordinates provided as decimal degrees (Lat/Long, WGS84) and as X/Y in a projected system
- Spatial projection: OSGB 1936
- Software environment: ESRI ArcGIS
- File formats included: .cpg, .dbf, .prj, .sbn, .sbx, .shp, .shp, .shx (shapefile components)

## Data Model and Attributes
- Key variables:
  - Saltmarsh surficial soil OC stock (tonnes OC)
  - Organic Carbon Storage (kg OC m^-2) for top 10 cm
  - Marsh zone and NVC class (vegetation/classifications)
- Data sources combined:
  - NERC C-Side project data (OC content, dry bulk density)
  - Marine Scotland data
  - Saltmarsh vegetation maps (England EA 2021; Scotland Haynes 2016; Wales NRW 2016)

## Methodology
- OC storage calculations per marsh class/zone using OC content (%) and dry bulk density (kg m^-3)
- Spatial assembly by overlaying OC data with saltmarsh extents to produce 10 cm depth maps
- Stock calculations conducted within a Monte Carlo Markov Chain (MCMC) framework
  - 1,000,000 samples drawn from normal distributions (area, OC content, density, etc.) within a pool of 100,000,000
  - Purpose: quantify uncertainty in OC storage and stock estimates

## Data Processing and Quality
- Calibration procedures: not applicable/NA
- Quality control procedures: not documented (NA)
- Emphasis on integration of multiple data sources and existing saltmarsh maps to create cohesive GIS layers

## Provenance and References
- Data sources include:
  - Environment Agency (England) saltmarsh extent and zonation
  - Haynes, Scottish saltmarsh survey
  - Natural Resources Wales saltmarsh extents
  - Ruranska et al. (2020, 2022) surficial soil OC content and bulk density
  - Miller et al. (2022) Marine Scotland data
- DOIs and references provided for reproducibility and data provenance

## Usage and Notes for GIS Specialists
- Suitable for map-based analyses of OC storage and stocks in GB saltmarshes
- Can be integrated with existing saltmarsh extents and vegetation maps for scenario analyses or policy briefings
- Units:
  - OC storage: kg OC m^-2
  - OC stocks: tonnes OC
- Depth consideration: top 10 cm of surficial soils
- Consider uncertainty bounds from the MCMC-derived stock estimates in any downstream interpretation