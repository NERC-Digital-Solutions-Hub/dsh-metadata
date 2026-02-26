# INTRODUCTION

- The Plynlimon experimental/research catchments (late 1960s) were created by the Institute of Hydrology ( IH, later CEH) to study how upland land use affects catchment water availability, flooding, and low flows downstream.
- Two adjacent catchments (Severn and Wye headwaters in mid-Wales) represent two major upland land uses: coniferous forestry and sheep-grazed grassland, chosen to be as similar as possible in other environmental respects.
- Intensive instrumentation and long-term climatic, streamflow, and soil moisture records were collected; surveys mapped topography, soils, vegetation, and land use; datasets include various thematic maps.

- Primary data aim: enable analysis of land-use effects on hydrology through high-quality, long-term measurements and spatial datasets.

- Spatial datasets available include:
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
  - Hydrologically corrected elevation grid (Plynlimon DEM)

- Core data sources and timeline:
  - Initial topographic maps produced from the Hunting survey (1967 aerial photography)
  - Late 1990s: digitisation of maps into GIS layers (elevation, catchment boundaries, river network)
  - Field surveys mapped soils, geology, vegetation, and land use (some datasets owned by others or lost)
  - Soil Hydrology study by J.P. Bell (1968–1969) produced the soil parental materials map; updated version published in 2005

- Data processing and GIS implementation:
  - Topographic maps at 1:5,000 (contours 2.5 m) and 1:10,000 converted to digital layers
  - Arcinfo used for digitising; Ground Control Points (GCPs) registered maps; elevation and contour data captured at 10 and 20 m intervals
  - Severn catchment contours digitised at Edinburgh University (method not fully documented)

- Hydrologically corrected elevation grid (Plynlimon DEM):
  - DEM created from a hydrologically corrected Digital Terrain Model (DTM)
  - Input data: 1:5,000 contour maps, spot heights, stream maps, catchment boundaries
  - Process: import into Arcinfo, build a TIN, derive hydrologically corrected grid
  - DEM details: Plyn_DEM GRID, 15 m cell size, floating point, British National Grid

- Data files and their purposes (sample of key layers):
  - PlynlimonCatchments.shp: catchment and subcatchment boundaries
  - PlynlimonRiverNetwork.shp: river network with FNODE, TNODE, LENGTH, Catchment, Type
  - PlynlimonSpotHeight.shp: spot elevations
  - Plynlimon_WyeElevationContours.shp: Wye contours (10 and 20 m)
  - Plynlimon_SevernElevationContours.shp: Severn contours (10 m)
  - Plynlimon_SoilParentalMaterials: soil parent materials with SOIL code and Descript
  - Plynlimon_VegetationMap2013: updated vegetation map (see method below)

- Vegetation mapping: background and approach
  - Base: CEH Land Cover Map 2000 (LCM2000) due to standard usage and to avoid IPR conflicts with LCM2007
  - 2012 soil carbon survey motivated integration of vegetation data for geostatistical analysis
  - 2013 field-checked map produced by digitising 2009 aerial photography in ArcGIS 10.1
  - Draft map classes interpreted from 2009 aerials; field observations in 2013 refined classifications
  - Classes align with LCM2000; notable reclassifications:
    - Rough acid grassland -> Acid grassland
    - Conifer plantation, new plantation, felled plantation -> coniferous woodland
  - An additional column (Variants) captures subtypes (e.g., felled/new plantation vs. woodland)
  - Final dataset: Plynlimon_VegetationMap2013 with id, VegClass, Variants

- Vegetation classification scheme (10 main classes)
  - Conifer plantation
  - New plantation
  - Felled plantation
  - Rough acid grass
  - Bracken
  - Open dwarf shrub heath
  - Improved grassland
  - Inland bare ground
  - Deciduous woodland
  - Inland water

- Data provenance and access considerations
  - Some datasets not available due to ownership or loss; some data from other organisations
  - Aerial photography and mapping data include the 1967 Hunting Survey; film negatives lost, but printed frames digitised
  - Updated vegetation map relies on 2009 aerials with 2013 field verification
  - Data formats and standards used for interoperability (Arcinfo/ArcGIS; British National Grid)

- Appendix and supporting context
  - Appendix A: Hunting Survey details; footprint and technical specs of the 1967 aerial photography
  - Key references: Brandt et al. (2004) on hydrology–physical attribute relationships; Bell (1969) on soil hydrology; IH Report No. 8 (1969) and its 2005 CEH revision

- Summary of purpose and use
  - The collection provides a long-term, multi-layer hydrological dataset to support analysis of land-use impacts on catchment hydrology
  - THE data support hydrological modelling, correlation analyses between land use, soils, vegetation, and hydrological response, and geostatistical work (e.g., SoilTrEC)
  - All layers are prepared for GIS analysis, with explicit metadata about structure, coordinate system, and attributes to facilitate discovery and reuse