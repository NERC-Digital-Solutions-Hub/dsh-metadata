# Plynlimon experimental/research catchments

- Overview
  - Plynlimon catchments (late 1960s) were established by the Institute of Hydrology (IH) as part of NERC, later CEH.
  - Main aim: understand how land use affects catchment water availability, flooding, and low flows downstream.
  - Two adjacent catchments represent main upland land uses in Wales: coniferous forestry and sheep-grazed grassland; chosen to be similar in other environmental respects.
  - Intensive instrumentation provides long-term climatic, hydrological, and soil moisture data; comprehensive surveys of physical characteristics and land use accompany the datasets.

- Data layers and datasets (spatial coverage)
  - Plynlimon Spatial datasets include:
    - Catchment and subcatchment boundaries
    - River network
    - Spot heights
    - Wye catchment contour lines
    - Severn catchment contour lines
    - Soil parental materials
    - Vegetation map (updated 2013)
  - Plynlimon hydrologically corrected elevation grid (DTM/DEM) created for hydrological analysis.

- Source maps and topographic data
  - Hunting survey (1967) produced large-scale topographic maps with streams, forest drains, tracks, and fences.
  - In the late 1990s, maps were digitised into GIS layers (elevation, catchment boundaries, river network).
  - Earlier field surveys mapped soils, geology, vegetation, and land use; some datasets remained unavailable due to ownership or loss.

- Topography, hydrography, soils
  - Topography: maps at 1:5,000 and 1:10,000 with 2.5 m contour intervals; references to IH/NERC publications (1968).
  - Hydrography: main channels and forest drains captured on topographic maps; catchment boundaries digitised.
  - Soils: Bell’s Soil Hydrology Map (1968–69) showing soil parent materials; updated 2005 CEH version available.

- Digitising hard copy maps
  - All layers (except Severn contours) digitised at CEH using CALCOMP digitising table; GCPs used to register maps; elevation points and contours captured at 10–20 m intervals.
  - Severn catchment contours captured at Edinburgh University and converted from points to lines.

- Creation of hydrologically corrected elevation grid
  - Inputs: 1:5,000 contours, spot heights, stream maps, catchment boundaries.
  - Process: data integrated in ArcInfo; TIN created and converted to a hydrologically corrected grid DEM.
  - Output: Plyn_DEM (Grid, 15 m resolution, British National Grid).

- File formats and attributes
  - Catchment boundaries: PlynimonCatchments.shp (BNG); attributes include Catchment and Subcatchment names.
  - River network: PlynlimonRiverNetwork.shp; attributes include FNODE, TNODE, LENGTH, Catchment, Type (natural or artificial).
  - Spot heights: PlynlimonSpotHeight.shp; attribute HEIGHTS (m).
  - Wye elevation contours: Plynlimon_WyeElevationContours.shp; attribute HEIGHTS (m).
  - Soil parental materials: Plynlimon_SoilParentalMaterials; attributes SOIL and Descript.
  - Vegetation map: Plynlimon_VegetationMap2013; attributes id, VegClass, Variants.
  - Severn elevation contours: Plynlimon_SevernElevationContours.shp; attribute HEIGHTS (m).
  - Coordinate systems consistently in British National Grid.

- Vegetation mapping (2013)
  - Background: CEH Land Cover Map 2000 (LCM2000) used as base; updated to include heath, bracken, and improved grassland for soil property analyses (e.g., SoilTrEC project).
  - Method: draft map created from 2009 Next Perspectives aerial photography; field validation conducted (2013); ArcGIS 10.1 used for digitising and editing.
  - Reclassification: some classes merged (e.g., rough acid grassland to acid grassland; coniferous plantation variants treated to support use as conifer woodland or plantation).
  - Output: Plynlimon_VegetationMap2013 with class codes and descriptions, including Variants for plantation status.

- Appendix A: Hunting Survey
  - Provides context for the aerial survey; notes that film negatives are lost but printed frames have been digitised and rectified to preserve data.
  - Footprints of the aerial frames documented.

- Data governance and accessibility considerations
  - Some historical data are unavailable due to ownership or loss; ongoing digitisation and metadata practices are implied.
  - Datasets are designed to support hydrological and environmental analysis, with clear coordinate systems, attribute schemas, and documented derivation processes.
  - The vegetation and soil datasets were integrated to support more advanced analyses (e.g., geostatistical analyses linked to SoilTrEC outputs).