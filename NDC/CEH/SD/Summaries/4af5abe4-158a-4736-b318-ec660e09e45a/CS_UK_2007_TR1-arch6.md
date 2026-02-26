# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Presents a GIS-based methodology for Countryside Survey 2007 field mapping of habitats and landscape features.
- Aims to report land cover change, map Broad Habitats (BH) and Priority Habitats (PH), and provide detailed habitat attributes for end users.
- Extends previous CS methods by integrating PHs with BHs, increasing data detail in unenclosed uplands, adding Wales squares, and capturing time-series data.

## Data model, flow and governance
- Uses the CS Surveyor extension in ArcMap to edit Areas (polygons), Lines (linear features) and Points (point features) within each 1 km square.
- A single digital map consolidates five prior themes; change recording is mandatory to distinguish real ecological change from mapping errors.
- Outputs support broad data products and future reuse; system logs edits and supports fault reporting.

## Habitat classification and attributes
- Two keys drive classification:
  - Vegetation Key: assigns primary and secondary attributes to BH/PH based on vegetation composition.
  - Woodland Types/Features: classifies woody vegetation (belt of trees, clump of trees, woodland/forest, hedges, etc.) with mosaic coding when needed.
- Broad Habitats (BH) include a range from BH1–BH19 plus mosaic variants; Priority Habitats (PH) are nested within BHs with GIS masks to constrain upland/lowland extents.
- Mosaic option allows percentage shares for components when a single BH/PH cannot be clearly delimited.

## Habitat and vegetation attributes
- Vegetation Key assigns primary attributes (dominant species, canopy cover, NVC associations) to BH/PH.
- Woodland Attributes: primary attributes (e.g., Belt of trees, Clump of trees, Woodland/Forest, Scrub) and secondary attributes (species, DBH, buffer, management).
- Tree and shrub data: record species, cover, DBH classes; veterans recorded (limited per square and per species).

## Mapping rules, geometry and change assessment
- Minimum Mapping Unit (MMU) is 0.4 ha (1/25 hectare); areas smaller than MMU are not mappable unless part of a larger boundary.
- A new polygon is created when the primary habitat attribute changes; minor species composition changes within the same habitat do not trigger new polygons.
- Enclosed vs unenclosed habitats use CS1998/CS1990 baselines where applicable to assess real change vs error.
- Areas may have multiple components; changes require a reason (real change, correction of previous error, new baseline PH, etc.).

## Plotting, editing operations and topology
- Copy, split, merge, modify and update operations supported; topology-aware edits ensure shared nodes and boundaries remain consistent.
- Reasons for change must be provided for edits; maintain audit trails via the editing toolkit.
- Saving edits is explicit (Save Session) and sessions can be terminated with End Session; edits are persisted only on save.

## Tools and editing workflow for lines and areas
- ArcMap with Landscape Feature Editing toolbox; editing scales and constraints:
  - Polygons: zoom to < 1:5000 for editing; MMU enforcement applies.
  - Lines: minimum length 5.0 m; lines cannot cross themselves; when lines intersect, lines split automatically.
  - Shared nodes: topology-aware modifications affect connected lines; end-point nodes can be edited only via Shared Node Modify.
- Create Line: adds a new Unsurveyed/Missing Data event along the new line; one line per edit; lines must be within square.
- Modify Line: edit vertices, insert/delete/move vertices; shared boundary endpoints require Shared Node Modify.
- Cut Line: define cut polygon along a line to remove or modify a segment; visual feedback shows cut lengths.
- Reshape Line: redefine shape along an existing line using a reshape graphic; requires scale < 1:5000 and length constraints.
- Copy Tool: reuse features from other layers to refine edits; supports complex cut-line sketching.
- Delete Line: removes a line only if all attached events have valid Reason for Change; scale constraints apply.
- Check Visit status for linear features: use Select By Attributes to highlight unvisited lines; loops with corrupted data require special handling (mark as Deleted Feature, complete visits, then re-create).

## Pond mapping and sampling
- Record all ponds in a square on a CS2007 Pond Mapping Recording Sheet.
- Select one pond per square as the survey pond for detailed condition assessment (randomized selection; preselected ponds may be used).
- Delineate pond boundaries with attention to complex cases (fen/marsh, connected ponds, ditches, dammed streams).
- Recording fields cover polygon ID, area, maximum winter water level, presence of water, and notes on pond changes.
- Appendix guidance details the random pond selection process and validation steps.

## Points, veteran trees and features
- Points represent landscape features smaller than 20 m x 20 m; spatial accuracy is not the primary goal, but feature accuracy is important.
- Woody features (trees/shrubs) recorded as points or clusters; attention to buffers and veteran trees (limits per square/species).
- Modal DBH captured; five DBH classes; multi-stem trees measured per stem.

## Linear features and margins
- Linear features are typically < 5 m wide but can extend long distances; record start/end positions, lengths, and events along lines (fences, hedges, ditches, walls).
- Edits include adding/deleting events, copying events, and adjusting line geometry to field reality.
- Margins and hedges: attributes include width, height, margin left/right, vegetation cover; can be mapped as line or area components depending on width.
- Wide woody linear features treated as belts of trees or scrub; narrow segments mapped as individual trees or hedges.

## Non-native species and orchard guidance
- Non-native species of concern identified and recorded within habitats (examples include Buddleia, Rhododendron, Impatiens glandulifera, etc.).
- Orchards documented as a special BH/PH case; traditional orchards may be PH and require Orchard attributes as additional data.

## Practical notes for data support
- Spatial accuracy is secondary to correct habitat extent, change status, and BH/PH allocation.
- Pond boundaries are carefully delineated to differentiate ponds from ditches, streams, and bogs.
- GIS masks and time-series analysis aid extent estimation and longitudinal analysis.
- Outputs emphasize data governance, continuity with older surveys, and enabling cross-time analyses.

## Appendices and legacy data
- Appendix 1–6 provide guidance on old field assessment frameworks (FABs), CS1990/CS2000 themes and codes, and lists of veterinary/veteran trees and loops with example data structures.
- Includes references to codesheets, plots, and field handbooks for cross-walks to CS2007 data.

## Support, updates and access
- Guidance for field support, helpdesk contacts, and updates via the Latest News section.
- Emphasizes data governance, filling gaps between older surveys and CS2007, and maintaining consistency for time-series analyses.