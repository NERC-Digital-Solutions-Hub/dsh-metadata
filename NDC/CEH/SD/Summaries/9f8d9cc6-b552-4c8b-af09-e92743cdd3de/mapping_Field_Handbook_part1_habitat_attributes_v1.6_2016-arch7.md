# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

## Visit status: purpose and values
- Every Event, Point, and Area has a VISIT STATUS field to track survey progress.
- Status values:
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- Using VISIT STATUS helps identify areas not surveyed, ongoing work, and completed features; also used to judge whether a square has been fully surveyed.

## How to use VISIT STATUS in the GIS workflow
- Three search methods to identify features by status:
  - Find (binoculars): select layer and field, search for 0 or 1; supports flashing to locate features on the map; can zoom to features from the list.
  - Select by Attribute: highlights features on the map for combined criteria (e.g., 0 or 1); can search across multiple criteria but does not produce a separate feature list.
  - Attribute Table: list of features with a top-based search; works like Find but limited to one criterion at a time; useful when surveying entire squares and inverting selections (e.g., completed vs not completed).
- Practical tips:
  - Keep the Find window open during edits; completed features disappear from the list as statuses change.
  - Use unique values to quickly access common status options (0, 1, 2, 3).
  - If multiple layers are used, ensure searches target the correct layer (Landscape Points, Landscape Events, or Landscape Areas).

## Managing Minimum Mapping Unit (MMU) and editing practices
- MMU governs whether a feature can be mapped; nothing smaller than MMU may be created.
- When a very small portion of a larger area crosses a square boundary:
  - Include it in the adjoining polygon if possible.
  - If you need to split a larger polygon, prefer using the UPDATE tool to split/merge in one operation, preserving fields.
- Multi-layer editing tips:
  - Use Copy + to add polygons from different layers; Copy - to remove selections.
  - You can combine selections from Mastermap and other layers; use freehand tools to adjust selections as needed.

## Lines, areas, and feature creation nuances
- Lines and points are created in an unsurveyed state within blank squares; a completely blank square will show unsurveyed lines/areas until split.
- Snapping, line editing, and segmentation rules govern linear features:
  - Lines must be at least 5 m long.
  - Lines can be split at intersections; lines cannot cross themselves; lines are directional (start vs end).
- When using mosaics, ensure component percentages sum to 100%.

## Handling refused access and square completion
- Any feature not surveyed due to access restrictions should be marked as REFUSED ACCESS.
- Upon finishing a square, all features should be either COMPLETED or REFUSED ACCESS; if unsure about extent, do not mark as COMPLETED.

## Ancient trees and veteran trees: identification and measurement
- Definition of ancient/veteran trees:
  - Trees that look old for their species and show characteristics such as large girth, substantial dead wood, hollow trunks, cavities, and other ecological indicators.
  - Dead trees and non-native species can also be important habitats.
- Girth and age indicators:
  - Megments include minimum species-specific girth thresholds and related DBH considerations.
  - Girth is typically measured at 1.3 metres (DBH).
  - Do not rely on girth alone; assess overall age indicators and other features (dead wood, cavities, iconic older appearance).
- Additional indicators of ancient trees:
  - Large dead wood in canopy, trunk cavities, water pools, bark loss, crevices, fungal fruiting bodies, epiphytic plants, high wildlife diversity, and cultural/historic context.
  - Visual cues may vary with species and management history (e.g., pollarding).
- Species-specific guidance:
  - The document provides a detailed table of girth thresholds by species to help classify trees as potentially interesting, valuable, or truly ancient, acknowledging that various species reach different girth thresholds.
  - Use girth as a guide, with a holistic assessment of age indicators.

## Practical notes for GIS workflow related to visit status and ancient trees
- Use VISIT STATUS to manage survey progress across events, points, and areas and to determine when a square is complete.
- When identifying ancient trees, combine girth criteria with other age indicators to avoid misclassification.
- Ensure data integrity by regularly updating status fields as surveys progress and by validating that completed squares have appropriate statuses recorded.