GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose and scope
  - Field mapping protocol for Glastir Monitoring and Evaluation (GMEP) using Surveyor within ArcMap.
  - Enables capturing, editing, combining, and attributing habitat polygons, lines, and points; supports creation of data products for end users.
  - Distinguishes between CS (countryside survey) squares and new squares; includes pond inventory and freshwater mapping components.

- Access and system overview
  - Use ArcMap with the CS Surveyor extension to edit data; log on with designated user credentials.
  - The interface comprises a map display and a table of contents with data frames and layers; surveyor tools are accessed via a dedicated Surveyor menu.
  - GPS may be used as an ancillary data source; avoid relying solely on GPS for mapping accuracy.

- Data model and general workflow
  - Data types: Areas (polygons), Lines (linear features), Points (point features); each type contains attributes and may have multiple components or events.
  - Basic workflow: edit sessions in Surveyor, use specific tools to Split, Modify, Merge, Update (areas); New/Modify/Delete/Attributes/Copy Attributes for points and lines.
  - Changes are saved via a structured edit session; regular saving is emphasized.

- Mapping Habitat Areas (polygons)
  - Split (2.1)
    - Create new polygons from a 1km square polygon; can be simple splits or doughnut (holes) polygons.
    - Can copy polygons from external layers (e.g., OS MasterMap) to form the edit sketch; final split requires an attribute pass.
    - If a fragment is below Minimum Mappable Unit (MMU), it is highlighted as invalid and can be redrawn.
  - Modify (2.2)
    - Adjust polygon boundaries using topology tools; shared boundary end points (shared nodes) are edited via Shared Node Modify.
  - Merge (2.3)
    - Merge multiple areas with identical attributes; attributes can be copied from a chosen source area to the merged polygon.
  - Update (2.4)
    - Create new areas by splitting and merging existing polygons or by copying from other layers; useful for unsurveyed squares or complex updates.
  - Attributes (2.5)
    - Polygon-level attributes: Area, Broad/Priority Habitat, BH Accuracy, Reason for Change, Visit Status.
    - Component-level attributes (2.5.2): add/copy/delete components; set primary/secondary attributes; ensure each area has at least one component.
    - Thematic grouping (Theme, Vegetation Type, Species, Cover, Qualifiers) supports efficient data entry on tablets.
  - Copy Attributes (2.6)
    - Copy attributes from a source area to target areas; target areas overwrite existing attributes.
  - Mapping changes in CS squares (2.7)
    - For CS squares, validate and update polygons against field observations; decide whether to change broad habitat or attributes; record Change Reason and BH Accuracy as appropriate.
  - Pond-related inventory (grid square ponds)
    - For squares containing ponds, complete the Grid Square Inventory for Ponds form for each pond; record square/pond references, area, presence, reasons for loss/creation, pond age, and creation reasons.
    - After mapping all ponds, identify the survey pond randomly and notify freshwater surveyors to perform condition assessments.
    
- Mapping Point Features (points)
  - New (5.1)
    - Add new point features only at scale 1:5000 or less; minimum 5m from existing points; assign an Unsurveyed/Missing Data component by default.
  - Modify (5.2)
    - Move points; preserve attributes; update when visit status is set to Completed.
  - Delete (5.3)
    - Delete points only if a valid Reason for Change exists.
  - Attributes (5.4)
    - Edit point attributes; each point may have multiple components; ensure mandatory fields are completed.
  - Copy Attributes (5.5)
    - Copy attributes from one source point to multiple target points; overwriting existing attributes accordingly.

- Mapping Linear Features (lines)
  - Background
    - Record linear features (minimum length 20m, max width 5m) as continuous lines with multiple events; large or composite features may be represented as a single line with multiple events.
  - New (6.1)
    - Create new lines within the square; minimum length adherence and no self-crossing; lines cannot be added outside the survey square.
  - Modify (6.2)
    - Edit line geometry by adding/moving/deleting vertices; handle shared nodes via Shared Node Modify; ensure edits do not create invalid intersections or shorten beyond minimum lengths.
  - Cut (6.3)
    - Digitise cut geometries along lines to remove sections; can copy polygons from other layers to assist with accurate cuts.
  - Delete (6.4)
    - Delete lines only if all events have valid Reasons for Change; some historic features may require alternate handling.
  - Reshape (6.5)
    - Reshape lines by drawing a reshape graphic that intersects the endpoints; save changes after editing.
  - Copy from other layers (6.6)
    - Copy relevant boundary or event geometry from external layers to support cuts or reshaping.
  - Checking visit status (6.6) [Note: labeled as 6.6 in document]
    - Use Select By Attributes to identify unvisited landscape events; update visit status and attributes as needed.
  - Copy Attributes (6.8)
    - Copy events from a source line to target lines; target lines gain the source line’s events and appearance after editing.

- Data management and exit procedures
  - Save Session regularly to ensure edits are captured; two exit options: Save Session (to commit changes) or End Session (to discard changes).
  - Log off from CS Surveyor DB when finished; close ArcMap as part of the exit process.

- Troubleshooting and support
  - Restore missing toolbars or table of contents via the Windows Customize options.
  - Contact helpdesk for Surveyor-specific queries and issues with the system.

- Practical tips for data quality and usability
  - Use OS MasterMap or other layers to speed up polygon creation via Copy Features.
  - Maintain a clear attribute record for changes (Reason for Change, Visit Status) to support audit trails.
  - Ensure scale constraints (primarily 1:5000 or better) are respected for editing points, lines, and attributes.
  - Coordinate pond inventory and survey pond selection with freshwater surveyors to streamline downstream condition assessments.