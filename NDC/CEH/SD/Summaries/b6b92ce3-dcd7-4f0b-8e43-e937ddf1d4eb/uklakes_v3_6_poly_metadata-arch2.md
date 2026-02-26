# Spatial inventory of UK waterbodies

## Overview
- A dataset of polygons corresponding to the UK Lakes Portal and the underlying database informing it.
- Originates from OS PANORAMA data (~1993) with edits over time; primarily represents historical lake outlines with some updates.
- Used widely for research on UK lakes and ponds; Water Body ID (WBID) is a common research identifier.
- Managed and updated by Philip Taylor; supports names expansion through local knowledge and maps.

## Access and licensing
- Data available under the Open Government Licence at https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43-e937ddf1d4eb
- When using the data, cite: Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43e937ddf1d4eb
- Portal for related information: https://eip.ceh.ac.uk/apps/lakes/

## What the dataset contains
- Polygons that accompany the UK Lakes Portal and the underlying database.
- WBID (Water Body ID) serves as a common identifier across institutions.
- NAME (Water Body Name) compiled from OS data, maps, and crowd-sourcing.
- POLY_AREA_HA and POLY_PERIMETER_KM computed from spatial data (may differ from historical values).
- geom geometry field for GIS software; dataset saved as a GeoPackage (gpkg).

## Data quality and limitations
- Based on Ordnance Survey data; post-publication changes may reflect rework.
- Some original quality issues may be replicated if present in the source data.
- Nearly 30 years since the dataset’s creation; real-world changes (especially for managed waterbodies) may not be reflected.
- New, larger waterbodies (e.g., reservoirs) generally not included; ponds under 1 ha are poorly represented.
- Crowd-sourced data incorporated with prior quality checks.

## Dataset details and format
- Format: GeoPackage (.gpkg), compatible with common GIS software.
- Projection: OSGB 1936 / British National Grid (EPSG: 27700).
- Filename: uklakes_v3_6_poly.gpkg (versioning aligns with the underlying database, updated regularly).
- Key attributes:
  - WBID: Water Body ID
  - NAME: Water Body Name
  - POLY_AREA_HA: Polygon area in hectares
  - POLY_PERIMETER_KM: Polygon perimeter in kilometers
  - geom: Geometry of the polygons

## Usage and provenance
- The dataset is widely used for research into lakes and ponds across the UK by many institutions and individuals.
- WBID is a widely adopted identifier to synchronize research across sources.
- Regularly used to support the UK Lakes Portal and related environmental monitoring efforts.

## References
- Hughes, M., Hornby, D.D., Bennion, H. et al. The Development of a GIS-based Inventory of Standing Waters in Great Britain together with a Risk-based Prioritisation Protocol. Water, Air, & Soil Pollution: Focus 4, 73-84 (2004). https://doi.org/10.1023/B:WAFO.0000028346.27904.83