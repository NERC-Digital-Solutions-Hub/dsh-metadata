# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

## Overview
- Defines field protocols for mapping habitat attributes to produce consistent, time-series data for environmental health and policy performance.
- Emphasises alignment with Countryside Survey methodologies to support trend analyses and flexible policy emphasis.
- Uses 1 km square mapping with GIS Editable Polygon/Habitats framework and standardized BH/PH classifications.
- Data governance: standardized formats, interoperability with CS data, and datasets reusable across monitoring programs.

## Visit status: recording survey progress
- Every Event, Point, and Area must have a VISIT STATUS to show survey progress and access restrictions.
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- REFUSED ACCESS indicates areas you are not allowed to survey; IN PROGRESS serves as a reminder to complete survey work in large areas or long linear features.
- COMPLETED should only be used when the feature is surveyed to its full extent; if uncertain about extent, internal changes, or contained patches, do not mark as COMPLETED.
- VISIT STATUS is used to assess whether a square has been fully surveyed; at square completion, all features should be marked as COMPLETED or REFUSED ACCESS.
- Status-aware layers will later change color/pattern to indicate current status; tools exist to search features by VISIT STATUS across layers (Landscape Points, Landscape Events, Landscape Areas).

## GIS tools and workflows for visit status
- Three primary search approaches, each with pros/cons:
  - Find (binocular icon)
    - Select layer, then field (VISIT STATUS), then enter criteria (0 or 1). Results appear in a list; feature can flash on the map for location.
    - Find does not search multiple layers simultaneously; can’t combine criteria easily.
  - Select by Attributes (Linears page 124)
    - Highlights all matching features on the map and allows searching for multiple criteria (e.g., 0 and 1) but does not produce a feature list.
    - Use the layer, field, and criteria (e.g., VISIT_STATUS = 0 OR VISIT_STATUS = 1) and APPLY to keep terms defined; can save search terms for reuse.
  - ATTRIBUTE TABLE
    - Table-based selection across features; show selection and navigate through items.
    - Limited to one criterion at a time unless using advanced operations (e.g., invert selection to find non-completed features).
- Practical tips:
  - Use unique values to quickly select 0, 1, 2, 3 from a dropdown.
  - Remove highlights via clear selection; you can keep the selection window open to adjust criteria without re-entering.
  - If you plan multiple surveys in a square, the search window can be left open between sessions for speed.
- Operational guidance:
  - For large squares or when features are obscured, use FIND or SELECT BY ATTRIBUTES to locate and prioritize surveying tasks.
  - The attribute table approach is useful for working through a complete square when a full list of items is available.

## Dealing with MMUs (Minimum Mapping Units)
- You cannot map features smaller than the MMU; if a small portion of a larger feature encroaches into your square, include it in the adjoining polygon.
- To split or merge polygons across MMU boundaries:
  - Use UPDATE to perform splits/merges in one operation so MMU-sized polygons do not persist.
  - Selection across layers can be done via Copy+ (add to selection) or Copy- (remove from selection) to combine areas from MasterMap and Landscape areas.
  - Freehand drawing plus layer-cross-copy operations allow incremental edits without losing previously entered fields.

## Identifying Ancient Trees: guidance and measurement
- Defines ancient (veteran) trees by multiple indicators beyond size, including structural and ecological features.
- Core definition elements:
  - Large girth for species
  - Large amount of dead wood in canopy
  - Major trunk cavities or hollowing
  - Naturally forming water pools or other distinctive ecosystem features
  - Additional indicators: bark loss, decay holes, fungi, epiphytic plants, high wildlife interdependence, old-looking appearance, cultural/historic value, pollard forms, and prominent landscape position.
- Girth measurements:
  - Girth (or DBH) measured at 1.3 meters above ground (breast height).
  - Species-specific minimum girth values are provided; these thresholds help classify as potentially interesting, valuable, or truly ancient.
  - Do not rely on girth alone; growth conditions, management history (e.g., pollarding), and other characteristics must be considered.
- Practical notes:
  - Measurements and classifications are context-dependent; use a combination of girth, visual indicators, and ecological features to assess ancient status.
  - A detailed species-specific table accompanies the guidance to determine appropriate thresholds.

## Practical data handling and QA related to visit status
- Focus on recording habitat extent and attributes, while treating precise polygon geometry as secondary to consistent extents suitable for time-series analysis.
- When multiple habitats exist within a polygon, mosaics can be recorded with explicit component attributes and percentages summing to 100%.
- Margins and cross-compliance boundaries are documented and can be additive across habitat types where relevant.
- Woody Linear Features are captured as distinct linears with natural vs non-natural shapes; record DBH, species composition, and associated margins.
- Data quality: maintain QA checks, ensure datasets are stored, and upload to appropriate portals; ensure time-series consistency across surveys.

## Additional context and appendices
- Field mapping notes, line editing tips, boundary decisions, and example mappings are provided as appendices.
- Emphasis on practical field approaches: map lines and areas first, ensure boundary accuracy, and document problems or uncertainties for later review.