# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Overview
- Identifies exposed objects at risk from floods originating from the Tsho Rolpa Lake, Nepal.
- Focuses on downstream area (coordinates provided) with a WGS 1984 Transverse Mercator projection.
- Spatially corrected to align with high-resolution imagery (Google Earth); accuracy not quantified due to lack of reference data.
- Presents exposure estimates for buildings, agriculture, roads, and various social and infrastructure categories under multiple flood scenarios.

## Data content and structure
- Exposure data are summarized under different GLOF (glacier lake outburst flood) scenarios, including various breach depths and water rise levels.
- Data types:
  - Agriculture land: raster (TIFF), 30 m x 30 m resolution.
  - Buildings, Infrastructure, Roads: vector data (shapefiles) representing points (buildings/infrastructure) and lines (roads).
- Dataset components:
  - 1 TIFF file: Agriculture land
  - 3 shapefiles: Buildings, Infrastructure, Road
- Exposure estimates cover diverse categories (e.g., schools, police, library, park, hospital, hotel, restaurant, commercial sectors, and various shops and services) across scenarios.

## Methods and data sources
- Scenarios generated with a simple dam breach model; flood hydrodynamics simulated with a high-performance hydrodynamic model.
- Socioeconomic information sourced and processed from:
  - OpenStreetMap
  - Google Earth
  - Other global data products
- Exposure of objects identified by overlaying predicted flood inundation maps with prepared exposure datasets.

## Data quality and processing
- Building data primarily from OpenStreetMap; positions deemed reasonably accurate using sub-meter imagery as references.
- Inundation area for the worst-case scenario revealed dozens of missing buildings that were manually added to the dataset.
- Some spatial imperfections were corrected through manual adjustments.
- Metadata and data provenance are managed through data processing steps to ensure consistency with the underlying maps and imagery.

## Spatial and technical details
- Location: downstream area of Tsho Rolpa Lake (27°30′–27°51′ N, 86°10′–86°29′ E).
- Projection: WGS 1984 Transverse Mercator.
- Data accuracy: not quantified due to lack of reference data; spatial corrections performed to align with high-resolution imagery.
- Data units:
  - Agriculture land: TIFF (raster, 30 m resolution)
  - Buildings, Infrastructure: point features
  - Road: line features

## Practical implications for monitoring and decision-making
- Provides a transparent workflow for estimating population- and asset-exposure under multiple GLOF scenarios.
- Supports monitoring framework needs by:
  - Using open or widely accessible data sources (OpenStreetMap, Google Earth) to assemble exposure datasets.
  - Documenting model-based scenario generation (dam breach model) and hydrodynamic simulation approach.
  - Detailing data processing steps, corrections, and quality controls to improve reproducibility.
- Highlights challenges relevant to monitoring frameworks, such as data gaps, the need for timely data access, and the importance of validating spatial data accuracy and completeness.