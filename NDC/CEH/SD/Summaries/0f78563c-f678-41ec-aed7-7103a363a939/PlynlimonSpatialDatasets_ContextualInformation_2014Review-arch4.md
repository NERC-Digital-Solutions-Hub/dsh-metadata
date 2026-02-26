# Plynlimon Spatial datasets

- Overview and purpose
  - Long-running experimental/research catchments in mid-Wales (headwaters of the River Severn and River Wye) established in the late 1960s by the Institute of Hydrology (IH, later CEH) to study how upland land use (conifer forestry vs. sheep-grazed grassland) affects water availability, flooding, and low flows.
  - Both catchments were intensively instrumented; datasets include climatic, hydrological, soil moisture measurements and surveys of physical characteristics and land use.
  - Datasets were created to support hydrological and environmental research, with a focus on enabling cross-cutting analyses and comparisons across land uses.

- Core spatial data layers (The Plynlimon Spatial datasets)
  - Catchment and subcatchments boundaries (PlynlimonCatchments.shp) – upland catchments, subcatchments drained by major tributaries; British National Grid.
  - River network (PlynlimonRiverNetwork.shp) – network of streams and artificial/ natural channels; attributes include node IDs, length, catchment, stream type.
  - Spot heights (PlynlimonSpotHeight.shp) – elevation points; height in metres.
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp) – 10 and 20 m interval contours; British National Grid.
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp) – 10 m interval contours; British National Grid.
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials) – distribution of soil parent materials; attributes include soil code and description.
  - Vegetation map (Plynlimon_VegetationMap2013) – updated vegetation classes (derived to align with LCM2000 classes; field-validated against 2013 observations); British National Grid.
  - Hydrologically corrected elevation grid (Plyn_DEM) – 15 m grid, floating point; hydrologically corrected digital terrain model (DTM) used for hydrological analyses; file format GRID; coordinate system British National Grid.
  - Background and additional data (e.g., vegetation variants for coniferous woodland vs. felled/new plantation) to support model inputs and geostatistics.

- Data provenance, digitisation, and major data sources
  - Hunting Survey (1967) – initial large-scale topographic maps (1:5000; 2.5 m contours) used to derive elevation, catchment boundaries, river channels, forest drains, tracks and fences.
  - Late 1990s digitisation – topographic and hydrographic data converted into GIS layers (Arc/Info): elevation-derived DTM, catchment boundaries, river network.
  - Soil Hydrology Study (JP Bell, 1968–1969) – foundational soil parental materials map; Institute of Hydrology Report No. 8; CEH updated in 2005.
  - Topographic references – 1:5000 and 1:10000 scale maps with 2.5 m contours produced by IH/NERC (1968).
  - Vegetation mapping (2013 update) – drafted from 2009 aerial photography (Next Perspectives) and ground truthing (2013); aligned with CEH Land Cover Map 2000 (LCM2000) with refinements for heath, bracken, improved grassland, and conifer variants.
  - Severn contour data – captured as points from 1:5000 maps, converted to lines; edited for artefacts; clipped to Severn catchment.
  - Aerial photography archive and Appendix A – Hunting Survey prints digitised and preserved; footprints of frames documented.

- Data formats, standards, and technical implementation
  - Vector data stored as shapefiles with British National Grid projection; attributes describe geometry and thematic context (e.g., catchment, subcatchment, river type, contour height).
  - Hydrologically corrected DEM (Plyn_DEM) created by integrating 1:5,000 contours, spot heights, stream maps, and catchment boundaries; a TIN was generated and converted to a hydrologically corrected GRID DEM (15 m cell size).
  - Vegetation map uses ArcGIS 10.1 for digitising and editing; classes correspond to LCM2000 with specific reclassifications (e.g., conifer plantation variants, rough acid grassland reclassified to acid grassland).
  - Data management notes include acknowledging data that are owned by other organisations or lost, and IPR considerations affecting accessibility.

- Vegetation data specifics
  - Vegetation classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, and inland water.
  - The 2013 vegetation map was produced to support soil carbon and geostatistical analyses (e.g., SoilTrEC project) and to provide a more accurate overlay with LCM2000 classes; an additional variants column supports using coniferous woodland or plantation states.

- Access, governance, and data quality considerations
  - Some data are not available due to ownership, sharing restrictions, or loss of original datasets; other datasets are available via CEH resources and publications.
  - Metadata and provenance are documented to support discoverability and reuse; data standards (LCM2000 alignment, British National Grid, DEM generation methods) underpin reproducibility.
  - The dataset collection represents a long-term, integrated data system with evolution over decades, including updates (e.g., vegetation maps in 2013, soil update in 2005, soil carbon surveys in 2012).

- Appendix and archival context
  - Appendix A describes the Hunting Survey aerial photography and the digitisation/rectification process, including footprint documentation and data preservation efforts.

- Use cases and applications for data leaders
  - Supports hydrological analyses to understand how land use influences evaporation, runoff, and catchment hydrology.
  - Enables cross-catchment comparisons between coniferous forestry and grassland systems.
  - Provides a framework for integrating legacy survey data with modern GIS, enhancing data discoverability and reusability for current research (e.g., SoilTrEC and soil carbon studies).
  - Demonstrates long-term data stewardship challenges and the importance of maintaining metadata, provenance, and access controls across partners.