# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Purpose and scope
- Identifies exposed objects subject to flooding risk from Tsho Rolpa Lake (glacier lake outburst flood risk assessment).
- Study area: downstream area (27°30′–27°51′ N, 86°10′–86°29′ E); map projection is WGS 1984 Transverse Mercator.
- Spatial accuracy not quantified due to lack of reference data; data have been spatially corrected to align with high-resolution imagery from Google Earth.
- Exposure data are provided under different flooding scenarios, summarized in Table 1 (including various breach depths and water rise levels) for buildings, agriculture, roads, schools, police, libraries, parks, playgrounds, hospitals, airports, hotels, shops, and other infrastructure.

## Data contents and structure
- Data types:
  - Agriculture land: 1 TIFF file (30 m × 30 m resolution).
  - Buildings, infrastructure, roads: 3 shapefiles (points for buildings/infrastructure, lines for roads).
- Data units:
  - Agriculture land: raster (30 m resolution).
  - Buildings and infrastructure: point features.
  - Roads: line features.
- Coverage: exposure estimations cover multiple object types (buildings, roads, public facilities, businesses, and other infrastructure) under various flood scenarios.

## Methods and collection
- Scenarios generated with a simple dam breach model.
- Flood dynamics simulated with a high-performance hydrodynamic model.
- Socioeconomic data compiled from OpenStreetMap, Google Earth, and other global datasets to support exposure analysis.
- Exposure identified by overlaying predicted flood inundation maps with the processed datasets.

## Data quality and curation
- Building data initially sourced from OpenStreetMap; positions cross-checked against sub-meter imagery (ArcGIS Server, Google Earth).
- Inundation area for the worst-case scenario contained missing buildings; dozens were manually added/adjusted in ArcGIS.
- Some obvious spatial imperfections corrected.
- No formal quantified accuracy metric provided; corrections documented via manual mapping and alignment to imagery.

## Detailed data characteristics
- Table 1 provides exposure estimates for each category (e.g., buildings, agriculture, roads, schools, police, hospitals, airports, commercial facilities, and various business types) under different scenarios (final breach depths and water rise levels).
- The dataset combines both physical exposure (area/length/counts) and potential impact across a range of local features (e.g., hotels, guesthouses, shops, parks, transit facilities).

## Practical use and interpretation
- Designed to support risk assessment, planning, and decision-making by identifying which assets are exposed under specific GLOF scenarios.
- Overlay capability enables analysts to quantify affected populations, infrastructure, and spatial planning needs.
- Datasets are prepared for GIS workflows and can be uploaded or linked with metadata for discoverability.

## Data provenance and access notes
- Data produced by combining simple breach modeling, hydrodynamic simulations, and spatially referenced socio-economic datasets.
- Primary sources include OpenStreetMap, Google Earth, and global data products; corrections were made within ArcGIS to improve completeness in inundation zones.