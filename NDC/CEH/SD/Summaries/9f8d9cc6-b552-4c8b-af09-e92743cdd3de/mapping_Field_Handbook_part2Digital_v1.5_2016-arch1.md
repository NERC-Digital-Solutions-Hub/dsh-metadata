# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field protocol for the Glastir Monitoring and Evaluation project (GMEP) using the CS Surveyor extension in ArcMap.
  - Captures and edits habitat areas (polygons), point features, and linear features with rich attribute data to support data analysis, correlations, and future predictions.
  - Data sources include OS MasterMap, aerial photos, OS raster data; copying features between layers is supported to aid mapping.
  - Emphasises data provenance, traceability, and an auditable workflow; emphasizes scale constraints (mainly 1:5000) and the Minimum Mappable Unit (MMU).

- System and workflow overview
  - Platform: ArcMap with CS Surveyor extension; specialized “Habitats” task manager; data frame named Countryside Survey.
  - Users log in to CS Surveyor, which loads necessary data layers and pre-set symbology for consistent viewing/editing.
  - Workflows are organized around three feature types:
    - Areas (Landscape Areas)
    - Points (Landscape Points)
    - Lines (Landscape Lines)

- Using the Digital Mapping System (CS Surveyor)
  - Launch Sequence: Open ArcMap, start CS Surveyor, verify database path, and log in.
  - Interfaces: Table of Contents and Map Display; Surveyor adds its own menu within ArcMap.
  - Tools and capabilities: ArcMap navigation (zoom, pan, measure, go to XY, etc.) plus Surveyor-specific editing tools for areas, points, and lines.
  - Data management: Save and log off procedures; ensure changes are saved before ending sessions; CS Surveyor manages edits and metadata within each square.

- Mapping Polygons (Habitat Areas)
  - 2.1 Split
    - Create new polygons from a single 1km square polygon (simple split) or copy polygons from external layers (e.g., OS MasterMap).
    - Edit sketches with a stylus; ensure splits respect MMU; use red/blue hatch to indicate areas to be split; use doughnut polygons for internal cuts.
  - 2.1.1 Copying polygons from existing layers
    - Use Copy features toolbox to bring polygons from other layers into the edit sketch; add with Copy+ and adjust with vertex editing.
  - 2.2 Modify
    - Edit polygon boundaries with topology-aware tools; shared end nodes (shared nodes) edited via Special Modify tools.
  - 2.3 Merge
    - Merge multiple areas; choose a source area whose attributes may be copied; copied attributes overwrite existing attributes at area and component levels.
  - 2.4 Update
    - Create a new landscape area by updating intersections of polygons; can be digitised or copied from other layers; allows creation of new habitat polygons by copying, useful for unsurveyed squares.
  - 2.5 Attributes
    - Attributes cover broad/priority habitat, species, physiology, etc., with a focus on how attributes align with vegetation keys.
  - 2.5.1 Polygon Level Attributes
    - Area, Broad/Priority Habitat, BH Accuracy (e.g., Not previously surveyed for new squares), Reason for Change, Visit Status (In progress, Completed, Refused access).
  - 2.5.2 Component Level Attributes
    - Areas may have multiple components; components can be added, copied, or deleted. At least one component per area; primary vs. secondary attributes managed within components.
    - Themes and fields organize habitat attributes (e.g., AGRICULTURAL CROPS, FORESTRY, INLAND WATER, VEGETATION TYPES, Species, Cover, Sward characteristics, etc.).
  - 2.6 Copy Attributes
    - Copy attributes from a source area to one or more target areas; target areas become identical to the source in attributes (one source, many targets).
  - 2.7 Mapping change in CS squares
    - For repeat CS squares, surveyors confirm or adjust polygon attributes from previous surveys rather than focusing on exact spatial accuracy; provide reasons for changes and note any new baselines or not previously surveyed statuses.

