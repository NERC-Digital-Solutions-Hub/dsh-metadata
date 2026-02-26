# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

- Purpose: Provides field mapping protocol for Glastir Monitoring and Evaluation using the CS Surveyor extension within ArcMap to capture habitats, ponds, and linear features; outlines editing, attributes, and data quality processes.

## Getting started and system overview
- System: ArcMap GIS with CS Surveyor extension; data stored in a Countryside Survey data frame with pre-set symbology.
- Access: Log on to CS Surveyor within ArcMap using provided usernames and passwords; hit Save Session regularly to preserve work.
- Landscape data: Layers include Landscape Areas (polygons), Landscape Points (points), Landscape Linears (lines), plus base map data (OS MasterMap, aerials, etc.).
- Scale and precision: Editing typically requires map scale of 1:5000 or finer; GPS use and multiple data sources (aerials, OS maps) supplement field data.

## Core data model and workflow
- Data objects:
  - Polygons: Habitat areas with polygon-level and component-level attributes (habitat type, species, physiography, etc.).
  - Points: Small features (<20x20 m) with one or more components and attributes; can be added, moved, deleted, and copied.
  - Lines (linear features): Features <5 m wide, represented as continuous lines with multiple events; have attributes per event.
- Editing philosophy: Work within edit sessions; use provided tools to split, modify, merge, update polygons; create/update points and lines; copy attributes/events between features; ensure consistency and metadata.
- Metadata and attributes: Attribute editing includes habitat codes (Broad/Priority), BH accuracy, reason for change, visit status, and component-level attributes; themes organize fields (e.g., agricultural, vegetation types, species, sward characteristics).

## Working with Polygons (Habitat Areas)
- 2.1 Split: Create new polygons from a 1 km square; can freehand digitise or copy polygons from existing layers (e.g., OS MasterMap); create doughnut polygons if needed.
- 2.2 Modify: Edit shared boundaries and vertices; modify using topology edit tools; shared nodes edited via Shared Node Modify.
- 2.3 Merge: Combine multiple polygons into one; attributes can be copied from a chosen source area to the merged area.
- 2.4 Update: Create or shape new polygons by digitising or copying from other layers; can be used for polygons intersecting multiple areas; can include small polygons below MMU.
- 2.5 Attributes: Polygon-level and component-level attributes; BH (Broad/Priority habitat), accuracy, reason for change, and visit status; themes and fields aid habitat/type selection.
- 2.6 Copy Attributes: Copy attributes from a source polygon to multiple target polygons; overwrites target attributes.
- 2.7 Mapping changes in CS squares: For repeat CS squares, review existing polygons, confirm or adjust attributes rather than focusing on exact spatial accuracy; mark issues with BH accuracy, attributes, and reason for change.

## Working with Points (Point Features)
- 5 Methodology for Mapping Point Features: Points include trees, standing water, ponds, etc.; spatial accuracy not primary but can be adjusted when necessary.
- 5.1 New: Add a new point at a scale 1:5000 or finer; ensure minimum distance from other points (5 m); assign initial Unsurveyed/Missing Data component.
- 5.2 Modify: Move an existing point; retain attributes; ensure moves are permissible at scale ≤1:5000.
- 5.3 Delete: Delete a point only if a valid Reason for Change exists.
- 5.4 Attributes: Update point attributes and components; mandatory/optional fields indicated; multiple components per point allowed.
- 5.5 Copy Attributes: Copy attributes from a source point to one or more target points; overwrites target attributes.

## Working with Linear Features (Lines)
- 6 Methodology for Mapping Linear Features: Record lines >=20 m in length and <=5 m wide; lines may contain multiple events (e.g., fences, hedges, woody features).
- 6.1 New: Create new line with a pen; minimum length 5 m per line; use vertex editing to refine; one line per action; lines cannot cross themselves.
- 6.2 Modify: Edit line shape and vertices; shared nodes edited via Shared Node Modify; ensure edits do not create invalid intersections or shorten below minimums.
- 6.3 Cut: Digitise a cut polygon along a line to remove a section; use copy features from other layers to improve accuracy; multiple cuts allowed but each must meet minimums.
- 6.4 Delete: Delete a line if each event has a valid Reason for Change; some historic features require alternative handling.
- 6.5 Reshape: Redraw a line by reshaping with a drawn graphic; supports reshaping to follow another feature or a copied line.
- 6.6 Checking Visit Status: Use Select by Attributes to identify unvisited linear features; update visit status and attributes accordingly.
- 6.7 Attributes: Edit line-level attributes and per-event attributes; events have mandatory/optional fields; length editing via map or editor.
- 6.8 Copy Attributes: Copy events from a source line to target lines; overwrites target events and attributes; one source, many targets.

## Ponds inventory and survey process
- If a square contains ponds, complete a Grid square inventory form for each pond (PC tablet) with:
  - Square reference, pond reference, and precise grid reference.
  - Pond area (max winter water level) and whether pond contains water (even if currently dry).
  - Reason for pond loss when present in base map but absent in field (L, I, B, O, U).
  - New ponds: indicate if not on base map and, if newly created (≤10 years), reason for creation (e.g., fishing, shooting, wildlife, golf, ornamental).
  - Randomly select a survey pond from mapped ponds for condition assessment; record the Pool Pond sampled attribute accordingly.
- Overview: Only one pond per square is sampled; selection depends on having fully mapped ponds in the square.

## Saving, exiting, and data integrity
- End-of-session options: Save Session to commit edits; End Session to discard changes; CS Surveyor saves all changes on exit.
- Log off: Use CS Surveyor DB logoff to close the session properly.
- Data integrity cues: Areas and lines require valid Reason for Change for edits to be saved; unsurveyed/missing data components indicate gaps.

## Practical considerations and tips
- GPS and field data: Use GPS alongside contextual data (aerials, OS MasterMap) to improve mapping; GPS accuracy can vary between devices.
- Data management: Be mindful of MMU thresholds, polygon/line length requirements, and the need to copy attributes or features from existing layers to save time.
- Visualization: Adjust layer transparency and drawing order to ensure important features are visible; OS Master Map polygons can be copied for rapid editing.
- User guidance: If problems arise with Surveyor, contact helpdesk; common issues include lost toolbars or tables of contents, which can be restored via customization and standard toolbars.

## Troubleshooting
- Restore Table of Contents or toolbars via Windows/customize options.
- Ensure edit sessions are saved frequently to prevent data loss.