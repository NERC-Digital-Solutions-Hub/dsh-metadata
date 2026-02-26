# Visit status

- Purpose: Each Event, Point, and Area includes a VISIT STATUS field to indicate survey progress, access refusals, and to aid data completeness and analysis.
- Status meanings:
  - REFUSED ACCESS: area cannot be surveyed; no data to analyze.
  - IN PROGRESS: partial mapping; used as a reminder to complete species composition and extent later.
  - COMPLETED: used only when the feature is mapped in its entirety; if uncertain about extent or composition, do not mark as completed.
- Square-level requirement: when a square is finished, all features should be either COMPLETED or REFUSED ACCESS; statuses help verify full square coverage.
- Status values:
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS

## How to search and manage VISIT STATUS

- Access options and layers:
  - Layers: Landscape Points, Landscape Events, Landscape Areas
  - Field: VISIT STATUS
- Search methods, with pros/cons:
  - Find (binocular): simple for 0 or 1; cannot search multiple criteria or across multiple layers; features appear in a list and can be flashed on the map.
  - Select by Attributes: highlights areas on the map for composite searches (e.g., 0 and 1 together using OR); no list, supports complex terms; can save and reload queries.
  - Attribute Table: work with a list of features; shows selections; supports one criterion at a time; can invert selection (e.g., find not completed).
- Practical tips:
  - Use 0/1 quick toggles via keyboard or unique values to populate criteria.
  - Clear highlights when needed; keep the selection tools open during edits to speed up workflow.
  - If features are obscured or look different, adjust layer or search terms; you can zoom to a feature from the list.
  - Save frequently used search terms for efficiency across different parts of a square.

## Dealing with Minimum Mapping Units (MMU) and edits

- MMU constraint: nothing smaller than MMU can be mapped; small fragments at square edges may be included in adjoining polygons.
- Splitting/merging polygons:
  - If needed, use UPDATE to split and merge in one operation; avoids creating an invalid small polygon.
  - Use Copy+ across layers to add to an existing polygon, and Copy- to remove; you can combine selections from different layers to build the final geometry.
  - Freehand selections can be integrated with Mastermap selections to avoid losing attribute data during edits.
- General guidance: map efficiently within the MMU constraint, prioritizing correct size and location for repeatability.

## Ancient Trees: definition and measurement

- What is an Ancient/Veteran tree?
  - Trees that are old for their species or show characteristics of ancient status.
  - Interchangeable terms: ancient tree and veteran tree.
- Key indicators beyond girth:
  - Large trunk girth (species-dependent)
  - High deadwood in canopy, cavities or hollowing
  - Epiphytic plants, fungal fruiting bodies
  - Signs of aging landscape value, historical management, or prominent landscape position
  - Other features: water pools nearby, structural damage, ecological richness
- Girth measurement:
  - Measured at 1.3 meters above ground (DBH proxy)
  - Use girth to categorize but do not rely on it alone; assess overall appearance and other indicators.
- Species-specific girth guidance:
  - The document provides a detailed table of minimum girth thresholds by species and corresponding categories (potentially interesting, valuable, truly ancient), with values converted to practical DBH equivalents.
  - The thresholds are derived from research and field guides and are intended as a decision aid, not an absolute rule.
- Practical note:
  - Girth can be misleading due to species growth variation, management (e.g., pollarding), or environmental conditions; always corroborate with other ancient-tree indicators.