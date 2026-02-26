# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Overview
- Field protocol for the Glastir Monitoring and Evaluation project using the CS Surveyor extension in ArcMap.
- Covers mapping habitat polygons (areas), point features, and linear features; freshwater mapping (ponds); and CS square changes.
- Includes data management, attribute schemas, and step-by-step editing workflows.

## System and Access
- Surveyor is an ArcMap extension customized for GMEP (CS Surveyor). Log in with:
  - Main survey user: WGEMUSER / password: 4nt34t3r
  - QA user: WGEM_QA_USER / password: 44rdv4rk
- Surveyor loads required data into a 1km square data frame and offers dedicated editing tools for areas, lines, and points.
- GPS may be less accurate on some hardware; use contextual data (Aerials, OS, Master Map) to supplement.

## Getting Started with the Digital Mapping System
- Launch via Habitats task manager, selecting the Surveyor application.
- ArcMap interface has:
  - Table of Contents (layers) and Map Display.
  - CS Surveyor adds a surveyor menu; dashboards and pre-set layer symbology.
- Data frame includes habitats grids, historic features, landscape points/linears/areas, aerials, and OS data.
- Tools to customize layer transparency, drawing order, and scale exposure.
- Editing requires zoom to < 1:5000 scale for most operations and logging in/out per session.

## Methodology for Mapping Polygons (Habitat Areas)
- Core tools: Split, Modify, Merge, Update; plus Attributes and Copy Attributes.
- 2.1 Split
  - Create polygons from a 1km square or copy polygons from external layers (e.g., OS MasterMap) to form a split sketch.
  - Use freehand/digitised sketch to define split; large or small MMU (minimum mappable unit) considerations apply.
  - After sketch, input attributes for each split segment; optionally create doughnut polygons.
- 2.1.1 Copying polygons from existing layers
  - Copy polygons from layers like OS MasterMap into the edit sketch to speed up splits.
  - Use Copy+ to add features to the edit sketch; Copy- to remove.
- 2.2 Modify
  - Edit polygon boundaries by topological editing; can modify boundaries and shared nodes (Requires Shared Node Modify for end nodes).
  - Save changes to apply edits; attribute editor opens for updated areas.
- 2.3 Merge
  - Select multiple areas to merge; choose a source area to copy attributes from (if desired).
  - The merged area inherits attributes (source attributes override current ones).
- 2.4 Update
  - Creates a new landscape area by splitting and merging existing polygons; can also copy from other layers.
  - Useful for unsurveyed squares or areas smaller than MMU; new area can be tied to an existing polygon or result from copied features.
- 2.5 Attributes
  - Polygon-level and component-level attributes define habitat descriptors.
  - Polygon-level fields include Area, Broad/Priority Habitat, BH Accuracy, Reason for Change, Visit Status.
  - Components can be added, copied, or deleted; each area must have at least one component.
  - Thematic attribute groups (e.g., Agricultural Crops, Forestry, Inland Physiography, Vegetation Type, Species, Cover) aid selection.
- 2.5.1 Polygon Level Attributes
  - BH Accuracy options and Reason for Change choices (e.g., No previous code, Real change, Error change).
  - Visit Status: In progress, Completed, Refused access.
- 2.5.2 Component Level Attributes
  - Supports multiple components per area; primary vs secondary attributes; management of attributes via the Landscape Areas Attribute Editor.
- 2.6 Copy Attributes
  - Copy attributes from a source area to one or more target areas; overwrites target attributes at area and component levels.
- 2.7 Mapping change in CS squares
  - For repeating CS squares, compare to previous surveys rather than perfect spatial accuracy.
  - Confirm or adjust polygon-level Broad Habitat; assess whether to change attributes based on field observations and prior data.
  - Use a set of change reasons (e.g., Not previously surveyed, Error change, Real change) and update BH accuracy accordingly.
- Stop Editing and Session Management
  - Save Session to persist edits; End Session to discard changes.
  - Log off CS Surveyor DB when finished.

