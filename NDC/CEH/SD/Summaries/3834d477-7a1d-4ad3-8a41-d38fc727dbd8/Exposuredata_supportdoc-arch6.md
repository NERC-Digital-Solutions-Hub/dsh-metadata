# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Purpose and scope
- Provides exposure analysis of objects (buildings, infrastructure, roads, agriculture, etc.) in downstream areas potentially affected by the Tsho Rolpa glacier lake outburst flood (GLOF).
- Spatially aligns predicted flood inundation with socio-economic datasets to identify exposed assets.
- Uses a defined geographic extent (downstream area around Tsho Rolpa) and a specified map projection (WGS 1984 Transverse Mercator).

## Data content
- 1 TIFF file: Agriculture land (30m × 30m resolution).
- 3 shapefiles: Buildings, Infrastructure, Road (vector representations; buildings and infrastructure as points, road as lines).
- Table 1 includes exposure estimations for different GLOF scenarios across various asset types (e.g., buildings, agriculture area, roads, schools, hospitals, businesses, and services).

## Collection methods
- GLOF scenarios produced with a simple dam breach model; flood hydrodynamics simulated with a high-performance hydrodynamic model.
- Socioeconomic data gathered from multiple sources including OpenStreetMap and Google Earth; overlay with predicted flood inundation to identify exposure.
- Exposed objects identified by spatially overlaying flood maps with the processed exposure datasets.

## Data quality and handling
- Building data primarily sourced from OpenStreetMap; positions refined using sub-meter imagery from ArcGIS Server and Google Earth.
- Within the worst-case inundation area, dozens of buildings were missing and were manually mapped into the dataset; other spatial imperfections were corrected.
- Spatial accuracy of the dataset is not quantified due to lack of reference data, but data were spatially corrected to align with high-resolution imagery.

## Data structure and attributes
- Agriculture land: stored as a TIFF file (raster) with 30m resolution.
- Buildings, Infrastructure: stored as point shapefiles (vector).
- Road: stored as a line shapefile (vector).

## Analytical approach
- Exposure analysis conducted by overlaying predicted flood inundation maps with the exposure datasets to determine which buildings, infrastructure, roads, and land areas are at risk under various GLOF scenarios.

## Practical applications and use cases
- Supports risk assessment, planning, and decision-making for affected regions in Nepal.
- Enables end-user self-service through geospatial products (e.g., exposure maps) and informs mitigation or response strategies.
- Data can be integrated into dashboards, reports, or further analyses for policy-making and public communication.

## Limitations and uncertainties
- Spatial accuracy not quantified due to limited reference data; corrections performed to align with high-resolution imagery.
- Some missing buildings within predicted inundation areas were manually added, indicating potential residual data gaps.
- Table 1 presents scenario-based exposure estimates that may vary with future data updates or methodological refinements.

## Access and data structure recap
- Location and projection: downstream area of Tsho Rolpa Lake; projection is WGS 1984 Transverse Mercator.
- Data products: 1 Agriculture land TIFF; 3 shapefiles (buildings, infrastructure, road).