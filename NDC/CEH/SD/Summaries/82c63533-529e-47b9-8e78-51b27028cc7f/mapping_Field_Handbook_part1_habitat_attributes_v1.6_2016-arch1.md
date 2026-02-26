# Visit status

- Purpose
  - Each Event, Point, and Area includes a VISIT STATUS field to indicate survey progress and data availability.
  - Statuses help identify unsurveyed areas, ongoing work, completed coverage, and areas with restricted access.

- Visit status codes
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- How statuses are used
  - REFUSED ACCESS marks locations where data will be missing and cannot be analyzed.
  - IN PROGRESS serves as a reminder to continue surveying and assign species as work progresses.
  - COMPLETED should only be used when the feature is fully surveyed; if the extent or changes are not yet clear, do not mark as COMPLETED.
  - After completing a square, all features should be recorded as either COMPLETED or REFUSED ACCESS to indicate square-wide survey status.

- Ways to search and identify features by visit status
  - General approach
    - Select the layer (Landscape Points, Landscape Events, or Landscape Areas) and the VISIT STATUS field.
    - Use the numeric codes (0–3) to filter features with unsurveyed, in-progress, completed, or refused statuses.
  - FIND command
    - Quick option to locate features with a specific VISIT STATUS in a chosen layer.
    - Type 0 or 1 to find unsurveyed or in-progress features; results flash on the map for easy identification.
    - Right-click list items to zoom to a feature; can be used while editing.
    - Limitations: cannot search across multiple criteria or multiple layers simultaneously.
  - SELECT BY ATTRIBUTE
    - Highlights all matching features on the map and allows searching for multiple criteria, including 0 and 1 together using OR.
    - Terms and criteria are entered via a guided UI; results are highlighted on the map rather than listed.
    - Options to save search terms for reuse; can highlight across layers; press APPLY to keep highlights active.
  - ATTRIBUTE TABLE
    - Opens a tabular view of features for selection-based filtering.
    - SHOW SELECTION must be used to view only selected features; supports one criterion at a time.
    - Can INVERT SELECTION to identify features not completed (unsurveyed or in-progress) when no REFUSED ACCESS features are present.

- Dealing with Minimum Mapping Units (MMUs)
  - You cannot map features smaller than the MMU.
  - If a small portion near a square edge is part of a larger feature, include it with the adjoining polygon; do not create sub-MMU polygons at the edge.
  - If you need to split out a small part before merging, use UPDATE to split/merge in one operation.
  - Use Copy+ and other tools to add to or modify selections across layers (Landscape Areas vs MasterMap) and manage overlaps.
  - Freehand drawing and copying can be combined from different layers to maintain coherent polygons.

- Identifying Ancient Trees and Veteran Trees
  - Definition and context
    - Ancient (veteran) trees are old-looking trees with characteristics indicating longevity beyond typical specimens.
    - Can include dead trees and non-native species that provide important habitats.
  - Key indicators
    - Large girth for the species (relative to age expectations)
    - Large amounts of dead wood in the canopy
    - Major trunk cavities or progressive hollowing
    - Epiphytic plants, decay features, bark loss, crevices, and signs of long-standing presence
    - Naturally forming water pools, high biodiversity, cultural/historic value, or pollard forms
    - Old-looking appearance and high aesthetic/historic importance
  - Measuring girth and thresholds
    - Girth is typically measured at 1.3 meters above ground (diameter at breast height, DBH).
    - Girth alone is not definitive; growth conditions and management (e.g., pollarding) can affect size.
    - A species-specific table provides maximum girth thresholds used to classify potentially interesting, valuable, and truly ancient trees (with a “rule of thumb” indicating notable status when surpassing the threshold). The table includes many common British/Northern European species and assigns categories such as potentially interesting, valuable, and truly ancient based on percentage thresholds of the max girth.
  - Practical notes
    - The assessment combines girth with other characteristics (dead wood, cavities, epiphytes, habitat features) to improve confidence in identifying ancient trees.
    - Species thresholds vary, and care should be taken not to rely solely on size to determine age/classification.