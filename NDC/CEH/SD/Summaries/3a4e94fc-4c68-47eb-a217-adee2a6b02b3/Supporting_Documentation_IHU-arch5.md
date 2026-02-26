# Integrated Hydrological Units of the United Kingdom

## Purpose and scope
- Defines a set of polygon layers representing hydrological units at multiple spatial resolutions for the UK:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Hydrometric Areas with Coastline and without Coastline represent the same entities; the difference is boundary treatment (coastline vs IHDTM-derived). The without Coastline layer is best for analyses that require exact IHDTM-aligned boundaries; not ideal for cartography.
- Hierarchical structure: Groups are medium-sized units consisting of Sections; Groups can combine to form Hydrometric Areas without Coastline; Sections drain between confluences; Catchments are the full upstream areas from each Section outlet.

## What data you get
- Layer-specific details:
  - Hydrometric Areas with Coastline: GB and NI; some minor rivers may be omitted.
  - Hydrometric Areas without Coastline: GB-focused; aligns with IHDTM for precise data compatibility.
  - Groups: typical size around 400 km² but ranges from 4 km² to 3019 km²; includes fields describing main rivers and area characteristics.
  - Sections: many attributes including upstream/downstream relationships, river names, polygon area, and outlet coordinates.
  - Catchments: upstream area from every Section outlet with coordinates and area metrics; this is the finest detailed level (and the only layer where polygons may overlap).
- Primary data format: Geodatabase (preserves NULLs). If downloading as Esri Shapefile, NULL values may be converted to zeros or empty strings.

## Data creation and lineage
- Boundaries are digitally derived from CEH's IHDTM (50 m grid resolution); GB coastline uses Ordnance Survey Meridian2; NI boundary/coastline from OS GB Panorama data.
- The current dataset construction followed historical conventions; 2014 updates merged islands into the nearest appropriate Hydrometric Area to achieve full UK surface coverage (examples: Isles of Scilly into HA49, Lundy into HA51, etc.).
- All Hydrometric Area boundaries are topologically correct (no gaps or overlaps); every point in the country is allocated to one Hydrometric Area.
- NI catchments are clipped to the national boundary and may not represent hydrologically complete cross-border catchments.

## Known limitations and quality
- Quality is determined by the underpinning IHDTM (50 m resolution).
- NI has limited river geometry detail in some layers; most non-coastline layers focus on Great Britain.
- Some minor rivers are not captured even in Great Britain.

## Updates and maintenance
- No routine, scheduled updates are planned.
- Updates may occur if errors are detected or if improvements to the underlying rivers or drainage grid data become available.

## Attributes and metadata (high-level)
- Tables summarize key attributes for each layer:
  - Hydrometric Areas with Coastline: identifiers (HA_NUM, HA_ID), names (HA_NAME).
  - Hydrometric Areas without Coastline: similar identifiers and names.
  - Groups: comprehensive fields including area metrics (CCA, G_AREA_KM2), identifiers (G_ID), names, relationships to HA, river and flow information, and classification (G_CAT).
  - Sections: detailed attributes such as cumulative catchment area (CCA), group/area IDs, outlet coordinates (OUTF_X/Y), river names, downstream/upstream identifiers, section ID (S_ID), zone names (S_NAME), and area (S_AREA_KM2).
  - Catchments: outlet and centroid coordinates (EAST/NORTH and CEAST/CNORTH), polygon area (KMSQ), downstream section (S_ID).
- Data steward guidance: use Geodatabase to preserve NULL values; if exporting to Shapefile, be aware of NULL value handling.

## Governance considerations for Data Stewards
- Ensure alignment with IHDTM-derived boundaries for IHUs without Coastline when precise data matching is required.
- Maintain awareness of cross-border NI limitations and clipping behavior in NI catchments.
- Document lineage from IHDTM and OS-derived boundaries to support reproducibility and data provenance.
- Manage and communicate limitations in data coverage (e.g., NI and minor rivers) to users.
- Establish processes for error-driven updates given the non-routine maintenance approach.

## Practical takeaways for use and sharing
- Use the Geodatabase format as the primary data product to preserve NULL values and data integrity.
- When combining layers, respect the hierarchical relationships: Groups -> Sections -> Catchments, and consider Catchments as the most detailed layer with potential overlaps.
- Be mindful of boundary definitions when performing spatial analyses that require exact coastline alignment versus IHDTM alignment.
- For cataloging and discovery, reference hydrometric area numbers (HA_NUM) and group/section identifiers (G_ID, S_ID) as stable keys linked to NRFA codes where relevant.