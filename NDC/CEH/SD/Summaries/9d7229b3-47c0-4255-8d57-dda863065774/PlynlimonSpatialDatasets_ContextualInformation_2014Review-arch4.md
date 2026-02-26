# Plynlimon Experimental Catchments

- Overview
  - Long-running hydrological study set up in the late 1960s by the Institute of Hydrology (IH), now part of CEH/NERC.
  - Located at the headwaters of the River Severn and River Wye in mid-Wales; compares upland land uses: coniferous forestry vs. sheep-grazed grassland.
  - Intensive instrumentation and detailed climatic, hydrological, and soil data; used to understand land-use impacts on water availability, flooding, and low flows.
  - Spatial and thematic datasets accompany the hydrological records, including maps and GIS-ready layers.

- Data assets (spatial datasets and layers)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Hydrologically corrected elevation grid (Plyn_DEM, GRID, 15 m cell size)
  - Background/topography and elevation data derived from aerial surveys and maps
  - Attribute highlights (e.g., LENGTH for river segments; FNODE/TNODE for network topology; HEIGHTS for elevations; SOIL codes and descriptions)

- Data creation and provenance
  - Aerial photography-based topographic foundation from the Hunting Survey (1967) used to produce 1:5000 scale maps (and 1:10000 derivatives).
  - Late 1990s digitisation of topographic/hydrography data into GIS layers (ArcInfo) from 1:5000 maps; contour lines captured at 10 m intervals (Severn lines captured separately at Edinburgh University with later line construction).
  - Soils: Bell’s 1969 Soil Hydrology map (IH Report No. 8) digitised; updated 2005 CEH edition available.
  - DEM creation workflow: integration of 1:5,000 contours, spot heights, stream maps, and catchment boundaries; hydrologically corrected DTM created via TIN to GRID (Plyn_DEM, 15 m cells).
  - Vegetation map development (2013): updated vegetation classes aligned with CEH Land Cover Map 2000 (LCM2000); enhanced to include heath, bracken, and improved grassland; workflow combined on-screen digitising with field verification (2013).
  - Appendix A describes the Hunting Survey aerial data, footprints, and technical specs; some film negatives lost but printed frames digitised.

- Data formats and structure
  - DEM: Plyn_DEM in GRID format (British National Grid; 15 m cells; floating point).
  - Vector layers: shapefiles with British National Grid CRS.
  - Layer-specific details:
    - Catchments: attributes include Catchment and Subcatch names.
    - River network: FNODE_/TNODE_ topology, LENGTH, Catchment, Type (natural/artefact).
    - Spot heights: HEIGHTS (elevation in metres).
    - Wye/S-Severn contours: HEIGHTS (contour elevations in metres).
    - Soil Parental Materials: SOIL code and Descript.
    - Vegetation map: id, VegClass, Varients (Variants for coniferous categories).
  - Vegetation map class integration included renaming/recoding to align with LCM2000 classes; enhanced for use in soil/land cover analyses.

- Data quality, gaps, and limitations
  - Some datasets are not available due to ownership/control by other organisations or data loss.
  - Older field surveys and maps may have incomplete or conflicting metadata; some topographic/land-use data require careful cross-checking.
  - Data lineage and provenance are documented, but access to certain layers may be restricted by IP rights or organizational boundaries.
  - The 2013 vegetation update acknowledges differences between aerial imagery (2009) and field observations (2013) due to timing, shade, and date discrepancies.

- Access, reuse, and related work
  - Foundational datasets are described for use in hydrological and environmental analyses; related CEH publications provide context and methodological details (e.g., Soil Hydrology of the Plynlimon Catchments; SoilTrEC project integration).
  - Primary sources and further information are available via the CEH website and CEH-science news pages.
  - Data useful for hydrological modelling, land-use impact studies, and geostatistical analyses, particularly when aligned with CEH models (LCM2000 reference) and soil/vegetation analyses.

- Notes for data governance and future considerations
  - Emphasises the importance of integrating diverse data types (topography, hydrology, soils, vegetation) into a coherent data system.
  - Highlights the need for metadata completeness, data standards adherence, and cross-institution collaboration to maintain discoverability and usability.
  - Data stewardship should address gaps, ownership issues, and ongoing updates to reflect new imagery and field observations.