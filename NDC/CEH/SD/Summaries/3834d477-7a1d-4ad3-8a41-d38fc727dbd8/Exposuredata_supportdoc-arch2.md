# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Overview
- Tsho Rolpa Lake is the largest moraine-dammed proglacial lake in Nepal and is identified as a high-risk glacier lake with potential for outburst floods (GLOF).
- The dataset identifies exposed objects downstream that would be affected by flooding from the lake.
- Location: downstream area (27°30′-27°51′ N, 86°10′-86°29′ E) with a WGS 1984 Transverse Mercator projection.
- Spatial accuracy is not quantified due to limited reference data; data have been spatially corrected to align with high-resolution Google Earth imagery.

## Data scope and content
- Exposures modeled under different GLOF scenarios using a simple dam breach model followed by hydrodynamic simulation.
- Objects analyzed include: buildings, agriculture, roads, schools, police, library, park, playground, hospital, medical practice, airport, gas station, bus station, bridge, commercial entities, and various service/amenity categories.
- The table summarizes exposure estimates under multiple breach depths and water levels, indicating how much area or how many objects are impacted under each scenario.
- Socioeconomic information and exposure data are derived from OpenStreetMap, Google Earth, and other global data products; exposure is determined by overlaying predicted flood inundation maps with these datasets.

## Collection methods
- GLOF scenarios generated with a simple dam breach model.
- Hydrodynamic model used to simulate flood dynamics.
- Detailed socioeconomic data collected and processed from multiple sources (OpenStreetMap, Google Earth, global data products).
- Exposure of objects identified by overlaying predicted flood maps with processed exposure datasets.

## Quality control
- OpenStreetMap-based building data cover most buildings; positions refined using sub-meter imagery from ArcGIS Server and Google Earth.
- Inundation area for worst-case scenarios revealed dozens of missing buildings; these were manually added to the dataset in ArcGIS.
- Some spatial imperfections were corrected to improve dataset reliability.

## Nature and units of recorded values
- Agriculture land: stored as TIFF with 30 m × 30 m resolution.
- Buildings and Infrastructure: represented as points.
- Roads: represented as lines.

## Analytical methods
- Exposure is determined by spatially overlaying predicted flood inundation maps with exposure datasets (buildings, infrastructure, roads, etc.).

## Details of data structure
- 1 TIFF file: Agriculture land.
- 3 shapefiles: Buildings, Infrastructure, and Road.

## Data accuracy and limitations (summary for monitoring analysts)
- Spatial accuracy not quantified due to lack of reference data; corrected to align with high-resolution imagery.
- Some buildings within the worst-case inundation area were initially missing and later manually added to improve completeness.
- Projection: WGS 1984 Transverse Mercator.

## Use and potential of the dataset
- Provides standardized exposure assessments across multiple GLOF scenarios for planning, risk communication, and policy performance monitoring.
- Aligns with standard monitoring practices: verify data, quality assure, clean, transform, apply standardised analytical methods, and present outputs (maps, charts, reports).
- Datasets are suitable for storage and sharing via appropriate portals; can be combined with other datasets to increase value and support broader environmental health and risk monitoring.