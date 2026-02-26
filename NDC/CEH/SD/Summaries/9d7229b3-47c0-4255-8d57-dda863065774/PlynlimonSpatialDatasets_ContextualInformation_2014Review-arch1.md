# Plynlimon Experimental Catchments

- Purpose and context
  - A long-term hydrological research project established in the late 1960s by the Institute of Hydrology (IH) to understand how upland land use affects catchment water availability, flooding, and low flows.
  - Located at the headwaters of the River Severn and the River Wye in mid-Wales, representing two main upland land uses: coniferous forestry and sheep-grazed grassland.
  - Intensive instrumentation and long-term climatic, hydrological, and soil data collection complemented by spatial surveys of topography, soils, vegetation, and land use.
  - Data support ongoing analyses of land-use impacts and model development; information on related projects (e.g., SoilTrEC) and CEH dissemination is available.

- Spatial data layers and grid (Plynlimon Spatial datasets)
  - Catchment and subcatchment boundaries; river network; spot heights.
  - Elevation contour data for Wye and Severn catchments; soil parental materials; vegetation map.
  - Hydrologically corrected elevation grid (DTM): PlynlimonDEM (GRID, 15 m cells, British National Grid).
  - Shapefiles describing: catchments (PlynlimonCatchments.shp), river network (PlynlimonRiverNetwork.shp), spot heights (PlynlimonSpotHeight.shp), Wye contours (Plynlimon_WyeElevationContours.shp), Severn contours (Plynlimon_SevernElevationContours.shp), soil parental materials (Plynlimon_SoilParentalMaterials), vegetation map (Plynlimon_VegetationMap2013).

- Data sources and historical context
  - Aerial photography from the Hunting Survey (1967) used to produce large-scale topographic maps (1:5000, 2.5 m contours) and to identify streams, drains, tracks, and fences.
  - In the late 1990s, topographic/hydrographic data were digitised into GIS layers (elevation from which hydrologically corrected DTMs were derived).
  - Some field-derived datasets still exist but some are owned by other organizations or have been lost; a key soil map (Bell, 1969) and IH Report No. 8 (revised 2005) provide soil parental materials data.

- Digitisation and data creation process
  - Most shapefiles digitised at CEH using CALCOMP digitising tablet; registration with ground control points; elevation and contour points captured at 10–20 m intervals from 1:5000 maps and saved as ArcInfo coverages.
  - Severn catchment contours digitised separately at Edinburgh University from 1:5000 maps; points converted to lines and cleaned to produce usable contours.
  - Hydrologically corrected DTM created by integrating contours, spot heights, stream maps, and catchment boundaries; a TIN was generated and converted to a hydrologically corrected GRID (Plyn_DEM).

- Data structure and metadata
  - File formats: GRID (Plyn_DEM), shapefiles for boundaries, networks, heights, contours, soils, vegetation.
  - Coordinate system: British National Grid.
  - Attributes of datasets include identifiers, line/point geometry details, catchment associations, stream type (natural/artificial), and height/elevation values.
  - Vegetation map development (2013): updated from CEH Land Cover Map 2000 (LCM2000) to include heath, bracken, improved grassland, and other classes; draft map produced from 2009 aerials, refined with ArcGIS 10.1 and ground truthing in 2013; conifer-related classes subdivided with a Variants field to support both LCM2000-compatible and plantation-specific analyses.

- Vegetation mapping methodology and classifications
  - A broad class scheme aligned with LCM2000, including conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, and inland water.
  - Final digital vegetation layer: Plynlimon_VegetationMap2013 with fields for id, VegClass, and Variants; rigorous editing against 2009 aerials and 2013 field observations to correct dated imagery issues and map features not previously captured.

- Appendices and background information
  - Appendix A: Hunting Survey provides technical context for the aerial photography basis and digitisation footprints (1967).
  - Background notes emphasize data alignment with SoilTrEC and integration with soil carbon surveys; rationale for choosing base vegetation data (LCM2000) to minimize IP conflicts and to support downstream geostatistical analyses.

- Practical implications for data users and analysts
  - Rich, multi-temporal, and multi-source spatial dataset suite suitable for hydrological modelling, land-use impact assessment, and landscape-scale analyses.
  - Comprehensive metadata and documented derivation processes enhance traceability and reproducibility of analyses.
  - Some data gaps and rights-related access limitations noted; certain datasets may be missing or held by other organizations, which can affect data completeness and local-level analyses.
  - The data are designed for integration with other CEH data products and projects (e.g., SoilTrEC), facilitating advanced ecological and hydrological investigations.