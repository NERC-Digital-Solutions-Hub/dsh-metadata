# Plynlimon experimental catchments

## Overview
- Run since the late 1960s by the Institute of Hydrology (IH) as part of NERC, now CEH.
- Aim: understand how land use affects catchment water availability, flooding, and low flows.
- Two adjacent catchments represent coniferous forestry vs sheep-grazed grassland, with long-term climatic and hydrological records.
- Datasets include maps, topography, soils, land use, and hydrological measurements gathered from the headwaters of the River Severn and River Wye.

## Data assets and layers
- Spatial datasets
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye and Severn elevation contours (Plynlimon_WyeElevationContours.shp; Plynlimon_SevernElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid
  - Plyn_DEM (GRID, 15 m cell size, British National Grid)
- Attributes (examples)
  - River network: FNODE_, TNODE_, LENGTH, Catchment, Type
  - Contours: HEIGHTS (metres)
  - Vegetation: id, VegClass, Varients
- Data provenance
  - Digitised from 1967-68 Hunting aerial survey and other field surveys
  - Some datasets owned by others; some data lost
  - SoilHydrology map Bell 1969; CEH 2005 revision available
- Vegetation mapping
  - Updated 2013 vegetation map aligned to CEH Land Cover Map 2000 (LCM2000), with on-screen digitising and field verification (2013)
  - Classes updated (e.g., conifer plantations reclassified; a Variants column added for flexibility)

## Data creation and workflows
- Digitising of hard-copy maps
  - CALCOMP digitising table; ground control points; elevations and contours captured
  - Data stored as ArcInfo coverages
- Contour and topography
  - Severn contours digitised at Edinburgh University; later cleaned and merged
- Hydrologically corrected DEM
  - DTM created from contour maps, spot heights, river networks, and catchment boundaries using a TIN-based workflow
  - Result: Plyn_DEM GRID (15 m, floating point, British National Grid)
- Data integration
  - ArcInfo workflow to combine datasets into usable GIS layers
  - Appendix A details the Hunting Survey and its footprints

## Data formats, standards, and accessibility
- Coordinate system: British National Grid
- Primary formats: shapefiles for boundaries, networks, heights, contours, soils, vegetation; GRID for DEM
- Accessibility notes
  - Data referenced on CEH site; some datasets with restricted access or owned by other bodies
  - Soil hydrology update and related publications available via CEH

## Applications, use cases, and value
- Supports hydrological research, runoff and flood analysis, and land-use impact studies in upland catchments
- Vegetation and soils data feed geostatistical analyses (e.g., SoilTrEC project) and model inputs
- Provides baseline spatial framework for hydrology and land-use interactions in CEH models

## Challenges and considerations for Data Leaders
- Data fragmentation and custodianship: some datasets owned by other organisations; some data lost
- Discoverability and metadata gaps due to dispersed sources
- Data standardization needs: vegetation mapping aligned to LCM2000; maintaining compatibility for modelling
- Temporal validation: field verification conducted years after imagery; integration of multi-temporal data
- Access and archival risk: reliance on older film negatives and multiple data origins

## Endnotes and references
- Brandt, Robinson, and Finch (2004) on project aims
- Bell (1969) and CEH 2005 revision: Soil Hydrology of the Plynlimon Catchments
- Appendix A: Hunting Survey details (1967 aerial survey; footprints of frames)