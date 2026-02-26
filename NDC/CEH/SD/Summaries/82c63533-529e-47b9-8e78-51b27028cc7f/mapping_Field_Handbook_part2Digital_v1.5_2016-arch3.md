# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Provides the field protocol for the Glastir Monitoring and Evaluation project (GMEP) using the CS Surveyor GIS tool to map habitat areas, points, and linear features.
  - Aims to capture high-quality environmental health data to scrutinise policy and inform future decisions.

- System context and setup
  - CS Surveyor is an ArcMap extension customized for GMEP, enabling data capture for habitat areas, points, and lines without requiring extensive ArcMap expertise.
  - Data are organised in 1km grid squares; the mapping workflow emphasizes consistency, metadata visibility, and data governance at the source.
  - The workflow involves logging into the CS Surveyor extension within ArcMap, accessing a pre-configured data frame, and using predefined layers and symbologies.

- 1 Using the Digital Mapping System
  - ArcMap is the base GIS; Surveyor adds a dedicated Surveyor extension with a habitats task manager.
  - Users log in, and the map displays a Countryside Survey data frame with multiple layers (e.g., grids, historic features, landscape points/lines/areas, aerials, OS data).
  - Navigation and general GIS tools are provided (zoom, pan, identify, find, measure), plus specific Surveyor tools for editing habitat areas, points, and lines.
  - GPS use is optional but recommended to supplement contextual data; GPS accuracy varies by device.

- 2 Methodology for Mapping Polygons (Habitat Areas)
  - The polygon editing toolbox supports creating, splitting, modifying, merging, and updating landscape areas.
  - Split
    - New squares start with a simple split or by copying polygons from external layers (e.g., OS MasterMap).
    - Split sketches can be refined with vertex editing; doughnut polygons are supported for holes.
  - 2.1 Copying polygons from existing layers
    - Copy features from polygon layers (e.g., OS MasterMap) to create an edit sketch, then split.
  - Modify
    - Boundary edits use topology-aware editing; end vertices on shared boundaries cannot be edited here (use Shared Node Modify).
  - Merge
    - Merge multiple areas when their attributes are identical; attributes from a chosen source area can overwrite others.
  - Update
    - Create new areas by splitting existing polygons or by copying features; useful for previously unsurveyed squares and when new areas intersect existing ones.
  - 2.5 Attributes
    - Areas and components have detailed attribute schemes.
  - 2.5.1 Polygon Level Attributes
    - Include area, Broad/Priority habitat, BH Accuracy, Reason for change, and Visit status.
  - 2.5.2 Component Level Attributes
    - Areas may have multiple components; components can be added, copied, or deleted. Primary and secondary attributes (e.g., vegetation, species, physiography) are organized under themes.
  - 2.6 Copy Attributes
    - Copy attributes from a source area to one or more target areas; overwrites target attributes.
  - 2.7 Mapping change in CS squares
    - For repeating CS squares, surveyors confirm or adjust polygons and their polygon-level attributes against prior data; spatial accuracy is less critical than the representation of habitats.
  - Stop Editing and session handling
    - End editing by saving the session or discarding changes; ensure changes are saved regularly.
  - Log off
    - Properly log off CS Surveyor DB when finished.

- Pond inventory and freshwater mapping (4 Freshwater Mapping)
  - If a square contains ponds, complete a Grid Square Inventory for Ponds form for each pond, recording: square/pond references, pond area, presence/absence, reasons for loss (if marked present in base map but absent in field), new ponds, pond age and creation reasons, and any notes.
  - Overview and survey pond selection
    - A single pond per square is randomly selected as the survey pond after all ponds in the square are mapped.
    - The selection uses a PC tablet lookup table; the determined survey pond is recorded as Pond sampled in the appropriate Landscape feature (Areas or Points).
  - For ponds below the MMU or on square boundaries, area calculations may differ between tablet records and field measurements; ensure the comprehensive pond data is reconciled.
  - After selecting the survey pond, freshwater surveyors proceed with condition assessment independently of the grid inventory steps.

- 5 Methodology for Mapping Point Features
  - Points are landscape elements under 20x20 m; they can be added, moved, or deleted as needed.
  - 5.1 New
    - Add new point features at scale 1:5000 or smaller; one point at a time; must avoid placing within 5 m of an existing point; all new points start as Unsurveyed/Missing Data.
  - 5.2 Modify
    - Move existing points; scale constraint applies; moved points retain updated attributes; one at a time; maintain minimum distances.
  - 5.3 Delete
    - Delete only with a valid Reason for Change; one at a time.
  - 5.4 Attributes
    - Edit point attributes; points may have multiple components; components can be added, copied, or deleted; interface highlights mandatory vs optional fields.
  - 5.5 Copy Attributes
    - Copy attributes from a single source point to multiple target points; overwrites target attributes.

- 6 Methodology for Mapping Linear Features
  - Linear features are lines under 5 m wide with a minimum length of 20 m (can have up to 20 m gaps); represented as continuous lines with multiple events.
  - Background
    - Record linear features unless they form curtilage or lie entirely within woodland canopy; edges of woodland edges must be captured; canals/rivers appear as areas.
  - Recording events
    - Use Surveyor to create, cut, delete, modify, reshape lines, and edit event attributes along a line.
  - 6.1 New
    - Add new line with pen; minimum length 5 m; one line at a time; lines cannot extend outside the survey square; ends coded for events.
  - 6.2 Modify
    - Edit line shape via vertex edits; shared nodes can be modified via Shared Node Modify; ensure edits do not create intersections or invalid topologies.
  - 6.3 Cut
    - Digitise a cut along the line; shows lengths to be cut vs remaining; ensure final line meets minimum length.
  - 6.4 Delete
    - Delete a line only if all events have valid Reason for Change; some historic features require alternative handling.
  - 6.5 Reshape
    - Reshape by drawing along the line; two modes: reshape to align with a copied line or with a digitised path; maintain minimum length and topology integrity.
  - 6.6 Checking Visit Status
    - Use Select By Attributes to identify unvisited linear features and then edit their events/attributes accordingly.
  - 6.8 Copy Attributes
    - Copy events from a source line to one or more target lines; overwrites events/attributes on targets; one source, multiple targets.

- 7 Troubleshooting
  - If the Table of Contents or toolbars disappear, use the interface customization options to restore them (Table of contents, standard toolbars, zoom tools, etc.).

- Notes on data governance and accessibility
  - The handbook emphasizes reliable metadata, consistency across polygons/points/lines, and transparent attribute schemas to support monitoring frameworks.
  - Public sharing and data governance considerations are part of the workflow, necessitating careful management of underlying data and its attributes throughout edits and merges.