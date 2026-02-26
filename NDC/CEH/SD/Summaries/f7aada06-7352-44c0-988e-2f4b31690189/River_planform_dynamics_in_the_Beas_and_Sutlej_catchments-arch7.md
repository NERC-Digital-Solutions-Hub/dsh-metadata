# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

## Overview
- Describes and analyzes human impacts on river planform using the Himalayan Sutlej-Beas system as a case study.
- Aims to assess planform changes across centennial to episodic timescales, link patterns to human-environment drivers, and conceptualize evolutionary trajectories by timescale.
- Dataset supports GIS-based visualization and analysis of multi-temporal river dynamics.

## Study area and scope
- Rivers: Beas and Sutlej.
- Beas scope: Pong Dam to confluence with Sutlej; Sutlej scope: Bhakra Dam to confluence with Beas.
- Each river divided into Reach 1 (below dams) and Reach 2 (wide plains of Punjab); Reach 2 subdivided into sections (4 for Beas, 5 for Sutlej).
- Coordinate System: WGS84.
- Extents defined by bounding coordinates: West 74.957, East 76.706, North 32.225, South 30.780.

## Dataset components (types and what they measure)
- Wet river area (post-monsoon, annual 1989–2018): derived from Landsat 5–8 imagery using mNDWI > 0.15; polygons created per year for Reaches 1 & 2 and Reach 2 sections.
- Active gravel bars (post-monsoon, annual 1989–2018): identified from Landsat reflectance (>0.16) within a Beas/Sutlej buffer; per-year features.
- Active channel area (maximum wetted extent 1989–2018): aggregating annual wet areas to form a single active-channel polygon per river.
- Active channel width (1989–2018): width of post-monsoon wet area (including enclosed gravel bars), measured every 2 km; also calculated from historic map (1847–1850) for Beas and Sutlej.
- Anabranching Index (AI) (1989–2018): number of active channels across cross sections spaced by braid-plain widths; calculated per Reach and per section.

## Temporal and spatial coverage
- Temporal: 1989–2018 for most indicators; historic map width (1847–1850) for reference.
- Spatial: Beas and Sutlej rivers, each with Reach 1 and Reach 2; Reach 2 subdivided into multiple sections.

## Data structure and formats
- Primary formats: ESRI Shapefiles with mandatory/optional accompanying files; CSV files for yearly metrics.
- Features and attributes:
  - Wet river area, gravel bars, and active channel: shapefile polygons per year; Year attribute applied to width data as necessary.
  - Active channel width: width values stored as attributes 'Year' and 'Width' (point features for width analysis years).
  - Anabranching index and related metrics: annual CSVs with values by reach/section.
  - Reaches/sections: provided as Reaches_sections.shp to define geometry and segmentation.

## Acquisition, processing, and methods
- Wet river area: automated extraction from Landsat 5–8 post-monsoon imagery using mNDWI; threshold > 0.15; manual pixel editing; raster-to-polygon conversion.
- Active gravel bars: identified via high red reflectance (>0.16) on post-monsoon Landsat; within a buffer defined by maximum observed wet area; raster-to-vector conversion.
- Active channel area: derived by unioning annual wet areas across years to define consistently wetted extents.
- Active channel width: computed as width of wet area perpendicular to riverbank; 2 km sampling increments; also derived from historic 1847 map for comparison.
- Anabranching index: computed from cross sections (minimum spacing equal to braid-plain width) across Reaches 1 and 2 and sections.
- Documentation references for methods: Huang et al. (2018), Langat et al. (2019), Li et al. (2017), and the Vercruysse & Grabowski (2021) paper.

## Data quality and validation
- Landsat spectral data include quality assessment bands to select cloud-free images.
- Processing includes project-team validation and spot checks against aerial photography.
- Data quality control performed by Cranfield University team.

## File listing (structure and contents)
- 1. Post monsoon season wet river area, annually 1989–2018
  - Beas_PM_Wetted_annual.shp
  - Sutlej_PM_Wetted_annual.shp
- 2. Post monsoon season active gravel bars, annually 1989–2018
  - Active_Gravel_Bars_Annual.shp
- 3. Active channel area (maximum extent 1989–2018)
  - Beas_ActiveChannel_BelowDam.shp
  - Sutlej_ActiveChannel_BelowDam.shp
- 4. Active channel width 1989–2018
  - Beas_Width_Annual.shp
  - Sutlej_Width_Annual.shp
- 5. Active channel width from historic map (1847–1850)
  - Beas_Width_1847.shp
  - Sutlej_Width_1847.shp
- 6. Metrics (AI, mean active channel width and wet river area), annually 1989–2018
  - Metrics_Annual_Beas.csv
  - Metrics_Annual_Sutlej.csv
  - Reaches_sections.shp (definition of Reach and section)

## Usage notes for GIS specialists
- Ideal for map-based visualization of multi-temporal river dynamics and for comparing current versus historic channel configurations.
- Layers can be joined by Year to build time-series visualizations of wet areas, gravel bars, and channel width.
- Reaches and sections provide a spatial framework for regional analyses and basin-scale comparisons.
- CSV metrics enable quantitative trend analysis (AI, mean width, wet area) alongside the spatial shapefiles.
- Coordinate system is WGS84; ensure project settings align with other GIS data for seamless integration.

## References
- Huang, C., Chen, Y., Zhang, S., & Wu, J. (2018). Detecting, Extracting, and Monitoring Surface Water From Space Using Optical Sensors: A Review.
- Langat, P. K., Kumar, L., & Koech, R. (2019). Monitoring river channel dynamics using remote sensing and GIS techniques.
- Li, H., et al. (2017). Mapping Urban Bare Land Automatically from Landsat Imagery with a Simple Index.
- Revenue Survey of India (1852). The Trans-Sutluj Division.
- Vercruysse, K., & Grabowski, R. C. (2021). Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system. Geomorphology.