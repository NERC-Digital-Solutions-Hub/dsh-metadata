GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Overview

- Purpose: Field data capture for the Glastir Monitoring and Evaluation project using the Surveyor extension in ArcMap.
- Data scope: Polygons (Areas), Points, and Lines with events/attributes to document landscape habitats, features, and changes within 1 km squares.
- System context: Surveyor integrates with ArcMap; users follow scripted editing workflows to create, modify, and update spatial features and their attributes.
- Data governance cues: Save sessions regularly; log off properly; maintain consistent attribute schemas and use of reference layers (e.g., OS MasterMap) for copying features.

## System and data model

- Core tools and interfaces:
  - ArcMap with CS Surveyor extension; login required; main map frame is Countryside Survey data.
  - Tools organized in Landscape Feature Editing toolbox (Areas, Points, Lines) with dedicated editing tabs.
- Feature types and structure:
  - Areas (polygons):
    - Polygon level attributes: Area, Broad/ Priority habitat, BH Accuracy, Reason for change, Visit status.
    - Component level attributes: one or more components per area; can add/copy/delete components; primary/secondary attributes organized by themes.
  - Points (point features, < 20 x 20 m):
    - New, Modify, Delete, Attributes, Copy Attributes.
    - Each new point starts with an Unsurveyed/Missing Data component; edits constrained to scale 1:5000 or less; minimum 5 m spacing from other points.
  - Lines (linear features, generally ≤ 5 m wide, minimum 20 m length):
    - Represent lines as continuous features with multiple events along their length.
    - Event attributes describe the line segment components (e.g., fences, walls, woody features); lines edited via New/Modify/Cut/Delete/Reshape/Copy Attributes.
    - Shared nodes and topology: certain endpoints and shared nodes can only be edited via specific “shared node modify” operations.
- Data integration and standards:
  - Copy features from external layers (e.g., OS MasterMap) to create/edit polygons or split shapes.
  - MMU and map scale controls affect editing actions and feature validity.
- Ponds core workflow:
  - Grid square inventory form records pond-level details for every pond; random survey pond selected after inventory is complete.
  - Survey pond is recorded as a primary attribute and used for freshwater condition assessment.

## Key workflows and editing guidance

- Polygons (Habitat Areas)
  - Split: create new polygons within a 1 km square; can digitise freehand or copy polygons from OS MasterMap; ensure minimum mappable unit (MMU) and edit with vertex tools.
  - Modify: adjust boundaries or shared nodes; use topology-aware editing; save changes after attribute updates.
  - Merge: combine multiple areas when attributes match; can copy attributes from a chosen source area to the merged polygon.
  - Update: create/adjust polygons by digitising update polygons; can copy attributes from other layers; useful for unsurveyed squares or complex habitat changes.
  - Attributes: set polygon-level and component-level attributes; Broad/PH habitat selection per vegetation key; BH Accuracy defaults for new squares; Reasons for change (e.g., No previous code, Real change); Visit status options (In progress, Completed, Refused access).
  - Copy Attributes: apply attributes from a source polygon to multiple target polygons; overwrites target attributes.
  - CS squares mapping changes: for repeating CS squares, confirm existing polygons against field observations; focus on polygon-level attributes; indicate errors or new baselines as needed.

- Points
  - New: add one point at scale ≤ 1:5000; minimum 5 m from other points; enter attributes after creation.
  - Modify: move a point; update attributes; completed status changes point appearance on refresh.
  - Delete: remove point only if it has a valid Reason for Change; otherwise edit attributes first.
  - Attributes: edit point attributes; components can be added/copied/deleted; mandatory fields flagged for entry.
  - Copy Attributes: copy attributes from a source point to multiple target points; overwrites target attributes.

- Lines (Linear Features)
  - New: create new line with a minimum length of 20 m; avoid crossing itself; edits scale at or below 1:5000; new line begins with a single Unsurveyed/Missing Data event.
  - Modify: adjust line geometry; edit vertices; handle shared nodes via shared-node modify; ensure edits do not create invalid intersections.
  - Cut: digitise cut polygons along a line to remove sections; length highlighted for cut vs remainder; multiple cuts allowed if validated.
  - Delete: remove lines with valid Reason for Change on all events; historic features may require different handling (see notes).
  - Reshape: reshape along an edit graphic or copied line; ensure edits intersect the line at endpoints; shared-node constraints apply.
  - Copy Attributes: copy events/attributes from a source line to target lines; overwrites target line attributes; supports multiple targets but only one source.
  - Checking visit status: use attribute query to identify unvisited lines; update line/event attributes accordingly; ensure mandatory fields are completed.
  - General rules: events must be at least 5.0 m; lines cannot be added outside square; cannot edit endpoints in some contexts; shape edits require careful vertex management.

## Data quality, validation and constraints

- Habitat and attribute accuracy:
  - BH Accuracy (Broad Habitat) management; default for new squares is “Not previously surveyed.”
  - Reason for change options (e.g., Error change, No change, Real change, Not previously surveyed).
- Spatial validity:
  - MMU considerations; updates/edits may result in areas below MMU which are highlighted and may be merged with adjacent polygons.
  - For lines and points, minimum length/spacing rules apply; edits must maintain topological integrity (no invalid intersections, proper shared-node handling).
- Data capture discipline:
  - After edits, surveyors must save sessions to persist changes; ending a session discards unsaved edits.
  - Use of Copy Features and Copy Attributes requires careful review of target features to ensure consistency.
- Ponds data integrity:
  - For each pond in a grid square, complete the grid square inventory form; select a survey pond after inventory; ensure a faithful reflection of pond existence, area, and changes for condition surveys.

## Practical use and collaboration

- Data accessibility and coordination:
  - OS MasterMap and other external layers can be used to accelerate polygon creation; careful management ensures consistency across the wider data community.
- User support and troubleshooting:
  - System prompts to log off, save, and reopen as needed; advisor/helpdesk contact for Surveyor queries.
  - Common issues documented (e.g., losing table of contents or toolbars) with straightforward restoration steps.

## Troubleshooting and tips

- Regularly save and end sessions properly to avoid data loss.
- Ensure map scale is at or below 1:5000 for edits; adhere to square boundaries; avoid editing outside the designated square.
- Validate that all required fields are filled (orange indicators for mandatory fields) before saving edits.