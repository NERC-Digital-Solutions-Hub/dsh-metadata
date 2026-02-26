# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Detailed methodology and data model for digital field mapping of habitats and landscape features in CS2007.
  - Aims to map Broad Habitats (BH) and Priority Habitats (PH), describe vegetation attributes, and support time-series policy monitoring.
  - Prioritises recording habitat extent and change over precise spatial accuracy; introduces a unified digital map integrating previous themes (forestry, agriculture/natural vegetation, boundaries, structures, physiography).

- Data model and classification
  - BH: 19 broadhabitats plus a Mosaic category; PH nested within BH framework; GIS masks used post-survey for reporting extents.
  - Mosaic: used when habitats can’t be delimited cleanly at polygon level; components described with percentage shares summing to 100%.
  - Vegetation and woodland keys: Vegetation Key assigns primary (and some secondary) attributes to polygons to allocate BH/PH; Woodland Keys classify canopy structure (belts, clumps, lines, woodland/forest units) to aid BH/PH assignment and mosaic handling.
  - Woodland attributes: canopy cover, principal woodland type, species, and ancillary attributes (e.g., DBH, regeneration) at polygon and component levels.

- Digital mapping system and data capture
  - CS Surveyor: a customized ArcMap extension used to capture/edit habitat data for each 1 km square.
  - Data model: layers for Areas (polygons), Lines (linear features), and Points (point features); components and attributes organized by themes.
  - Minimum mapping unit (MMU): 1/25 ha (400 m2); smaller areas generally not mapped unless new habitat occurs or is part of a larger polygon.
  - Change recording: mandatory recording of genuine ecological change since 1998 CS and corrections; real changes vs error changes clearly defined.

- Editing areas, components, and attributes
  - Area editing: adjust boundaries, copy attributes, split/merge areas; explicit reason-for-change logging required.
  - Component attributes: multiple components per area; thematic grouping (physiography, agriculture/natural vegetation, forestry, etc.).
  - Tools and workflows:
    - Copy Area, Split Areas, Merge Areas, Modify Area, Update Areas.
    - Stop editing steps to ensure data integrity.
  - Change logic emphasis: real change, error change, and new baseline allocations (e.g., new PH/BH classifications).

- Recording and managing habitats and attributes
  - Areas: BH/PH assignments via vegetation key; accuracy codes indicate attribute correctness; visit status indicators (In progress, Completed, Refused access).
  - Components: primary attributes (belt/clump of trees, woodland, scrub patches, etc.) with secondary attributes (species, cover, DBH, etc.); thematic groupings across physiography, water, coast, agriculture/vegetation, forestry, recreation, transport, structures.
  - Boundary and linear features: recorded as lines with events (fences, hedges, woody lines); wide linear features used when width warrants; events can be subdivided along lines.
  - Points and woody linear features (WLFs): individual trees, scrub, veteran trees; density, species, DBH, buffers, provenance; WLFs include historic management and margin details; decisions on natural vs. man-made shapes or hedge-like forms.
  - Pond mapping and inland water: map all ponds within a square; select a single survey pond for detailed assessment via randomized criteria; pond attributes captured on a dedicated CS2007 Pond Mapping Recording Sheet; process accommodates temporary ponds and distinctions from ditches/streams/bogs.
  - Monitoring and outputs: outputs structured for country- and UK-level reporting by BH/PH; time-series enable monitoring and policy analyses; GIS masks support post-survey extent estimation.

- Practical guidance and cautions
  - Complex upland unenclosed BHs require nuanced vegetation interpretation; vegetation keys assist PH allocations.
  - Non-native species monitored as an additional data layer for habitat descriptions.
  - Orchards treated specially to distinguish historical/intense management from broader arable/natural vegetation contexts.
  - Spatial accuracy is secondary to accurate representation of habitat extent and change; MMU and mosaic approaches help maintain data consistency.

- Quick reference to key processes
  - Use vegetation key to determine BH/PH from canopy and species composition; use woodland key for canopy structure and woodland BH/PH attribution.
  - Edit areas with splitting/merging/copying while maintaining a clear reason-for-change log.
  - Edit linear features with Create, Modify, Cut, Copy, Delete, and Reshape operations; manage shared nodes and topology constraints; edits require scale 1:5000 or less for spatial changes.
  - Record ponds comprehensively and select a survey pond via randomized process; maintain dedicated pond recording sheet with essential attributes.

- Data usage, reporting, and support
  - Outputs enable country- and UK-level habitat reporting; time-series data support monitoring and policy analysis.
  - CS Surveyor helpdesk available; bug reporting via Wiki; latest methodologies communicated through Latest News.
  - Historical references: CS1990 and CS2000 mapping themes and forms; transition to CS2007 data model and codes.

- Contact and governance
  - Field mapping methodology supported by a helpdesk; updates published as methodology evolves.
  - Countryside Survey coordinated by CEH with support from Defra and other partners; data usage governed by NERC Defra partnership.