# Plynlimon Spatial datasets

- Purpose and context
  - Long-term experimental catchments at Plynlimon (late 1960s) to study land use effects on catchment water availability, flooding, and low flows in the headwaters of the Severn and Wye.
  - Two main upland land uses represented: coniferous forestry and sheep-grazed grassland; datasets support analysis of hydrology and land-use impacts over time.
  - Data are produced, quality assured, and stored to enable monitoring of environmental health and policy performance.

- Data layers and data model
  - Spatial layers include:
    - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
    - River network (PlynlimonRiverNetwork.shp)
    - Spot heights (PlynlimonSpotHeight.shp)
    - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
    - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
    - Soil Parental Materials (Plynlimon_SoilParentalMaterials)
    - Vegetation map (Plynlimon_VegetationMap2013)
  - Data are in British National Grid coordinates.
  - DEM and derived products:
    - Hydrologically corrected digital terrain model (Plyn_DEM), GRID format, 15 m cell size, floating point, British National Grid.

- Data provenance and history
  - Initial datasets stem from extensive field surveys and maps from the late 1960s, including topography, land use, soils, and climate/stream records.
  - Early source maps came from the Hunting Survey (1967–1968) aerial photography; later digitised into GIS layers in the late 1990s.
  - Soil hydrology map (Bell, J.P. 1969) remains a key reference; updated version published in 2005.
  - Vegetation map updated in 2013–2014 using 2009 aerial photography and ground truthing to align with CEH Land Cover Map 2000 classes; designed to support soil carbon analyses.

- Digitisation workflow and data products
  - Hard-copy maps digitised using CALCOMP and ArcInfo; elevation and river networks captured from 1:5000 topographic maps (contours at 10–20 m intervals).
  - Ground control points used to register maps; data converted to ArcInfo coverage files.
  - Severn contour lines originally captured at 1:5000 scale by Edinburgh University with irregular point data later converted to lines.
  - Hydrologically corrected DEM created by integrating contours, spot heights, river maps, and catchment boundaries; flow diagram (Figure 1) documents the process.
  - Key outputs and file names:
    - Plyn_DEM (Plynlimon hydrologically corrected DEM)
    - PlynlimonCatchments.shp (catchment and subcatchment boundaries)
    - PlynlimonRiverNetwork.shp (river network with node references and attributes)
    - PlynlimonSpotHeight.shp (spot heights)
    - Plynlimon_WyeElevationContours.shp (Wye contours)
    - Plynlimon_SevernElevationContours.shp (Severn contours)
    - Plynlimon_SoilParentalMaterials (soil parent materials)
    - Plynlimon_VegetationMap2013 (vegetation classification and variants)
  - All primary datasets use the British National Grid coordinate system; DEM specifics: GRID format, 15 m cell size, floating point.

- Hydrologically corrected elevation grid
  - Derived by building a TIN from 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries; produced a hydrologically corrected DTM for more accurate hydrological analysis.

- Vegetation mapping
  - Updated vegetation map (Plynlimon_VegetationMap2013) prepared to support soil property and carbon analyses.
  - Classes aligned with CEH Land Cover Map 2000; refined to include coniferous woodland, new/felled plantations, various grassland types, bracken, heath, inland bare ground, water, and woodland variants.
  - Method combined interpretation of 2009 aerial imagery (Next Perspectives) with on-site field verification (2013); differences noted due to timing and shadow effects, then refined using ArcGIS 10.1 with aerial imagery as reference.

- Accessibility and limitations
  - Some datasets are owned by other organisations or not fully available; certain field- and site-specific datasets are lost.
  - Soil and vegetation data are supplemented by published references and updated maps; some older maps were digitised for internal CEH use.

- Appendix and supplementary context
  - Appendix A describes the Hunting Survey aerial photography, its scope, and the framing footprints used to derive the original topographic maps.
  - The dataset collection supports ongoing environmental monitoring by providing a standardized, quality-assured geospatial foundation for hydrology, land-use change, and related policy evaluations.