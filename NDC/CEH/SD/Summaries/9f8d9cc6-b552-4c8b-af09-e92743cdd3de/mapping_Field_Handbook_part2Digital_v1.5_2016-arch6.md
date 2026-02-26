# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose: This handbook documents the mapping field protocol for the Glastir Monitoring and Evaluation project, detailing how to use the CS Surveyor extension within ArcMap to capture and edit habitat polygons, points, lines, and ponds for GMEP data products.

- System and access
  - Software: ArcMap with the CS Surveyor extension; Surveyor is built on ArcMap and integrates habitat mapping tools.
  - Login: Users log into the Surveyor extension (example usernames/passwords provided in the guide). Main survey square workspace is a data frame named Countryside Survey.
  - Data scope: Supports mapping of areas (polygons), point features, and linear features within 1 km square cells, plus pond data collection for freshwater mapping.
  - Help and support: Users are advised to contact helpdesk for Surveyor queries.

- Data model and editing framework
  - Data types:
    - Areas/Polygons: Landscape Areas with polygon-level and component-level attributes.
    - Points: Landscape Points for features under 20 m x 20 m.
    - Lines/Linear Features: Landscape Lines representing features <5 m wide, mapped as events along a single line.
    - Ponds: Specific pond data recorded via grids, with a separate grid-square pond inventory form.
  - Attribute structure:
    - Polygon-level attributes: Area size, Broad/Priority Habitat, BH Accuracy, Reason for Change, Visit status.
    - Component-level attributes: May have multiple components per area; supports adding, copying, deleting components; primary/secondary attributes, species, cover, etc.
    - Point and line attributes: Points can have components; lines have events with attributes, including lengths and visit status.
  - Tools and editing framework:
    - Landscape Feature Editing toolbox with separate tabs for Areas, Points, and Lines.
    - Copy Attributes and Copy Features tools to reuse attributes or geometry from existing layers (e.g., OS MasterMap).

- 1. Using the Digital Mapping System (overview of workflow and interface)
  - Initiation: Launch Surveyor via ArcMap; sign in; access the survey square in the map.
  - Interface: Main ArcMap window plus a Surveyor extension panel; a pre-styled data frame holds map layers for visibility.
  - Navigation and auxiliary tools: Standard ArcMap tools (zoom, pan, select, identify, find, measure) plus Surveyor-specific controls for editing features.
  - GPS note: Optional GPS initialization; use contextual data (aerial photos, OS maps) to support mapping accuracy.

- 2. Methodology for Mapping Polygons (Habitat Areas)
  - 2.1 Split (creating polygons from 1 km square polygons)
    - Simple split: Digitise a split area using the sketch tool; large or edge-at-square splits are common.
    - When small (MMU) areas are too tiny, red highlights indicate issues; refine by modifying the split sketch.
    - Optional use of Copy Features to import existing polygons from other layers (e.g., OS MasterMap) into the split edit sketch.
  - 2.1.1 Copying polygons from existing layers
    - Copy polygons from layers like OS MasterMap to build an edit sketch; use Copy+ to add features to the sketch and Copy- to remove.
  - 2.2 Modify
    - Modify boundaries or shared nodes; use topology edit tools; save changes to update geometry and attributes.
  - 2.3 Merge
    - Merge multiple areas when attributes align; selection highlights areas to merge; attributes from a chosen source area overwrite merged area attributes.
  - 2.4 Update
    - Create a new polygon by splitting and merging existing polygons; can be used to incorporate new habitat areas or copy from other layers.
  - 2.5 Attributes
    - Editing area attributes: Broad/Priority Habitat, accuracy, reason for change, and visit status (with defaults).
  - 2.5.1 Polygon Level Attributes
    - Fields include area, habitat classification, BH accuracy, reason for change, visit status.
  - 2.5.2 Component Level Attributes
    - Manage multiple components per area; add/copy/delete components; primary/secondary attributes; vegetation type, species, cover, etc.
  - 2.6 Copy Attributes
    - Copy attributes from a source area to multiple target areas; overwrites existing attributes in targets.
  - 2.7 Mapping change in CS squares
    - For repeating CS squares, review and adjust polygon attributes based on field observations; confirm or change BH and attributes; record reason for change.

- 3. Pond attributes to record (Grid square inventory for ponds)
  - When ponds exist in a square, complete a Grid Square Inventory form for each pond (on tablet).
  - Attributes collected per pond include:
    - Square reference, pond reference, full grid reference
    - Pond area (m²) and whether the pond contains water
    - If pond is present on base map but absent in field, reason for loss (L, I, B, O, U)
    - New ponds: whether pond is not mapped previously and age/creation reason
    - Creation reasons (e.g., fishing, wildlife, golf hazard, etc.)
  - Overview of process:
    - Map all ponds, complete inventory forms; randomly identify a survey pond from the inventory for condition assessment; record the “Pond sampled” attribute in the system to reflect the selected pond.

- 4. Methodology for Mapping Point Features
  - Points represent individual landscape elements under 20x20 m; new points can be added, moved, or deleted as needed.
  - 5.1 New: Add new point; must be at scale 1:5000 or smaller; minimum distance from other points; default component is Unsurveyed/Missing Data.
  - 5.2 Modify: Move existing point; maintain attributes; must be at 1:5000 or smaller; single-point edits.
  - 5.3 Delete: Remove point with valid Reason for Change; otherwise edit attributes first.
  - 5.4 Attributes: Edit point attributes; at least one component per point; mandatory vs optional fields indicated.
  - 5.5 Copy Attributes: Copy attributes from a source point to multiple target points; overwrites target attributes.

- 6. Methodology for Mapping Linear Features
  - Background: Record linear features less than 5 m wide which are at least 20 m long (with possible gaps up to 20 m); often represented as a single line with multiple events.
  - 6.1 New: Add new line (minimum length 5 m; scale 1:5000 or smaller); endpoints must not cross themselves; intersections split lines automatically.
  - 6.2 Modify: Edit line shape and events; modify shared nodes; ensure edits do not create invalid topology.
  - 6.3 Cut: Digitise a cut along a line; visualize cut length vs remaining length; ensure minimum lengths are preserved; can copy features from other layers to assist.
  - 6.4 Delete: Delete a line with valid Reason for Change on all events; historic features may require alternative handling since they lack “Reason for Change” fields.
  - 6.5 Reshape: Reshape a line by drawing a reshape graphic; endpoints must align with the original line; ensure edits maintain valid geometry.
  - 6.6 Checking Visit Status on Linear Features: Use Select by Attributes to identify unvisited lines; edit line and event attributes accordingly; ensure required fields are completed.
  - 6.8 Copy Attributes: Copy events from a source line to target lines; overwrites target event attributes with source line attributes.

- 7 Troubleshooting
  - Tips for recovering lost Table of Contents or toolbars in the ArcMap environment.
  - Guidance on restoring tools and panel configurations.

- Practical notes for data support and reuse
  - The workflow emphasizes reproducible data editing within a standardized GIS environment.
  - Attribute structures (polygon and component levels; BH, habitat keys, species, coverage) support structured data exploration and downstream analysis.
  - Copy and update operations enable efficient propagation of attributes across multiple areas, lines, or points, aiding data consistency and re-use in dashboards and reports.
  - The process for CS squares vs new squares highlights how data validation and attribute updates are carried out across repeated surveys, ensuring data reflect field observations while preserving historical context.