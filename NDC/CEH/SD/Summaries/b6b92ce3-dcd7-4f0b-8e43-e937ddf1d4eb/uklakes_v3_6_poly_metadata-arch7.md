# Spatial inventory of UK waterbodies

- Data access and licensing
  - Available at https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43-e937ddf1d4eb under the Open Government Licence.
  - Usage requires citation: Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre.

- Data description
  - Contains polygons that accompany the UK Lakes Portal and the underlying database.
  - Source and history
    - Polygons originally from OS PANORAMA data, edited over time.
    - Primarily reflects OS data from ~1993; some outlines updated; few new lakes added.
    - Additions mainly in Northern Ireland (WFD lakes) and some large lakes where basins were split.
    - Changes driven by project focus, improvements, or targeted work; managed under Philip Taylor.
  - Identifiers and naming
    - Water Body ID (WBID) used as a common identifier across institutions.
    - Water Body Names (NAME) sourced from OS data, maps, and crowd-sourcing.
  - Usage
    - Regularly used for lakes/ponds research by multiple institutions and individuals.
    - Portal management and naming enhancements also reflected in the dataset.

- Quality control and limitations
  - Based on Ordnance Survey data; published changes checked and approved; any original quality issues may persist.
  - Nearly 30 years since creation; real-world changes may not be reflected (e.g., new reservoirs).
  - Ponds smaller than 1 hectare are underrepresented.
  - Some new NI waterbodies added; crowd-sourced data checked prior to publication.

- Dataset details
  - Format: GeoPackage (.gpkg), suitable for widely used GIS software.
  - Projection: OSGB 1936 / British National Grid (EPSG: 27700).
  - File: uklakes_v3_6_poly.gpkg; versioning tied to the underlying database, updated regularly.
  - Attributes
    - WBID: Water Body ID (cross-institution identifier).
    - NAME: Water Body Name (from multiple sources).
    - POLY_AREA_HA: Polygon area in hectares (computed; may differ from historical values).
    - POLY_PERIMETER_KM: Polygon perimeter in kilometres (computed; may differ from historical values).
    - geom: Geometry detailing polygon shapes (for GIS software; not typically in the attribute table).

- References
  - Hughes, M. et al. (2004). The Development of a GIS-based Inventory of Standing Waters in Great Britain together with a Risk-based Prioritisation Protocol. Water, Air, & Soil Pollution: Focus 4, 73-84. DOI: https://doi.org/10.1023/B:WAFO.0000028346.27904.83