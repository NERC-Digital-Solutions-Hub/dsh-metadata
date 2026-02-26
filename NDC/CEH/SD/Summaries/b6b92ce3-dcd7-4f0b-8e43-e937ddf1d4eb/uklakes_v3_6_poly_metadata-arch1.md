# Spatial inventory of UK waterbodies

## Overview
- A GIS dataset of polygons corresponding to UK lakes and waterbodies, linked to the UK Lakes Portal.
- Polygons originally come from OS PANORAMA data (~1993) with edits over time.
- Water Body ID (WBID) serves as a common identifier across institutions.
- The dataset supports research into lakes and ponds across the UK and underpins the Lakes Portal.

## Data access and licensing
- Available under the Open Government Licence.
- Data can be accessed via DOI: https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43-e937ddf1d4eb
- When used, cite: Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43e937ddf1d4eb

## Data content and structure
- Polygons and the underlying database inform the UK Lakes Portal.
- Northern Ireland additions include WFD lakes; some large lakes have basins split and added individually.
- Some changes reflect project focus areas or improvements; older data largely retained.
- Core attributes:
  - WBID: Water Body ID (shared research identifier)
  - NAME: Water Body Name (from OS data, maps, crowd-sourcing)
  - POLY_AREA_HA: Polygon area in hectares (computed)
  - POLY_PERIMETER_KM: Polygon perimeter in kilometres (computed)
  - geom: Geometry for GIS software (not usually in attribute table)
- File format and projection:
  - GeoPackage (.gpkg)
  - OSGB 1936 / British National Grid (EPSG: 27700)
  - Filename: uklakes_v3_6_poly.gpkg

## Data provenance and maintenance
- Managed by Philip Taylor (CEH), with ongoing updates to the underlying database.
- Versioning tied to dataset updates; the polygon dataset is updated periodically.
- The dataset aligns with the broader UK Lakes Portal and its database.

## Quality control and limitations
- Based on Ordnance Survey data; post-publication changes may still reflect original quality issues.
- Real-world changes (e.g., new reservoirs) may not be reflected; ponds under 1 ha are generally underrepresented.
- When crowd-sourced data is used, it has been checked prior to publishing.
- Data limitations to consider for analyses:
  - Potential misalignment with current lake boundaries due to time lag.
  - Scale limitations for local-level analyses or rapidly changing landscapes.
  - Differences between computed polygon metrics and historical portal values.

## Use and applications
- Ideal for researchers needing a common lake identifier, spatial boundaries, and basic metrics.
- Supports analyses across UK lakes and ponds and integration with the UK Lakes Portal.
- Useful as a base layer for ecological, hydrological, or governance-related studies at national and regional scales.

## References
- Hughes, M., Hornby, D.D., Bennion, H. et al. (2004). The Development of a GIS-based Inventory of Standing Waters in Great Britain together with a Risk-based Prioritisation Protocol. Water, Air, & Soil Pollution: Focus, 4, 73-84. doi:10.1023/B:WAFO.0000028346.27904.83