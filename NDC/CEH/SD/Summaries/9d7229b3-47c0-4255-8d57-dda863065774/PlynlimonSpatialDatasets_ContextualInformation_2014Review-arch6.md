# Plynlimon experimental/research catchments

- Aim and context
  - A long-term hydrological research project (late 1960s) by the Institute of Hydrology (IH, later CEH, NERC) to understand how upland land use affects catchment water availability, flooding, and low flows.
  - Located in mid-Wales, headwaters of the River Severn and River Wye; compares two major upland land uses: coniferous forestry vs sheep-grazed grassland.
  - Intensive instrumentation and high-quality climatic, hydrological, and soil data collected since the 1960s; surveys of topography, soils, and land use conducted; aim to enable understanding of evaporation losses and hydrological variation.

- Data collections and spatial data layers
  - Spatial datasets (digital GIS layers) include:
    - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
    - River network (PlynlimonRiverNetwork.shp)
    - Spot heights (PlynlimonSpotHeight.shp)
    - Wye catchment elevation contours (Plynlimon_WyeElevationContours.shp)
    - Severn catchment elevation contours (Plynlimon_SevernElevationContours.shp)
    - Soil parental materials (Plynlimon_SoilParentalMaterials)
    - Vegetation map (Plynlimon_VegetationMap2013)
  - Hydrologically corrected elevation grid (Plyn_DEM, GRID, 15 m cell size) forming the core DEM for hydrological analysis.
  - All data originally aligned to the British National Grid; several datasets include attribute fields (e.g., river segment IDs, catchment associations, contour elevations, soil types, vegetation class codes).

- Data sources, digitising, and provenance
  - Aerial photography from a Hunting Survey (1967) formed the base for topographic maps (1:5000 and 1:10000 scales) with contours at 2.5 m.
  - In the late 1990s, topographic and hydrographic data were digitised into GIS layers (Arcinfo). Elevation, catchment boundaries, and river networks were derived from these sources.
  - Severn catchment contours were digitised separately at Edinburgh University and later converted to lines; some processing artefacts were corrected.
  - Soil maps: Bell, J.P. (1969) “The Soil Hydrology of the Plynlimon Catchments” (IH Report No. 8) informing soil parent materials; updated version published by CEH in 2005.
  - Field surveys mapped soils, geology, vegetation, and land use; some datasets are unavailable due to IP restrictions or loss of data.
  - Appendix A documents the Hunting Survey and the status of original film negatives.

- Hydrologically corrected elevation model (DTM/DEM) workflow
  - Inputs: 1:5,000 contour maps, spot heights, river maps, and catchment boundaries.
  - Process: data imported into Arcinfo, TIN created, hydrologically corrected DEM produced (Plyn_DEM).
  - Output: Plynlimon hydrologically corrected Digital Terrain Model (GRID) with 15 m resolution, designed for watershed and hydrological analyses.

- Vegetation and land cover mapping
  - Vegetation map updated in 2013 (Plynlimon_VegetationMap2013) to support SoilTrEC analyses and improve linkage to soil carbon data.
  - Base reference: CEH Land Cover Map 2000 (LCM2000), chosen to avoid IP conflicts with newer datasets (LCM2007) and to align with CEH models.
  - Methodology: draft classification from 2009 aerial photography, on-screen digitising in ArcGIS 10.1, and ground-truthing in 2013; field observations helped refine classifications.
  - Classes include conifer plantations (and variants: new/felled), various grassland types, bracken, heath, shrublands, bare ground, deciduous woodland, inland water, etc.
  - Final class definitions were reconciled to LCM2000 standards; an additional Variants column provides flexibility for dataset users.

- Contour and hydrological features by catchment
  - Wye and Severn contour datasets created from original topographic data and subsequently refined for geospatial analyses.
  - Severn contours derived from Edinburgh University point dataset, edited to form continuous contour lines and clipped to the catchment boundary.

- Data products and potential uses
  - Hydrologically corrected DEM (Plyn_DEM) for watershed analyses and hydrological modelling.
  - Boundaries, river networks, spot heights, and contour datasets for spatial analysis of land-sea interactions, drainage, and catchment properties.
  - Soil parental materials map for hydrological interpretation and soil–water processes.
  - Vegetation map (2013) enabling correlations between land cover, soil properties, and hydrology; supports SoilTrEC geostatistical analyses.
  - Supporting documentation and provenance enable reuse in hydrological, geomorphological, and ecological research.

- Access considerations and caveats
  - Some datasets not available due to ownership/IP restrictions or data loss.
  - Variation in dates (e.g., vegetation mapped using 2009 imagery with 2013 ground-truthing) introduces temporal uncertainty for change detection.
  - Historical data and digitisation workflows (e.g., CALCOMP digitising, GCP-based registration) documented to aid data users in understanding lineage and potential limitations.

- References and context
  - Brandt, Robinson, and Finch (2004) on the project’s initial aims and hydrology emphasis.
  - CEH project pages and SoilHydrology of the Plynlimon Catchments (Bell, 1969; CEH 2005 update) for data provenance and methodological background.
  - Appendix A ( Hunting Survey ) documents the original aerial survey and framing, including digitisation status.