# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field protocol for mapping habitat areas, ponds, and landscape features within Glastir Monitoring and Evaluation Programme (GMEP) using the CS Surveyor extension in ArcMap.
  - Supports polygon (habitat areas), point features, and linear features with standardized attribute schemes and change workflows.
  - Emphasises data quality, reproducibility, and auditable edits; includes guidance on sharing data and safeguarding metadata where applicable.

- System and workflow overview
  - Surveyor is a CS extension to ArcMap, built to capture and edit GMEP data; aimed to be user-friendly without requiring deep ArcMap expertise.
  - Users log in with predefined surveyor accounts; data resides in a 1km square framework within a Countryside Survey data frame.
  - Typical workflow: edit within a square, use dedicated tools for splitting/modifying/merging polygons, editing attributes, and saving sessions before logging off.
  - Editing requires appropriate map scale (mostly 1:5000 or less), and edits must be saved to take effect.

- Mapping Polygons (Habitat Areas)
  - 2.1 Split
    - Create new polygons from a single 1km square polygon (simple split) or by copying polygons from external layers (e.g., OS MasterMap).
    - Use digitising/sketch tools to define split areas; invalid or MMU-below polygons are highlighted and must be redrawn.
  - 2.1.1 Copying polygons from existing layers
    - Copy features from layers like OS MasterMap into the split edit sketch; use Copy+ to include features in the edit sketch.
    - Areas to be split are shown with protective outlines; attributes are assigned during the split edit.
  - 2.2 Modify
    - Modify polygon boundaries or shared nodes; use topology edit tools to adjust vertices, add/delete/move vertices.
    - Endpoints of shared boundaries can only be edited via Shared Node Modify.
  - 2.3 Merge
    - Merge multiple polygons when their attributes are identical; choose a source polygon for attributes to overwrite onto the merged polygon.
  - 2.4 Update
    - Create new areas by splitting/merging; useful for adding polygons that intersect existing ones or copying from other layers.
  - 2.5 Attributes
    - Attributes describe broad/priority habitat, species/physiography, etc. Access via Landscape Feature Editing toolbox.
  - 2.5.1 Polygon Level Attributes
    - Record area, Broad/Priority habitat, BH accuracy (e.g., new squares: “Not previously surveyed”), reason for change, and visit status (In progress, Completed, Refused access).
  - 2.5.2 Component Level Attributes
    - Areas may have multiple components; add/copy/delete components and edit their attributes.
    - Themes organize attributes (e.g., agricultural crops, vegetation types, species, cover, sward characteristics).
  - 2.6 Copy Attributes
    - Copy attributes from a source polygon to multiple target polygons; one source, multiple targets; target attributes overwrite existing ones.
  - 2.7 Mapping change in CS squares
    - Repeating CS squares: confirm or adjust polygons and their polygon-level attributes against prior surveys; focus on extent and attributes rather than precise spatial accuracy. Record changes with appropriate reason codes or mark as not previously surveyed.

- Ponds: Grid square inventory and survey selection
  - If a square contains ponds, complete the Grid square inventory for ponds form (per pond): IDs, full grid reference, area (m2), presence/absence, reason for loss if absent in field, notes on new ponds, age and reason for creation, and any additional observations.
  - After inventory, identify the survey pond (randomly) for condition assessment; record the pond as a landscape feature (Areas or Points) and communicate to freshwater surveyors.
  - The survey pond is selected from the inventory using a lookup table and then recorded as Pond surveyed in the appropriate CS Surveyor layer.

- Mapping Point Features
  - 5 Methodology for Mapping Point Features
  - 5.1 New
    - Add new points at scale 1:5000 or less; ensure minimum 5.0m from other points; each new point starts with a single Unsurveyed/Missing Data component.
  - 5.2 Modify
    - Move existing points; preserve visibility and attributes; map scale must be 1:5000 or less; one point at a time.
  - 5.3 Delete
    - Delete points with a valid Reason for Change; mandatory Reason for Change required to delete.
  - 5.4 Attributes
    - Edit point attributes; a point may have multiple components; use the Points Attribute Editor toolbox to add/copy/delete components.
  - 5.5 Copy Attributes
    - Copy attributes from a source point to one or more target points; one source, many targets; targets overwrite existing attributes.

- Mapping Linear Features
  - 6 Methodology for Mapping Linear Features
  - Linear features are lines under 5m wide but longer than 20m; record continuous lines as events along a line; events describe fences, walls, woody features, etc.
  - 6.1 New
    - Add new lines within the square (minimum length 5.0m; not crossing itself); lines are created with a single Unsurveyed/Missing Data event.
  - 6.2 Modify
    - Edit line shape by adding/deleting/moving vertices; Shared Nodes modify allows adjustment at line intersections; end points of shared boundaries are protected.
  - 6.3 Cut
    - Cut line segments with a digitised polygon; show length to be cut and remaining length; supports copy-from-external-layer edits.
  - 6.4 Delete
    - Delete lines with valid Reason for Change for all attached events; lines must be within the 1:5000 scale.
  - 6.5 Reshape Line
    - Reshape a line by drawing a reshape graphic; supports two modes: following an existing line or following a copied line boundary; edit with vertex tool if needed.
  - 6.6 Checking Visit Status on Linear Features
    - Use Select By Attributes to identify unvisited lines (Landscape Events, VISIT_STATUS = 0); edit line attributes accordingly.
  - 6.7 Attributes
    - Edit line-level attributes (top) and event-level attributes (under themes); event lengths can be set on the map and edited via Event From/To fields or Set button.
  - 6.8 Copy Attributes
    - Copy events from a source line to target lines; one source, multiple targets; target lines adopt source attributes and events.

- Troubleshooting and general guidance
  - Save work frequently: use Save Session to persist edits; End Session discards edits.
  - Log off CS Surveyor DB when finished to avoid data loss.
  - If layout or toolbars are lost, use the Windows customization features to restore standard toolbars and Table of Contents.

- Practical notes and scale considerations
  - Edit operations generally require the map to be at or below 1:5000 scale.
  - MMU and quality checks are used to ensure polygons meet minimum mapping units and hierarchy requirements.
  - Copy features from OS MasterMap or other layers to support efficient editing and data consistency.
  - Attribute schemas and themes are used to streamline data capture and ensure consistent reporting across squares and surveys.