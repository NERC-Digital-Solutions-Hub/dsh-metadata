# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose: Outline the field protocol for mapping habitat areas, ponds, points, and linear features in the Glastir Monitoring and Evaluation Programme using the CS Surveyor extension within ArcMap; aims to capture data, manage attributes, and support reproducible analyses.

- System and Access
  - Surveyor is an ArcMap extension developed for CS, customized from Forestry Commission and ESRI tools.
  - Requires logging into CS Surveyor with provided usernames/passwords; data is loaded into a 1 km square framework under a Countryside Survey data frame.
  - Tools and data are organized in ArcMap; specific navigation, editing, and data management commands are described.
  - Save/Exit process: changes are only saved via the Save Session option; logging off ends the session and closes ArcMap.

- Data Structure and Sources
  - Work is conducted on 1 km grid squares (CS squares) within a square-based mapping framework.
  - Data layers include Landscape Areas, Landscape Points, Landscape Lines, and related OS MasterMap, aerial, OS raster data, and other base maps.
  - Copying from external layers (e.g., OS MasterMap) is supported to speed polygon creation and edits.
  - Emphasis on maintaining data provenance, with attributes and components tracked at polygon/area or line/point level.

- Mapping Polygons (Habitat Areas)
  - 2.1 Split
    - Create new polygons from a 1 km square polygon via freehand splits or by copying polygons from external layers.
    - MMU constraints and editing using a sketch/digitising approach; support for doughnut polygons (holes).
    - Attribute editor opens after split; area components can be attributed or copied.
  - 2.2 Modify
    - Modify boundaries using a topology-aware tool; changes reflect on shared boundary nodes (Shared Nodes Modify).
    - Edges, vertices, and boundary adjustments are supported; attribute editors open post-edit.
  - 2.3 Merge
    - Merge multiple areas only when their attributes match; can copy attributes from a chosen source area to merged area.
  - 2.4 Update
    - Create new areas by splitting and merging existing polygons, or by copying from other layers; useful for previously unsurveyed squares and areas smaller than MMU.
  - 2.5 Attributes
    - Polygon-level and component-level attributes include Broad/Priority habitat, vegetation type, species, physiography, etc.
    - Polygon-level: area, BH/PH, BH accuracy, reason for change, visit status; defaults provided.
    - Component-level: multiple components per area; attributes edited in the Landscape Areas Attribute Editor; components can be added, copied, or deleted.
    - Thematic grouping (themes) aids attribute selection (e.g., agricultural crops, forestry, inland physiography, vegetation, species, cover, sward characteristics).
  - 2.6 Copy Attributes
    - Copy attributes from a source area to one or more target areas; only one source, many targets; targets overwrite existing attributes.
  - 2.7 Mapping change in CS squares
    - For repeating CS squares, surveyors review existing polygons against field observations rather than spatial coordinates; focus on polygon-level attributes and BH accuracy.
    - Record changes with defined reasons for change and update BH accuracy and related fields accordingly.
  - End-of-session: after mapping edits, save and log off; confirm changes or discard if End Session is chosen.

- Ponds (Grid Square Inventory)
  - If ponds exist in a square, complete a Grid square inventory for ponds form for each pond.
  - Attributes collected include square reference, pond reference, area, presence/absence of water, reasons for loss if absent, whether newly created, age, and creation reasons.
  - After recording all ponds, identify the survey pond randomly from the inventory using a lookup table, and mark it as “Pond sampled” for condition assessment by freshwater surveyors.

- Methodology for Mapping Point Features
  - Points are features under 20x20 m; includes trees, standing water bodies, ponds, etc.
  - Editing tasks require zooming to 1:5000 or less; points cannot be added within 5 m of another point.
  - 5.1 New: create new points; enter attributes; one point at a time.
  - 5.2 Modify: move points; maintain attributes; completed status changes point appearance.
  - 5.3 Delete: delete points with valid Reason for Change; scales restricted to 1:5000 or less.
  - 5.4 Attributes: edit point attributes; points may have multiple components.
  - 5.5 Copy Attributes: copy attributes from a source point to multiple target points.

- Methodology for Mapping Linear Features
  - Linear features are lines up to 5 m wide, minimum length 20 m; may contain gaps up to 20 m.
  - All linear features unless part of curtilage or within woodland canopy; edge-of-woodlands lines must be recorded.
  - Represented as continuous lines with multiple events; events describe components along the feature.
  - 6.1 New: add new line with pen, ensure minimums; typically one Unsurveyed/Missing Data event covering length.
  - 6.2 Modify: edit shape via vertices; shared nodes also editable via Shared Node Modify.
  - 6.3 Cut: digitise cut polygons to remove sections; length previews shown; multiple cuts allowed; still requires minimum lengths.
  - 6.4 Delete: delete lines with valid Reason for Change across events.
  - 6.5 Reshape: reshape lines by drawing a reshape graphic; two variants for reshaping following existing or copied lines.
  - 6.6 Checking Visit Status: use Select By Attributes to identify unvisited lines and then edit events/attributes.
  - 6.7 Attributes: manage line-level and event-level attributes; event length and positions are adjustable; scale constraint 1:5000.
  - 6.8 Copy Attributes: copy events from a source line to target lines; targets adopt copied events and attributes.

- Troubleshooting and Tips
  - If toolbars or table of contents are lost, use the Windows customization and Table of Contents options to restore.
  - General guidance on navigating the Surveyor interface and maintaining workflow continuity.

- Practical Constraints and Workflow Notes
  - All edits are governed by scale constraints (1:5000 or smaller) and minimum feature sizes.
  - Data integrity is enforced through stepwise saving, explicit reason-for-change values, and validation of mandatory fields before delete or modification.
  - The workflow emphasizes data provenance, cross-layer copying, and updating attributes to reflect ground observations.
  - Differences between new CS squares and repeating CS squares are handled via emphasis on polygon-level attributes and careful review of previous survey data.