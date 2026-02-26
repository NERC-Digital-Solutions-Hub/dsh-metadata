# Plynlimon Catchment Spatial Datasets

- Overview
  - Plynlimon experimental/research catchments in mid-Wales were established in the late 1960s to study how upland land use (conifer forestry vs sheep-grazed grassland) affects catchment water availability, flooding, and low flows.
  - The catchments host the headwaters of the River Severn and the River Wye and were densely instrumented to provide long-term climatic, hydrological, and soil data.
  - The project combined surveys of physical characteristics (topography, soils, land use) with extensive datasets and thematic maps, later digitised for GIS use.
  - Datasets support analysis of land-use impacts on hydrology and provide basemap, vegetation, soils, and elevation information for modelling and policy/research purposes.

- Spatial data components included
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
  - Hydrologically corrected elevation grid (DEM)

- Data sources and development timeline
  - Initial topographic maps created from the Hunting survey (1967–68) via aerial photography; later digitised in the 1990s into GIS-ready layers.
  - Field surveys in early years mapped soils, geology, vegetation, and land use; some data owned by other organisations or lost (notably some datasets).
  - Soil Parental Materials map derived from JP Bell’s 1969 Soil Hydrology Study (IH Report No. 8); updated version (2005) by CEH accompanies this document.
  - Vegetation map (Plynlimon_VegetationMap2013) created by updating and reclassifying CEH Land Cover Map 2000 classes based on 2009 aerial photography and 2013 field validation.

- Data creation and processing workflow
  - Topography
    - 1:5,000 scale topographic maps with 2.5 m contours derived via photogrammetry from Hunting Survey photography.
    - 1:10,000 scale topographic maps with the same contour interval produced from photogrammetric reduction.
  - Digitising and GIS capture
    - Most datasets digitised at CEH; elevation points and contours captured with ground control points (GCPs) using CALCOMP digitising tables; data saved as ArcInfo coverage.
    - Severn catchment contours captured at Edinburgh University from 1:5,000 maps; later edited and merged into full contour lines.
  - Hydrologically corrected DEM
    - Derived from a hydrologically corrected DEM using a TIN created from 1:5,000 contours, spot heights, stream maps, and catchment boundaries.
    - DEM technical details: Plyn_DEM, GRID format, 15 m cell size, floating point, British National Grid.
  - Data formats and keys
    - Shapefiles and GRID used for data products.
    - British National Grid coordinate system across all vector layers.
    - Key shapefiles and their purposes:
      - PlynlimonCatchments.shp – catchment and subcatchment boundaries; attributes: Catchment, Subcatch.
      - PlynlimonRiverNetwork.shp – river network; attributes include FNODE, TNODE, LENGTH, Catchment, Type.
      - PlynlimonSpotHeight.shp – spot heights; attribute: HEIGHTS (elevation in metres).
      - Plynlimon_WyeElevationContours.shp – Wye contour lines; attribute: HEIGHTS.
      - Plynlimon_SoilParentalMaterials.shp – soil parent materials; attributes: SOIL, Descript.
      - Plynlimon_VegetationMap2013.shp – updated vegetation map; attributes: id, VegClass, Varients.
      - Plynlimon_SevernElevationContours.shp – Severn contour lines; attribute: HEIGHTS.
      - Plyn_DEM.grid – hydrologically corrected DEM (15 m resolution, GRID format).
  - Vegetation mapping approach
    - Draft vegetation classes interpreted from 2009 Next Perspectives aerial photography; refined through field observations and updated to align with CEH Land Cover Map 2000 (LCM2000) classes.
    - Conifer plantation, new plantation, felled plantation merged into coniferous woodland with a Variant field to preserve distinctions for analytical flexibility.
    - Final map (Plynlimon_VegetationMap2013) produced by editing draft map on screen against digital aerial backdrop; field verification conducted; differences mainly due to timing (photography 2009 vs fieldwork 2013).

- Data gaps, limitations, and notes
  - Some datasets not available due to ownership/IP constraints; some data have been lost.
  - Severn contour data have a documented capture method and provenance; processing steps described to ensure spatial integrity.
  - Vegetation mapping incorporates temporal differences (photography date vs field observations) and was refined through ground truthing.

- Appendices and references
  - Appendix A: Hunting Survey documentation and the aerial photography survey of 1967; footprints of frames digitised to preserve data.
  - Reference context and access: CEH project pages and CEH publications for Soil Hydrology (Bell 1969; updated 2005) and related CEH data products.

- Practical relevance for GIS work
  - Provides a comprehensive, multi-layer GIS-ready suite of catchment-scale data for hydrological modelling, land-use impact analyses, and visualization of watershed characteristics.
  - Demonstrates end-to-end data lineage from aerial photography to GIS-ready layers, including QA through field checks and alignment with established land cover classifications.
  - Supports reproducibility by detailing data sources, processing steps, coordinate system choices, and file formats, enabling integration with other CEH datasets and external projects (e.g., SoilTrEC).