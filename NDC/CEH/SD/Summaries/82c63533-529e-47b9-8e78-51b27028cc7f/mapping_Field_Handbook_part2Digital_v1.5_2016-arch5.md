# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field protocol handbook for the Glastir Monitoring and Evaluation Programme (GMEP) describing how to map using the CS Surveyor software within ArcMap.
  - Provides instructions for data capture, editing, attributes, and workflow to support consistent, auditable datasets.

- System and access
  - Surveyor is an ArcMap extension customized for CS Surveyor workflow; login is required to access survey squares.
  - The interface includes a Countryside Survey data frame and a pre-set layer symbology for visibility and usability.

- Data model and attributes
  - Data are organized as Landscape Features: Areas (polygons), Points, and Lines, each containing one or more components and associated events/attributes.
  - Attributes are defined at two levels:
    - Polygon (Area) level: area, Broad or Priority habitat (BH/PH), BH accuracy, reason for change, and visit status (In progress, Completed, Refused access).
    - Component level: multiple components per area with ability to copy or modify attributes; themes group related attributes (e.g., agricultural crops, vegetation, coastal features, forestry, inland water, structures, transport, wide linear features, unsurveyed/missing data).
  - Event-level attributes exist for linear features; copy and edit operations apply to events as well as lines.

- Working with polygons (Areas)
  - Split
    - Create polygons from a single 1km square polygon; can draw freehand or copy from external layers (e.g., OS MasterMap).
    - Simple split vs. doughnut polygons; MMU constraints apply (small pieces highlighted in red).
  - Modify
    - Edit boundaries between polygons; use topology edit tools; shared boundary end-points (shared nodes) edited via Shared Node Modify.
  - Merge
    - Merge multiple areas when attributes are identical; can copy attributes from one area to the merged polygon; overwritten at both area and component levels.
  - Update
    - Create new areas by splitting and merging; can copy areas from other layers; useful for previously unsurveyed squares.
    - Can handle updates that intersect multiple existing areas; updated areas may include Unsurveyed/Missing Data components if no source area is selected.
  - Attributes
    - Polygon-level attributes include area, Broad/Priority Habitat classification, BH accuracy (default for new squares is Not previously surveyed), reason for change, and visit status.
    - Component-level attributes allow multiple components; can add, copy, delete components; copy attributes between areas.
  - Copy Attributes
    - Copy attributes from a source area to one or more target areas; overwrites existing attributes at both area and component levels.
  - Mapping changes in CS squares
    - For repeating CS squares, surveyors confirm or adjust attributes (polygon-level BH accuracy and related attributes) rather than focusing on precise geometry; emphasis on ensuring attributes reflect field observations.

- Working with existing data and sharing
  - Copying from existing layers (e.g., OS MasterMap) speeds polygon creation and editing.
  - Copy attributes and copy events enable consistent attribute propagation across multiple areas or lines.
  - Changes are logged within the edit session; saving is required to persist edits.

- Working with points (Point Features)
  - New, Modify, Delete, Attributes, Copy Attributes
  - Points are features smaller than 20x20 m; spatial accuracy is not critical but allowed where needed.
  - Edits require scale 1:5000 or less; points cannot be added or moved within 5 m of an existing point; points are created with a single Unsurveyed/Missing Data component.
  - Points can have multiple components; components can be added, copied, or deleted; attribute editing follows the point-level workflow.
  - Copy Attributes allows transferring attributes from a source point to multiple target points.

- Working with linear features (Lines)
  - Linear features (minimum length 20 m, maximum width 5 m) are recorded as lines with multiple events (e.g., fences, walls, woody linear features).
  - For lines wider than a threshold or where multiple components occur, a single line may hold multiple events.
  - Editing tools are used to add, modify, cut, delete, reshape, and copy features:
    - New: draw a new line; minimum length requirement; lines cannot be added outside the survey square; one line at a time; each new line starts as an Unsurveyed/Missing Data event.
    - Modify: adjust line geometry; shared nodes edited via Shared Node Modify; end-point vertices cannot be edited in this step.
    - Cut: digitise cut polygons along a line; shows length to be cut vs. remaining length; multiple cuts allowed if valid.
    - Delete: remove a line; requires valid Reason for Change for each event; historic features may require alternative handling.
    - Reshape: modify lines by drawing a reshape graphic; supports reshape along copied lines or existing boundaries; length constraints apply.
  - Copy from other layers
    - Use copy features to bring in lines or polygons from other layers (e.g., OS MasterMap) to support accurate editing.
  - Attribute editing and events
    - Each line contains events with attributes; event lengths are adjustable; mandatory fields are highlighted; length constraints exist (minimum 5 m per event).
  - Checking visit status
    - Use Select By Attributes to identify lines with unvisited status (VISIT_STATUS = 0) and edit events as needed.
  - Copy Attributes
    - Copy attributes and events from a source line to target lines; overwrites target line attributes and events as appropriate.

- Pond inventory and survey ponds
  - Grid square inventory for ponds form (PC tablet) required for every pond in a square.
  - Attributes to record per pond include: square reference, pond reference, fullest grid reference, pond area (mmu considerations), presence of water, reason for loss if absent from field, whether pond is new or previously unmapped, approximate age, and creation reasons (e.g., fishing, shooting, wildlife, golf, ornamental).
  - After mapping all ponds in a square, identify a survey pond for condition surveys using a lookup table; record pond sampled as a primary attribute under Inland Water in the Landscape Features toolbox.

- Session management and workflow
  - At the end of editing, choose Save Session to persist changes; End Session discards changes.
  - CS Surveyor saves all changes and returns to the main ArcMap screen; log off from CS Surveyor DB when finished.
  - Regular saving is advised to avoid data loss; the process creates an auditable trail of edits.

- Troubleshooting and customization tips
  - If toolbars or the Table of Contents are lost, use the Windows/Customize options to restore them.
  - Map display and layer properties can be adjusted (transparency, drawing order, show at all scales) to improve usability.

- Data governance implications for Data Stewards
  - The handbook establishes clear data standards for geometry (areas, points, lines), attributes (habitat classifications, accuracy codes, visit status), and change management (Reason for Change, Unsurveyed/Missing Data, etc.).
  - Emphasizes auditability through explicit edit sessions, mandatory fields, and explicit save/end session controls.
  - Encourages reuse of existing data layers (e.g., OS MasterMap) to promote consistency and interoperability.
  - Defines workflow constraints (scale thresholds, minimum feature lengths, shared node handling) to ensure data quality and comparability across surveys and squares.
  - Provides structured procedures for updating previously collected data, including how to handle repeats and how to record changes in a standardized way.
  - Includes specialized forms (pond inventory) to capture habitat-specific data and ensure comprehensive metadata capture for water-related features.
  - Supports data governance goals of discoverability, standardization, and up-to-date, usable datasets across large dataset collections.