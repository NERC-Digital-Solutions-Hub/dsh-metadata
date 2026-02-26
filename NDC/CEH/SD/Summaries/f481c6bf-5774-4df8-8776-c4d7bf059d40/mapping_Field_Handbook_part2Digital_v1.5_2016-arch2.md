# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field protocol for the Glastir Monitoring and Evaluation Programme (GMEP) mapping using the Surveyor software within ArcMap.
  - Supports consistent, standards-based recording of habitats (areas), points, lines (linear features), and ponds for environmental monitoring over time.
  - Emphasises data verification, quality assurance, transformation, and storage for later scrutiny and policy performance assessment.

- System overview
  - Surveyor is an ArcMap extension customized for GMEP, built on a CS/ESRI foundation; it simplifies data capture without requiring full ArcMap expertise.
  - Users log in with designated accounts; data are loaded into a Countryside Survey data frame with predefined layer symbology.
  - Workflows require editing at scales of 1:5000 or smaller; all edits are saved within the CS Surveyor session.

- Mapping polygons (Areas)
  - 2.1 Split: create new polygons from a single 1 km square polygon; options include freehand split or copying polygons from external layers (e.g., OS MasterMap); can produce doughnut shapes for holes.
  - 2.1.1 Copy polygons from existing layers: use Copy Features to bring in polygon shapes and refine with the edit sketch.
  - 2.2 Modify: adjust polygon boundaries or shared nodes; uses topology-aware editing; saves changes with updated attributes.
  - 2.3 Merge: combine multiple areas when attributes match; copied attributes overwrite existing area and component attributes.
  - 2.4 Update: creates new polygons by splitting and merging existing ones; useful for unsurveyed squares and for copying areas from other layers.
  - 2.5 Attributes: manage polygon-level and component-level attributes, including Broad/Priority Habitat (BH), habitat specifics, species, and physiography.
    - Polygon-level: area, BH, BH accuracy (Not previously surveyed for new squares), reason for change, visit status.
    - Component-level: multiple components per area; attributes edited via the Landscape Areas Editor; components can be added, copied, or deleted.
  - 2.6 Copy Attributes: copy attributes from a source area to target areas, overwriting existing attributes.
  - 2.7 Mapping change in CS squares: for repeating CS squares, review and confirm attributes against previous surveys; record changes with reasons (e.g., error change, new baseline, not previously surveyed).

- Ponds (Grid square inventory for ponds)
  - Form-based recording for every pond in a square; captures reference numbers, area, presence/absence, reasons for loss, new/existing pond status, and age/reason for creation.
  - Determines the survey pond for condition assessment via a random selection process after inventory completion.
  - The selected “survey pond” is recorded as Pond sampled in the appropriate area or point tab.

- Mapping point features
  - Defined as features under 20x20 m; recorded across themes with optional movement when necessary.
  - 5.1 New: add points at scale 1:5000 or smaller; points require attributes and cannot be placed within 5 m of another point.
  - 5.2 Modify: move points; retain attributes; can move one point at a time.
  - 5.3 Delete: remove points with valid Reason for Change; otherwise edit attributes first.
  - 5.4 Attributes: update attributes for the selected point; components can be added, copied, or deleted.
  - 5.5 Copy Attributes: copy attributes from a source point to one or more target points.
  - Points editing is restricted to 1:5000 or smaller and requires at least one component per point.

- Mapping linear features
  - Defined as lines <5 m wide but longer than 20 m; capture length, boundaries, and events (e.g., fences, walls, woody features) along the line.
  - Lines can represent multiple events along a single continuous feature; events may change along the length.
  - 6.1 New: create new lines (minimum 5 m length, cannot cross outside square, one line at a time); vertices editable.
  - 6.2 Modify: edit line shape and vertices; shared nodes edited via Shared Node Modify; must avoid creating invalid intersections.
  - 6.3 Cut: cut a line at a digitised polygon; length cut vs remaining length shown; multiple cuts allowed.
  - 6.4 Delete: delete lines with valid Reasons for Change on all events; historic features may require alternative handling.
  - 6.5 Reshape: reshape lines by drawing a reshape graphic; two modes: follow existing line or copied boundary; requires valid intersections.
  - 6.6 Checking visit status: use Select By Attributes to identify unvisited linear features; edit events as needed.
  - 6.7 Attributes: line-level attributes and per-event attributes; events have mandatory fields; editing is done one line at a time.
  - 6.8 Copy Attributes: copy events from a source line to target lines; overwrites target line attributes and events.
  - Editing is scale-sensitive (1:5000 or less) and restricted to single edits at a time.

- Session management and data handling
  - Before exiting an edit session, save changes via Save Session; End Session discards edits.
  - CS Surveyor stores changes and returns to the main ArcMap screen; log off from CS Surveyor DB when finished.
  - Important: regular saving is required to avoid data loss; after edits, end session and then log off.
  - Pond and CS square forms guide subsequent freshwater and habitat condition surveys.

- Troubleshooting and tips
  - If toolbars or table of contents are lost, re-enable via Windows customization options.
  - Ensure scale remains at or below 1:5000 for editing points, lines, and attributes.
  - Use Copy features from external layers to improve speed and accuracy; check topology to avoid invalid edits.

- Supported outputs and governance
  - Outputs include structured datasets (areas, points, lines, ponds) with standardized attributes and themes.
  - Datasets are intended to be stored and uploaded to appropriate portals, enabling consistent monitoring of environmental health and policy performance over time.
  - The document emphasizes standardized methods, data verification, and the ability for others to access underlying data used to produce outputs.