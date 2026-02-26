# Social-economic-environmental trade-offs in managing the Land-River-Interface

## Overview
- A data-driven study linking human-driven changes in river flow and riparian land management to vegetation changes along the Sutlej and Beas Rivers in India.
- Vegetation and land cover quantified via winter-season NDVI trends (Punjab plains) and seasonal Landsat-based land cover classifications over a 30-year period.

## Data components
- River Section, Zone and Test Site delineation (plains; shapefiles)
- Winter Season average NDVI by section and zone (plains; 1989–2020; CSV)
- Landcover maps (seasonal; plains and upper Beas; GeoTIFF)
- Landcover fractions by section and zone (seasonally; plains; CSV)
- Test Site data and related NDVI/landcover metrics

## Scope and Spatial Extent
- Beas River: Pong Dam downstream to confluence with Sutlej
- Sutlej River: Bhakra Dam downstream to confluence with Beas
- Upper Beas: Palchan downstream to just upstream of Pong Dam (landcover only)
- Coordinate System: WGS84
- Geographic bounds: West 74.957, East 77.357, North 32.393, South 30.780

## Section, Zone and Test Site delineation
- Longitudinal sections defined from prior work; plains sections S0 (below dams) and S1–S4/5 in Punjab plains; Upper Beas divided into S1–S11 (with S5 and S3A referencing dam lakes).
- Geomorphic zones: Active Channel, Valley Bottom, Valley Slopes (derived from wetting patterns and geomorphon classification).
- Test sites in plains: Goindwal-Sahib (Beas S4), Zindanpur (Sutlej S1), Mau (Sutlej S3).

## Data generation and processing methods
- NDVI analysis
  - Winter Landsat (TOA) imagery 1989–2020; January–March window
  - Cloud masking with Google Earth Engine (GEE); water pixels via mNDWI threshold; NDVI averaged per year by section/zone
- Landcover mapping
  - Seasonal landcover maps (winter, pre-monsoon, monsoon, post-monsoon) produced in GEE using Gradient Tree Boost classifier (10 trees)
  - Spectral inputs: Landsat bands 1–7 (depending on sensor)
  - Training data created by manual inspection; separate training sets for plains vs. Upper Beas to account for spectral differences
- Landcover fractions
  - For each season, counts of pixels per class within each section/zone; fractions computed relative to total area
  - Includes analysis for test sites without section/zone differentiation

## Data formats and organization
- Formats: ESRI Shapefiles, CSV, GeoTIFF
- Two primary groups: Plains (below Bhakra/Pong Dams) and Upper Beas (above Pong Dam)
- File naming conventions:
  - Seasonally tiled landcover rasters with explicit naming for Plains vs. Upper Beas
  - CSVs providing training points, class keys, and NDVI summaries
- Key datasets include:
  - Sections.shp, TestSites.shp, Zones.shp (plains) and Sections Upper Beas.shp, UpBeas_Zones.shp (Upper Beas)
  - NDVI CSVs: SUTLEJ_BEAS_NDVI_1989_2020.csv; TEST_SITES_NDVI_1989_2020.csv
  - Landcover rasters and training data (multiple seasonal sets for Plains and Upper Beas)
  - Landcover fraction CSVs: Landcover Section and Zone.csv; Landcover Test Sites.csv; Upper Beas Landcover Section and Zone.csv

## Quality control and validation
- Cloud-free imagery selected using Landsat QA bands
- Validation against aerial imagery; quality checks by Cranfield University team
- Spectral consistency addressed by separate Plains vs. Upper Beas training datasets

## Project context and references
- Project SEELARI (NE/S01232X/1): Social-economic-environmental trade-offs in managing the Land-River-Interface
- Key methodological references: Gradient Tree Boosting (Friedman 2002), Google Earth Engine (Gorelick et al. 2017), geomorphon classification (Jasiewicz & Stepinski 2013)
- Related methodological work on river planform changes and multi-timescale dynamics (Vercruysse & Grabowski, 2021a, 2021b)

## How analysts can use this data
- Identify correlations between geomorphic changes (section/zone delineations, dam-induced planform changes) and vegetation responses (NDVI trends, landcover transitions)
- Compare landcover dynamics across seasons and between plains and upper Beas to assess regional differences
- Compute area-specific vegetation:water distribution shifts and their relation to river channel modifications
- Build predictive or scenario models to explore socio-economic-environmental trade-offs at the land-river interface
- Reproduce or extend analyses with the provided training points, classification outputs, and zonal statistics

## Considerations and limitations
- Scale sensitivity: some targets are at coarse grid/seasonal resolutions; local, fine-scale patterns may require higher-resolution data
- Spectral differences between plains and upper Beas necessitate separate training datasets
- Data accessibility and integration across multiple formats and portals may require careful data management

## Contact
- Dr Robert Grabowski
- Email: r.c.grabowski@cranfield.ac.uk
- Tel: +44 (0) 1234 758360