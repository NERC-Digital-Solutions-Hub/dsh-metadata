# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Purpose and scope
- Provides the mapping field protocol for the Glastir Monitoring and Evaluation project using the Surveyor software integrated with ArcMap.
- Defines workflows for capturing, editing, and updating polygon (areas), point, and linear feature data within CS survey squares.
- Emphasizes data integrity, standardised attributes, and procedures to ensure datasets are consistent, up-to-date, and usable for analysis and discovery.

## System context and data model
- Surveyor is a specialised extension within ArcMap for capturing CS/GMEP data, built on an ESRI framework.
- Data are organized into three feature types:
  - Areas (polygons) with polygon-level and component-level attributes.
  - Points (point features) with point-level attributes and components.
  - Lines (linear features) comprising multiple events along a continuous line.
- Primary interfaces and data organization:
  - ArcMap with CS Surveyor extension; a Countryside Survey data frame holds layers and symbology.
  - Attribute editing and event management are theme-driven (e.g., Broad/Priority Habitat, vegetation types, species, physiography).
- Data capture is performed within 1 km square CS Surveyor extents, with explicit handling of updates, splits, merges, and copy operations across layers.

## Data capture workflow by feature type

### Areas (Polygons)
- Primary operations: Split, Modify, Merge, Update.
- Split: create new polygons from a 1 km square; can digitise freehand or copy polygons from external datasets (e.g., OS MasterMap). Supports doughnut polygons and complex splits.
- Modify: adjust shared boundaries or shared nodes; topology rules restrict editing ends of shared boundaries to Shared Node Modify.
- Merge: combine multiple areas, with attributes copied from a chosen source area.
- Update: create new polygons by splitting and merging; can copy from other layers and handle areas smaller than the Minimum Mappable Unit (MMU).
- Attributes:
  - Polygon-level: area, Broad/Priority habitat, BH accuracy (e.g., 98 for allocation), reason for change, visit status (In progress, Completed, Refused access).
  - Component-level: multiple components per area; components can be added, copied, or deleted; primary/secondary attributes organized by themes (e.g., agricultural crops, forestry, inland physiography, vegetation types, species, cover).
  - Copy Attributes: copy from a source area to one or more target areas (overwrites existing attributes).
- Mapping changes for CS squares: for repeating squares, surveyors verify and adjust attributes rather than exact locations; emphasis on habitat classification changes and data accuracy.

### Points
- New, Modify, Delete, Attributes, Copy Attributes.
- Scale requirement: map must be at 1:5000 or less to edit points.
- New points: created one at a time; minimum distance of 5.0 m from existing points; default Unsurveyed/Missing Data component.
- Modify: relocate points; maintain attributes; changes reflected after saving.
- Delete: requires valid Reason for Change; points without it cannot be deleted.
- Attributes: point-level attributes with one or more components; mandatory/value fields are indicated; completed edits reflect in map upon refresh.
- Copy Attributes: copy attributes from a source point to multiple target points; overwrites target attributes.

### Linear features (Lines)
- Linear features must be at least 20 m long; maximum width 5 m.
- Recording approach: lines are stored as continuous features with multiple events along their length (events carry attributes).
- Editing tools in the Lines toolbox: New, Modify, Cut, Delete, Reshape, Copy from other layers; shared nodes editing via Shared Node Modify.
- New: draw lines with the pen, refine via vertex editing; initial event is Unsurveyed/Missing Data; must be at 1:5000 or less; cannot cross survey square boundaries; length constraints enforced.
- Modify: edit line shape or shared nodes; ensure edits do not create self-intersections or invalid topologies.
- Cut: digitise a cut along the line to remove a segment; supports copying from OS MasterMap for precision; multiple cuts possible.
- Delete: removes line and all its events; requires valid Reason for Change on all events.
- Reshape: edit an existing line by drawing a reshape graphic; must intersect the target line at start and end; enforce minimum length rules.
- Copy Attributes: copy events from a source line to target lines; overwrites attributes on target lines; affects all events along the lines.
- Checking visit status for lines: use Select By Attributes to identify unvisited lines (VISIT_STATUS = 0) and update attributes per event as needed.
- Event attributes: each line can contain multiple events with attributes; line-level attributes control overall properties, while event-level attributes describe segment-specific details.

## Data quality, governance, and provenance considerations
- Metadata and attribute standards are embedded in the editing toolbox (themes, attributes, and event structures) to ensure consistency across squares and surveys.
- Key fields and codes:
  - BHPH and habitat classifications with accuracy indicators; reasons for changes (e.g., Error change, No change, Real change, Not previously surveyed).
  - Visit status indicators at polygon and event levels to track data completeness.
  - Reasons for change and rules guiding updates to maintain a clear audit trail.
- Data provenance through copy operations:
  - Copy Attributes and Copy Events enable efficient propagation of attributes/events but overwrite existing data, necessitating careful review per target feature.
  - Use of external layers (e.g., OS MasterMap) to support edits; copying is allowed but with exclusions where required.
- Data validation and field procedures:
  - Minimum polygon length, minimum line length, and non-crossing constraints enforce data integrity.
  - For repeating CS squares, emphasis on attribute verification and habitat classification rather than precise spatial perfection.
- Ponds and grids:
  - Grid square inventory form for ponds captures pond-level data and flow into the condition survey; includes pond presence, area, water presence, reasons for loss, creation, and age.
  - A single survey pond is selected per square from all mapped ponds using a lookup in the Grid square inventory form.

## Data management, workflow controls, and session management
- Logging in and using the CS Surveyor extension is required; session state and data saving are explicit:
  - Save Session must be used to persist edits; End Session discards edits.
  - CS Surveyor DB can be logged off from within ArcMap; unsaved ArcMap documents prompt a save decision.
- Map scale and workflow controls:
  - Editing of points and lines constrained to 1:5000 or less.
  - Editing operations restricted to features within the current square; cross-square edits are not permitted.
- Troubleshooting and guidance:
  - If toolbars or ToC are lost, use the Windows customization and Table of Contents recovery steps.
  - Access to helpdesk is recommended for queries about the Surveyor system.

## Particular challenges highlighted
- Incomplete understanding of user needs or priorities for certain datasets.
- Timely access to data from data creators; ensuring metadata and standardization across diverse data sources.
- Managing data across multiple formats and systems (e.g., OS MasterMap, ArcMap, Surveyor) with bespoke adaptations.
- Handling large datasets and complex edits (especially in areas with many features, or when dealing with SD edges and urban cores).

## Endnotes and supplementary procedures
- Pond inventory and survey workflow provides a structured approach to selecting and recording a survey pond, including reference numbers, area, presence, and creation reasons.
- The document includes detailed step-by-step procedures for each operation, including how to use the provided tools, how to view and edit attributes, and how to manage session termination and data saving.