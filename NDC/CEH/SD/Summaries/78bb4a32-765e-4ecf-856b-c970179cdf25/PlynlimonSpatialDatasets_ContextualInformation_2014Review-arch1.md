# Plynlimon Spatial datasets and Vegetation Map

- Introduction and aim
  - Plynlimon experimental catchments (late 1960s) studied the impact of upland land use on catchment water availability, flooding, and low flows.
  - Two adjacent catchments represent coniferous forestry and sheep-grazed grassland, with long-term climatic, hydrological, and topographic data.
  - Datasets support analyses of land use, hydrology, soils, and vegetation across the Severn and Wye headwaters.

- Spatial datasets and hydrological grid (core layers)
  - Catchment and subcatchment boundaries (British National Grid)
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil Parental Materials
  - Vegetation map
  - Hydrologically corrected elevation grid (Plyn_DEM; 15 m cell size, floating point GRID)

- Data provenance and maps
  - Large-scale topographic maps prepared from Hunting Survey aerial photos (1967–1968) at 1:5,000 and 1:10,000 scales; contour interval 2.5 m.
  - In the 1990s, topographic/hydro data digitised into GIS layers (ARC/INFO): elevation, catchment boundaries, river network.
  - Some field datasets are missing or owned by other organisations; soil hydrology map by JP Bell (1969) later revised (IH Report No. 8; CEH 2005).

- Digitising process and data production
  - Hard-copy maps digitised at CEH using CALCOMP digitising tablet; ground control points used for registration; elevation points and 10–20 m contours captured and saved as Arcinfo coverages.
  - Severn catchment contours digitised separately at Edinburgh University (original method not fully documented; points converted to lines later).
  - Hydrologically corrected DTM created by integrating contours, spot heights, stream maps, and boundaries; a TIN was used to produce the 15 m hydrologically corrected DEM (Plyn_DEM).

- Data files and structure (examples)
  - PlynlimonCatchments.shp — Catchment and subcatchment boundaries
  - PlynlimonRiverNetwork.shp — River network
  - PlynlimonSpotHeight.shp — Spot heights
  - Plynlimon_WyeElevationContours.shp — Wye contour lines (10/20 m)
  - Plynlimon_SoilParentalMaterials.shp — Soil parental materials
  - Plynlimon_VegetationMap2013.shp — Updated vegetation map (see Vegetation map details)
  - Plynlimon_SevernElevationContours.shp — Severn contour lines
  - Plynlimon DEM file: Plyn_DEM (GRID, 15 m, British National Grid)
  - Coordinate system for all layers: British National Grid

- Vegetation map development and classes
  - Updated vegetation map created in 2013 to support soil carbon and geostatistical analyses; bases on CEH LCM2000 with refinements.
  - Classes include: Conifer plantation, New plantation, Felled plantation, Rough acid grass, Bracken, Open dwarf shrub heath, Improved grassland, Inland bare ground, Deciduous woodland, Inland water.
  - Method: draft map from 2009 aerial photography (Next Perspectives) interpreted and digitised; field verification in 2013; adjustments for date differences and features.
  - Final product: Plynlimon_VegetationMap2013 with attributes id, VegClass, Varients (variants for coniferous areas).
  - Rationale: to align with LCM2000 classes while accommodating vegetation changes and to support related soil and carbon analyses.

- Appendix A: Hunting Survey
  - Aerial photography survey (1967) that underpinned the topographic mapping; film negatives lost but printed frames have been digitised and rectified.
  - Footprints of aerial frames documented; data preservation efforts described.

- Background and usage context
  - Vegetation and soils datasets support SoilTrEC objectives and geostatistical analyses of soil carbon and related properties.
  - LCM2000 serves as a base to avoid IPR issues; updates incorporate heath, bracken, and various grassland types affecting soil properties.
  - Some datasets are limited by access restrictions or historical data gaps, highlighting the importance of provenance and metadata for robust analyses.