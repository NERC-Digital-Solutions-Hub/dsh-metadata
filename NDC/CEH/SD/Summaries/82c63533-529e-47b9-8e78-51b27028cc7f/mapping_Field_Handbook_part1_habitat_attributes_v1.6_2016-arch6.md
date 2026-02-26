# Visit status

- Purpose and usage
  - Every Event, Point, and Area must have a VISIT STATUS field.
  - Values indicate: 0 Uns surveyed, 1 IN PROGRESS, 2 COMPLETED, 3 REFUSED ACCESS.
  - VISIT STATUS helps show where access is restricted, tracks progress, and ensures a feature or square is fully surveyed before marking as completed.

- How to use during surveying
  - IN PROGRESS acts as a reminder to finish surveying and assigning species when full extent isn’t visible.
  - COMPLETED should be used only when the feature is mapped in its entirety and no unresolved questions remain about extent, patches, or directional changes.
  - When a square is finished, all features should be marked as COMPLETED or REFUSED ACCESS.
  - Color/pattern changes on the map will reflect current status to aid review, especially for small features.

- Searching and filtering options
  - Three methods exist to locate features by VISIT STATUS, each with trade-offs:
    - FIND command
      - Choose layer (Landscape Points, Landscape Events, or Landscape Areas) and VISIT STATUS (0–3).
      - Type the numeric code in the search box; features appear in a list and can be flashed on the map.
      - Pros: quick for single-criteria searches; easy to zoom to features.
      - Cons: cannot search multiple criteria or multiple layers at once.
    - SELECT BY ATTRIBUTE
      - Build queries (e.g., VISIT_STATUS = 0 OR VISIT_STATUS = 1) to highlight features on the map.
      - Pros: can search multiple criteria and view all highlighted features together.
      - Cons: no automatic list of results; selection terms must be managed by the user; more complex to set up.
      - Tips: save queries for reuse; use “use unique values” to simplify input; can invert selections.
    - ATTRIBUTE TABLE
      - Open the table for the layer and SHOW SELECTION to work through matched features.
      - Pros: provides a list to work through; can batch-process.
      - Cons: typically limited to one criterion at a time; may require manual navigation.
  - Practical note: the FIND and SELECT BY ATTRIBUTE methods are especially useful for prioritising unsurveyed or in-progress features within a square.

- Working with MMUs (Minimum Mapping Units)
  - Do not map features smaller than the MMU.
  - If a small sliver enters a square edge, include it in the adjoining polygon.
  - To split a larger polygon without losing attribute data, use UPDATE to split/merge in one operation rather than creating MMU-sized fragments.
  - Editing workflow: use a combination of freehand drawing and copying between layers to adjust selections without losing data.

- Ancient trees (veteran trees) guidance
  - Definition: Ancient/veteran trees are old-for-their-species and often have features indicating age.
  - Core indicators:
    - Large girth for the species
    - Abundant dead wood in the canopy
    - Visible trunk hollows or progressive hollowing
    - Other aging signs (epiphytic plants, cavities, decay, bark loss, crevices)
    - Associated habitat features (water pools, high wildlife diversity) and cultural/historic value can accompany age signals
  - Girth guidance (measurement and use):
    - Measure at 1.3 metres (DBH) to inform girth thresholds.
    - Species-specific thresholds exist to indicate potential status (e.g., potentially interesting, valuable, truly ancient) but are not sole criteria.
    - A table provides minimum girth values by species; these are guidelines and must be considered with other age indicators.
  - Cautions:
    - Girth alone can be misleading (growth conditions, management like pollarding can affect size).
    - Always assess multiple aging indicators beyond girth.
  - Practical approach: use girth as a guideline, but document age-related features and context to support veteran-tree status.

- Data quality and workflow implications
  - VISIT STATUS is key for auditing survey completeness and guiding data validation.
  - Use the three search methods to efficiently locate and revisit features needing completion or verification.
  - Ensure consistent application of COMPLETED vs REFUSED ACCESS to enable reliable downstream analyses and reporting.

- Summary for Data Support practice
  - Maintain rigorous status tracking for all spatial features to enable self-service data quality checks.
  - Leverage search tools to prioritize work and improve reusability of completed maps and reports.
  - Apply MMU and editing best practices to preserve data integrity while enabling timely square-level mapping.
  - Incorporate ancient-tree guidelines as part of woodland and habitat data, balancing girth data with multiple aging indicators for robust veteran-tree identification.