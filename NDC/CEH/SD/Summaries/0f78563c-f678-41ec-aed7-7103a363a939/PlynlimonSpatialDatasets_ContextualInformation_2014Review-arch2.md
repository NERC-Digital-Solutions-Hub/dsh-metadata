# Plynlimon Spatial datasets

- Overview
  - Plynlimon experimental catchments (late 1960s) studied how upland land use (conifer forestry vs. sheep-grazed grassland) affects catchment water availability, flooding, and low flows.
  - Two adjacent catchments contain the headwaters of the River Severn and River Wye; intensive instrumentation and long-term climatic, hydrological, and soil surveys underpin the data.
  - Aims include high-quality, long-term climate/flow/soil monitoring and development of a spatial data framework for analyzing environmental health and policy-relevant outputs.

- Datasets included (spatial layers and grid)
  - Catchment and subcatchments boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Plynlimon hydrologically corrected elevation grid (Plyn_DEM; 15 m grid, British National Grid)
  - Coordinate system: British National Grid; formats include GRID and shapefiles

- Data sources and history
  - Initial topography from the Hunting Survey (1967 aerial photography) used to produce large-scale 1:5000 and 1:10000 topographic maps with key features.
  - Late 1990s: digitisation of topo/hydro data into GIS layers (elevation, boundaries, river network).
  - Soil hydrology map derived from JP Bell’s 1968–1969 Soil Hydrology Study; IH Report No. 8; updated version published by CEH (2005) and available online.
  - Some field maps and data are unavailable due to rights or loss; exceptions include the Bell soil map (digitised in late 1990s).

- Topography and hydrography
  - Topographic maps created at 1:5000 (contour interval 2.5 m) and 1:10000 scales; used for delineating catchments and subcatchments.
  - Main streams and forest drains captured on 1967–68 maps; subcatchment boundaries derived from elevation data.
  - Hydrography-derived layers align with the photogrammetric topography to support hydrological analyses.

- Digitising and GIS creation
  - Data captured as ArcInfo coverages from scanned maps; calibration used ground control points (GCPs) for registration.
  - Elevation points and contours digitised at 10–20 m intervals; Severn contour lines captured separately at Edinburgh University (method not fully documented).
  - Hydrologically corrected DEM created via a TIN-based approach, then transformed into a grid (Plyn_DEM) with 15 m cell size; used to derive hydrologically correct terrain.

- Vegetation mapping
  - Updated vegetation map (Plynlimon_VegetationMap2013) to support soil carbon studies and CEH models; based on CEH Land Cover Map 2000 (LCM2000) and enhanced with 2009 aerial photography interpreted through ArcGIS 10.1, with 2013 field verification.
  - Classes include conifer plantations (and variants), new/felled plantations, rough acid grass, bracken, heaths, improved grassland, bare ground, inland water, and deciduous woodland.
  - Final product reclassified some LCM2000 classes (e.g., coniferous plantation variants) to improve consistency with CEH classifications; field checks resolved discrepancies.

- Soil information
  - Soil Parental Materials map documents distribution of soil types affecting hydrology; originally Bell 1969 (IH Report No. 8) with CEH 2005 update.
  - Used to inform soil hydrology understanding and model inputs.

- Data accessibility and usage
  - Some datasets are owned by other organisations or not publicly available; others are accessible via CEH resources.
  - The datasets are designed to be stored and uploaded to appropriate portals to support wide access and reuse, aligning with the Analysts Monitoring the Environment aim to increase data value and enable data access for downstream users.

- Appendix and provenance
  - Appendix A describes the Hunting Survey aerial photography used as the basis for the original topographic data.
  - The project provides a historical, well-documented chain of data creation, from aerial surveys to digital GIS layers and hydrologically corrected terrain models.

- Practical relevance for environmental monitoring
  - Enables standardized, long-term analyses of how upland land use influences hydrology, flood risk, and low-flow regimes.
  - Supports cross-layer analyses by linking boundaries, river networks, elevation, soils, and vegetation to environmental health outputs.
  - Demonstrates a reproducible workflow from photogrammetry to DEM creation and multiple derived geospatial datasets, suitable for integration into monitoring dashboards or policy performance assessments.