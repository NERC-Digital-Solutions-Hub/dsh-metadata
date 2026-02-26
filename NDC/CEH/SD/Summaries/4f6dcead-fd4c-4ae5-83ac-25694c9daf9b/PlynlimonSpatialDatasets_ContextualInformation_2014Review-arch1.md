# Plynlimon Spatial datasets

- Aim and context
  - Plynlimon experimental catchments (late 1960s) established to study how upland land use affects catchment water availability, flooding, and low flows.
  - Compared two main upland land uses in Wales: coniferous forestry vs sheep-grazed grassland; involved long-term climatic, hydrological, and soil measurements.
  - Datasets support analysis of land-use impacts on hydrology and are used for modelling and interpretation.

- Core spatial data layers (Plynlimon spatial datasets)
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights (elevations)
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil Parental Materials
  - Vegetation map
  - Hydrologically corrected elevation grid (Plynlimon DEM)

- Source maps and historical mapping
  - Hunting Survey (1967–68) aerial photography enabled large-scale topographic maps and features (streams, drains, tracks, fences).
  - Late 1990s digitisation converted topographic and hydrography data into GIS layers (elevation, catchment boundaries, river network).
  - Field surveys mapped soils, geology, vegetation, and land use; some datasets are unavailable or owned by others; Soil Hydrology Study (Bell, 1969) produced the soil parental materials map, later digitised.

- Topography and hydrography
  - Topographic maps created at 1:5000 and 1:10000 scales with 2.5 m contour intervals.
  - Hydrographic features (streams, drains) derived from aerial data; subcatchment boundaries inferred from elevation data.
  - Severn catchment contours digitised from 1:5000 maps; some processes/techniques undocumented.

- Soils
  - Bell’s Soil Hydrology Map (1969) shows distribution of soil parent materials; updated edition published by CEH in 2005.
  - Used to inform hydrological understanding of runoff processes.

- Digitising and data capture
  - All layers (except Severn contours) digitised at CEH using CALCOMP digitising table with ground control points; ArcINFO used for GIS conversion.
  - Severn contours captured at Edinburgh University as point data and later converted to lines; manual edits to remove artefacts.
  - Hydrologically corrected DEM created from elevation data, spot heights, stream maps, and catchment boundaries via a TIN-based workflow.

- Hydrologically corrected elevation grid and DEM
  - DEM file: Plyn_DEM (GRID, 15 m cell size, floating point) in British National Grid.
  - Purpose: hydrologically correct terrain for accurate hydrological modelling.

- Data products and file formats
  - PlynlimonCatchments.shp: Catchment and subcatchment boundaries; attributes include Catchment and Subcatch.
  - PlynlimonRiverNetwork.shp: River network; attributes include FNODE_, TNODE_, LENGTH, Catchment, Type.
  - PlynlimonSpotHeight.shp: Spot heights; attribute HEIGHTS.
  - Plynlimon_WyeElevationContours.shp: Wye elevation contours; attribute HEIGHTS.
  - Plynlimon_SoilParentalMaterials: Soil type codes and descriptions.
  - Plynlimon_VegetationMap2013: Vegetation map; attributes include id, VegClass, Varients.
  - Plynlimon_SevernElevationContours.shp: Severn contour lines; attribute HEIGHTS.

- Vegetation mapping (2013 update)
  - Background: Required for SoilTrEC project to align vegetation boundaries with soil surveys; based on CEH Land Cover Map 2000 (LCM2000) to avoid IP conflicts with newer datasets.
  - Method: Draft map created from 2009 aerial photography (Next Perspectives), then field-checked in 2013; edited in ArcGIS 10.1 with aerial imagery as backdrop.
  - Classes mapped (aligned with LCM2000): conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water.
  - Final vegetation map (Plynlimon_VegetationMap2013) refines classes to match LCM2000; an additional Variants column allows representation of coniferous woodland vs felled/new plantation.
  - Limitations noted: differences between aerial interpretation (2009) and ground truth (2013) due to timing and shading.

- Severn catchment contours
  - Derived from Edinburgh University point dataset; converted to lines, cleaned of artefacts, and clipped to the Severn boundary.

- Appendix: Hunting Survey
  - Details of the 1967 aerial photography campaign by Hunting Survey Ltd; technical specifications documented in a working sheet.
  - Film negatives are lost; printed frames digitised and rectified to preserve data.
  - Footprints of all aerial frames documented for reference.

- Data provenance, access, and usage notes
  - Data span multiple sources and formats; some datasets may be owned by other organisations or have gaps due to loss.
  - Historical data and metadata support hydrological analyses, model development, and cross-site comparisons.
  - The documents and datasets cater to long-term hydrological research, with explicit links to CEH publications and SoilTrEC project use.