# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Guidelines for digital field mapping and reporting for Countryside Survey 2007 (CS2007).
  - Aims to report land-cover change and map Broad Habitats (BH) and Priority Habitats (PH) within a single digital GIS model.
  - Data captured as Areas (polygons), Lines (linear features), and Points (point features) with consistent attributes.

- Data model and mapping units
  - Mapping units: Areas (polygons), Lines, Points.
  - Minimum mapping unit (MMU) of 1/25 hectare; minimum polygon ~20 m x 20 m; smaller elements generally not mapped unless part of a boundary change.
  - Mosaic mapping allowed where boundaries are indistinct; single digital model integrates forestry, agriculture/natural vegetation, boundaries, structures, and physiography.

- Themes, attributes and classifications
  - Thematic grouping of attributes (Inland Physiography, Inland Water, Coast, Agriculture/Natural Vegetation, Forestry, Structures, Recreation, Transport, etc.).
  - Primary vs secondary attributes; species, cover classes, and qualifiers for habitat classification.
  - Vegetation Key assigns polygons to BH and PH based on composition and habitat traits.
  - Recording rules include capturing at least two species per habitat polygon (up to four) and clearly separating BH vs PH attributes where applicable.

- Digital mapping system and workflows
  - CS Surveyor extension for ArcMap: centralized data frame, predefined layers/symbols, live database connection, and in-session editing of Areas, Lines, and Points.
  - Editing capabilities across geometry and attributes:
    - Areas: copy, split, merge, boundary modification, component attributes.
    - Lines: event management along linear features (fences, walls, woody lines); handling of shared nodes.
    - Points: creation, modification, deletion with validation.
  - Change management: mandatory change-status logging (REAL change, ERROR, NO CHANGE); baselines from 1990 and 1998 guide decisions.
  - Quality and workflow controls: mandatory fields, regular saves, proper log-off procedures; emphasis on accurate habitat extent and change depiction.

- Pond mapping and condition surveys
  - CS2007 Pond Mapping: identify and record ponds within each square; one survey pond per square undergoes detailed condition assessment.
  - Preselection and reselection rules for survey ponds; boundary definitions for ponds, including temporary ponds and ditches.

- Woody features, point features and line features
  - Points: trees and shrubs (including veterans); buffers and curtilage considerations.
  - Woody Linear Features (WLFs): hedges, lines of trees, belts, scrubs; characterized by form (natural vs managed) and DBH data.
  - Attributes for woody features include canopy proportions, species composition, veteran status (up to two per species per square), and related management signs (e.g., cutting, laying, coppicing).

- Methodology for mapping and editing
  - Topological editing with consistent attributes; maintain BH/PH assignments and change status.
  - Area operations: split/merge/allocate new polygons; manage shared boundaries and component attributes.
  - Update mechanisms: create new polygons from edits or external boundary data; ensure minimum feature length and avoid invalid intersections.
  - Data integrity: edits must have justifications; erroneous edits can be flagged and corrected.

- Outputs and reporting
  - Outputs organized by BH/PH with polygon- and component-level details across themes.
  - Example habitat classes include Broadleaved Woodland, Coniferous Woodland, Boundaries/Linear Features, Arable and Horticulture, Grasslands, and various BH/PH components.
  - Pond data contribute to inland water and fen/marsh/swamp analyses; special habitats (e.g., Machair, Montane) mapped with detailed data where applicable.

- Data quality, access and support
  - Field data collection is iterative; support channels and a wiki-based fault logging system are provided.
  - Methodology updates published in Latest News; surveyors encouraged to stay current.
  - Emphasis on cross-dataset data integration, standardized attribute schemas, and thorough documentation for reproducibility.

- Challenges and considerations for data support
  - Time spent “understanding the ask” and choosing the best data approach.
  - Handling patchy or multi-format data and integrating legacy data (CS1990/CS2000) with CS2007 datasets.
  - Communicating complex habitat classifications in accessible outputs for end users and stakeholders.
  - Promoting data sharing, reuse, and iterative feedback to refine dashboards, reports, and maps, and to influence data creation practices.

- Appendices and supplementary material (high-level)
  - CS2000 and CS1990 mapping themes and coding schemes; data recording forms and codesheets.
  - CS2007 Pond Mapping Recording Sheet and process for selecting survey ponds.
  - Appendix on veteran trees, including girth-based assessment guidelines and species-specific rules.
  - Appendix listing squares with loops and data integrity considerations.

- Data provenance and rights
  - Copyright and licensing information; guidance for reuse and attribution.
  - Contact and further information: Countryside Survey project office and CEH, with Defra/NERC partnership context.