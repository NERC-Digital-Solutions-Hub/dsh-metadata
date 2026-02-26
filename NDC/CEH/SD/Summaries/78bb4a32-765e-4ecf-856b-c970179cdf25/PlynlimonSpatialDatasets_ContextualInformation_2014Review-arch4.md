# Plynlimon Spatial datasets

- Overview
  - Plynlimon experimental catchments in mid-Wales were established in the late 1960s by the Institute of Hydrology (IH), later part of CEH/NERC, to study how land use affects catchment water availability, flooding, and low flows.
  - Two adjacent catchments represent predominant upland land uses: coniferous forestry and sheep-grazed grassland; both were instrumented for long-term climatic, hydrological, and soil data, with surveys of topography and land use.
  - Spatial datasets were compiled to support analyses of hydrology and land surface processes, including maps, grids, and various thematic layers.

- Key datasets and layers
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Hydrologically corrected elevation grid (Plyn_DEM; GRID, 15 m cell size)
  - WGS/Coordinate system: British National Grid across layers
  - Descriptions and attributes accompany each layer (e.g., lengths, catchment names, elevation values, soil codes)

- Creation and digitisation of data
  - Source maps: Large-scale topographic maps from the Hunting Survey (1967–68) derived from aerial photography; included main streams, forest drains, tracks, and fences.
  - Digitisation timeline: 1990s digitisation of topographic/hydrographic data into GIS layers; some datasets created by CEH, others by external organisations.
  - Data capture methods:
    - Elevation, contour, and river network derived from photogrammetry and 1:5000 maps (then converted to 1:10000 for some products)
    - Ground control points used for registration during digitisation
    - Severn catchment contours captured separately (at Edinburgh University)
  - DEM creation: Hydrologically corrected DTM produced by integrating contours, spot heights, streams, and catchment boundaries into a TIN, then grid-based DEM (Plyn_DEM, 15 m cells)

- Vegetation and soils
  - Vegetation map 2013: Updated map created by photo-interpretation of 2009 aerial photography, ground-truthed in 2013; aligned with CEH Land Cover Map 2000 classes; includes conifer plantations, new/felled plantations, grassland types, heaths, bracken, woodland, water, etc.
  - Vegetation data structure: Shapefile Plynlimon_VegetationMap2013 with id, VegClass, and Variants for flexible classification (e.g., coniferous woodland vs felled/new plantation)
  - Soil Parental Materials: Based on Bell, J.P. (1969) Soil Hydrology study; IH Report No. 8; updated version provided alongside the document (CEH 2005)

- Contours and hydrography
  - Wye and Severn elevation contours: Wye (10/20 m intervals) and Severn (10 m intervals) contour shapefiles
  - River network: Includes natural and artificial (man-made) streams with upstream/downstream node identifiers
  - Spot heights and catchment boundaries support hydrological analyses and drainage routing

- Data provenance, access, and gaps
  - Data stewardship: CEH assembled most vector layers; Severn elevation contours were captured at Edinburgh University
  - Not all field surveys are available; some datasets are owned by other organisations or have been lost
  - Some datasets require IPR considerations; data are provided with metadata and descriptions to facilitate discoverability and reuse

- Appendices and provenance details
  - Appendix A (Hunting Survey): Details of the 1967 aerial photography survey, technical specifications, and footprint of frames; negatives are lost but printed frames have been digitised and rectified to preserve data
  - Original topographic references include 1:5000 and 1:10000 scale sheets for Severn and Wye catchments; later digital production used ArcInfo and ArcGIS workflows

- Practical implications for data leaders
  - Comprehensive, multi-layer spatial dataset supports analysis of land-use impacts on hydrology across two contrasting catchments
  - Long-term data provenance and explicit metadata enable traceability and reuse, though some data are incomplete or restricted due to ownership or loss
  - Updated vegetation classifications align with CEH land cover standards, enhancing integration with other CEH models and datasets
  - Data products are provided in standard GIS formats (shapefiles, grid DEM) with clear coordinate system and attribute schemas, aiding discoverability and applicability across projects

- Notes on access and references
  - Related information and project context available via CEH website and CEH-science blogs
  - Foundational reference: Bell, J.P. 1969. The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8) with a revised 2005 CEH edition

- Enduring value and considerations
  - The dataset collection serves as a valuable, long-running open-air laboratory for hydrology and land-use experiments
  - Ongoing considerations include data standardization, metadata completeness, discoverability, and coordination with partner datasets to mitigate data gaps and access barriers