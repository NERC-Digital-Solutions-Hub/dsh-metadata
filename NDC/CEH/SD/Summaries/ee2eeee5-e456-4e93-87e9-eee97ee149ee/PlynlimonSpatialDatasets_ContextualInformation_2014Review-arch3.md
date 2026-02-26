# Plynlimon experimental/research catchments

- Purpose and background
  - Long-running study set up in the late 1960s by the Institute of Hydrology (IH, later part of CEH/NERC) to understand how upland land use (coniferous forestry vs. sheep-grazed grassland) affects catchment water availability, flooding, and low flows.
  - Two adjacent catchments drain the headwaters of the River Severn and the River Wye in mid-Wales, selected to be similar in all other environmental aspects.
  - Intensive instrumentation and long-term climate, streamflow, and soil moisture records exist; surveys of physical characteristics and land use were conducted to support analyses of evaporation, hydrology, and related processes.

- Spatial datasets and their components
  - Plynlimon Spatial datasets (layers)
    - Catchment and subcatchment boundaries
    - River network
    - Spot heights
    - Wye catchment contour lines
    - Severn catchment contour lines
    - Soil parental materials
    - Vegetation map
  - Grid/DEM
    - Plynlimon hydrologically corrected elevation grid (Plyn_DEM): 15 m cell size, GRID format, British National Grid
  - File formats and coordinates
    - Shapefiles (British National Grid) for boundaries, river network, spot heights, soils, and vegetation
    - Elevation contours for Severn and Wye catchments (10 m contours for contours; 10/20 m intervals for Wye)
  - Key shapefile names and descriptions
    - PlynlimonCatchments.shp: upland catchments and subcatchments
    - PlynlimonRiverNetwork.shp: river/stream network with attributes (FROM/TO node IDs, length, catchment, type)
    - PlynlimonSpotHeight.shp: spot heights (elevations)
    - Plynlimon_WyeElevationContours.shp: Wye contours (10/20 m)
    - Plynlimon_SoilParentalMaterials: distribution of soil parent materials
    - Plynlimon_VegetationMap2013: updated vegetation map with classes aligned to CEH LCM2000
    - Plynlimon_SevernElevationContours.shp: Severn contours (10 m)
  - Vegetation map details
    - Basis: updated from LCM2000 to better reflect heath, bracken, improved grassland, etc.
    - Classes include conifer plantations, new plantation, felled plantation, acid grass, bracken, dwarf heath, improved grassland, bare ground, deciduous woodland, water
    - Variant field to differentiate coniferous woodland vs felled/new plantation

- Source maps, digitising, and topography
  - Hunting survey (1967) provided large-scale topographic maps with features such as main streams, forest drains, tracks, and fence lines
  - Late 1990s digitisation of topographic/hydrographic data into GIS
  - Some field data (e.g., soil/land characteristics) were collected in early years; some data owned by other organisations or lost
  - Severn contour data digitised separately at Edinburgh University; process with irregularly spaced points later converted to lines

- Hydrologically corrected elevation model and data flow
  - Hydrologically corrected DTM created by integrating:
    - 1:5,000 contour maps (photogrammetric topography)
    - spot heights
    - stream maps
    - catchment boundaries
  - Steps
    - Import into ArcInfo, build a TIN, derive hydrologically corrected grid
    - DEM file: Plyn_DEM (15 m grid, floating point, British National Grid)
  - Data products and structure
    - Catchment boundaries: PlynlimonCatchments.shp
    - River network: PlynlimonRiverNetwork.shp
    - Spot heights: PlynlimonSpotHeight.shp
    - Elevation contours: Severn and Wye contour shapefiles
    - Soil and vegetation datasets with descriptive attributes

- Vegetation mapping process and rationale
  - Based on CEH Land Cover Map 2000 (LCM2000) due to standard usage and IP considerations
  - Vegetation classes expanded/edited to reflect:
    - Coniferous woodland (including new and felled plantations)
    - Acid grassland and bracken
    - Heath and improved grassland
    - Open bare ground and inland water
    - Deciduous woodland
  - Draft map created via on-screen digitising using 2009 aerial photography; refined through 2013 field verification and alignment with LCM2000 classes
  - Final product: Plynlimon_VegetationMap2013 with class codes and variant descriptions to allow flexible use

- Appendix A Hunting Survey
  - Details the 1967 aerial photography survey by Hunting Survey Ltd
  - Footprints and technical specifications are documented; negatives lost but printed frames digitised and rectified to preserve data

- Background, data relevance, and governance notes
  - The vegetation map and soil datasets support soil carbon analyses (e.g., SoilTrEC project)
  - LCM2000 used to avoid IP conflicts with later LCM2007 versions
  - Some historical data may have limited accessibility due to ownership or loss
  - Data provenance includes IH reports (e.g., Bell, 1969; IH Report No. 8) and CEH updates (2005)

- Implications for monitoring frameworks
  - Demonstrates a comprehensive approach to assembling long-term environmental monitoring data
  - Emphasises provenance, multiple data sources, and the creation of standardized, interoperable spatial layers
  - Highlights metadata considerations, data transformation needs, and the balance between openness and data governance (ownership, IP, and sharing constraints)
  - Provides a model for documenting data creation workflows, quality considerations, and field validation to support transparency and reuse in monitoring programs

- Notable data constraints and gaps relevant to monitoring
  - Some data layers not available due to ownership or loss
  - Metadata gaps in certain historical datasets may hinder verification
  - Data transformation requirements and potential barriers to immediate reuse due to format or provenance
  - Need for ongoing data updates to keep classifications and geographic extents current