# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Purpose and scope
- Provides the mapping field protocol for GMEP using the CS Surveyor extension within ArcMap.
- Aims to standardise data collection of habitat areas, point features, and linear features for environmental monitoring and policy evaluation.
- Emphasises verifying and transforming data from established sources, applying standardised methods, and storing datasets in appropriate portals.

## System setup and access
- Surveyor is a customised ArcMap extension developed for CEH/CS2007 and tailored to GMEP.
- Start ArcMap, open Habitats task manager, and launch Surveyor. Log on to the CS Surveyor extension.
- Data frame: Countryside Survey; layers are pre-symbologyed for visibility and usability.
- Helpdesk should be contacted for queries or issues with Surveyor.

## Navigation and basic concepts
- ArcMap interface consists of the Table of Contents (layers) and the Map Display.
- Surveyor adds a dedicated menu to access main functions.
- GPS can be used as an ancillary context, but multiple data sources (aerials, Master Map, OS data) should inform mapping.
- Tools include standard ArcMap navigation (zoom, pan, go to extent, identify, find, measure) and Surveyor-specific editing tools.
- Editing requires scale checks (generally 1:5000 or finer for edits) and attention to data integrity (e.g., shared nodes).

## 1) Using the Digital Mapping System (Surveyor)
- Access via Habitats task manager; log on to CS Surveyor extension.
- A data frame (Countryside Survey) holds layers with pre-set visibility.
- The extension enables viewing and editing of point features, linear features, and polygon features within the chosen 1km square.

## 2) Methodology for Mapping Polygons (Habitat Areas)
- Start with creating polygons for a 1km square (simple split) or copying polygons from external datasets (e.g., OS MasterMap).
- Edit tools are in the Landscape Feature Editing toolbox with three tabs for Areas, Lines, and Points.
- Split: create new polygons by digitising or copying existing polygons; validate against minimum mapping unit (MMU). Split can produce doughnut polygons.
- Modify: adjust boundaries, including shared nodes; changes saved per edit.
- Merge: combine multiple polygons when attributes are identical; copied attributes overwrite existing ones.
- Update: creates new areas by splitting/merging; can incorporate polygons from other layers; useful for unsurveyed squares and when many intersections occur.
- Attributes (polygon and component levels):
  - Polygon level: Area, Broad/Priority Habitat (BH), BH Accuracy (Not previously surveyed for new squares), Reason for change, Visit status (In progress, Completed, Refused access).
  - Component level: multiple components per area; add/copy/delete components; update attributes; ensure at least one component per area.
  - Thematic attribute groups (e.g., AGRICULTURAL CROPS, FORESTRY, INLAND WATER, etc.) guide selection of Primary attribute, qualifiers, vegetation type, species, and coverage.
- Copy Attributes: copy attributes from a source area to target areas; can have one source and multiple targets; overwrites target attributes.
- Mapping changes in CS squares: for repeating CS squares, use prior data to confirm or adjust polygons and attributes; focus on polygon-level attributes; provide reasons for any changes.

## 3) Pond Attributes in Grid Square Inventory
- If ponds exist in a square, complete the Grid square inventory for ponds form (PC tablet) for each pond.
- Required pond attributes include square and pond references, area, presence, and reasons for loss if marked absent, new pond status, age, and creation reasons.
- Identify a single survey pond per square using the inventory form and a lookup table; record the Pond sampled attribute under Inland Water themes (Areas or Points).
- When all ponds are mapped, the survey pond is selected and passed to freshwater surveyors for condition assessment.

## 4) Methodology for Mapping Point Features
- Points are landscape elements under 20x20 m; examples include trees, standing water bodies, ponds.
- Access the Points tab in Landscape Feature Editing toolbox.
- New: create a new point at a mapped location; ensure scale is 1:5000 or less; points cannot be closer than 5 m to existing points; each new point starts with an Unsurveyed/Missing Data component.
- Modify: move existing points; maintain attributes; when completed, visit status should be set to Completed for visual updates.
- Delete: remove points with a valid Reason for Change; scale must be 1:5000 or less; only one point at a time.
- Attributes: edit point attributes and components; points can have multiple components; create, copy, or delete components.
- Copy Attributes: copy attributes from a source point to multiple target points; overwrites attributes in targets; only one source point allowed.

## 5) Methodology for Mapping Linear Features
- Linear features are lines under 5 m wide, length generally at least 20 m, with possible gaps up to 20 m.
- All relevant linear features (fences, walls, woody features, hedges, etc.) are recorded as continuous lines with events.
- If a linear feature becomes a polygon (area > MMU), use the boundary/linear features approach (wide linear feature).
- Events: describe different segments along a line; events can be additive (multiple features along a single line) or replacements.
- Recording: create new lines, cut lines, delete lines, modify shapes, reshape to follow other features, and edit event attributes along lines.
- New: lines must be created within a square, minimum 5 m length, no self-crossing; intersections split lines automatically; each new line starts with a single Unsurveyed/Missing Data event.
- Modify: adjust line geometry; handle shared nodes via Shared Node Modify; avoid edits that create invalid topologies.
- Cut: digitise cut polygons along a line; the cut length and remaining length are shown for validation; supports copying polygons from other layers as edit sketches.
- Delete: remove lines with valid Reason for Change on all events; some themes (Historic Features) may have no reason for change fields.
- Reshape: adjust lines by drawing a reshape graph; must intersect the line at start/end; ensure resulting line meets minimum length.
- Copy from other layers: use Copy features tool to import reference polygons from OS MasterMap or other layers into edit sketches.
- Checking visit status for lines: use the Select By Attributes tool to identify unvisited lines (VISIT_STATUS), then edit line or event attributes accordingly.
- Copy Attributes: copy events from a source line to target lines, overwriting target line attributes; only one source line, multiple targets.

## 6) Troubleshooting and best practices
- Save progress frequently: End or Save Session to ensure all edits persist; unsaved edits are lost if not saved.
- If tools or toolbars disappear: use Windows customization options to restore Table of Contents or standard toolbars.
- Ensure scale remains appropriate for edits (commonly 1:5000 or finer for edits; points/lines often require 1:5000 or less).

## Key practices for Analysts Monitoring the Environment
- Use standardised workflows to ensure consistent outputs across time.
- Verify and quality-assure data before transformation into outputs (maps, reports, datasets).
- Ensure data lineage by storing and uploading datasets to appropriate portals.
- Focus on expanding the utility of datasets by integrating with other data where possible and enabling access to underlying data.