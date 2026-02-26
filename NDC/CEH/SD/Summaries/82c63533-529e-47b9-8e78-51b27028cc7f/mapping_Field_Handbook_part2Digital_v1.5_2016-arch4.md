# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 2: using Surveyor software

## Overview and purpose
- Field protocol handbook for GMEP mapping using the CS Surveyor extension in ArcMap.
- Enables capture and management of habitat polygons (areas), point features, and linear features (lines) across 1 km squares.
- Provides guidance on editing sessions, data attributes, and updates over time to support consistent data across the monitoring programme.
- Emphasises verification of data against field observations, spatial constraints, and systematic attribute recording.

## System, access, and workflow
- Uses ArcMap with the CS Surveyor extension; login required to access the survey square and data layers.
- Data are organized in a Countryside Survey data frame; editing happens within CS Surveyor sessions.
- Important data workflow controls: start an edit session (E), set schema (M), perform edits, then Save Session or End Session; log off when finished.
- Data quality and provenance are enforced through:
  - Minimum mapping unit (MMU) considerations.
  - Mandatory and optional attribute fields, Reasons for Change, and Visit Status.
  - Visual indicators (e.g., color codes) for attributes and changes.
- Coordinate management and spatial accuracy are framed around representation of habitat extents rather than exact positions; field checks inform attribute updates.

## Data model and attributes
- Features are organized into:
  - Areas (polygons) with polygon-level and component-level attributes.
  - Points (single features under certain size constraints).
  - Lines (linear features with events along their length).
- Broad Habitat (BH) and Priority Habitat (PH) attributes guide habitat classification; BH Accuracy and Reasons for Change track data quality and updates.
- Components allow multiple descriptors per area; operations include add, copy, delete, and attribute editing.
- Mandatory and optional fields are defined, with certain fields defaulting to non-mandatory values (e.g., BH Accuracy, Visit Status).
- Copying attributes and copying events/functions exist to propagate characteristics across features.
- Data constraints include:
  - MMU checks for polygons and lines.
  - Minimum lengths (points require 1:5000 scale or smaller; lines minimum 5.0 m; lines cannot cross themselves).
  - Shared nodes and topology considerations during edits.

## Mapping polygons (habitat areas)
- Primary tools: Split, Modify, Merge, Update, and Copy Attributes.
- Split
  - Create new polygons from a single 1 km square polygon; can be done freehand or by copying polygons from OS MasterMap.
  - Edit sketches with vertices; ensure MMU compliance; input area-specific attributes after split.
  - Doughnut polygons can be created by split edits.
- Copy polygons from existing layers
  - Use Copy Features to bring in polygons from layers like OS MasterMap; refine with vertex editing.
- Modify
  - Edit shared boundaries and nodes; use topology edit tools; save changes to update attributes.
- Merge
  - Combine multiple polygons with identical attributes; copied attributes overwrite existing attributes in merged polygon and components.
- Update
  - Create new polygon areas by updating existing polygons; can digitize new areas or copy from other layers; useful when surveying previously unsurveyed squares or when many areas intersect.
- Attributes
  - Polygon-level: area, Broad/PH, BH Accuracy, Reason for Change, Visit Status (In progress, Completed, Refused access).
  - Component-level: multiple components per area; can add/copy/delete components; supports complex habitat descriptions with themes such as agricultural crops, vegetation, coastal features, forestry, inland physiography, etc.
- Copy Attributes
  - Copy attributes from a source area to multiple target areas, overwriting existing attributes.

## Mapping changes in CS squares
- New squares: create and map from scratch with editable polygons; ensure accurate attribution of new habitat areas.
- Repeating CS squares: use existing data as a baseline; confirm or adjust polygon attributes; indicate spatial or attribute changes using Reason for Change and appropriate BH accuracy updates.

## Mapping points (point features)
- Points are features occupying less than 20x20 m; include trees, standing water bodies, ponds, etc.
- Tools: New, Modify, Delete, Attributes, Copy Attributes.
- Guidelines:
  - Map at 1:5000 scale or smaller to edit; points must be at least 5.0 m apart.
  - Each new point starts with one Unsurveyed/Missing Data component.
  - Points can be moved or relocated to reflect field observations when necessary.
  - Attribute editing follows a structured editor; components can be added, copied, or deleted; status changes affect map appearance on refresh.
- Copy Attributes
  - Copy attributes from a source point to multiple target points, overwriting existing attributes.

## Mapping linear features (lines)
- Linear features are lines (minimum length 20 m, maximum width 5 m) representing fences, walls, hedges, corridors, etc.
- Features are recorded as events along a single continuous line; can include multiple events along a line (e.g., a hedge with adjacent fence).
- If a line crosses another, lines are split at intersections; lines cannot cross themselves; end points shared with other lines are edited via shared-node modify.
- Tools: New, Modify, Cut, Delete, Reshape, Copy Attributes, and checking visit status.
- Editing principles:
  - New lines created with an Unsurveyed/Missing Data event along the length.
  - Modify allows vertex-level edits with insert/delete/move, respecting topology constraints.
  - Cut allows digitized removal along the line; adjacent segments adjust accordingly.
  - Copy from other layers (e.g., OS MasterMap) to create edit sketches and refine shapes.
  - Reshape supports re-drawing along a chosen segment to align with field realities.
- Attribute editing
  - Line-level attributes: event attributes across the line; each event has its own attributes and must be at least 5.0 m long.
  - Event editing includes setting Event From/To positions along the line, with feedback on resultant lengths.
- Copy Attributes
  - Copy events from a source line to target lines; target lines adopt attributes from the source line.

## Checking visit status and data quality for lines
- Use the Select By Attributes tool to identify unvisited Landscape Events; filter by VISIT_STATUS equals 0 (unvisited).
- Event attributes highlight mandatory fields in orange; optional fields in blue; completed status updates may change map appearance after refresh.

## Ponds inventory and grid square workflow
- For squares containing ponds, complete a Grid square inventory form for each pond (on tablet) with attributes:
  - Square reference, pond reference, fullest grid reference.
  - Pond area (m2), presence in field, and reason for loss if absent.
  - New ponds: indicate if not on base map; age estimation and creation reason.
- Determine the survey pond from among ponds in the square using a random-looking lookup on the tablet form; record the survey pond as a primary attribute under Inland Water.
- The survey pond is the single pond to be surveyed for condition; the selection occurs after all ponds in the square are mapped.

## Troubleshooting and utilities
- If UI elements are missing (Table of Contents, toolbars), use the software’s customize options to restore toolbars or tables of contents.
- General guidance and standard workflow recovery tips are included to re-enable essential tools.

## Endnotes
- The document provides a comprehensive, field-oriented workflow for mapping habitats, ponds, and linear features using Surveyor within CS ArcMap, emphasizing data integrity, standardized attributes, and structured editing sessions to support long-term data consistency for the Glastir Monitoring and Evaluation Programme.