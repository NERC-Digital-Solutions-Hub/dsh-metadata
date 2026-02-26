# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Aim and scope
- Provides methodology for nationwide field mapping of habitats and landscape features (CS2007).
- Focuses on reporting change in Broad Habitats (BH) and Priority Habitats (PH); covers data capture, classification, GIS-enabled editing.
- Introduces the CS Surveyor system for field data capture, editing, and change logging; emphasizes extent and change over precise spatial accuracy.

## Data model and structure
- Three core feature types:
  - Areas (polygons) for habitats and features
  - Lines (linear features)
  - Points (specific landscape elements)
- The data model is organized by themes (e.g., Inland Physiography, Inland Water, Coastal features, Forestry, Agriculture/Natural Vegetation, Structures, Recreation, Transport).
- Attributes are structured around BH/PH at the polygon level and component-level attributes under thematic groups (e.g., Physiography, Vegetation, Species, DBH); woodland has primary, secondary attributes, and modifiers.

## Keys, habitat allocation, and mosaics
- Habitat allocation uses keys (Vegetation Key, Woodland Types/Features) to assign BH/PH and related attributes based on canopy, composition, and species indicators.
- Nested PHs within BHs allowed to record new baselines; mosaics are managed with component-level percent cover to total 100%.

## The CS Surveyor digital mapping system
- A customised ArcMap-based system for CS2007 data capture; surveyors log in, load map squares, and access fixed data layers.
- Data capture prioritises extent and change over precise spatial accuracy.
- Features are editable within a single edit session; changes are saved via “Save Session” and must end the session to commit.
- Change recording is mandatory for all habitat/feature edits (REAL changes vs. ERROR corrections).
- Support channels are provided (helpdesk, Wiki, Latest News).

## Editing workflow and rules (Areas, Lines, Points)
- Areas (Polygons)
  - Edit BH/PH and habitat attributes; determine Change type (REAL, ERROR, new PH baseline).
  - Component-level editing (add/copy/delete components); components must share attributes to modify primary attribute.
  - Boundary edits with topology tools; ability to copy attributes between areas; merge/split/update areas.
  - Rules: continuous woodland within a polygon maps to BH/PH as woodland; MMU observed; new habitat changes require new polygons; updated areas require Change-forced fields (Reason for Change, BH accuracy).
- Points
  - Edited via Points tab; add/copy/delete components; one-at-a-time creation; editing scale <= 1:5000.
  - Veteran trees and buffer zones recorded as optional attributes.
- Lines (Linear features)
  - Edit events along lines; create, copy, delete, cut, reshape; minimal line length and topology checks apply.
  - Edits include creating new lines, splitting, merging, and modifying event attributes; margins and related features recorded as part of line events.
  - Lines typically > five metres wide and longer than 20 m; scale limits apply (1:5000 or less for certain edits).
  - Shared nodes and topology must stay consistent; special handling for shared boundary vertices.

## Pond mapping and methodology
- Each square with ponds is mapped; all ponds recorded on a Pond Mapping Recording Sheet.
- One pond per square is sampled for a detailed condition survey (survey pond), chosen randomly or preselected if possible.
- Attributes include polygon ID, area, water presence, reason for loss/creation, and notes.
- Detailed pond condition surveys occur only after all ponds in the square are mapped.
- Boundary and classification use winter water level and vegetation/water-edge cues; temporary ponds (dry at survey) may be recorded if they met historical four-month water-holding criteria.
- Distinctions made between ponds and ditches/flushes/dammed streams using connectivity and basins.

## Habitat types and woodland specifics
- Broad Habitats (high-level examples include BH1–BH22, and mosaic) with non-specific primary attributes applicable across BH/PH (e.g., bare ground, scattered trees, drainage signs).
- Woodland types/features include Belt of trees, Clump of trees, Wood/Forest, Scattered trees, Patch of scrub, etc.
- Primary attributes for woodland components cover canopy conditions, species composition, DBH categories, and modifiers (parkland, underplanting, fencing, etc.).
- Vegetation data captured as percentages (cover thresholds).
- Veteran trees: up to 10 per square, max 2 per species, with buffer zones, DBH, and condition details; girth guidelines included (Appendix 5).

## Non-native/invasive species and orchard mapping
- Non-native/invasive species recorded where present (examples provided in guidance).
- Orchards receive a dedicated Orchard attribute within Agricultural Crops, with orchard-specific notes.

## Coastal and mosaic guidance
- Machair and coastal complexes treated with component-based mapping; mosaics detail per-component percent cover.

## Key takeaways for data support and usage
- CS2007 provides a detailed, GIS-based framework for capturing habitat extent, type, and change across large areas with explicit rules for splitting/merging polygons, change logging, and handling complex woodland/linear features.
- Data quality focuses on correct habitat classification and change detection to enable robust time-series habitat extent analyses.
- The system supports end-user data products (dashboards, reports) via standardized attribute schemas, structured keys, and explicit data quality rules to enable reuse and cross-square comparability across survey cycles.

## Legacy data and CS2000 context
- CS2000 featured themes with unique parcel-based numbering and separate data recording forms; some attributes align with CS2007 but use different coding and forms.
- Overview of how CS2000 data were organized and how transitions to the 2007 framework are managed (e.g., codesheets, plot maps, and FABs).

## Appendices and supplementary guidance
- Appendix 1–3: Tools, forms, and mapping sheets for CS2007 components (ponds, lines, events) and CS2000 context.
- Appendix 5: Girth sizes for veteran trees with threshold-based classifications (e.g., potentially interesting, valuable, truly ancient by species).
- Appendix 6: Squares with loops and related data management notes.

## Data rights, disclaimer, and contacts
- Copyright held by Natural Environment Research Council (NERC); reproduction allowed for research and internal use with attribution.
- Disclaimer of liability for decisions based on the report.
- Contact information for Countryside Survey project office and reference to the Countryside Survey 2007 program.