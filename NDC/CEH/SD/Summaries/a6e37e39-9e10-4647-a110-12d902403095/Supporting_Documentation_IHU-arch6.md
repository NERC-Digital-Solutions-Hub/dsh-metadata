# Integrated Hydrological Units of the United Kingdom

## Overview
- The Integrated Hydrological Units (IHU) of the United Kingdom consist of five polygon layers that represent different levels of spatial detail:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Key relationships:
  - Groups are medium-resolution units composed of Sections.
  - Groups can be combined to form Hydrometric Areas without Coastline.
  - Sections are drainage areas between confluences with named rivers.
  - Catchments represent the full area upstream from an outlet of every Section (can overlap with other layers).

## Coverage and Boundaries
- Hydrometric Areas with Coastline: covers Great Britain and Northern Ireland (coastal representation).
- Hydrometric Areas without Coastline, Groups, Sections, Catchments: cover Great Britain (NI data limited/not present for these layers).
- The boundary alignment differs between coastline (coastline following coast) and without Coastline (follows IHDTM boundaries).
- Northern Ireland catchments are clipped to national boundaries, so some hydrological completeness is not shown across borders.
- Some minor rivers may not be captured even within Great Britain.

## Data Creation, Provenance, and History
- Origins trace to the Inland Water Survey Committee (1930s) and national hydro-data frameworks; numbering conventions described in historical sources.
- The dataset was integrated into the Integrated Hydrological Units in 2015.
- Boundaries for GB are derived from CEH’s IHDTM (digital terrain model); GB coastline uses the Ordnance Survey Meridian2 coastline.
- Northern Ireland boundaries/coastlines derived from OS GB Panorama data.
- Islands were merged to the nearest relevant Hydrometric Area in 2014 to achieve complete UK surface-area coverage (examples listed: Isles of Scilly, Lundy, St Kilda group, etc.).

## Data Structure and Attributes
- Primary format: Geodatabase (preserves NULL values; Shapefile may convert NULLs to zeros or empty strings when downloaded).
- Hydrometric Areas with Coastline (HA_NUM, HA_NAME, HA_ID, etc.).
- Hydrometric Areas without Coastline (HA_NUM, HA_NAME, HA_ID, etc.).
- Groups (attributes include G_ID, G_NAME, G_AREA_KM2, RIVER-related fields, HA_ID, etc.).
- Sections (attributes include S_ID, S_NAME, S_AREA_KM2, G_ID, HA_ID, RIVER fields, OUTF_X/Y, etc.).
- Catchments (attributes include coordinates of outlet, centroid, KMSQ area, S_ID for downstream section, etc.).
- Most datasets are designed to maintain topological integrity and provide unique identifiers for cross-layer relationships (e.g., S_ID, G_ID, HA_ID).

## Quality, Limitations, and Maintenance
- Quality tied to the underlying IHDTM resolution of 50 m.
- Some rivers and drainage features may be missing or not perfectly captured, even in Great Britain.
- No routine updates are planned; updates may occur to fix errors or incorporate improvements to underlying rivers or drainage grid data.
- Outputs are designed to be topologically correct with no gaps or overlaps, ensuring every UK point is allocated to a single Hydrometric Area.

## Usage and Considerations
- The layered structure supports hydrometric data management and analyses that require alignment with hydrological boundaries.
- Coarse-to-fine fidelity: Coastline layer suitable for cartography; without Coastline layer suitable for analyses requiring exact IHDTM boundary matching.
- Users should be aware of potential data gaps in NI and the possibility of missing minor rivers; consider cross-border continuity limitations when analyzing NI-GB hydrology.
- When exporting to Shapefile, NULL values may be converted, so prefer Geodatabase for preserving NULLs.

## Naming, Numbering, and Cross-References
- Hydrometric Areas are numbered using a two-digit code; Irish hydrometric areas have regional prefixes (e.g., 2 for Ireland).
- National River Flow Archive (NRFA) gauging station numbers reuse the regional identifier and Hydrometric Area number with additional digits.
- Islands and cross-border features were reconciled to maintain consistent UK coverage and naming conventions.