# Plynlimon Spatial datasets

## Overview
- Plynlimon experimental/research catchments (late 1960s) studied land-use impacts on catchment hydrology, particularly upland conifer forestry vs. sheep-grazed grassland.
- Rich, long-term climatic, hydrological, and spatial data collected; multiple thematic maps compiled.
- Primary aim for GIS-focused data products: enable map-based exploration and analysis of spatial attributes (topography, soils, vegetation, hydrology) across catchments.

## Data layers and grids
- Catchment and subcatchment boundaries (PlynlimonCatchments.shp; British National Grid)
  - Attributes: Catchment, Subcatch
- River network (PlynlimonRiverNetwork.shp; British National Grid)
  - Attributes: FNODE, TNODE, LENGTH, Catchment, Type (natural/ artificial)
- Spot heights (PlynlimonSpotHeight.shp; British National Grid)
  - Attributes: HEIGHTS (elevation in metres)
- Wye catchment contour lines (Plynlimon_WyeElevationContours.shp; British National Grid)
  - Attributes: HEIGHTS (contour elevation)
- Severn catchment contour lines (Plynlimon_SevernElevationContours.shp; British National Grid)
  - Attributes: HEIGHTS (contour elevation)
- Soil parental materials (Plynlimon_SoilParentalMaterials; British National Grid)
  - Attributes: SOIL, Descript
- Vegetation map (Plynlimon_VegetationMap2013; British National Grid)
  - Attributes: id, VegClass, Varients (variant descriptions)
- Hydrologically corrected elevation grid (Plyn_DEM, GRID; British National Grid)
  - Description: 15 m, floating point, hydrologically corrected digital terrain model (DTM)
- Background context: Aerial-derived topographic data and field-verified layers underpin several of the above datasets.

## Data creation and digitising workflow
- Source imagery and mapping
  - Hunting survey (1967–1968) provided large-scale topographic maps with key features (streams, forest drains, tracks, fence lines).
  - Late 1990s: topographic and hydrographic data digitised into GIS layers (elevation-derived DTMs, catchment boundaries, river network) from 1:5000 and 1:10000 maps.
- Digitising specifics
  - CEH digitised most layers on CALCOMP with ground control points; elevation and contour data captured at 10 m and 20 m intervals from 1:5000 maps (converted to Arcinfo).
  - Severn catchment contour lines digitised at Edinburgh University; contours captured as irregular point sequences later converted to lines.
- Data formats and environment
  - ArcInfo/ArcGIS workflows; shapefiles and GRID format used; coordinate system: British National Grid.

## Hydrologically corrected elevation model
- DEM construction workflow
  - Inputs: 1:5,000 contour maps (photogrammetric topography), spot heights, stream maps, and catchment boundaries.
  - Process: import into ArcInfo, build a TIN, derive a hydrologically corrected grid-based DEM (Plyn_DEM).
- Output
  - Plyn_DEM GRID, 15 m cell size, floating point, British National Grid.
  - Used to support hydrological analyses for the Plynlimon catchments.

## Vegetation mapping and background
- Vegetation map development (2013)
  - Base used: CEH Land Cover Map 2000 (LCM2000) as a standard; updated to better reflect heath, bracken, and improved grassland.
  - Data sources: draft map created by photo-interpretation of 2009 aerial photography; ground truthing in 2013.
  - Field verification: differences noted due to date gaps between photography (2009) and field checks (2013); adjustments made using ArcGIS 10.1 with aerial backdrop.
  - Reclassification and flexibility
    - Conifer plantation, new plantation, and felled plantation reclassified into coniferous woodland with a Variants field to preserve distinctions (felled/new plantation).
  - Final map: Plynlimon_VegetationMap2013
- Vegetation classes align with CEH LCM2000 categories; includes coniferous woodland, improved grassland, bracken, heath, bare ground, water, etc.

## Contour data and supplementary notes
- Wye and Severn elevation contours
  - Wye: Plynlimon_WyeElevationContours.shp (10 and 20 m intervals)
  - Severn: Plynlimon_SevernElevationContours.shp (10 m intervals)
- Appendix A Hunting Survey (aerial photography basis)
  - 1967 aerial photography by Hunting Survey Ltd; film negatives lost, but prints digitised and rectified to preserve frame footprints.

## Background and context
- Rich historical datasets support hydrological and land-use analyses for the two upland land-use types in mid-Wales.
- Data intended to support cross-disciplinary modelling (e.g., soil, vegetation boundaries, climate, hydrology) and later SoilTrEC project activities.
- Some datasets are incomplete or unavailable due to data ownership, loss, or archival gaps.

## Data availability and considerations
- Not all original field surveys are available; some datasets from other organisations are inaccessible or lost.
- Legacy formats and long-term archival practices require careful provenance and metadata review for reuse.
- All primary layers are tied to the British National Grid, with explicit scale/contour characteristics and attribute schemas to assist GIS integration and map-based analysis.