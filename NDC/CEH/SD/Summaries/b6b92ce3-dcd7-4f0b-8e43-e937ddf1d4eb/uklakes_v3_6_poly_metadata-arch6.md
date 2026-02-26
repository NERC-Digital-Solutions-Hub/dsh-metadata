# Spatial inventory of UK waterbodies

- Data access and licensing
  - Available at https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43-e937ddf1d4eb
  - Open Government Licence; must cite Taylor, P.J. (2021) when using the data
  - Dataset DOI provided for citation

- Data description and content
  - Contains polygons for the UK Lakes Portal and the underlying database
  - Polygons originate from OS PANORAMA data (~1993) and have been edited over time; few new lakes added
  - Notable additions: Northern Ireland WFD lakes and some large lake basins split and added
  - Water Body ID (WBID) functions as a common identifier across institutions
  - Efforts to increase lake names using local knowledge and maps
  - Dataset management and general oversight by Philip Taylor

- Data quality and limitations
  - Based on Ordnance Survey data; published changes are reviewed and approved
  - Given ~30 years since creation, real-world changes may not be reflected
  - Large reservoirs and new water bodies may be missing; ponds <1 ha are poorly represented
  - Crowd-sourced contributions are checked prior to publishing

- Dataset details and structure
  - Format: GeoPackage (.gpkg)
  - Projection: OSGB 1936 / British National Grid (EPSG: 27700)
  - File name: uklakes_v3_6_poly.gpkg (versioning tied to the underlying database, updated regularly)
  - Key attributes:
    - WBID: Water Body ID
    - NAME: Water Body Name
    - POLY_AREA_HA: Polygon Area in hectares
    - POLY_PERIMETER_KM: Polygon Perimeter in kilometres
    - geom: Geometry for GIS software
  - Regularly used for research into UK lakes and ponds by many institutions; WBID is a widely used research sync identifier

- Usage and implications for data products
  - Supports data exploration and self-serve analysis via the Lakes Portal
  - Provides standardized, downloadable GIS-ready data for broad policy, research, and planning use
  - Outputs can be integrated with other datasets; awareness of potential outdated areas and underrepresented small ponds is important

- References
  - Hughes, M. et al. (2004). The Development of a GIS-based Inventory of Standing Waters in Great Britain... (DOI provided)
  - Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre. (Dataset) (DOI provided)