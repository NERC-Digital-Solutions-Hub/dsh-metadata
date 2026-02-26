# Plynlimon experimental/research catchments

- Purpose and context
  - Long-term, intensive hydrological and climatic monitoring to study the impact of land use on water availability, flooding, and low flows in upland Wales.
  - Two adjacent catchments (Severn headwaters with conifer forestry; Wye headwaters with sheep-grazed grassland) chosen to represent major upland land uses while being similar in other environmental aspects.
  - Data collected since the late 1960s include climate, streamflow, soil moisture, topography, soils, vegetation, and land use; used to compare evaporation losses and hydrological responses.

- Spatial data layers (as part of Plynlimon Spatial datasets)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
  - Hydrologically corrected elevation grid (Plyn_DEM; GRID, 15 m)
  - Coordinate system for all layers: British National Grid

- Datasets and file details
  - Plynlimon DEM (Plyn_DEM): hydrologically corrected digital terrain model; 15 m resolution; floating point grid.
  - Catchment datasets: shapefiles defining upland catchments and major subcatchments.
  - River network: includes upstream/downstream node identifiers and segment lengths; includes natural vs artificial (man-made) streams.
  - Spot heights and contour lines: elevation data at 10–20 m intervals for Wye and Severn catchments.
  - Soil Parental Materials: distribution of soil parent materials with codes and descriptions.
  - Vegetation map (2013): updated from LCM2000 to include coniferous woodland, plantations, heath, acid grassland, bracken, improved grassland, bare ground, and water; includes a Variants field for coniferous plantation status; created via ArcGIS 10.1 with 2009 aerial imagery and 2013 ground-truthing.
  - Severn elevation contours: created from Edinburgh University point dataset, edited to form continuous contour lines and clipped to Severn boundary.

- Data creation and provenance
  - Source maps: initial large-scale topographic maps produced from Hunting Survey aerial photography (1967–68); later digitised in the late 1990s to produce GIS layers.
  - Field surveys: undertaken to map soils, geology, vegetation, and land use; some datasets are unavailable due to data ownership or loss; notable exception is the Soil Hydrology Study (Bell 1969) with IH Report No. 8; updated CEH version (2005) provided alongside this document.
  - Digitising workflow: hard copy maps digitised on CALCOMP table; ground control points used for georeferencing; data stored as ArcInfo coverages.
  - DEM creation workflow: integration of contours, spot heights, streams, and boundaries to build a hydrologically corrected DEM via a TIN and grid derivation.

- Vegetation mapping methodology and considerations
  - Base used: CEH Land Cover Map 2000 (LCM2000) due to standard usage and IP considerations; updated to better reflect heath, bracken, improved grassland, and to align with soil carbon studies.
  - Draft vegetation map created from 2009 aerial photo interpretations, then refined with 2013 field observations to adjust for date differences and shading effects.
  - Final digital vegetation map (2013) edited within ArcGIS 10.1; new features added (water, bare ground); polygons classified to CEH LCM2000-compatible classes; an additional Variants column enables use as coniferous woodland or plantation status.

- Background and data usage notes
  - The vegetation and soil data were developed to support SoilTrEC analyses, including geostatistical analyses of soil carbon.
  - LCM2000 was chosen to avoid IP conflicts; data updates intended to improve representation of land cover types relevant to soil properties.
  - Some datasets are publicly usable, while others are held by different organisations or are no longer available; CEH provides updated soil hydrology (Bell 1969, revised 2005) for reference.

- Appendix A: Hunting Survey
  - The 1967 Hunting Survey aerial photographs formed the basis for the original topographic maps; film negatives are lost, but printed frames have been digitised and rectified to preserve footprints and data fidelity.