# Integrated Hydrological Units of the United Kingdom

## Overview
- A multi-level dataset of hydrological units across the United Kingdom, designed to standardise river catchment information for hydrometric data management and environmental monitoring.
- Levels include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- Supports organisation of UK river flow measurements and hydrometric data, with areas and boundaries aligned to drainage and terrain data.

## Layers and definitions
- Hydrometric Areas with Coastline: coarser administrative groupings of river catchments with coastlines used for mapping and data management.
- Hydrometric Areas without Coastline: same entities as above but with boundaries following the Integrated Hydrological Digital Terrain Model (IHDTM) for precise matching to gridded data; better for analysis requiring exact IHDTM alignment, less suited for cartography.
- Groups: medium-scale units (~4–400 km2 typical), comprising one or more Sections; can be combined to form Hydrometric Areas without Coastline.
- Sections: drainage area between two confluences with named watercourses; each Section belongs to one Group and to one Catchment.
- Catchments: finest level of detail, representing the full area upstream from an outlet of every Section; can overlap multiple Sections and Groups.

## Data creation and structure
- Boundaries correspond to catchment outlines derived from CEH's IHDTM using an in-house tool; Great Britain coastline uses the Ordnance Survey Meridian2 coastline; NI boundaries and coastlines derived from OS GB Panorama data.
- In 2014, islands without defined Hydrometric Areas were merged into nearest appropriate areas to achieve full UK coverage (examples include Isles of Scilly merged to HA 49; St Kilda group merged into HA 106, etc.).
- All Hydrometric Areas are topologically correct with no gaps or overlaps; NI catchments are clipped to the national boundary, and some cross-border catchments may be incompletely hydrological.
- Coverage: Hydrometric Areas with Coastline covers Great Britain and Northern Ireland; other layers cover Great Britain only due to data limitations for NI rivers and names.
- Data structure uses a Geodatabase (preferred to preserve NULL values); Esri Shapefile exports convert NULLs to zeros or empty strings.

## Quality, limitations, and coverage
- Data quality depends on the underpinning IHDTM (50 m grid resolution).
- Some minor rivers may not be captured, even within Great Britain.
- Northern Ireland NI catchment completeness is limited by clipping to national boundaries; cross-border hydrology may be partially represented.
- The two coastline-related layers differ in boundary boundaries: the Coastline version is better for mapping aesthetics, while the Without Coastline version aligns precisely with IHDTM.

## History and context
- Hydrometric Areas emerged from the Inland Water Survey Committee in the 1930s to support integrated hydro-meteorological data collection; Northern Ireland designation followed later.
- Numbering: GB hydrometric areas use two-digit codes (1–97 around the coast, with island prefixes like 101–108); NRFA gauging numbers are based on this system with a regional identifier.
- The initial digital boundaries were created in the 1980s; later versions aligned with IHDTM for consistency with CEH and NRFA datasets.
- In 2015, Hydrometric Areas became part of Integrated Hydrological Units of the United Kingdom, extending to multiple spatial resolutions.

## Attributes and data schema
- Datasets are primarily provided as five tables describing the attributes for each layer:
  - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID, etc.
  - Hydrometric Areas without Coastline: HA_NUM, HA_NAME, HA_ID, etc.
  - Groups: fields include area metrics, river names, identifiers (G_ID), and related HA_IDs.
  - Sections: fields include upstream area, river names, coordinates of outlets, S_ID, S_NAME, and cross-references to G_ID and HA_ID.
  - Catchments: fields include outlet coordinates, centroid, area (KMSQ), and downstream section ID (S_ID).
- The Geodatabase format preserves NULL values; shapefile exports may convert NULLs to zeros or empty strings.

## Practical considerations for analysts
- The IHU framework provides a consistent, hierarchical basis for storing and analysing hydrological information across the UK.
- When integrating with other datasets (e.g., NRFA gauges), be mindful of the regional identifiers and the potential NI data limitations.
- For precise data alignment with terrain models, prefer Hydrometric Areas without Coastline; for cartographic outputs, use Hydrometric Areas with Coastline.
- Expect occasional updates only to correct errors or to incorporate improvements to underlying rivers or drainage data; routine updates are not planned.