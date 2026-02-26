# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

## Overview
- Purpose: produce map-ready deposition and concentration data for UK protected sites to support assessment of exposure and policy analysis.
- Scope: integrates CBED deposition maps (5x5 km grid) with PCM concentration maps (1x1 km grid) for SAC, SPA and SSSI sites, focusing on 2017–2019 three-year rolling means.
- Outputs: datasets suitable for GIS visualisation and spatial analysis, including minimum, maximum, and grid-average values per site.

## Data sources and boundaries
- Protected sites: SAC, SPA, SSSI/ASSI boundaries downloaded from national portals and clipped to UK grid grids.
- CBED data: derived from concentration-based deposition estimates for nitrogen and sulphur species; includes wet and dry deposition components.
- PCM data: 1x1 km background concentration maps for multiple pollutants; includes road-side values and projections for policy analysis.
- Time frame: 3-year rolling means (2017–2019); non-marine Ca+Mg values at non-marine years limited to 2019 in some datasets.
- Units:
  - Deposition: kilo-equivalents per hectare per year (keq ha-1 year-1); conversions provided for S and N to kg ha-1 year-1.
  - Concentrations: micrograms per cubic metre (µg m-3).

## Grid mapping and data integration
- Step 1: Create a UK-wide 5x5 km grid, clip to SAC/SPA/SSSI boundaries, and merge with the 3-year CBED output to produce a UK protected sites CBED dataset (plus specific 1x1 km NOx and SO2 concentration datasets).
- Step 2: For each protected site, compute:
  - Grid-average deposition/concentration values by weighting grid cell values by area overlap with the site (GridArea / SiteArea) and summing across cells.
  - Use a site-level equation: CBEDDepositionValue × (GridArea / TotalSiteArea) to obtain grid-average deposition, then sum across the site’s clipped grid cells.

## CBED modelling details
- What CBED models provide:
  - Wet deposition: from gas/particle concentrations and an annual precipitation map; includes occult deposition (direct deposition from cloud droplets) and an orographic enhancement factor for upland regions (based on field studies).
  - Dry deposition: gas and PM deposition to vegetation with land-cover-specific deposition velocities across five categories (forest, moorland, grassland, arable, urban).
  - Seasonal/annual variability: inter-annual variation recognized; results are averaged over a rolling 3-year period to reduce variability.
  - Ecosystem-specific deposition: separate deposition values for moorland and forest; grid-average values derived from these ecosystems per 5x5 km cell.
- Outputs: per-grid-square and per-site deposition values for 3-year means; values reported for multiple nitrogen and sulfur species (e.g., NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg NM).

## PCM modelling details
- Purpose: produce 1x1 km background concentration maps for UK pollutants in support of EU reporting requirements and policy assessment.
- Features:
  - Separate models per pollutant (e.g., NOx, NO2, SO2, PM, etc.) with base-year and projection runs.
  - Outputs include roughly 9,000 road-side values in addition to grid-background maps.
  - Used for scenario assessments and to aid Time Extension Notifications (TEN) where applicable.

## Output structure and data files
- Data are organized into multiple CSV files (by grid, by site, and by ecosystem type) with fields including:
  - SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY/DESIGNATION, YEAR, GRIDAREA.
  - Deposition fields: NH3/NH4, NO2/NO3, SO2/SO4, CA/MG_NM (various composite categories), each with MIN, MAX, AVG and/or GRIDAVERAGE as applicable.
  - Concentration fields: NH3_CONC, NO2_CONC, SO2_CONC, and related MIN/AVG/MAX per site or grid.
- Example data organization:
  - Files 1–3: deposition by grid (forest, moorland, or grid-average) at 5x5 km resolution.
  - Files 4–6: ammonia, NOx, and SO2 concentrations by grid at 1x1 km resolution.
  - Files 7–9: minimum, maximum, and average deposition by site for different ecosystem types (forest/moorland) at 5x5 km or grid-average resolutions.
  - Files 10–12: concentration data by site and by grid (ammonia, NOx, SO2) with MIN/AVG/MAX values.
- Purpose: these structured outputs support map-making and spatial queries in GIS, enabling per-site aggregation and visualization of deposition and concentration patterns.

## Quality control and validation
- Methods aligned with government QA practices and peer-reviewed validation:
  - CBED data and calculations undergo extensive peer review and inter-comparison exercises.
  - Version control, documented method changes, and centralized storage.
  - Mass-balance checks and cross-year consistency with published work in the field.

## Practical considerations for GIS work
- Multi-resolution integration: combine 5x5 km deposition data with 1x1 km PCM concentration data and protect-site polygons for rich map products.
- Temporal aspect: results reflect 3-year rolling means; suitable for trend-aware mapping but not single-year snapshots.
- Data interpretation: use GridArea/SiteArea weighting to understand how grid-level data contribute to site-scale values; be mindful of ecosystem weighting (moorland vs forest) in deposition values.
- Recommended workflow: join site-boundary polygons to 5x5 km grid deposition layers and 1x1 km concentration layers, compute per-site min/max/avg values, and create standard map templates for communication with policy colleagues or the public.