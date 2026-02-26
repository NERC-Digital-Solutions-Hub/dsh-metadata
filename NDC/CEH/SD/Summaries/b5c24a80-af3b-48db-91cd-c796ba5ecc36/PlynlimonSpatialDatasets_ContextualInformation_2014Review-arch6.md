# Plynlimon Experimental Catchments

- Overview
  - The Plynlimon experimental/research catchments (late 1960s) study how land use (conifer forestry vs sheep-grazed grassland) affects catchment water availability, flooding, and low flows in the headwaters of the River Severn and River Wye in mid-Wales.
  - The project collected high-quality, long-term climatic, hydrological, soil, topographic, and land-use data, with themes mapped to support analysis and modelling.

- Spatial datasets and grid (Plynlimon Spatial Datasets)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Plynlimon hydrologically corrected elevation grid (Plyn_DEM; GRID)
  - Coordinate system: British National Grid; data in vector shapefiles and a 15 m grid DEM (floating point)

- Data creation and provenance
  - Source maps from the Hunting Survey aerial photography (1967-68) produced large-scale topographic maps with contour lines, streams, drains, and tracks.
  - In the late 1990s, topographic and hydrographic data were digitised into GIS layers (Arcinfo) using photogrammetric-derived elevation, catchment boundaries, and river networks.
  - Some field surveys mapped soils, geology, vegetation, and land use; some data are unavailable due to ownership or loss (an exception is Bell’s 1969 Soil Hydrology map, later revised by CEH in 2005).
  - The Severn catchment contour data were captured at Edinburgh University from 1:5000 maps and converted to lines.

- Hydrologically corrected elevation model (DEM)
  - DEM created by integrating 1:5,000 contours, spot heights, stream maps, and catchment boundaries.
  - A TIN was used to derive a hydrologically corrected grid-based DEM (Plyn_DEM): 15 m cell size, British National Grid, floating-point format.
  - A flow diagram in the accompanying documentation outlines the production steps.

- Vegetation mapping (method and updates)
  - Base used CEH Land Cover Map 2000 (LCM2000) for consistency with CEH models; updated to include heath, bracken, and improved grassland.
  - Vegetation draft created by interpreting 2009 aerial photography (Next Perspectives); refined through ArcGIS 10.1 digitising and field verification (2013).
  - Differences between draft and field observations due to photograph date (2009) vs field survey (2013) and shading effects.
  - Final vegetation map (Plynlimon_VegetationMap2013) aligns with LCM2000 classes; conifer categories are facilitated by a Variants field to distinguish woodland vs felled/new plantation.

- Data products and accessibility
  - Vector layers and the DEM provide a self-contained data suite for hydrological and land-use analyses.
  - The CEH website hosts project information and related publications; the vegetation mapping was produced to support SoilTrEC analyses (soil carbon data in the top 30 cm, 2012).

- Data limitations and notes
  - Some datasets are not available due to IP restrictions or loss of data; there is incomplete access to certain field-mapped characteristics from early surveys.
  - The Hunting Survey film negatives are lost, but portions were digitised to preserve footprints of the frames.
  - The dataset package emphasizes data provenance, with explicit references to Bell (1969), IH/CEH publications, and CEH methodologies.

- Appendix and references
  - Appendix A: Hunting Survey details and digitisation workflow.
  - Key references include Brandt et al. (2004) on the project aims and the Soil Hydrology study by Bell (1969) and its 2005 CEH revision.