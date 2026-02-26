GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Provides the mapping field protocol for the Glastir Monitoring and Evaluation (GMEP) project.
  - Uses CS Surveyor extension within ArcMap to capture habitat data across 1 km squares.
  - Aims to produce standardized, auditable habitat maps and attributes to inform policy scrutiny, evaluation, and future decisions.

- System, data structure and outputs
  - Platform and data model
    - ArcMap with CS Surveyor extension; a Countryside Survey data frame holds layers and predefined symbology.
    - Data captured as three feature types: Areas (polygons), Points (≤20x20 m features), and Lines (linear features ≤5 m wide, minimum length 20 m).
    - Each feature can contain multiple components and events; attributes cover habitat type, species, physiography, and other descriptors.
  - Data quality and governance
    - Emphasizes data quality: minimum polygon size (MMU), valid Reason for Change values, Visit Status, and BH accuracy.
    - Encourages use of external datasets (e.g., OS MasterMap) to support edits while maintaining data provenance.
    - Edits require explicit saving (Save Session) and logging off; unsaved work is not retained.

- Core workflows and procedures
  - Mapping polygons (Areas)
    - Split: create new polygons within or around a 1 km square; can be done freehand or by copying polygons from external layers; supports doughnut polygons.
    - Modify: adjust boundaries or shared nodes; edits preserve topology; requires Save Changes to commit.
    - Merge: combine multiple areas when attributes are identical; copied attributes override existing ones.
    - Update: create new areas by merging splits and potentially copying from other layers; useful for including new habitats and for areas below MMU.
    - Attributes: polygon-level attributes (Area, Broad/ Priority Habitat, BH Accuracy, Reason for Change, Visit Status) and component-level attributes; supports detailed habitat typing and provenance.
    - Copy Attributes: apply attributes from a source area to multiple target areas to ensure consistency.
  - Ponds (site-specific inventory)
    - Grid square inventory form records pond count, area, presence, reason for loss, and whether new ponds exist.
    - Overview: one pond per square is surveyed as the “survey pond,” selected randomly from mapped ponds after inventory is complete.
    - Pond data feeds into the Inland Water theme as appropriate attributes (areas or points).
  - Mapping point features (Points)
    - New: add new points (scale ≤ 1:5000); ensure minimum 5 m from other points; each new point starts with an Unsurveyed/Missing Data component.
    - Modify: move points; preserve attribute edits; scale constraint applies.
    - Delete: remove points with valid Reason for Change; otherwise editing required first.
    - Attributes: update point attributes; points may have multiple components; mandatory values highlighted.
    - Copy Attributes: copy attributes from a source point to multiple target points.
  - Mapping linear features (Lines)
    - New: create new lines (minimum 20 m length, ≤ 5 m width); use vertex editing to refine; automatic handling of line intersections.
    - Modify: adjust line shape, including shared nodes; use vertex edit and shared node modify for complex topology.
    - Cut: remove segments via a digitised cut polygon; target length and resulting lines validated.
    - Delete: remove lines with valid Reason for Change on all events; some limitations for historic features.
    - Reshape: reshape following the original or copied line using reshape tools; ensure no invalid intersections.
    - Copy from other layers: use external layer features to inform edits; supports following landscape area boundaries.
    - Event attributes: each line comprises events with attributes; events have length constraints (minimum 5 m) and can be edited, added, copied, or deleted.
    - Copy Attributes: copy events from a source line to one or more target lines; target lines receive a new Unsurveyed feature to be edited.
  - Spatial checks and status
    - Visiting and attribute checks for linear features involve filtering by VISIT_STATUS (unvisited highlighted).
    - All edits are visualized in the map and reflected after refresh.

- Practical considerations for monitoring framework authors
  - Standardization and reproducibility
    - A unified, step-by-step protocol for polygon, point, and line editing ensures consistent data collection across squares and years.
    - Use of copy tools (from OS MasterMap or other layers) accelerates editing while maintaining an auditable trail.
  - Data scope and metrics
    - Outputs include polygon extents, habitat types, Broad/ Priority habitat classifications, and attribute histories (Reason for Change, Visit Status).
    - Pond inventories and survey pond selection provide aquatic habitat metrics and conditions for monitoring.
    - Linear features yield length, events, and condition data suitable for trend analysis.
  - Data quality and governance
    - Explicit validation rules (e.g., BH Accuracy, Reason for Change, Event lengths) support reliable policy evaluation.
    - Clear save and logout procedures reduce data loss; warnings emphasize the need to save during long edits.
  - Handling data gaps and evolution
    - Split/Update workflows accommodate new habitat data and changes over time, enabling monitoring of habitat change while maintaining linkage to existing records.
    - The methodology acknowledges that spatial accuracy is not always the priority; emphasis is on accurate extents and habitat representation for monitoring purposes.

- Support and troubleshooting
  - System support is available via the helpdesk for Surveyor-related queries.
  - Basic troubleshooting includes restoring the Table of Contents or toolbars in ArcMap as needed.

- Key references within the workflow
  - 1. Using the Digital Mapping System: Access, login, and ArcMap/Surveyor integration details.
  - 2. Methodology for Mapping Polygons (Habitat Areas): Split, Copy, Modify, Merge, Update, Attributes, and Copy Attributes.
  - 3. Methodology for Mapping Point Features: New, Modify, Delete, Attributes, Copy Attributes.
  - 4. Methodology for Mapping Linear Features: New, Modify, Cut, Delete, Reshape, Copy Attributes, and event-level workflows.
  - 5. Mapping change in CS squares: guidance for repeating CS squares, including attribute checks and change rationale.
  - 6. Troubleshooting: common interface and tool issues.

- Note
  - For queries or problems with the Surveyor system, contact the helpdesk as recommended in the document.