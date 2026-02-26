# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Focuses on field mapping of woody linear features (WLFs), including unnatural shapes, stumps, height classifications, species composition, management evidence, and related attributes for CS2007.
- Provides detailed data coding schemes, on-device editing workflows within CS Surveyor (a customised ArcGIS extension), and procedures to maintain data integrity and provenance.

## Key WLF data elements and coding

- Unnatural shape / line of stumps: Yes or No
- Height categories: <1m, 1-2m, 2-3m, >3m, 3-4m, 4-6m, >6m
- Base height indicator: <2m or >2m
- Species composition: mixed species, >50% hawthorn, >50% other
- Evidence of recent management: none, newly planted, cutting (e.g., flail or saw <3 yrs), laying or coppicing (<5 yrs)
- Line of stumps: Yes or No
- Vertical gappiness: <10%, 10-<25%, 25-<50%, 50-<75%
- Margin Left: not present, <2m, 2m-<4m, 4m-<6m, 6m-<12m
- Margin Right: not present, <2m, 2m-<4m, 4m-<6m, 6m-<12m, 12m-20m
- Staked trees: Yes or No
- Tree protectors: Yes or No

- Note: If base height >2m, ensure components cut or trimmed to avoid natural shape; otherwise record as WLF natural shape.

## Data capture and interpretation guidance

- Distinguish unnatural shape versus natural shape and record accordingly; use imagery to support coding.
- Images illustrate example WLFs and corresponding coding.
- Use the full set of attributes to describe each WLF, including structural, compositional, and management-related characteristics.

## Line editing workflow (CS Surveyor)

- Create New Line: 
  - Map area at scale ≤ 1:5000; lines must be at least 5.0 m; lines cannot cross themselves; add one line at a time; new line starts with an Unsurveyed/Missing Data event.
- Modify Line:
  - Select and edit line geometry using vertices; end-point shared nodes may require Shared Node Modify; ensure edits do not create invalid intersections; save changes.
- Shared Nodes:
  - Modify intersection nodes where multiple lines meet; move node to update adjacent lines; ensure topology remains valid.
- Cut Line:
  - Digitise cut polygon along the line; pink/white indicates cut length; red indicates remaining length; multiple cut edits allowed; must maintain minimum length.
- Modifying the Edit Sketch:
  - If the cut polygon shape is unsatisfactory, adjust vertices and redraw the edit sketch before re-cutting.
- Copy Tool:
  - Use features from other layers (e.g., Landscape Areas) to build a cut edit sketch; Copy+ adds features to the sketch, Copy- removes; finalize with Cut.
- Delete Line:
  - Delete one line at a time; all attached events must have a valid Reason for Change; map scale must be ≤1:5000.
- Reshape Line 1:
  - Draw a reshape line along the existing line; the reshape must intersect the line at start and end; ensure resultant line remains valid and above minimum length.
- Reshape Line 2 (following a copied line):
  - Use a reshape graphic to move the line to follow a boundary or copied line; ensure intersection and validation with the copied feature boundaries.
- General editing constraints:
  - Edits must not create intersections with revised lines; minimum feature lengths must be respected; shared end nodes are edited via Shared Node Modify.

## Checking visit status and data integrity

- Visit status: use Select By Attributes to highlight unvisited Landscape Events (VISIT_STATUS = 0) within a square.
- Loops with corrupted data:
  - There are known loop anomalies; remediation involves changing the theme to Deleted Feature, setting Reason for Change to No Change, Visit Status to Completed, saving, deleting the line, and reinserting it with correct attributes.

## Practical notes and supporting materials

- Appendix references: access to Field Assessment Books (FABs) electronically; Fieldhandbook for CS2000 available for deeper interpretation.
- CS2000 and CS1990 context:
  - CS2000 used a theme-based mapping approach with separate data sheets per theme; CS1990 combined map and attributes on paper with coded attributes; transition to CS2007 emphasizes digital, provenance-rich data with explicit change tracking.
- Data governance and reuse:
  - The workflow emphasizes traceable edits, change reasons, and consistent attribute coding to support cross-year analyses and biodiversity monitoring.

## Relevance to data support and reuse

- Provides a structured, codified approach to capturing WLF-related data, enabling reliable querying, tracking of changes, and reproducible updates.
- Supports integration of line-based features with polygonal habitat data, contributing to longitudinal studies of woodland structure, habitat connectivity, and landscape-scale biodiversity monitoring.
- The documented editing protocols and validation steps underpin data quality, auditability, and governance necessary for end-user dashboards, analyses, and policy evaluations.