# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model rv4.36 and WRF model v4.1.1.
- Intended for map-based analysis and spatial visualization of atmospheric deposition patterns.

## What is included
- Modelled annual total deposition data for the UK, including:
  - Dry deposition of oxidised sulphur (SOx) and oxidised nitrogen (OXN)
  - Dry deposition of reduced nitrogen (RDN)
  - Area-weighted and land-cover specific deposition (e.g., coniferous forest, deciduous forest, coniferous crops, semi-natural, water)
- Units and grid information are defined per variable (e.g., mgS/m2, mgN/m2; Area_Grid_km2).

## Spatial and temporal scope
- Temporal: annual totals for 2018.
- Spatial: UK domain nested within a EU-wide model grid.
  - UK native resolution: 1 x 1 km2.
  - Outer EU domain: 27 x 27 km2.
  - Only UK model results are included here.

## Data format and projection
- File format: NetCDF (example dataset EMEP4UK_2018_fullrun).
- Projection: polar stereographic grid.
  - Proj4 string: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs
- Requires a NetCDF library compatible with R, Python, or FORTRAN.

## Variables, content, and units
- Area and deposition data:
  - Grid area: Area_Grid_km2 (km2)
  - Dry deposition for various species and targets, with NetCDF variable names like:
    - DDEP_SOX_m2Grid (dry deposition of oxidised sulphur, area weighted)
    - DDEP_SOX_m2Conif (to coniferous forest)
    - DDEP_SOX_m2Seminat (to semi-natural)
    - DDEP_SOX_m2Water_D (to water)
    - DDEP_OXN_m2Grid / DDEP_OXN_m2Conif / DDEP_OXN_m2Seminat / DDEP_OXN_m2Water_D / DDEP_OXN_m2Decid / DDEP_OXN_m2Crops (oxidised nitrogen)
    - DDEP_RDN_m2Grid / DDEP_RDN_m2Conif / DDEP_RDN_m2Seminat / DDEP_RDN_m2Water_D / DDEP_RDN_m2Decid / DDEP_RDN_m2Crops (reduced nitrogen)
- Land-cover specific deposition targets are provided (coniferous forest, semi-natural, water, deciduous forest, coniferous crops).

## NetCDF structure (example)
- Main dimensions: time (unlimited), i (765), j (1254)
- Variables include:
  - time: days since 1900-01-01
  - i: EMEP grid x-coordinate (km)
  - j: EMEP grid y-coordinate (km)
  - lon: longitude (deg)
- The dataset exposes standard NetCDF conventions for time and spatial coordinates.

## Data quality and provenance
- QA/QC: simple QA/QC performed for 2018; reports available on request.
- Models (WRF and EMEP4UK) are peer-reviewed and widely used; emissions inputs cross-checked against official inventories.
- Note: Content is provided without warranty; suitability for a given use is the user’s responsibility.

## Usage guidance for GIS
- Suitable for map-based visualizations of deposition patterns at 1 km UK resolution.
- Ensure correct handling of NetCDF data and the polar stereographic projection in GIS software.
- Align with other UK atmospheric deposition datasets by reprojecting if necessary to a common CRS.
- Data is suitable for policy analysis, client reporting, and public-facing maps that illustrate spatial deposition burdens and land-cover-specific deposition.

## Access, provenance, and references
- Data produced from EMEP4UK rv4.36 with WRF v4.1.1.
- UK emissions inputs: rescaled 2019 National Atmospheric Emission Inventory to 2018; non-UK emissions from CEIP at 0.1° resolution.
- Emissions and model details cited in associated publications and NATO/NAEI references.
- Primary references include model descriptions and supporting literature (specific citations provided in the document).