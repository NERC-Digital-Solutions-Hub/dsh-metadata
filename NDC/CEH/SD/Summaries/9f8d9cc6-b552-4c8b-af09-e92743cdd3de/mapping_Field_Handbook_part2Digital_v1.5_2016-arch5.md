# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose: Provide field protocol for mapping habitats and landscape features in the Glastir Monitoring and Evaluation Programme using the CS Surveyor extension within ArcMap.
- Scope: Covers setup, data model (areas/polygons, points, linear features), workflows, attribute schemas, and editing operations for new and repeat surveys.

## Access, setup, and data governance

- Use ArcMap with the CS Surveyor extension to edit data for a chosen 1 km square.
- Log in to CS Surveyor; the system loads relevant landscape data layers and pre-set symbology for visibility.
- System prompts for helpdesk support for queries or problems.
- Ensure mapping scale is appropriate (generally 1:5000 or less) before edits; maintain an auditable trail of changes and session saves.

## Data model and layers

- Three main feature types:
  - Areas (polygons): landscape areas with attributes and components.
  - Points: small landscape features (e.g., trees, standing water, ponds) recorded as points (or as components within areas).
  - Lines (linear features): features less than 5 m wide, represented as continuous lines with multiple events.
- Each feature type has an Attribute Editor with domain-specific fields (habitat, species, physiography, etc.) and supports copying attributes between features.

## Mapping workflow overview

- Begin editing by opening CS Surveyor in ArcMap and selecting a square.
- Use the Landscape Feature Editing toolbox to edit Areas, Points, and Lines without leaving the edit session.
- Tools include creating, modifying, copying, updating, and deleting features, with attributes managed in the respective editors.
- Save edits frequently; end sessions with a Save Session command to ensure changes are recorded.

## 2. Mapping Polygons (Habitat Areas)

- 2.1 Split
  - Create polygons from a 1 km square polygon or copy from external layers (e.g., OS MasterMap).
  - Use split to carve out new polygons; ensure minimum mappable units (MMU) rules are respected.
  - Modify split shapes via vertex editing; can create doughnut polygons by splitting within a polygon.
- 2.1.1 Copying polygons from existing layers
  - Copy features from another polygon layer to form the edit sketch; use Copy+ to add features to the sketch.
  - Areas to be split are shown with outlines; the attribute editor opens to input attributes for each split part.
- 2.2 Modify
  - Adjust boundaries or shared nodes with topology edits; changes affect adjacent polygons.
  - Endpoints of shared boundaries (shared nodes) can only be modified via Shared Node Modify.
- 2.3 Merge
  - Merge multiple areas after ensuring attributes are identical; choose a source area for attributes if needed.
- 2.4 Update
  - Create new polygons by splitting and/or merging existing polygons; suitable for adding areas that intersect multiple existing areas; less sensitive than split for small areas.
- 2.5 Attributes (Area and Components)
  - Polygon Level: area, Broad/Priority habitat, BH accuracy (e.g., 98 for correct allocation), reason for change, visit status (In progress, Completed, Refused access).
  - Component Level: components within an area can be added, copied, or deleted; each component holds its own attributes.
  - Thematic attribute structure guides selection (e.g., AGRICULTURAL CROPS, INLAND WATER, FORESTRY, etc.) with fields for primary attributes, qualifiers, vegetation type, species, cover, height/variations, etc.
- 2.6 Copy Attributes
  - Copy attributes from a source area to one or more target areas; target areas adopt the source attributes, overwriting existing values.
- 2.7 Mapping change in CS squares
  - For repeating CS squares, surveyors confirm or adjust polygons from previous surveys; focus on polygon-level attributes and overall habitat representation rather than perfect spatial accuracy.

## 5. Mapping Point Features

- 5 Overview: Points represent features under various themes; spatial accuracy is secondary to representing habitat presence. Points can be added, moved, or deleted as needed.
- 5.1 New
  - Add a point at scale 1:5000 or finer; one point at a time; minimum distance of 5 m from other points; new points start with an Unsurveyed/Missing Data component.
- 5.2 Modify
  - Move an existing point; maintain attributes; moves allowed only at 1:5000 or less; one point at a time; 5 m separation constraint.
- 5.3 Delete
  - Delete a point only if it has a valid Reason for Change; otherwise, edit attributes before deletion.
- 5.4 Attributes
  - Update point attributes and components; some fields mandatory (orange) and others optional (blue); a point may have multiple components.
- 5.5 Copy Attributes
  - Copy attributes from a source point to multiple target points; targets adopt source attributes; one source, many targets; overwrites target attributes.

## 6. Mapping Linear Features

- 6 Overview: Linear features are lines representing features up to 5 m wide, with events describing segment details. Minimum length per line is 20 m; lines may include gaps up to 20 m.
- Recording approach: represent as continuous lines with multiple events; if a line comprises multiple changes, code as distinct events along the same feature.
- 6.1 New
  - Create a new line with at least 20 m length; minimum width 5 m; lines must be within a survey square; initial event is Unsurveyed/Missing Data.
- 6.2 Modify
  - Edit line geometry through vertex editing; shared nodes (endpoints involved with other lines) require Shared Node Modify; edits must avoid self-intersection and maintain minimum lengths.
- 6.3 Cut
  - Digitise a cut polygon along the line to remove a section; the cut length is previewed; finalise with Cut.
- 6.4 Delete
  - Delete a line and all its events; ensure all events have valid Reason for Change; historic features may require alternative handling since some themes lack a Reason for Change field.
- 6.5 Reshape
  - Reshape a line by drawing a reshape graphic that intersects the line at start/end; allows refining the line’s path; shared node rules apply.
- 6.6 Checking Visit Status on Linear Features
  - Use Select By Attributes to identify unvisited lines (VISIT_STATUS = 0) and edit attributes accordingly; color-coding highlights status.
- 6.7 Attributes
  - Event-level attributes describe the specific detail along a line (e.g., fence, woody linear feature, boundary changes); lines have a top-level length attribute; events can be edited, copied, or added.
- 6.8 Copy Attributes
  - Copy events from a source line to target lines; one source line and multiple target lines allowed; target lines receive copied events with new unsurveyed components to be edited.

## Pond inventory and grid square form (for ponds)

- If ponds exist in a square, complete the Grid Square Inventory for Ponds form for every pond.
- Attributes to record per pond:
  - Square reference, pond reference, fullest grid reference.
  - Pond area (m2) and winter water level; presence/absence in field vs base map; reason for loss if absent.
  - New ponds: indication of novelty, estimated age, and reason for creation (evidence categories: fishing, shooting, wildlife, golf hazard, ornamental, etc.).
- Overview: identify a single survey pond per square for condition assessment, selected randomly from ponds in the inventory; survey pond is recorded under Inland Water → Areas or Points with Pond sampled attribute.
- Process steps: complete inventory forms for all ponds, determine survey pond, update Surveyor accordingly, and coordinate with freshwater surveyors for condition assessment.

## Cleaning up and ending sessions

- At end of edit session, choose Save Session to persist changes; End Session discards unsaved edits.
- Log off from CS Surveyor DB when finished; ArcMap will prompt to save the untitled document if applicable.

## Troubleshooting and tips

- If toolbars or table of contents are missing, use Windows and Customize menus to restore standard toolbars and interface elements.
- For queries or problems with Surveyor, contact the helpdesk as advised in the manual.