## Methodology for Mapping Freshwater (Ponds)
- If ponds exist in a square, complete the Grid Square Inventory for Ponds form (PC tablet) for every pond.
- Attributes include square reference, pond reference, area, presence/absence of water, and reason for loss if not present.
- New ponds: indicate if not on the base map; assess age (up to ~10 years) and probable creation reasons (fishing, shooting, wildlife, etc.).
- Selecting the survey pond
  - After inventory, randomly identify a single survey pond to assess condition.
  - Use the lookup table on the form to pick the survey pond and record it as Pond sampled under Inland Water on Areas or Points in Surveyor.
- Overview
  - One pond per square is surveyed for condition; selection is random among mapped ponds.
  - The form guides the surveyor to record pond details and pass the information to freshwater surveyors for condition assessment.

## Methodology for Mapping Point Features
- Points are landscape elements under 20x20m; examples include trees, standing water bodies, ponds.
- 5.1 New
  - Points added at scale ≤ 1:5000; minimum distance of 5.0m from existing points.
  - Create a new point; enter attributes; each point starts with a single Unsurveyed/Missing Data component.
- 5.2 Modify
  - Move existing points; scale requirement remains ≤ 1:5000; one point at a time; ensure distance constraints.
  - After edits, attribute updates set to Completed to reflect changes.
- 5.3 Delete
  - Delete a point with a valid Reason for Change value; otherwise, edit attributes first.
- 5.4 Attributes
  - Update attributes for a selected point; components can be added, copied, or deleted.
  - All mandatory fields must be completed; single component minimum per point.
- 5.5 Copy Attributes
  - Copy attributes from a source point to selected target points; overwrites existing attributes in targets.
  - Only one source point; multiple targets allowed.

## Methodology for Mapping Linear Features
- Linear features are lines < 5m wide; minimum length 20m; may contain gaps up to 20m; canals and watercourses treated as areas.
- Each linear feature is a continuous line composed of events (attributes) along its length.
- Recording events allows multiple features along a single line (e.g., fence with woody line), or replacements (e.g., field boundary with hedge).
- 6.1 New
  - Create new lines at scale ≤ 1:5000; minimum length 5.0m; lines cannot cross themselves; one line at a time.
  - New line starts with a single Unsurveyed/Missing Data event.
- 6.2 Modify
  - Modify line geometry by editing vertices; shared nodes require Shared Node Modify; ensure edits do not create intersections with other lines.
- 6.3 Cut
  - Digitise a cut polygon along the line to remove a section; visual indicators show cut length vs remaining length.
  - Multiple cuts can be applied; check minimum line length constraints after cuts.
- Copying from other layers
  - Use Copy features to bring in polygons from OS MasterMap or Landscape Areas to refine cuts.
- 6.4 Delete
  - Delete a line; all events must have valid Reason for Change values; historic features may require alternative handling.
- 6.5 Reshape
  - Reshape lines by defining a redraw along the existing line using a reshape graphic; end points must intersect the line.
- 6.6 Checking Visit Status on Linear Features
  - Use Select By Attributes to identify unvisited lines by VISIT_STATUS; update attributes as needed.
- 6.7 Attributes
  - Event editing within a line; events must be at least 5.0m long; set Event From and Event To points; update line length as needed.
- 6.8 Copy Attributes
  - Copy events from a source line to target lines; overwrites target events; one source line, multiple targets.

## Troubleshooting
- If Table of Contents or toolbars disappear, re-enable via Window customization:
  - Table of contents: Window > Table of Contents
  - Toolbars: Customize > Toolbars > select Standard
- If data tools vanish, re-enable through the Customize/Tools menus.

## Additional notes
- The handbook provides extensive step-by-step screen guidance for editing sessions, including schema setup, edit sessions, and field-specific dialogs.
- The workflow emphasizes careful attribute management, cross-layer data consistency, and explicit change reasons to ensure traceability of habitat and landscape feature edits.