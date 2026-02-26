# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides methodology for Countryside Survey 2007 (CS2007), focusing on field mapping of Broad Habitats (BH) and Priority Habitats (PH) at country and UK levels.
- Introduces a digital data model and GIS-enabled workflow to record habitats, landscape features, and changes across 1 km squares, including new squares in Wales.
- Emphasises mapping change against earlier surveys (CS1990/CS2000) and validation against prior vegetation data.
- Aims to enable biodiversity monitoring and policy-oriented reporting aligned with national action plans.

## Data model
- Spatial structure across 1 km squares using three feature types:
  - Areas (polygons) for BH/PH and other habitat units.
  - Lines (linear features) for boundaries and linear features.
  - Points for trees, ponds, and other discrete elements.
- Minimum mapping units (MMU):
  - Most vegetation polygons: 400 m2 (with some exceptions).
  - Lines have width/length constraints; ponds mapped with specific rules.
  - Mosaic option allows multiple habitat components within a polygon summing to 100%.
- Classification tools:
  - Vegetation Key for BH/PH attribution based on plant composition.
  - Woodland keys classify woody vegetation into belts, clumps, woodland/forest, and woody linear features; used at polygon level; component woodland attributes stored under Forestry theme.
- Data components and themes are recorded under a Landscape Feature Editing toolbox; areas can contain multiple components.

## Data collection system and workflow
- CS Surveyor: ArcMap extension for digital capture, editing, and management of survey data.
- Workflow essentials:
  - Sign in, select square, apply pre-set symbology, and edit Areas, Lines, and Points within a session.
  - Spatial accuracy prioritises habitat extent/change over precise geolocation.
- Editing operations:
  - Areas: set BH/PH, accuracy, change reason; verify against previous data; manage components; perform splits/merges; create new baselines if needed.
  - Points: represent trees, ponds, etc.; multiple components possible; scale for editing ≤ 1:5000; minimum one component per point; include buffer zones.
  - Lines: long linear features composed of events (e.g., fence, hedge); edit length, add/copy/delete events; manage multiple events; ensure minimum event lengths; use shared nodes for topology; copied lines can anchor edits; lines must not self-cross.
- Topology and governance:
  - Mosaic and multi-component areas require consistent component-level BH/PH attribution with mosaic summaries.
  - Edits are constrained to maintain consistent topology; certain edits require shared node modification.
  - Lines and events must maintain a minimum length; edits that would create invalid intersections or very short features are disallowed.

## Pond mapping
- Every pond in a square must be identified; a Pond Mapping Recording Sheet tracks all ponds and statuses.
- A survey pond per square undergoes detailed plant, environmental, and water chemistry sampling.
- Pre-selected ponds may be used if valid; otherwise, random selection may be used when multiple ponds exist.
- Pond attributes capture area, presence of water, reasons for pond loss/creation, drivers, and notes; condition sampling occurs after mapping.
- Annexes and forms provide the structure for pond data collection and status tracking.

## Special themes and data fields
- Non-native species: records flag habitat quality and management needs.
- Orchard guidance: traditional orchards treated as PH or as orchard attributes within other habitat classes.
- Margins and buffers: record habitat margins (e.g., hedges) and buffer zones around features to reflect cross-compliance.
- Veteran trees: up to 10 per square; detailed attributes collected (DBH, health, epiphytic species, ivy, canopy, deadwood, etc.).
- Additional thematic data fields cover broader habitat context, management indicators, and use classifications.

## Data quality, change and governance
- Distinguishes REAL ecological change from corrections to past data (REAL vs ERROR changes).
- GIS masks are applied post-survey to delineate PH native ranges (upland vs lowland) for reporting extents; potential reassignment after masking.
- Mosaic and multi-component areas require consistent, complete composition (sum to 100%) and coherent component-level classifications.
- Data access and governance support, including versioning and traceability of changes.

## Outputs and end-user guidance
- Outputs are designed for end users to self-serve, explore habitat change and distribution across BH/PH and related features.
- Supports biodiversity monitoring and policy-oriented reporting, including alignment with UK Biodiversity Action Plans.

## Data access, support and training
- CS Surveyor includes helpdesk support, Wiki-based fault logging, and regular methodology updates (Latest News).
- Emphasis on focusing on habitat extent and change rather than precise spatial accuracy; spatial accuracy can be adjusted via attribute changes if necessary.

## Operational notes and legacy data
- Edge cases and practical rules cover mosaics, rough boundaries, hedges vs belts, and updating/validating data through ArcMap and CS Surveyor.
- Legacy datasets (CS1990/CS2000) provide context for integration; Appendix materials outline coding schemes and historical data handling (including transposition of attributes, codesheets, and cross-referencing parcel identifiers).
- Some data are flagged as loops or corrupted (notably certain linear event data); explicit procedures exist to delete, correct, and reinstate such features to maintain data integrity.
- The document includes extensive appendices with example codes, pond forms, and historical mapping frameworks to aid data compatibility and continuity.