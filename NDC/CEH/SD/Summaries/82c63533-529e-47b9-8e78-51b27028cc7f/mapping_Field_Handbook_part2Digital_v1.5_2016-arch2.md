# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose: Provides the field protocol for mapping habitat areas, ponds, and other landscape features in the Glastir Monitoring and Evaluation Programme (GMEP) using the CS Surveyor tool within ArcMap; focuses on standardised data capture, verification, editing workflows, and attribute management to support consistent environmental monitoring over time.

## System and data environment

- CS Surveyor is an ArcMap extension customized for GMEP; built on a Forestry Commission/ESRI heritage, with ongoing updates.
- Login and data: Use ArcMap to open Surveyor, log in (Main Survey User WGEMUSER / password, QA user available), loads the Countryside Survey data frame.
- Data structure: Data frame includes layers such as Grids/sectors, Fishnet grids, Landscape Areas/Points/Linears, Historic Features, Aerials, OS MasterMap, etc.; layers can be transparently adjusted and order changed for editing.
- Map editing prerequisites: Editing typically requires a scale of less than 1:5000; begin edits with the Edit session and switch to the Landscape Feature Editing toolbox for Areas, Points, or Lines.
- Data handling: Save edits via the Save Session option; end sessions with End Session to discard changes if needed; log off from CS Surveyor when finished.

## Using Surveyor: navigation, tools, and workflow

- Navigational basics: Zoom, pan, measure, identify attributes, search (Find), go to XY, and map extents; use the OS MasterMap and other basemaps for context.
- Editing context: When editing, a data frame named Countryside Survey holds layers pre-set for visibility; specific editing tools exist for Areas, Points, and Lines within the Landscape Feature Editing toolbox.
- GPS note: If using GPS data, be aware positional accuracy may vary between devices; use contextual data (aerials, OS maps, MasterMap) to validate ground truth.

## Methodology for Mapping Polygons (Habitat Areas)

- 2.1 Split
  - Create new polygons from a single 1km square polygon, either freehand or by copying polygons from external layers (e.g., OS MasterMap).
  - Simple split: digitise the new polygon, with the area to be split highlighted; ensure minimum mapping unit (MMU) rules; you can modify the split shape by editing vertices.
  - Doughnut polygons: create splits that cut out a region from within the parent polygon.
  - Copying from existing layers: use Copy features to bring in external polygon shapes and include them in the split edit sketch; split areas are then edited and attributed.

- 2.2 Modify
  - Edit boundaries between polygons or shared nodes; use topology edit tools to move vertices or shared nodes; saved changes apply to spatial geometry and attributes.
  - Shared nodes: modify them via the Shared Node Modify tool; changes propagate to adjoining polygons.

- 2.3 Merge
  - Merge multiple polygons (attributes must be consistent); select target areas, choose a source area for attributes, then merge; resulting polygon inherits merged attributes (source attributes overwrite target attributes).

- 2.4 Update
  - Create new polygons by splitting existing ones or copying from other layers; can handle areas smaller than MMU; update polygon shapes and attributes, then complete with the Update button.
  - Update is a flexible operation that can replace multiple Split/Merge steps when adding new habitat areas.

- 2.5 Attributes
  - Polygon-level attributes: area, Broad/Priority habitat, BH accuracy, reason for change, visit status; default values provided for non-mandatory fields.
  - Component-level attributes: areas may have multiple components; add, copy, or delete components; ensure at least one component per area.
  - Habitat and vegetation taxonomies: structured themes (e.g., Agricultural Crops, Forestry, Inland Physiography, Vegetation Type, Species, Cover) to guide attribute selection.
  - Primary and secondary attributes: use the theme-based organization to input correct habitat and species details.

- 2.6 Copy Attributes
  - Copy attributes from a source area to one or more target areas; only one source, multiple targets; target areas overwrite existing attributes.

- 2.7 Mapping change in CS squares
  - For repeating CS squares, surveyors confirm or adjust polygons from previous surveys with emphasis on polygon-level attributes; spatial accuracy is less critical than accurate representation of habitat extents and attributes.
  - Reasons for change include verifying BH accuracy, broad habitat correctness, or marking as not previously surveyed; update the “Reason for change” field accordingly.

