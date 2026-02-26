# Visit status

- Purpose: The VISIT STATUS field is mandatory for every Event, Point, and Area. It tracks survey progress, access refusals, and completion status to ensure data coverage and inform subsequent analysis.

- Status values:
  - 0 = Unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS

- How statuses are used:
  - REFUSED ACCESS indicates no data will be available from that feature.
  - IN PROGRESS serves as a reminder to continue surveying and to add details (e.g., species) later.
  - COMPLETED should only be used when the feature is fully mapped; if the extent is not yet verifiable (e.g., far end unknown, patches of other habitat present, or path/wall direction unclear), do not mark as COMPLETED.
  - After finishing a square, each feature should be marked as COMPLETED or REFUSED ACCESS.

- Status-based data handling and navigation:
  - The map will support status indicators via color/pattern changes on layers; large features are visible, but small features may be hard to see.
  - The software provides three main ways to search for features by VISIT STATUS: Landscape Points, Landscape Events, and Landscape Areas layers.

- GIS search methods (three approaches, with trade-offs):
  - Find (binocular tool): Search a single layer for VISIT STATUS values (0 or 1 commonly). Features matching criteria are listed, can “flash” on the map, and zoomed to. Multiple searches across layers require switching layers.
  - Select by Attribute: Highlights features across a chosen layer with complex criteria. Can search for multiple criteria (e.g., 0 and 1) but typically does not produce a feature list; useful for highlighting across the map. Selections can be saved and reloaded.
  - Attribute Table: Opens a table of features for selection and sequential processing. Allows searching by one criterion at a time; SHOW SELECTION must be used to view only selected features. Inversion can help identify non-completed features if no REFUSED ACCESS features are present.

- Working in practice on a square:
  - Lines and points start unsurveyed; once work begins, the status updates reflect progress and the state of the feature.
  - When a square is blank, the first split triggers the disappearance of the unsurveyed state on subsequent edits.

- Minimum Mapping Units (MMUs) and editing guidance:
  - You cannot map items smaller than the MMU. If a small portion intrudes at a boundary, include it in the adjacent polygon; if it’s an end segment of a longer feature, leave it.
  - To split a large polygon before merging (to avoid losing attributes), use UPDATE to perform split/merge in one operation. Selection can combine areas from MasterMap and Landscape Areas; freehand selections can be added or removed using Copy+ and Copy-.

- Identifying Ancient Trees (veteran trees) within the VISIT STATUS framework:
  - Definition: Trees that look old relative to their species, with characteristics such as large girth, hollow trunks, and other signs of aging.
  - Measurement and criteria: Tree girth (DBH) is typically measured at 1.3 meters above ground. Species-specific minimum girth values are used as a guide, but girth alone is not definitive.
  - Additional indicators of ancient status include: abundant dead wood, trunk cavities, water pools on the trunk, bark loss, cracks or crevices, epiphytic plants, high wildlife diversity, and an overall old appearance.
  - Cautions: Pollarding or site-specific growth can affect girth; use a holistic assessment rather than relying solely on girth thresholds.
  - Example thresholds and species-specific notes are provided for a wide range of species, illustrating how to interpret girth in the context of veteran-tree status.

- Practical governance and monitoring implications:
  - The VISIT STATUS framework supports traceable field progress, enabling rigorous QA of coverage and progress for monitoring programs.
  - It facilitates planning, prioritization, and time management in field campaigns, and supports downstream time-series analyses of data completeness and data quality.