# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- The document provides field mapping methodology for CS2007, focusing on habitat extent and change captured via the CS Surveyor (ArcMap extension), with emphasis on editing woodland line features (WLFs) and related data structures.
- Data collection and editing are performed in a digital workflow to support biodiversity monitoring and time-series analyses, with standardized attributes and change-tracking requirements.

## Key data model: Woodland Line Features (WLF) and related attributes

- WLF attributes cover:
  - Height categories for the base canopy and changes to height: height classes such as <1m, 1-2m, 2-3m, >3m, etc.
  - Base height: height of the base of the canopy.
  - Species composition: primarily mixtures or dominance by hawthorn or other species.
  - Evidence of management: no recent management, newly planted, cutting, laying or coppicing, etc.
  - Line of stumps: whether the WLF is represented as a line of stumps.
  - Vertical gappiness: percentage breaks from canopy to ground.
  - Margins: margin widths on left and right sides.
  - Staked trees and tree protectors indicators.
- Shape classification and rules:
  - Distinguish WLF as unnatural shape/line of stumps or natural shape.
  - If feature height exceeds 2m, check whether woody components are trimmed to maintain natural shape; record as natural shape if appropriate.
- Images and examples accompany the coding guidance to aid consistent interpretation.

## Data collection and digital workflow

- Data are captured using CS Surveyor within a survey data frame, with emphasis on habitat extent and change rather than precise geolocation.
- Operational rules link field observations to habitat logic and codes to support consistent classification across squares.

## Editing tools and procedures

- Create New Line
  - Must be created within the survey square at a map scale of 1:5000 or less.
  - Minimum length: 5.0 meters.
  - Lines cannot cross themselves; intersections split lines automatically.
  - A new line starts with a single Unsurveyed/Missing Data event; subsequent attribute edits record details.
- Modify Line
  - Edit along the line using vertex editing; can insert, delete, or move vertices.
  - End vertices (shared with other lines) cannot be edited directly; use Shared Node Modify for these.
  - The modification must produce a valid line; edits that would create invalid results are blocked.
- Shared Nodes
  - Shared nodes (intersections) can be moved; adjoining lines adjust accordingly.
  - Special care to avoid creating intersections with other revised lines.
- Cut Line
  - Digitize a cut polygon along the target line to remove a segment.
  - The length cut is highlighted; the remaining portion is shown in red.
- Reshape Line
  - Reshape edits use a follow/intersect approach to ensure edits align with original line boundaries.
  - Must intersect the line to be reshaped and obey minimum feature length constraints.
- Copy Tool
  - Use existing polygons from other layers (e.g., OS Mastermap) to construct cut-line edit sketches.
  - Supports assembling multiple features into the edit sketch before finalizing the cut.
- Delete Line
  - Deleting a line requires all associated events to have a valid Reason for Change.
  - Can only delete one line at a time; map scale must be 1:5000 or less.
- Reshape Line follow copies
  - Reshape following a copied line allows alignment to landscape area boundaries; requires appropriate copying and vertices editing.
- Checking Visit Status for linear features
  - Use Select By Attributes to highlight unvisited Landscape Events (VISIT_STATUS = 0).
- Loops and data integrity
  - There are known data loops (corrupted event data) that require a specific remediation procedure:
    - Change the theme to Deleted Feature, Reason for Change: No Change, Visit Status: Completed for loop events.
    - Delete the loop lines and reinstate the feature by re-adding a line and its attributes.

## Change management, governance, and quality control

- All edits must maintain alignment with habitat logic; changes should be justified and logged with reasons.
- Two-tier change statuses for historical allocations (REAL vs ERROR) guidance appears in related material and informs data lineage and reproducibility.
- Data integrity is supported by enforcing mandatory fields and ensuring that edits do not compromise the spatial topology or attribute consistency.
- Documentation and metadata capture are emphasized to enable reproducibility and time-series analyses.

## Practical implications for Data Stewards

- Enforce standardized WLF attributes and coding to ensure consistency across survey squares and cycles.
- Maintain data lineage by clearly distinguishing REAL changes from corrections (ERROR) and logging explicit reasons for each change.
- Ensure metadata completeness for WLFs, including height categories, margins, management evidence, and woody features.
- Balance data quality with spatial precision by prioritizing accurate habitat extent and change detection over exact line geometry.
- Align data governance with biodiversity monitoring goals, supporting downstream reporting and policy-relevant analyses.

## Appendices and supplemental guidance (highlights)

- Veteran trees and girth guidance (Appendix 5): rules of thumb for categorizing veteran trees based on girth measurements to support scoring of notable specimens.
- Appendix 6: Squares with loops (loop data) detailing unique square identifiers and spatial metadata relevant to loop handling.
- Appendices related to field assessment tools and legacy datasets (FABs, CS2000/1990 references) to support interpretation and historical context.