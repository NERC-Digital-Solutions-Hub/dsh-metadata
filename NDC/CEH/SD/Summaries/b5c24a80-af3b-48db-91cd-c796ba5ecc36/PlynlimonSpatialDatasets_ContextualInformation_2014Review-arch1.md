# Plynlimon Catchments Spatial Data and Datasets

## Overview
- Plynlimon experimental/research catchments established in the late 1960s by the Institute of Hydrology (IH), later part of CEH, to study land use impact on catchment water availability, flooding, and low flows.
- Two adjacent catchments represent upland Wales land uses: coniferous forestry and sheep-grazed grassland, designed to be similar in other environmental aspects.
- Intensive instrumentation provided long-term climatic, hydrological, and soil moisture data; surveys mapped topography, soils, land use, and vegetation.
- Datasets include multiple thematic maps and a hydrologically corrected digital terrain model (DTM/DEM) for hydrological analyses.
- Vegetation, soils, and land cover data updated with recent surveys to support analyses such as soil carbon studies (SoilTrEC project).

## Source Maps
- Initial large-scale topographic maps produced from Hunting survey aerial photography; later digitised into GIS layers.
- Some datasets are unavailable due to ownership or loss; the Soil Hydrology Study map (Bell 1969) is digitised and updated by CEH (2005).
- Maps and data capture include elevation, catchment boundaries, river networks, and other physical attributes.

## Topography
- 1:5,000 scale topographic maps with 2.5 m contour intervals; 1:10,000 scale maps with the same contour interval.
- Publications and references from 1968 detail the maps; aerial photography appendix describes survey specifics.
- Elevation data used to derive hydrologically corrected topography (DTM/DEM).

## Hydrography
- Main stream channels and forest drains shown on topographic maps.
- Catchment and subcatchment boundaries digitised; subcatchment boundaries inferred from elevation data, though not explicitly outlined on all maps.
- River network dataset includes segment endpoints and attributes (e.g., catchment, type: natural or artificial).

## Soils
- Bell, J.P. 1969 soil map (Soil Hydrology of the Plynlimon Catchments) shows distribution of soil parental materials; original IH Report No. 8 (50 pages).
- 2005 CEH revised version provided; available via CEH publications.
- Soil data underpin hydrological understanding of runoff processes.

## Digitising of Hard Copy Maps
- Datasets digitised at CEH using CALCOMP digitising table; ground control points (GCP) used for registration; elevation and contour data captured at 10–20 m intervals.
- Severn catchment contour data captured at Edinburgh University from 1:5,000 maps as irregular points, later converted to lines.

## Creation of Hydrologically Corrected Elevation Grid
- Input datasets: 1:5,000 contour maps, spot heights, stream networks, and catchment boundaries.
- Process: data imported into Arcinfo, TIN created, then hydrologically corrected grid-based DTM produced.
- Deliverables:
  - Plynlimon DEM (GRID, 15 m cells, floating point, British National Grid) named Plyn_DEM, description: hydrologically-corrected DEM for the catchments.
  - Catchment and subcatchments boundaries shapefile: PlynlimonCatchments.shp with attributes Catchment and Subcatch.
  - River network shapefile: PlynlimonRiverNetwork.shp with FNODE/TNODE, LENGTH, Catchment, Type.

## Data Layers (Shapefiles and Grids)
- Catchment and subcatchments boundaries (PlynlimonCatchments.shp).
- River network (PlynlimonRiverNetwork.shp).
- Spot heights (PlynlimonSpotHeight.shp).
- Wye catchment contour lines (Plynlimon_WyeElevationContours.shp).
- Severn catchment contour lines (Plynlimon_SevernElevationContours.shp).
- Soil Parental Materials (Plynlimon_SoilParentalMaterials).
- Vegetation map (Plynlimon_VegetationMap2013).

## Vegetation Map
- Updated vegetation map created to support SoilTrEC soil carbon analysis; base developed from CEH Land Cover Map 2000 (LCM2000) to include heath, bracken, improved grassland, etc.
- Method: draft vegetation classes interpreted from 2009 aerial photography, digitised in ArcGIS 10.1, field-checked in 2013, and updated to align with LCM2000 classes.
- Final map: Plynlimon_VegetationMap2013 with attributes id (code), VegClass (description), Varients (subclass description).
- Classes include conifer plantation/new plantation/felled plantation, coniferous woodland; grassland types; bracken; heath; bare ground; woodland; water features.

## Appendix A Hunting Survey
- Aerial photography survey conducted June 1967 by Hunting Survey Ltd; film negatives are lost but printed frames have been digitised and rectified.
- Footprints of each frame documented; technical specifications and frame footprints included in appendix.

## Background and Use
- Vegetation and soil data support broader research goals including SoilTrEC and model development.
- The combined datasets enable analyses of land-use impacts on hydrology, soils, and vegetation at a catchment scale, with attention to local detail and cross-dataset compatibility.