- Pond recording and grid-square inventory (ponds)
  - If ponds exist in a square, complete the Grid square inventory for ponds form (PC tablet) for each pond.
  - Attributes to record per pond include: square reference, pond reference, full grid reference, pond area (MMU and boundary considerations), presence/absence, reason for loss if absent, newly mapped ponds, pond age and creation reasons, notes.
  - Overview: one survey pond per square; selection is random from the mapped ponds after inventory is completed; record the selected pond as Pond sampled in the Landscape Feature Editing toolbox to reflect the correct pond for condition assessment.
  - Process to select survey pond is guided via the PC tablet form, including a confidence assessment on complete pond mapping and a lookup-based selection.

## Methodology for Mapping Point Features (points)

- Points are features smaller than 20x20 m; list includes trees, standing water bodies, ponds, etc.; spatial accuracy not primary, but can be adjusted where necessary.
- 5.1 New
  - Add points at or near the intended location; points must be created at scale 1:5000 or finer; a single point with one Unsurveyed/Missing Data component by default; minimum distance 5 m from other points.
- 5.2 Modify
  - Move an existing point; preserve its attributes after move; ensure scale is suitable (≤ 1:5000) and distance constraints apply.
- 5.3 Delete
  - Delete a point; must have a valid Reason for Change to proceed.
- 5.4 Attributes
  - Update point attributes via the Points tab; points may have multiple components; add/copy/delete components; attribute updates require the point to be in the Completed status to reflect on map.
- 5.5 Copy Attributes
  - Copy attributes from a source point to target points; supports one source and multiple targets; target points adopt the source attributes.

## Methodology for Mapping Linear Features (lines)

- Linear features: lines up to 5 m wide, minimum length 20 m; may comprise multiple parts called events; canals and rivers are represented as areas.
- Recording approach: create, cut, delete, modify, reshape lines; lines can include multiple events along their length to capture differing conditions or features.

- 6.1 New
  - Create a new line using a pen tool; minimum length 5.0 m for a new line; one line at a time; line length runs across the entire created event; new lines start with a single Unsurveyed/Missing Data event.
- 6.2 Modify
  - Modify line geometry via vertex edits; shared nodes can be modified via Shared Node Modify; edits must maintain minimum length and avoid creating self-crossing lines; end points on shared boundaries are restricted to shared-node edits.
- 6.3 Cut
  - Cut a line by digitising a cut polygon; the length cut is shown, and the remaining portion is marked; multiple cuts can be applied to a single line.
  - You can copy polygon outlines from other layers (e.g., OS MasterMap) to build the cut sketch and refine with vertex edits.
- 6.4 Delete
  - Delete a line; all associated events must have a valid Reason for Change; otherwise, delete is blocked; historic features may require alternative handling since no reason-for-change field exists for them.
- 6.5 Reshape (two modes)
  - Reshape line by drawing a reshaping guide along the line, or reshape to follow a copied line feature; reshaping requires a proper intersect and preserve minimum lengths.
- 6.6 Checking Visit Status on Linear Features
  - Use Select By Attributes to identify unvisited lines (Landscape Events layer, VISIT_STATUS = 0); edit events and attributes accordingly; ensures field verifications align with survey status.
- 6.7 Attributes
  - Edit line and event attributes; events have mandatory and optional fields; lengths of events can be adjusted on the map or via the attribute editor; events require a minimum length of 5.0 m.
- 6.8 Copy Attributes
  - Copy events from a source line to target lines; one source line, multiple targets; target lines adopt the source attributes and events; all edits must be performed at scale ≤ 1:5000.

## Troubleshooting and tips

- If the Table of Contents is lost, restore via the Windows tab: Table of Contents.
- If toolbars disappear, use Customize > Toolbars and re-enable Standard.
- If the zoom/tools toolbar is missing, re-enable under Tools > Toolbars as needed.

## Summary for environmental analysts

- The document provides a comprehensive, standardized workflow for capturing and editing habitat polygons, ponds, points, and linear features within a GIS environment (Surveyor within ArcMap) for long-term environmental monitoring.
- Emphasizes data integrity, reuse, and cross-referencing with external layers (notably OS MasterMap) to build accurate, up-to-date habitat maps.
- Details robust attribute schemes at polygon, component, point, and line levels, including change provenance (Reason for Change, BH accuracy, visit status) and species/habitat taxonomy to support policy monitoring and health assessments over time.
- Sets clear operational constraints (scale, minimum distances/lengths, one-at-a-time edits, save/end session discipline) to ensure consistency and reproducibility of monitoring outputs.
- Provides explicit pond inventory procedures and survey-pond selection to standardize aquatic habitat condition assessments within grid squares.