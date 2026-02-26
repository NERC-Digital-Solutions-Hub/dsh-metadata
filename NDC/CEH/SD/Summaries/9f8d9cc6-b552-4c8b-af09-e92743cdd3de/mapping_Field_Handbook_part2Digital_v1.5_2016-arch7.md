# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field protocol for the Glastir Monitoring and Evaluation project using the Surveyor software within ArcMap.
  - Focuses on mapping habitat areas (polygons), point features, and linear features across CS squares; supports data capture for GIS-based outputs and analysis.

- 1 Using the Digital Mapping System
  - Surveyor is a CS extension inside ArcMap; no full ArcMap expertise required.
  - Access via Habitats task manager; login to CS Surveyor with provided usernames.
  - Data frame “Countryside Survey” contains pre-set layers; extensive use of OS MasterMap and aerial imagery for context.
  - GPS may be used; do not rely on it exclusively; combine with other data sources.
  - Editing requires scale of 1:5000 or better for areas, points, and lines; object creation and editing tools available in Surveyor.
  - Navigation and tools include zoom, pan, identify, find, measure, and layer visibility/ordering controls.
  - Customizable layer transparency and draw order; OS MasterMap top-layer behavior affects editing visibility.

- 2 Methodology for Mapping Polygons (Habitat Areas)
  - 2.1 Split
    - Create polygons from a single 1km square polygon; can draw freehand or copy polygons from external layers (e.g., OS MasterMap).
    - Use the edit sketch with a sketch/doughnut polygon to define the split; check minimum polygon size (MMU) and use red/blue hatch indicators for status.
    - Modify the edit sketch by moving vertices; complete with attribute editing.
  - 2.1.1 Copying polygons from existing layers
    - Copy features from polygon layers (e.g., OS MasterMap) into the split edit sketch; use Copy+ to include features; adjust with vertex edit tools; split completed to reflect new polygons.
  - 2.2 Modify
    - Edit shared boundaries; use topology edit tools; adjust vertices and shared nodes; save changes to apply edits.
  - 2.3 Merge
    - Select areas to merge; choose a source area for attributes; merged polygon inherits attributes from the chosen source; overwrites at area and component levels.
  - 2.4 Update
    - Creates a new landscape area by splitting/merging existing polygons or copying areas from other layers; useful for unsurveyed squares and areas smaller than MMU.
    - Updated area(s) shown with blue/red hatches; edit as needed and assign attributes; can serve as an alternative to multiple Split/Merge edits.
  - 2.5 Attributes
    - Manage attributes for areas (broad/priority habitat, habitat type, species, physiography, etc.) via the Landscape Feature Editing toolbox.
  - 2.5.1 Polygon Level Attributes
    - Record polygon area, Broad/ Priority habitat, BH accuracy (default: Not previously surveyed for new squares), Reason for change, Visit status (In progress, Completed, Refused access).
  - 2.5.2 Component Level Attributes
    - Areas may have multiple components; add/copy/delete components; edit component attributes; ensures at least one component per area.
    - Thematic groups (Theme) organize primary/secondary attributes (e.g., agricultural crops, forestry, inland physiography, vegetation, etc.).
  - 2.6 Copy Attributes
    - Copy attributes from a source area to one or more target areas; target areas overwrite existing attributes; only one source, many targets allowed.
  - 2.7 Mapping change in CS squares
    - For repeat surveys, use existing data and confirm or adjust polygons and attributes from previous surveys.
    - Focus on polygon-level attributes; use predefined reason codes (e.g., Error change, Real change, Not previously surveyed) and update BH accuracy and related fields accordingly.
    - Spatial accuracy is less critical than accurate representation of habitat extent; adjust shapes and sizes as needed.

- 3 Freshwater Mapping (Pond-related procedures)
  - Pond attribute data are recorded on a Grid Square Inventory for Ponds form (PC tablet) for each pond in the square.
  - For every pond: square reference, pond reference, full grid reference, area, presence/absence in field, reason for loss if marked absent, notes on new ponds, age and creation reasons.
  - Survey pond: after mapping all ponds in a square, randomly select a pond to sample for condition; record the Pond sampled attribute on the corresponding Areas or Points tab to guide freshwater surveys.
  - Overview process: one surveyed pond per square; ensure inventory form completion for all ponds before selecting the survey pond.

- 5 Methodology for Mapping Point Features
  - Points are landscape elements under 20x20 m; examples include trees, standing water, ponds; spatial accuracy is secondary; points can be added/relocated as needed.
  - 5.1 New
    - Add a new point at scale 1:5000 or finer; points must be added one at a time; minimum distance of 5 m from existing points; enter attributes after creation.
  - 5.2 Modify
    - Move an existing point; preserve attributes; one point at a time; move scale constraint of 1:5000 or better applies.
  - 5.3 Delete
    - Delete a point with a valid Reason for Change; points without valid reasons cannot be deleted.
  - 5.4 Attributes
    - Edit point attributes; points may have multiple components; add/copy/delete components; completion updates point appearance after saving.
  - 5.5 Copy Attributes
    - Copy attributes from a source point to target points; only one source, many targets; overwrite target attributes; ensure scale constraint is met.

- 6 Methodology for Mapping Linear Features
  - Linear features are lines up to 5 m wide, with a minimum length of 20 m; include fences, walls, hedges, and other boundaries; canals/rivers treated as areas.
  - 6.1 New
    - Create new lines; minimum length 20 m; no crossings; line endpoints may create new events; each new line starts with a single Unsurveyed/Missing Data event; must edit within square at scale 1:5000 or better.
  - 6.2 Modify
    - Edit line geometry; add/delete/move vertices; handle shared nodes; ensure edits do not create invalid geometries; save changes.
  - 6.3 Cut
    - Digitise cut polygons along a line; visualize length cut vs remaining; edit sketch as needed; multiple cuts allowed; validations apply (minimum length constraints).
  - 6.4 Delete
    - Delete a line with valid Reason for Change for all attached events; historic features require alternative handling as there are no dedicated Reason for Change fields for them.
  - 6.5 Reshape
    - Reshape lines by drawing a reshape graphic; options include reshaping along the same line or following a copied line boundary; must intersect the original line; save when satisfied.
  - 6.6 Checking Visit Status
    - Use Select By Attributes to identify unvisited Landscape Events; filter for VISIT_STATUS and apply updates as needed.
  - 6.7 Attributes
    - Edit line-level events and their attributes; events must be at least 5 m long; event attributes edited one at a time; mandatory fields highlighted.
  - 6.8 Copy Attributes
    - Copy events from a source line to target lines; one source, multiple targets; target lines gain the source events and attributes; overwrite target attributes as needed.

- 7 Troubleshooting
  - Common issues with Table of Contents or toolbars; restore via Windows customization options (Table of contents, toolbars, standard toolbar, etc.).

- Saving, exiting, and session management
  - End Edit sessions via Save Session when edits are complete; use End Session to discard changes.
  - Log off from CS Surveyor DB when finished; ArcMap will prompt to save the untitled document as needed.
  - Regularly save changes to prevent data loss during fieldwork.