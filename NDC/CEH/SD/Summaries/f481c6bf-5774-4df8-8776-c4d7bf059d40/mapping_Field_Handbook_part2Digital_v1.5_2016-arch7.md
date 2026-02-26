# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Overview
- Field protocol handbook for the Glastir Monitoring and Evaluation project, focusing on mapping with the Surveyor software integrated into ArcMap.
- Surveyor provides tools to capture, edit, and manage polygon (habitat areas), point (landscape features), and line (linear features) data within 1km grid squares.
- Emphasis on working with end users, data verification, data cleaning, and iterative testing.

## System, data, and interface
- Built on ArcMap with a CS Surveyor extension; required login to access the surveyor tools and database.
- A dedicated data frame named “Countryside Survey” holds layers and pre-set symbology for visibility and usability.
- Data sources include OS MasterMap, aerial photos, OS raster/maps; copying features between layers is supported to aid editing.
- Surveyor adds a specialized editing workflow and a landscape feature toolbox with separate tabs for Areas (polygons), Points, and Lines.
- Editing typically requires map scale ≤ 1:5000; distances and minimum sizes (e.g., MMU) govern edit feasibility.

## Mapping Habitat Areas (Polygons)
- 2.1 Split
  - Create new polygons from a 1km square, either freehand or by copying polygons from external layers (e.g., OS MasterMap).
  - Use sketch tools and vertex editing to define the split; large splits are preferred over many small polygons.
  - If a part is below the Minimum Mappable Unit (MMU), it is flagged; can be redrawn or cleared and redone.
  - Doughnut polygons (holes) are supported as standard splits.
- 2.2 Modify
  - Modify boundaries or shared nodes; use topology tools to adjust vertices; save changes to apply edits.
- 2.3 Merge
  - Merge multiple areas with identical attributes; the merged polygon inherits attributes from the chosen source area.
- 2.4 Update
  - Create new areas by splitting/merging or by copying polygons from other layers; can handle areas smaller than MMU.
- 2.5 Attributes
  - Polygon and component levels; Broad/ Priority habitats, accuracy, reason for change, and visit status.
  - Thematic attribute groups (e.g., AGRICULTURAL CROPS, FORESTRY, INLAND WATER, etc.) guide data entry.
- 2.5.1 Polygon Level Attributes
  - Include area, Broad/ Priority habitat, BH accuracy, reason for change, and visit status (In progress, Completed, Refused access).
- 2.5.2 Component Level Attributes
  - Areas can have multiple components; components can be added, copied, or deleted.
  - Attributes organized by themes (vegetation type, species, cover, sward, physiography, etc.).
- 2.6 Copy Attributes
  - Copy attributes from a source area to one or more target areas; target areas receive the source attributes, overwriting existing ones.
- 2.7 Mapping change in CS squares
  - For repeat CS squares, researchers confirm or adjust polygons based on field observations.
  - Emphasis on polygon-level attributes; spatial accuracy is secondary to habitat representation.
  - Reason-for-change options include error changes, new baselines, not previously surveyed, etc.
- Saving workflow
  - Editing sessions are ended via Save Session (to persist changes) or End Session (to discard); confirmation prompts ensure deliberate actions.
  - Log off from CS Surveyor when finished.

## Freshwater Mapping (Ponds)
- Grid square inventory form (on tablet) records pond-level data; one form per pond per square.
- Attributes include: square reference, pond reference, fullest grid reference, pond area (m², including boundary considerations), presence or absence of water, reason for loss if present in base map but absent in field, new ponds status, age of new ponds, and creation reasons.
- After all ponds are mapped, select a single “survey pond” randomly for condition assessment; use a lookup table to pick the pond.
- Record the survey pond using the Pond sampled attribute under Inland Water (Areas or Points) in Surveyor.

## Methodology for Mapping Point Features
- Points are landscape elements < 20m x 20m (e.g., trees, standing water, ponds); editing occurs under Points tab.
- 5.1 New
  - Add new point at ≤ 1:5000 scale; minimum distance 5m from existing points; each new point starts with an Unsurveyed/Missing Data component.
- 5.2 Modify
  - Move point; preserve attributes; changes visible after refresh; scale ≤ 1:5000; one point at a time; 5m separation rule.
- 5.3 Delete
  - Delete point only with a valid Reason for Change; otherwise editing is required first.
- 5.4 Attributes
  - Edit point attributes; points may have multiple components; ensure mandatory fields are completed.
- 5.5 Copy Attributes
  - Copy attributes from a source point to multiple target points; overwrites target attributes.

## Methodology for Mapping Linear Features
- Linear features: lines < 5m wide, length ≥ 20m; can include gaps up to 20m; may be woodlands, hedges, walls, fences, banks, etc.
- General rules: record along the line; use events to reflect varying features along its length; avoid curtilage areas and woodland canopy; canals/rivers treated as areas.
- Recording uses events along a single line; multiple events reflect changes along the feature.
- 6.1 New
  - Add new line with pencil; minimum length 5m; one line at a time; ensure lines do not cross themselves; auto-splitting at intersections when created.
- 6.2 Modify
  - Edit line shape and vertices; shared nodes can only be modified via Shared Node Modify; scale ≤ 1:5000.
- 6.3 Cut
  - Cut a line with a digitised polygon; lengths shown on-map; copy features from OS MasterMap or other layers to aid accurate cuts.
- 6.4 Delete
  - Delete line with valid Reason for Change on all events; some themes have no reasons for change; deletion may be restricted.
- 6.5 Reshape
  - Reshape a line along its length or following a copied line; ensures intersections and minimum lengths remain valid.
- 6.6 Checking Visit Status
  - Use Select By Attributes to identify unvisited Landscape Events; VISIT_STATUS and other fields guide editing.
- 6.7 Attributes
  - Edit event-level attributes; events must be at least 5.0m long; length is adjustable in the Attribute Editor or on-map set points.
- 6.8 Copy Attributes
  - Copy events from a source line to multiple target lines; overwrites target event attributes; one source line, many targets.

## Troubleshooting
- Common issues: missing or mislaid toolbars or Table of Contents; restore via Windows customization options (Table of Contents, toolbars, standard toolbar).