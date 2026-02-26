# Supporting document for: GB_saltmarsh_OC_resources.zip

## Overview
- Spatial mapping of surficial (top 10 cm) soil organic carbon (OC) storage and OC stocks across 438 Great British saltmarshes.
- OC density (kg OC m−2) and OC stocks (tonnes OC) derived for surficial soils.
- Coverage includes saltmarshes identified in current maps for Scotland, England, and Wales; spatial extent covers 451.65 km2.
- Data built on surficial soil bulk density and carbon data from the NERC C-Side project and Marine Scotland, combined with existing vegetation maps.

## Data sources and inputs
- OC content (% wt) and dry bulk density (kg m−3) for surficial soils provided by:
  - NERC C-Side project (Ruranska et al., 2020, 2022)
  - Marine Scotland data (Miller et al., 2022)
- Saltmarsh vegetation maps:
  - Environment Agency (2021)
  - Haynes (2016)
  - Natural Resources Wales (2016)

## Methodology
- For each saltmarsh vegetation class/zone, compute mean OC storage (kg OC m−2) and combine with marsh mapping to produce bespoke GIS layers mapping OC storage to a depth of 10 cm.
- OC stock calculations performed within a Monte Carlo Markov Chain (MCMC) framework:
  - 1,000,000 samples drawn from distributions (e.g., area, OC content, dry bulk density) to populate stock estimates (from a pool of 100,000,000 samples per variable).

## Data products and formats
- GIS-ready spatial layers with OC storage and OC stock data:
  - Formats include .cpg, .dbf, .prj, .sbn, .sbx, .shp, .shp, .shx.
- Projection: OSGB 1936.
- Software: ESRI ArcGIS.
- Observations include:
  - Marsh area (km2)
  - Organic carbon storage (kg OC m−2) for top 10 cm
  - Location data (sample locations with latitude/longitude and X/Y coordinates)
  - 451.65 km2 coverage across 438 marshes

## Location, scale, and coverage
- Geographic scope: Great Britain (Scotland, England, Wales)
- Locations provided as decimal degrees (lat/long) and projected coordinates

## Data quality, calibration, and limitations
- Calibration procedures: not applicable (NA) for some steps; stock calculations rely on Monte Carlo simulations.
- Quality control/validation details are not extensively specified beyond the Monte Carlo framework.
- Limitations include reliance on surficial 10 cm depth, potential scale and regional variability, and integration of data from multiple sources with varying formats and times.

## Access, metadata, and provenance
- Data resource ID: Spatial mapping of surficial (top 10 cm) soil OC storage and stocks across Great British saltmarshes.
- Grounded in multiple primary data sources and published datasets; metadata and provenance linked to NERC C-Side, Marine Scotland, Environment Agency, Haynes (2016), and Natural Resource Wales (2016).

## Key references
- Environment Agency (2021). Saltmarsh extent and zonation.
- Haynes, T.A. (2016). Scottish saltmarsh survey national report.
- Natural Resources Wales (2016). Saltmarsh extent.
- Ruranska, P. et al. (2020, 2022). Dry bulk density, loss on ignition, and OC content for surficial soils (English/Welsh and Scottish salt marshes).
- Miller, L.C. et al. (2022). Physical and geochemical properties of Scottish saltmarsh soils. Marine Scotland Data.