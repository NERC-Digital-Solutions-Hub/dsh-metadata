# Spatial inventory of UK waterbodies

## Access, licensing and citation
- Data accessible under the Open Government Licence.
- Citation required: Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre. (Dataset).
- DOI link provided for access.

## Data description and scope
- Contains polygons corresponding to the UK Lakes Portal and the underlying informing database.
- Polygons largely originate from OS PANORAMA data (~1993) with edits over time.
- Notable updates: additions in Northern Ireland (WFD lakes) and some large lakes split into basins.
- Water Body ID (WBID) used as a common cross-institution identifier; lake names expanded via local knowledge and maps.
- Managed and maintained by Philip Taylor.

## Data access and format
- Dataset provided as a GeoPackage (.gpkg) named uklakes_v3_6_poly.gpkg.
- Projection: OSGB 1936 / British National Grid (EPSG: 27700).
- Primary attributes:
  - WBID: Water Body ID (cross-institution identifier).
  - NAME: Water Body Name (from OS data, maps, crowd-sourcing).
  - POLY_AREA_HA: Polygon area in hectares (computed from spatial data; may differ from historical values).
  - POLY_PERIMETER_KM: Polygon perimeter in kilometres (computed; may differ from historical values).
  - geom: Geometry for GIS software (not typically in attribute table).
- Polygons largely reflect OS data, with updates noted in project-specific areas; dataset emphasizes discoverability and interoperability.

## Data quality, provenance, and caveats
- Quality control: changes checked and approved before publishing; any original quality issues may persist.
- Age of data: nearly 30 years since creation; real-world changes (new or altered lakes) may not be reflected.
- Gaps: new larger waterbodies (e.g., reservoirs) not reflected; ponds smaller than 1 hectare are poorly represented.
- Crowd-sourced data incorporated with prior quality checks before publication.
- Name and boundary adjustments occur when projects focus on specific areas.

## Governance, metadata, and versioning
- Versioning tied to the underlying database; dataset updated regularly.
- WBID used as a stable cross-institutional key to keep research aligned.
- Primary maintenance and dataset management associated with CEH staff (Philip Taylor).

## Implications for data strategy and use
- Supports cross-institutional data integration and policy/academic research through a stable lake/waterbody reference.
- Highlights the importance of ongoing data updating to capture new/larger waterbodies and granular definitions.
- Important considerations for data leaders:
  - Ensure timely updates to reflect real-world changes in lake boundaries and new waterbodies.
  - Assess and document limitations for small ponds and older data layers.
  - Maintain robust metadata and clear provenance to support discoverability and reuse.
  - Leverage WBID for harmonization across datasets and partners.

## References
- Hughes, M., Hornby, D.D., Bennion, H. et al. (2004). The Development of a GIS-based Inventory of Standing Waters in Great Britain together with a Risk-based Prioritisation Protocol. Water, Air, & Soil Pollution: Focus, 4, 73-84.