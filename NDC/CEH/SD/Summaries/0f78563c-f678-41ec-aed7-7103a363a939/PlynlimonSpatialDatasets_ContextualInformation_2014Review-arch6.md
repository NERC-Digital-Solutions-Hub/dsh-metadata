# Plynlimon experimental/research catchments

## Overview
- Plynlimon catchments in mid-Wales host the headwaters of the River Severn and River Wye.
- Set up in the late 1960s by IH (NERC) to study how upland land use (conifer forestry vs sheep-grazed grassland) affects catchment water availability, flooding, and low flows.
- The catchments were intensively instrumented with long-term climatic and hydrological records and associated surveys to map physical characteristics and land use.
- Datasets and maps were created to support analysis and public data exploration, including various GIS layers and a hydrologically corrected digital terrain model (DTM).

## Data assets (GIS layers and products)
- Catchment and subcatchments boundaries (PlynlimonCatchments.shp)
- River network (PlynlimonRiverNetwork.shp)
- Spot heights (PlynlimonSpotHeight.shp)
- Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
- Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
- Soil parental materials (Plynlimon_SoilParentalMaterials)
- Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid (Plyn_DEM; GRID, 15 m cells)
- Coordinate system: British National Grid; data designed for GIS display and analysis
- Key attributes include catchment/subcatchment names, river segment endpoints, line lengths, soil codes/descriptions, vegetation class codes/descriptions, and contour elevations

## Data creation and processing
- Topography and maps
  - Original large-scale topographic maps from Hunting survey (1967–68) used to derive elevation, catchment boundaries, river network, and drainage features
  - 1:5,000 scale maps with 2.5 m contours; 1:10,000 scale maps produced from photogrammetric reduction
  - Elevation data used to derive hydrologically corrected DTM (15 m grid) via TIN interpolation
- Digitising of hard copy maps
  - Most layers digitised at CEH from 1:5,000 maps; Severn contours digitised at Edinburgh University
  - Ground control points (GCPs) used for registration; data saved as ArcInfo coverages
- Hydrologically corrected DEM
  - Integrated 1:5,000 contours, spot heights, stream maps, and catchment boundaries
  - Created a TIN, then hydrologically corrected grid-based DEM (Plyn_DEM)
- Vegetation mapping
  - Updated CEH Land Cover Map 2000 (LCM2000) as a base to avoid IPR issues with newer versions
  - Draft vegetation map created from 2009 Next Perspectives aerial photography, digitised in ArcGIS 10.1
  - Field validation: 2013 ground truthing; adjustments based on timing differences between 2009 imagery and 2013 observations
  - Classes aligned with LCM2000 with refinements:
    - Conifer plantation, new plantation, felled plantation
    - Rough acid grass, bracken, open dwarf shrub heath
    - Improved grassland, inland bare ground
    - Deciduous woodland, inland water
  - Final VegetationMap2013 includes an extra Variants field to flexibly treat coniferous plantations as woodland or plantation variants
- Contour lines and hydrography
  - Wye and Severn elevation contours created from digitised point data and clipped to respective catchments
  - Severn contours derived from Edinburgh University point dataset and converted to lines

## Source maps and provenance
- Hunting Survey aerial photography (June 1967) formed the basis for topographic maps
- 1967–68 imagery used to generate elevation, streams, drains, tracks, and fences
- Late 1990s digitisation converted topographic and hydrographic data into GIS layers
- Some field datasets (e.g., certain soil data) are held by other organisations or lost; Soil Parental Materials map (Bell 1969) is a key exception with a CEH 2005 update
- SoilHydrology of the Plynlimon Catchments (Bell, 1969; IH Report No. 8) remains a primary reference
- Vegetation update (2013) linked to SoilTrEC and CEH Land Cover Map 2000 classifications

## Appendix and background
- Appendix A Hunting Survey documents the 1967 aerial survey specifications, footprint of frames, and data preservation efforts
- The project environment and data products were intended to support long-term hydrological and land-use analyses, enabling researchers to explore patterns and relationships between land use, soils, vegetation, and hydrology

## Access and reuse notes
- Data are structured to enable use in GIS for self-service exploration (e.g., dashboards or pivot-like analyses in end-user tools)
- Some limitations exist due to data ownership (some datasets not available), data age, and the need for field validation where discrepancies occurred between imagery dates and on-ground conditions
- References include CEH project pages and SoilHydrology publications for deeper methodology and historical context