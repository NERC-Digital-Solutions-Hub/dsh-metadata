# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Overview
- Describes a data product identifying exposed objects downstream of Tsho Rolpa Lake, Nepal, a high-risk glacier lake outburst flood site.
- Focuses on identified exposure to flooding risk for buildings, infrastructure, roads, agriculture, and population within the downstream area (27°30′–27°51′ N, 86°10′–86°29′ E).
- Map projection: WGS 1984 Transverse Mercator. Spatial corrections performed to align with high-resolution imagery (Google Earth); spatial accuracy not quantified due to lack of reference data.

## Data content
- Exposure objects are categorized and summarized under different flood scenarios (glacier lake outburst flood, GLOF).
- Key asset types included: buildings, infrastructure, roads, agriculture area, schools, police, libraries, parks, hospitals, medical facilities, banks, tourism-related assets, hotels, guesthouses, campsites, restaurants, and various commercial entities.
- Units vary by asset type:
  - Agriculture: area in square kilometers (saved as a 30 m × 30 m TIFF).
  - Buildings, infrastructure: represented as points.
  - Roads: represented as lines.
- Dataset structure comprises 1 TIFF file (Agriculture land) and 3 shapefiles (buildings, infrastructure, road).

## Exposure and scenarios
- Table 1 (Exposure estimations) lists exposure under multiple GLOF scenarios, including:
  - Scenario variables such as final breach depth (m), current water levels (10/20/30), and water level rise (1m, 5m, 10m, 20m, 30m).
  - Corresponding metrics for each asset type (e.g., number of affected buildings, affected road length, agriculture area impacted).
- The table covers a wide range of asset categories (e.g., buildings, roads, schools, hospitals, banks, hotels, tourist sites, commercial premises, and various small businesses) with scenario-based impact counts/areas.

## Collection methods
- GLOF scenarios created using a simple dam breach model, followed by a high-performance hydrodynamic model to simulate flood dynamics.
- Detailed socioeconomic information gathered from multiple sources (OpenStreetMap, Google Earth, global data products) to support exposure analysis.
- Exposure of objects identified by overlaying predicted flood inundation maps with processed exposure datasets.

## Quality control
- Building data derived from OpenStreetMap; positions cross-checked using sub-meter imagery from ArcGIS Server and Google Earth.
- Inundation area for the worst-case scenario revealed missing dozens of buildings; these were manually mapped into the building dataset in ArcGIS.
- Some obvious spatial imperfections are corrected to improve dataset reliability.

## Nature and units of recorded values
- Agriculture land: raster TIFF (30 m × 30 m resolution).
- Buildings and infrastructure: point features.
- Roads: line features.

## Analytical methods
- Exposure identification achieved by spatially overlaying predicted flood inundation maps with exposure datasets.

## Details of data structure
- 1 TIFF file: Agriculture land.
- 3 shapefiles: buildings, infrastructure, road.

## Projection and accuracy notes
- Projection: WGS 1984 Transverse Mercator.
- Spatial accuracy is not quantified due to lack of reference data; data have been spatially corrected to align with high-resolution imagery, with manual adjustments where necessary.

## Practical implications for GIS workflows
- Suitable for map-based data products showing spatially explicit exposure under multiple flood scenarios.
- Requires integration with other GIS layers to support decision-making for policy, planning, and emergency response.
- Highlights the need for ongoing data cleaning and validation when incorporating multi-source data (OSM, Google Earth, others) and when modeling flood extents.