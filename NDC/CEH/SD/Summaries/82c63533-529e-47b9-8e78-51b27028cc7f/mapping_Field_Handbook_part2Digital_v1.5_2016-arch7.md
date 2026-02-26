# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Overview and purpose
- Field protocol for Glastir Monitoring and Evaluation (GMEP) mapping using the CS Surveyor extension within ArcMap.
- Surveyors edit and manage habitat polygons (areas), point features, and linear features across 1 km grid squares.
- Emphasizes data quality, reuse of existing layers (e.g., OS MasterMap), and consistent attribute schemas.

## Access, setup, and interface
- Software: ArcMap with CS Surveyor extension; CS Surveyor added as a menu in ArcMap.
- Logging in: use provided usernames/passwords to access the Surveyor extension and the CS Surveyor database.
- Data frame: a Countryside Survey data frame holds layers with pre-set symbology for visibility.
- Tools: navigation (zoom/pan, go to XY, measure), identify, find, and data copy utilities are available; GPS can be initiated as needed.
- Scale requirement: editing generally requires a map scale of 1:5000 or better.

## Using the CS Surveyor workflow
- Always start and end edit sessions via the Landscape Feature Editing toolbox; save regularly.
- CS Surveyor edits affect three feature types: Areas (habitat polygons), Points (point features), and Lines (linear features).

## 2 Methodology for Mapping Polygons (Habitat Areas)

### 2.1 Split
- Create polygons from a single 1 km square (new squares) or by copying polygons from external layers (e.g., OS MasterMap).
- Split process: digitise the new area with the split tool; use sketch/drawing with vertex editing to define the split.
- Validation: minimum polygon size MMU may trigger red highlights; if large enough, proceed to input attributes for each split part.

### 2.1.1 Copying polygons from existing layers
- Copy polygons from a source layer (e.g., OS MasterMap) via Copy features toolbox; add features to the edit sketch with Copy+.
- Complete split; areas to be split show with outlines and hatch patterns; attributes are entered in the attribute editor.
- You can copy multiple features; each new area retains editable attributes.

### 2.2 Modify
- Modify boundaries between polygons using topology edit tools; shared boundary end-points (shared nodes) are edited via Shared Node Modify.
- Edits include moving vertices and adjusting the boundary; save changes to apply.
- After modification, attributes are edited per area/part.

### 2.3 Merge
- Merge selected areas when attributes are identical; select target areas and choose a source area to copy attributes from.
- Attributes from the chosen source overwrite existing attributes on both area and component levels.

### 24 Update
- Create a new landscape area by splitting existing polygons or by copying polygons from other layers, then merging as needed.
- Useful for adding new habitat polygons that intersect existing areas; can handle sub-MMU updates.
- Update polygon intersects highlight affected areas; after final shape, input updated attributes.

### 25 Attributes
- Attributes cover broad/priority habitat, habitat type, species, physiography, etc.
- Polygon level attributes include area, BH (Broad/ Priority Habitat), BH accuracy, reason for change, and visit status.
- The themes and fields (e.g., Agricultural Crops, Forestry, Inland Physiography) guide attribute selection.

### 25.1 Polygon Level Attributes
- Set area, select Broad or Priority habitat, set BH accuracy (e.g., Not previously surveyed for new squares), and reason for change.
- Visit status options: In progress, Completed, Refused access.

### 25.2 Component Level Attributes
- Areas may contain multiple components; components can be added, copied, or deleted.
- To modify, select all components with the same primary attribute to change primary attributes; otherwise adjust secondary attributes.
- Ensure each area has at least one component.

### 26 Copy Attributes
- Copy attributes from a source area to one or more target areas via Copy Attributes.
- Only one source allowed; multiple targets can receive attributes; overwritten attributes apply to area and component levels.

### 27 Mapping change in CS squares
- For repeating CS squares, surveyors confirm or adjust polygons and attributes from previous surveys.
- Emphasizes updating polygon-level attributes; spatial accuracy is less critical than accurate extent and attribute representation.
- Use “Error change” and the provided codes to record where necessary.

## 4 Pond mapping and grid square inventory (Freshwater Mapping)

