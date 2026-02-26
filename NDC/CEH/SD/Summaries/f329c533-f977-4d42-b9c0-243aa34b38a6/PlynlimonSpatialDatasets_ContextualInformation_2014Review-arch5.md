# INTRODUCTION

- Project background and aim
  - Plynlimon experimental/research catchments established in the late 1960s by the Institute of Hydrology (IH), later part of CEH, to study how land use affects catchment water availability, flooding, and low flows.
  - Paired catchments adjacent to each other (headwaters of River Severn and River Wye) representing two main upland land uses in Wales: coniferous forestry and sheep-grazed grassland, designed to be as similar as possible otherwise.
  - Intensive instrumentation and long-term climatic, hydrological, and soil measurements; surveys of spatial physical characteristics (topography, soils, land use) and various thematic maps.

- Data assets and structure
  - Spatial datasets (layers):
    - Catchment and subcatchment boundaries
    - River network
    - Spot heights
    - Wye catchment contour lines
    - Severn catchment contour lines
    - Soil Parental Materials
    - Vegetation map
  - Grid data:
    - Plynlimon hydrologically corrected elevation grid (Plyn_DEM), GRID, 15 m cell size, British National Grid, floating point
  - Shapefiles:
    - PlynlimonCatchments.shp (catchments and subcatchments)
    - PlynlimonRiverNetwork.shp (river network with attributes for node IDs, length, catchment, and stream type)
    - PlynlimonSpotHeight.shp (spot heights)
    - Plynlimon_WyeElevationContours.shp (Wye contour lines)
    - Plynlimon_SoilParentalMaterials (soil materials)
    - Plynlimon_VegetationMap2013 (vegetation classifications and variants)
    - Plynlimon_SevernElevationContours.shp (Severn contour lines)
  - Vegetation classes updated to align with CEH Land Cover Map 2000 (LCM2000) for consistency with models; 2013 update includes refined classes and variants to accommodate conifer plantations and other land covers.
  - Key attributes provided for each dataset (e.g., heights, contour elevations, catchment names, vegetation class descriptions, etc.).

- Data sources and digitisation history
  - Hunting Survey (1967–1968): initial large-scale topographic maps derived from aerial photography; maps included main stream channels, forest drains, tracks, and fence lines.
  - Late 1990s digitisation: topographic and hydrographic data converted to GIS layers (elevation, catchment boundaries, river network) from 1:5000 / 1:10000 maps; creation of a hydrologically corrected DTM from these data.
  - Some field surveys mapped soils, geology, vegetation, and land use; some datasets owned by other organisations or lost.
  - Soil Hydrology Study (Bell, J.P., 1968–1969) produced a foundational soil parental materials map (IH Report No. 8; updated 2005 by CEH).
  - Vegetation mapping (2013) updated from CEH LCM2000 basis to better capture heath, bracken, improved grassland, and other classes; field validation conducted in 2013.

- Topography and hydrography data
  - Topographic maps originally at 1:5000 (contour interval 2.5 m) and 1:10000 scales derived from photogrammetric reductions; boundaries and subcatchment delineations inferred from elevation and maps.
  - Hydrography includes main stream channels and forest drains depicted on large-scale maps; Severn and Wye catchment boundaries digitised from these sources.
  - Hydrologically corrected elevation grid produced by integrating contours, spot heights, stream maps, and catchment boundaries; DEM details:
    - File: Plyn_DEM
    - 15 m cell size, British National Grid, floating point

- Data processing and formats
  - Digitising process used CALCOMP digitising table with ground control points; data captured into ArcInfo coverage files.
  - Severn contour lines originally captured as point features and converted to lines; later editing and merging to form complete contour lines.
  - Vegetation map created by on-screen digitisation in ArcGIS 10.1 with aerial photo backdrop; field observations used to refine classifications and align with LCM2000 classes.
  - Coordinate system across datasets: British National Grid.

- Soils and vegetation details
  - Soils: Bell’s soil map (Parental materials) used to understand soil hydrology and runoff; IH Report No. 8 (1969) with CEH update available online.
  - Vegetation: draft map created from 2009 aerial photography, refined through field checks (2013). Classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water; variants allow using coniferous woodland or plantation status for flexibility.

- Access, metadata, and documentation
  - Some datasets owned by other organisations or restricted by IP considerations; LCM2000 used as baseline to avoid IP conflicts with LCM2007.
  - Background documentation and references available via CEH website and publications.
  - Appendix A (Hunting Survey) details and figures discuss the 1967 aerial survey technical specifications and data footprint; negatives are lost but printed frames have been digitised and rectified.

- Appendix A: Hunting Survey
  - Describes the aerial photography survey used to derive the original topographic maps; includes figures detailing technical specs and frame footprints.
  - Indicates limitations due to lost film negatives but preserved digitised prints.