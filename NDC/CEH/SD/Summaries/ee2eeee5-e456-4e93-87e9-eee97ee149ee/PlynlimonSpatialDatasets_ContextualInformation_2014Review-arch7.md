# INTRODUCTION

- Context and aim
  - Plynlimon experimental/research catchments set up in the late 1960s by IH/NERC (now CEH) to study how upland land use affects catchment water availability, flooding, and low flows.
  - Two adjacent catchments represent the two main upland land uses in Wales: coniferous forestry and sheep-grazed grassland; designed to be as similar as possible otherwise.
  - Intensive instrumentation with long-term climatic, hydrological, and soil moisture records since the late 1960s; surveys of spatial characteristics (topography, soils, land use) were undertaken; combined datasets include thematic maps.

- Purpose for GIS specialists
  - Compilation of spatial datasets and a hydrologically corrected DEM to support map-based analyses of hydrology and land-use impacts.

- Primary spatial datasets (Plynlimon Spatial datasets)
  - Catchment and subcatchments boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil Parental Materials
  - Vegetation map
  - Hydrologically corrected elevation grid (Plyn_DEM; GRID, 15 m)

- Background and data context
  - Datasets originate from topographic maps derived from the Hunting aerial survey and later digitised (late 1990s) into GIS layers (elevation/DTM, boundaries, river network).
  - Field surveys mapped soils, geology, vegetation, and land use; some data are unavailable or owned by other organizations; Soil Hydrology map (Bell, 1969) digitised in the late 1990s; updated version published by CEH in 2005.
  - Vegetation map updated in 2013 to align with CEH Land Cover Map 2000 classes and to support SoilTrEC analyses; uses 2009 aerial photography with ground truthing (2013).

- Data production and formats
  - Digitising workflow: hard-copy maps digitised at CEH with ground control points; elevation and contours captured from 1:5000 maps (2.5 m contours); Severn contours digitised at Edinburgh University and converted to lines.
  - Hydrologically corrected DEM creation: integrates 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries; ArcInfo workflow with TIN to derive hydrologically corrected grid-based DEM (Plyn_DEM; 15 m cell size; British National Grid).

- Data products and file details
  - Plynlimon DEM: Plyn_DEM.grid; 15 m, floating-point; hydrologically corrected DEM.
  - Catchment boundaries: PlynlimonCatchments.shp; attributes include Catchment and Subcatch.
  - River network: PlynlimonRiverNetwork.shp; attributes include FNODE_, TNODE_, LENGTH, Catchment, Type.
  - Spot heights: PlynlimonSpotHeight.shp; HEIGHTS (m).
  - Wye elevation contours: Plynlimon_WyeElevationContours.shp; HEIGHTS (m) at 10/20 m intervals.
  - Severn elevation contours: Plynlimon_SevernElevationContours.shp; HEIGHTS (m).
  - Soil parental materials: Plynlimon_SoilParentalMaterials; SOIL, Descript.
  - Vegetation map: Plynlimon_VegetationMap2013; classes aligned with LCM2000; includes id, VegClass, Variants.
  - Appendix-specific: Hunting Survey (1967 aerial photography) with frame footprints and digitisation notes.

- Vegetation mapping methodology
  - Base: CEH Land Cover Map 2000 (LCM2000) updated to include heath, bracken, improved grassland, etc.
  - Process: draft vegetation map created from 2009 aerial photography; on-screen digitising with ArcGIS 10.1; field verification via track-based observations; discrepancies due to date differences and interpretation; final product edited against aerials and field data; conifer categories reconciled to LCM2000 classes; additional Variant field to reflect plantation status.

- Appendix A: Hunting Survey
  - Aerial survey from Hunting Survey Ltd (June 1967); film negatives lost; printed frames digitised; footprints mapped to preserve spatial coverage.

- Access and references
  - Related information: CEH project pages and SoilHydrology of the Plynlimon Catchments (Bell 1969; CEH 2005 revision).
  - Live links referenced for additional publications and dataset details.