# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Overview
- Dataset supports assessment of flood exposure from Tsho Rolpa Lake, Nepal (GLOF) for downstream areas.
- Location: downstream area of Tsho Rolpa Lake (27°30′-27°51′ N, 86°10′-86°29′ E).
- Projection: WGS 1984 Transverse Mercator; spatially corrected to match high-resolution imagery (Google Earth); spatial accuracy not quantified due to lack of reference data.
- Exposure objects considered under different flooding scenarios; exposure estimates summarized in a comprehensive table.

## Data contents
- 1 TIFF file: Agriculture land (30m x 30m resolution).
- 3 shapefiles: Buildings, Infrastructure, Road.
- Additional exposure-related data across multiple asset categories (e.g., schools, police, libraries, parks, playgrounds, hospitals, medical practices, airports, gas stations, bus stations, bridges, and various commercial/amenity types) with scenario-based values (e.g., final breach depths, current water levels, and water level rise scenarios).
- Dataset specifies that exposure is determined by overlaying predicted flood inundation maps with these asset datasets.

## Collection methods
- Flood scenarios generated using a simple dam breach model; flood hydrodynamics simulated with a high-performance hydrodynamic model.
- Socioeconomic information gathered from multiple sources: OpenStreetMap, Google Earth, and global data products.
- Exposure of objects identified by overlaying predicted inundation maps with processed datasets.

## Quality control
- Building data primarily sourced from OpenStreetMap; positions refined using sub-meter imagery from ArcGIS Server and Google Earth.
- Inundation area for worst-case scenario had dozens of buildings missing; these were manually mapped into the dataset.
- Manual corrections applied to obvious spatial imperfections.

## Data structure and units
- Data structure comprises:
  - Agriculture land: a single TIFF file.
  - Buildings: a shapefile with point features.
  - Infrastructure: a shapefile with point features.
  - Road: a shapefile with line features.
- Units:
  - Agriculture land: TIFF (30m x 30m grid).
  - Buildings and infrastructure: points.
  - Roads: lines.

## Analytical approach
- Exposure of objects determined by spatially overlaying predicted flood inundation maps with the corresponding exposure datasets.
- Provides scenario-based exposure estimates for multiple asset types and areas, enabling prioritization of mitigation and response planning.

## Implications for data leadership and governance
- Demonstrates end-to-end data workflow: from hazard modelling to exposure mapping and socio-economic overlay.
- Highlights the importance of data provenance, integration of diverse data sources (OSM, Google Earth), and the need for manual QA to address gaps.
- Useful for risk assessment, planning and coordination with partners, and informing data product development (e.g., dashboards, alerts, and decision-support tools).

## Limitations and considerations
- Spatial accuracy not quantified; rely on corrections to high-resolution imagery.
- Notable data gaps in inundation area (missing buildings) required manual supplementation.
- Granularity of some exposure estimates is constrained by data resolution (30m grid for agriculture; point/line features for other assets).

## Practical next steps for Data Leaders
- Establish metadata standards and versioning to track model updates and data corrections.
- Maintain and share documentation on data sources, modelling assumptions, and QA processes to improve transparency and trust.
- Explore integration with other datasets (e.g., population demographics, critical facilities) to enhance decision-support products.
- Plan for periodic updates as new imagery and data become available, and consider automating QA checks to minimize manual corrections.