# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- The Visit Status field is present on every Event, Point, and Area to track survey progress, access restrictions, and data completeness.
- Status values:
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- Purpose of Visit Status:
  - Indicates where surveys are not possible and where data will be absent.
  - Acts as a reminder to complete long or partially observed features.
  - Used to assess whether a square has been fully surveyed; ensures accurate completion indicators.

- How to search and filter by Visit Status (three approaches):
  - Find (binocular tool)
    - Choose layer (Landscape Points, Landscape Events, or Landscape Areas) and field (VISIT STATUS).
    - Enter 0, 1, 2, or 3 to locate features.
    - Features flash on the map; right-click in the list to “Zoom to feature.”
    - Keep the Find window open during editing; matching features disappear from the list as you update.
  - Select by Attributes
    - Similar to Find but can highlight all matching features on the map at once.
    - Can search for multiple criteria (e.g., 0 or 1) in one operation, but no automatic feature list.
    - Build criteria by layering VISIT_STATUS and logical operators; apply to highlight features.
    - Save search terms for reuse; use unique values option to quickly select 0/1/2/3.
  - Attribute Table
    - Opens a tabular view of features; use SHOW SELECTION to focus on selected items.
    - Generally supports one criterion at a time; can invert selection (e.g., find not-completed).
    - Useful for systematic, row-by-row processing when surveying entire squares.

- Practical editing and workflow implications:
  - Layers typically show unsurveyed or in-progress features until you split or complete them.
  - Completing a square requires all features to be either COMPLETED or REFUSED ACCESS.
  - If part of a feature’s extent is not yet known, keep it IN PROGRESS rather than marking COMPLETED.
  - The Search tools help locate remaining work quickly, supporting timely square completion.

- Managing Minimum Mapping Unit (MMU) and polygon updates:
  - MMU constraints prevent mapping features smaller than the defined threshold.
  - For tiny or edge-case portions of larger polygons, either merge and re-split later or use UPDATE to perform splits/merges in one operation.
  - UPDATE enables adding to selections from multiple layers (MasterMap and Landscape Areas) and combining them without losing fields; Copy+ and Copy- tools support iterative selection management.

- Ancient Trees guidance (data quality and identification):
  - Ancient/veteran trees are identified by a combination of indicators, not girth alone.
  - Core indicators include large girth for the species, substantial dead wood, hollows, cavities, and an “old look” with high ecological or cultural value.
  - A species-specific girth table provides thresholds, but researchers should integrate multiple indicators and site context.
  - The guidance emphasizes that environmental context and multiple attributes should drive ancient-tree designations rather than girth alone.

- Data capture and quality considerations:
  - Ensure VISIT STATUS is consistently filled across events, points, and areas to support analytics and policy evaluation.
  - Use the status-driven workflow to drive data completeness checks and reporting on square-level progress.
  - Leverage the available search methods to identify and finalize outstanding survey work efficiently.

- Endnote on data products and use:
  - VISIT STATUS and associated workflows underpin reliable, analysable habitat attribute data, enabling consistent time-series analyses, policy support, and public dissemination.