# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and Aim
- Describes the CS2007 Field Mapping Handbook for Countryside Survey 2007 (CS2007) led by CEH/NERC.
- Goal: produce a national, digitally captured map of habitats and landscape features to report change, extend coverage (including Wales), and support monitoring of Broad Habitats (BH) and Priority Habitats (PH).
- Focus: mapping land cover change, reporting BH/PH, capturing detail in unenclosed uplands, and integrating five earlier themes into a single digital map.

## Data Model and Classifications
- Two main habitat classifications: Broad Habitats (BH1–BH23, plus rivers/streams, arable, woodlands, etc.) and Priority Habitats (PH) nested within BHs where applicable.
- Allocation keys:
  - Vegetation Key: assigns polygons to BH/PH based on vegetation composition and habitat indicators.
  - Woodland key: classifies woody vegetation and supports PH/BH attribution.
- Habitat mapping distinctions:
  - Enclosed (lowland) vs unenclosed (upland) habitats; unenclosed uplands mapped with more detail; enclosed BHs editable from 1998 mapping where available.
- Two-level approach:
  - Polygon-level BH/PH allocation and component-level attributes (physiography, vegetation, species, density).
  - Mosaic option when boundaries are indistinct or patches are below the minimum mapping unit (MMU).

## Data Collection, Tools and Workflow
- Digital system: CS Surveyor (ArcMap extension) for editing polygons, lines, and points; built on ESRI platform; includes a helpdesk.
- MMU: minimum mappable unit of 1/25 hectare (400 m2); polygons below are generally not mapped unless needed for a new habitat occurrence.
- Habitats and attributes:
  - For each habitat polygon: record primary and secondary attributes, species counts (2–4), and percent cover categories (<10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).
- Change and validation:
  - REAL change vs corrections of past mapping errors (ERROR).
  - Spatial accuracy is not the primary concern; emphasis is on habitat extent and change.
- Editing tools and processes:
  - Landscape Feature Editing toolbox: Edit (Areas), Copy Attributes, Split Areas, Merge Areas, Modify Area, Update Areas, etc.
  - Component-level editing: add/copy/delete components; edit primary/secondary attributes.
  - Copy tools for attributes between areas, lines, or points.
  - Split/merge workflows for boundary changes (including doughnut polygons) and updating intersected areas.
- Data integrity and sessions:
  - End sessions with Save Session to persist edits; End Session discards changes.
  - Log off CS Surveyor DB when finished.
- Ponds and waters:
  - Every square maps ponds with a CS2007 Pond Mapping Recording Sheet; one survey pond per square selected for detailed assessment.
  - Ponds tracked with detailed attributes; selection can be preselected or random; seasonal changes accounted for in boundaries.

## Ponds, Wetlands and Water Features
- Pond boundaries defined by the winter waterline or water-edge indicators; temporary ponds noted when currently dry.
- Distinctions among water features:
  - Ditches, dammed streams, flushes; canals/river segments mapped as areas.
  - Water features recorded under Inland Water; ponds have dedicated fields and are key targets.

## Woodland, Vegetation and Species Data
- Woodland types: BH1 Broadleaved Woodland and BH2 Coniferous Woodland.
- Sub-attributes: modal DBH, species composition, canopy cover.
- Components vs polygon-level BH: components include belts, clumps, scattered trees, scrub patches, parkland, orchards.
- Non-native/invasive species noted; orchard guidance via Orchard attribute under Agriculture/Natural Vegetation Use; cautions around curtilage trees.
- Key woodland attributes include canopy cover, dominant species, presence of belts/lines, and management signs (fencing, grazing, windthrow, regeneration).
- Buffer zones: record presence/absence around linked features.

## Data Governance, Access and Use for Data Leaders
- CS2007 dataset represents a major nationwide data asset for habitat extent and change monitoring.
- Data leadership considerations:
  - Coordinate cross-network data sharing and co-ownership of data products with partners and policy colleagues.
  - Govern metadata, data quality, versioning, and updates across themes (habitat mapping, woodland features, ponds, streams, urban features, etc.).
  - Ensure alignment with UK Biodiversity Action Plans through consistent BH/PH reporting.
  - Manage access barriers (paywalls, data protection) and identify data gaps to prioritise workstreams.
- Collaboration and learning:
  - Engage with wider data communities and practitioners to strengthen sector data standards and best practices.
  - Use field-user feedback loops to iteratively improve data products and mapping practices.

## Particular Challenges and Implications for Data Leaders
- Understanding user needs across diverse policy and public audiences; enabling co-ownership of data products.
- Achieving an overview of scattered data sources and identifying data gaps at required granularity.
- Access barriers (paywalls, data protection) and the need for clear metadata and standards.
- Rapid data verification in the field; managing inconsistent data quality and metadata.
- Sector coordination to avoid duplication; fostering communities of practice.
- Handling upland unenclosed habitats and post-survey GIS masking for PHs and BHs, including mosaic approaches and post-survey PH allocations.

## Quick Takeaways for Data Leaders
- CS2007 delivers a digital, national habitat map with robust BH/PH allocation, change detection, and time-series analysis.
- Data model integrates polygons (areas), lines (events), and points (features) with MMU rules and comprehensive attribute schemas.
- CS Surveyor enables controlled, auditable editing and structured pond mapping on a unified platform.
- Governance, metadata, and cross-network collaboration are central to turning field mapping into a reusable, policy-supporting data asset.

## Context and Legacy
- Reference to CS2000 and CS1990 themes and mapping approaches, illustrating evolution from multi-theme paper maps with unique parcel numbers to a unified, digital framework.