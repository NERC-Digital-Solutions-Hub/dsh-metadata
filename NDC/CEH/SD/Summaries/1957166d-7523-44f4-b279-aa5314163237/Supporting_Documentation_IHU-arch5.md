# Integrated Hydrological Units (IHU) of the United Kingdom

- Multi-layer polygon dataset describing UK hydrological units at multiple spatial resolutions: 
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Purpose: support organization of UK river flow measurement and hydrometric data management; definitions and naming follow historical and contemporary conventions; layers interrelate to form hierarchical hydrological units.

## What each layer represents
- Hydrometric Areas with Coastline: coastal administrative groupings of river catchments; used for cartography and management; numbering and naming conventions align with NRFA and historical records.
- Hydrometric Areas without Coastline: same entities as with Coastline but boundaries follow the IHDTM; suitable for analyses requiring exact IHDTM alignment; not ideal for cartography.
- Groups: medium-resolution units (~400 km2 typical); comprised of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
- Sections: drainage area between two confluences; names built from participating rivers; each Section links to one Group and one Catchment; may include UNKNOWN/Source/Sea indicators where details are missing.
- Catchments: finest level, representing full upstream area from each Section outlet; can overlap multiple Sections/Groups; only layer with overlapping polygons.

## Data creation and lineage
- Boundaries digitally derived from CEH IHDTM using in-house tooling; Great Britain coastline aligned to OS Meridian2; Northern Ireland boundaries/coastlines from OS GB Panorama data.
- Islands reassigned in 2014 to the most appropriate existing Hydrometric Area based on proximity and conventions (e.g., Isles of Scilly merged with HA 49).
- 2014–2015: Islands and cross-boundary considerations addressed; in 2015 Hydrometric Areas incorporated into the IHU framework; boundaries made topologically correct with no gaps/overlaps within coverage constraints.
- NI catchments are clipped to the national boundary; cross-border catchments may be incomplete.

## Quality, limitations, and coverage
- Quality tied to the underpinning IHDTM at 50 m resolution; some minor rivers may be missing even in GB.
- Coverage: Hydrometric Areas with Coastline (GB+NI); other layers (Groups, Sections, Catchments) primarily GB, with NI limitations noted.
- Limitations: NI river geometries not as complete as GB; NI cross-border hydrology may not be fully represented in all layers.

## Attributes and data model
- Primary format: Geodatabase (preserves NULL values; Shapefile converts NULLs to zeros or empty strings).
- Tables describe attributes for each layer:
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID, etc.
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID, etc.
  - Groups: area/catchment metrics, RIVER identifiers, G_ID, G_NAME, G_AREA_KM2, etc.
  - Sections: S_ID, S_NAME, RIVER-related fields, S_AREA_KM2, CCAREA_KM2, HA_ID, G_ID, etc.
  - Catchments: geographic coordinates (EAST/NORTH), centroid coordinates, area (KMSQ), S_ID reference, etc.
- Note: If downloading as Shapefile, NULL values may be converted to zeros or empty strings.

## Updates and maintenance
- No routine updates anticipated; updates may occur if errors are found or if improvements to underlying river or drainage grid data become available.
- January 20, 2015 release date; data creation and structure reflect contemporary harmonization with IHDTM and CEH NRFA datasets.