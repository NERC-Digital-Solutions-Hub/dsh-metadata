# Visit status

- Purpose and statuses
  - Every Event, Point, and Area includes a VISIT STATUS field to track survey progress and access restrictions.
  - Status codes:
    - 0 = unsurveyed
    - 1 = IN PROGRESS
    - 2 = COMPLETED
    - 3 = REFUSED ACCESS
  - REFUSED ACCESS marks areas you aren’t allowed to survey and will not contribute data.
  - IN PROGRESS serves as a reminder to return and add species data or finalize details.
  - COMPLETED should be used only when the feature has been surveyed in its entirety; if parts remain uncertain (e.g., extent, internal patch, or path/feature direction), do not mark as COMPLETED.

- Governance and data quality implications
  - VISIT STATUS helps determine whether a square has been fully surveyed and whether data are suitable for analysis.
  - Statuses enable transparent provenance of survey progress and inform QA/workflow decisions.
  - When a square is finished, all features should be recorded as either COMPLETED or REFUSED ACCESS.

- How to search and manage VISIT STATUS (GIS workflows)
  - Layers to search: Landscape Points, Landscape Events, Landscape Areas
  - Field to search: VISIT STATUS
  - Criteria values: 0, 1, 2, 3
  - Four search methods:
    - Find (binocular): select layer and field, type 0/1 to locate unsurveyed or in-progress features; results appear in a list; features can be flashed on the map or zoomed to.
      - Pros: simple, quick single-criterion search.
      - Cons: cannot search multiple criteria simultaneously; cannot search across multiple layers at once.
    - Find with multiple criteria (Select by Attribute): similar to Find but can search for multiple criteria (e.g., 0 or 1) at once and highlight features; does not produce a list.
      - Pros: highlights all matching features; can search for 0 and 1 together.
      - Cons: may require careful interpretation of highlighted features; no separate result list.
    - Attribute Table: open the table for a layer, apply selections, and use SHOW SELECTION to focus on matching features.
      - Pros: lets you iterate through features one-by-one; can invert selection to find not-completed features.
      - Cons: typically single-criteria at a time unless combined via manual steps.
    - Quick value option: use Use Unique Values to directly pick 0, 1, 2, 3 from a palette for faster selection.
      - Pros: faster typical workflow.
  - Practical notes
    - Selecting by attributes can be used to identify unsurveyed and in-progress features that need finishing.
    - When you finish a feature, it should disappear from the active selection list as its status changes.

- Working with MMUs (Minimum Mapping Units) and editing
  - You cannot map features smaller than MMU (1/25 ha).
  - If a small portion of a larger area intrudes into a square, include it with the adjoining polygon or leave it if it cannot be cleanly delineated.
  - To split/merge polygons under MMU constraints:
    - Use UPDATE to split and merge in a single operation, preserving attributes.
    - You can copy selections between layers (Copy+ added selections from Landscape areas or Mastermap) to combine areas without losing data.
  - Freehand selection tools allow adding or removing areas from a selection for efficient editing.

- Ancient Trees guidance (context for data attributes)
  - The section provides criteria for identifying ancient/veteran trees, including girth thresholds by species and qualitative indicators (dead wood, cavities, bark loss, epiphytic plants, etc.).
  - Girth alone is not definitive; assess multiple characteristics and historical/contextual factors.
  - If captured, tree girth data contribute to heritage and biodiversity attributes within habitat datasets.

- Practical data governance considerations
  - Use VISIT STATUS to evaluate data completeness across squares and time, supporting repeat surveys and provenance tracking.
  - Ensure status changes are reflected in metadata and linked to the square-level QA processes.
  - Document survey progress, access refusals, and completion status to aid discoverability, integrity, and reuse of the dataset.
  - Maintain layer color/pattern conventions as status indicators to facilitate quick visual assessment in GIS tools.