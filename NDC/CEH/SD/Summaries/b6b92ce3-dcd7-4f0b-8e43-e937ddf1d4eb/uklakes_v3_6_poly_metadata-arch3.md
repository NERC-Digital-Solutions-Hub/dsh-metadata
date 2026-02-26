# Spatial inventory of UK waterbodies

## Overview
- A dataset of polygons for UK lakes linked to the UK Lakes Portal and its underlying database.
- Based largely on OS PANORAMA data from circa 1993, with edits over time; some additions in Northern Ireland (WFD lakes) and splits of large lake basins.
- Water Body ID (WBID) serves as a common identifier across institutions.
- Managed and maintained by Philip Taylor; dataset widely used for lake and pond research in the UK.

## Access and licensing
- Available under the Open Government Licence.
- Must be cited as: Taylor, P.J. (2021). Spatial inventory of UK waterbodies. NERC EDS Environmental Information Data Centre. Dataset. DOI provided in the data link.

## Data description and scope
- Contains polygons corresponding to the UK Lakes Portal and the supporting database.
- Originates from OS data (~1993) with revisions; some areas updated through project-specific improvements.
- Many lakes have not been newly added; a focus on updating and improving existing records.
- Limitations: new, larger waterbodies (e.g., reservoirs) may not be reflected; ponds smaller than ~1 ha are poorly represented.
- Data widely used for research, with WBID facilitating cross-institution research and data integration.

## Dataset format and attributes
- Format: GeoPackage (.gpkg), compatible with common GIS tools.
- Projection: OSGB 1936 / British National Grid (EPSG 27700).
- Filename: uklakes_v3_6_poly.gpkg; versioning ties to the underlying database (updated regularly).
- Key attributes:
  - WBID (Water Body ID): cross-institution identifier.
  - NAME: water body name (from OS data, maps, or crowd-sourced sources).
  - POLY_AREA_HA: polygon area in hectares (computed from spatial data; may differ from historical values).
  - POLY_PERIMETER_KM: polygon perimeter in kilometers (computed from spatial data; may differ from historical values).
  - geom: polygon geometry for GIS use.

## Quality control and limitations
- Original data based on Ordnance Survey; changes checked and approved before publication, though some original quality issues may persist.
- Real-world changes since ~1993 mean some outlines may be outdated; large waterbodies may be missing from updates.
- Ponds under 1 ha are underrepresented.
- Crowdsourced data incorporated after validation and publishing checks.

## Governance, maintenance, and updates
- Dataset management and lake naming enhancements carried out over time; updates to the underlying database are ongoing.
- Sustained oversight by Philip Taylor; regular updates reflect improvements and data additions where available.

## References
- Hughes, M., Hornby, D.D., Bennion, H. et al. The Development of a GIS-based Inventory of Standing Waters in Great Britain together with a Risk-based Prioritisation Protocol. Water, Air, & Soil Pollution: Focus 4, 73-84 (2004). DOI: 10.1023/B:WAFO.0000028346.27904.83

## Usage notes for monitoring frameworks
- Provides a canonical, GIS-ready dataset of UK standing waters with a common identifier (WBID) for cross-study comparability.
- Enables calculation of area and perimeter metrics for environmental health assessments.
- Useful for policy monitoring, trend analysis, and informing future decision-making, while requiring attention to data freshness and metadata quality.
- Open license and clear citation requirements support transparent data governance and reproducible analyses.