### Recording ponds in grid squares
- For squares with ponds, complete a Grid square inventory for ponds form (PC tablet) for every pond.
- Attributes to record per pond:
  - Square reference, pond reference, and full grid reference.
  - Pond area (max winter water level) in m²; note if below MMU but within square boundary.
  - Is the pond present? Yes/No (dry mud = No).
  - If present in base map but absent in field, record reason (L, I, B, O, U).
  - If not marked on base map, indicate new pond and age (up to ~10 years) with creation reasons (F, S, W, L, G, X, O, U).
  - Additional notes as needed.
- Determining the survey pond: randomly select from all ponds in the square using a lookup table; record the pond as the survey pond via the “Pond sampled” attribute in the Landscape Features toolbox.
- After all ponds are recorded, provide survey pond details to freshwater surveyors for condition assessment.

### Overview and workflow
- One survey pond per square, randomly selected from all ponds in the square after inventory is complete.
- Process is designed to ensure unbiased sampling and consistent data capture for pond condition surveys.

## 5 Methodology for Mapping Point Features

### 5.1 New
- Points are for features under 20x20 m; add one point at a time at scale 1:5000 or better.
- Create new point at map location; relocate if needed; enter attributes; each new point starts with a single Unsurveyed/Missing Data component.
- Points must not be within 5 m of an existing point.

### 5.2 Modify
- Move an existing point; maintain the point’s component structure; editing scale remains at 1:5000 or better.
- After moving, update attributes; completed status changes the point’s appearance on refresh.

### 5.3 Delete
- Delete a point with a valid Reason for Change; points lacking valid change reasons cannot be deleted.

### 5.4 Attributes
- Edit point attributes; points may have multiple components; add/copy/delete components as needed.
- Ensure completed status is set; changes reflect in map upon refresh.

### 5.5 Copy Attributes
- Copy attributes from a source point to target points; multiple targets allowed.
- Only one source point; target points are updated to match the source attributes.

## 6 Methodology for Mapping Linear Features

### Background
- Linear features are elements less than 5 m wide, forming lines; minimum length 20 m; maximum width 5 m.
- Record along lines with events (e.g., fences, walls, woody features). If a line’s width or length changes to create a larger area, use a polygon as a wide linear feature.

### Recording Events
- Use Surveyor to create, cut, delete, modify, reshape lines, and edit events along lines.
- If a step change occurs along a feature, code the segment as a new event with its own attributes.
- Edit lines via the Lines tab in the Landscape Feature Editing toolbox.

### 6.1 New
- Add a new line (min 20 m); draw with pen; vertices can be refined; initial event is Unsurveyed/Missing Data over entire length.
- Editing scale must be 1:5000 or less; lines cannot extend beyond the square; lines cannot self-cross.

### 6.2 Modify
- Modify by editing the line’s shape; use vertex editing; shared nodes edited through Shared Node Modify.
- Ensure edits do not produce invalid lines or violate minimum length constraints.

### 6.3 Cut
- Cut a line by digitising a cut polygon along the line; show the cut and remaining lengths; refine with vertex editing if needed.
- Multiple cuts possible; validate length constraints.

### 6.4 Delete
- Delete a line; lines with events lacking valid Reason for Change cannot be deleted.

### 6.5 Reshape Line
- Reshape by drawing a reshape graphic along the target line; edits applied to the affected segment.
- Use reshape tool to adjust start/end intersections; validate length.

### 6.6 Checking Visit Status on Linear Features
- Use Select By Attributes to identify unvisited Landscape Events; highlight unvisited lines for follow-up attribute editing.

### 6.7 Attributes
- Edit event attributes; line-level attributes (length) and event-level attributes are editable.
- Mandatory fields are highlighted; map must be at 1:5000 or better to edit; each line must have at least one event; events minimum length 5 m.

### 6.8 Copy Attributes
- Copy events from a source line to target lines; only one source line; multiple target lines allowed.
- Target lines adopt the source line’s attributes and events; ensure consistency after editing.

## 7 Troubleshooting
- If Table of Contents or toolbars are lost, use the Windows menu or Customize options to restore them.
- Specifically re-enable missing toolbars (e.g., Standard, Zoom/Navigation) via the Customize/Toolbars menus.

## Troubleshooting and workflow reminders (general)
- Regularly save sessions to prevent loss of edits.
- End sessions to discard unwanted edits; Save Session to commit changes.
- Log off CS Surveyor DB when finished.
- Use the Copy and Paste features thoughtfully to leverage existing polygons and ensure consistent attribute propagation.