- Freshwater Mapping and Ponds (4)
  - Pond attributes to record on Grid Square Inventory for Ponds form
    - For each pond: square reference, pond reference, full grid reference; area (m2) including MMU boundaries; water presence status; reasons for pond loss if mapped on base map but absent in field; notes on new ponds and creation reasons.
  - Overview and survey pond selection
    - In squares with multiple ponds, randomly identify a single survey pond after completing the grid square inventory for all ponds.
    - Use a PC tablet form to determine the survey pond via a lookup table; record pond sampled under Inland Water themes as appropriate (Areas or Points).
  - Process steps
    - Complete inventory for all ponds, assess coverage confidence, determine pond counts, select the survey pond, and record the survey pond attributes accordingly.

- Mapping Point Features (5)
  - 5.1 New
    - Add new points at scale 1:5000 or smaller; single point at a time; minimum distance from other points; default Unsurveyed/Missing Data component.
  - 5.2 Modify
    - Move an existing point; ensure scale constraint; one point at a time; maintain data integrity with a new position and updated attributes.
  - 5.3 Delete
    - Delete a point with a valid Reason for Change; must be at scale 1:5000 or less and single-point operations; mandatory reasons required for deletion.
  - 5.4 Attributes
    - Update point-level attributes; points may have multiple components; mandatory vs optional fields are indicated in the attribute editor.
  - 5.5 Copy Attributes
    - Copy attributes from one source point to one or more target points; one source, many targets; target points adopt source attributes after editing.

- Mapping Linear Features (6)
  - Background
    - Record linear features (min length 20m, max width 5m) unless part of curtilage or within woodland canopy; record along woodland edges; canals/rivers are treated as areas.
    - Each linear feature is represented as a single line with multiple events (Event Attributes) along its length (e.g., fences, walls, woody linear features).
  - 6.1 New
    - Create new lines on tablet; minimum 5.0m length; lines cannot cross themselves; one line at a time; new line starts with an Unsurveyed/Missing Data event.
  - 6.2 Modify
    - Edit line shape with vertex editing; shared node modification for end points; maintain topological integrity (no intersections from edits).
  - 6.3 Cut
    - Digitise cut polygons along a line to remove portions; shows cut length versus remaining length; supports copying features from OS MasterMap or other layers to refine the cut.
  - 6.4 Delete
    - Delete a line if all events have valid Reason for Change; special handling for Historic Features (no dedicated reason field in that theme).
  - 6.5 Reshape
    - Reshape lines by adding a reshape graphic that intersects the line at start and end; can reshape along an existing line or follow a copied boundary; ensures resulting line meets constraints.
  - 6.6 Checking Visit Status on Linear Features
    - Use Select By Attributes to identify unvisited lines (VISIT_STATUS = 0); then edit attributes for those lines as needed.
  - 6.7 Attributes
    - Edit event-level attributes along the line; events have From/To positions along the line; mandatory vs optional fields flagged; events must be at least 5.0m long.
  - 6.8 Copy Attributes
    - Copy events from a source line to target lines; one source, many targets; target lines adopt source events and attributes; ensure scale restriction for editing.

- Troubleshooting and best practices
  - Ensure you have the correct table of contents and toolbars in the ArcMap environment.
  - Save sessions regularly; ensure End Session or Save Session choices are properly used to commit changes.
  - Use the Copy Features tool and vertex editing to refine edits; manage shared nodes carefully to maintain topology.

- Data integrity and analyst-facing considerations
  - The handbook supports rigorous data capture, auditing, and attribute management to enable later statistical analysis, correlations, and predictive modeling.
  - Attribute schemas emphasize habitat classification keys, species, physiography, and other thematic attributes to support ecological analytics.
  - Copying attributes and events across features promotes consistency across large map areas, supporting reproducibility and comparability of datasets over time.
  - The workflow accommodates both new mapping efforts and quality checks against previous CS surveys, balancing spatial accuracy with habitat extent and attribute correctness.