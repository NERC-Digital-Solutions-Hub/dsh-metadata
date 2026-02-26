# Plynlimon Catchments Spatial Datasets and Data Archive

- Aim and scope
  - Long-running experimental/research catchments in mid-Wales, headwaters of the River Severn and River Wye.
  - Compared land uses: coniferous forestry vs sheep-grazed grassland to study effects on hydrology, evaporation, flooding, and low flows.
  - Rich, long-term climatic, hydrological, soil, and land-use data beginning in the late 1960s.

- Data inventory (spatial datasets)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Hydrologically corrected elevation grid (Plyn_DEM GRID, 15 m cell size)
  - Coordinate system: British National Grid; formats include shapefiles and GRID

- Data sources and lineage
  - Hunting Survey (1967) used for large-scale topographic maps; later digitised in the 1990s into GIS layers.
  - Field surveys mapping soils, geology, vegetation, land use; some datasets not available due to ownership or loss.
  - Soil Hydrology study by J.P. Bell (1969); Institute of Hydrology Report No. 8; updated 2005 by CEH.
  - Severn contour lines digitised at Edinburgh University; later converted to line features.
  - Vegetation base aligned with CEH Land Cover Map 2000 (LCM2000); updated 2013 via interpretation of 2009 aerial photography and field verification (2013).

- Topography and hydrography details
  - Topographic maps at 1:5000 scale with 2.5 m contour intervals; 1:10000 scale with same contour interval.
  - Hydrographic features include main streams and forest drains; catchment boundaries derived from elevation data.
  - Hydrologically corrected digital terrain model (DTM) derived from a TIN built from contours, spot heights, streams, and boundaries.
  - Plynlimon DEM (Plyn_DEM) specifics: GRID format, 15 m resolution, floating point, British National Grid.

- Data creation workflow and provenance
  - Hard-copy maps digitised (CALCOMP) with ground control points; elevation and contour data captured at specified intervals; data stored as ArcINFO coverages.
  - Hydrologically corrected DEM produced via flow-structure: creating TIN from integrated datasets, then generating the hydrologically corrected grid.
  - Documentation includes a flow diagram (Figure 1) describing DEM production steps.

- Vegetation mapping methodology
  - Draft map created from 2009 Next Perspectives aerial photography; classes mapped in ArcGIS 10.1 and refined in the field (2013).
  - Major classes: conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water.
  - Final map aligns with LCM2000 classes with refinements; additional “Variants” column to differentiate plantation states (coniferous woodland vs felled/new plantation).
  - Vegetation map dataset: Plynlimon_VegetationMap2013; attributes include id, VegClass, Variants.

- Appendix A: Hunting Survey
  - Aerial photography survey from June 1967 by Hunting Survey Ltd; film negatives lost but printed frames digitised and rectified.
  - Footprints of all frames documented; used to inform topographic basemaps.

- Data accessibility and usage for analysts
  - Datasets curated to support hydrological modeling, land-use impact assessments, and geostatistical analyses (e.g., soil carbon studies within SoilTrEC context).
  - Metadata and dataset provenance are emphasized to enable reproducibility and data discoverability; data are suitable for integration in GIS analyses, hydrologic models, and landscape-scale studies.

- Limitations and challenges
  - Some datasets unavailable due to ownership or loss; some high-detail data restricted by IP or access barriers.
  Data across the archive originate from different time periods, scales, and methods, requiring careful handling when unifying datasets.
  Potential gaps at local scales or in boundary detail for certain layers.