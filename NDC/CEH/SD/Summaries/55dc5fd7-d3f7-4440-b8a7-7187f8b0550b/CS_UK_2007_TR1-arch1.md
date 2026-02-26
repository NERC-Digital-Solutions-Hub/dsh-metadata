# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and purpose
- Defines field mapping methodology used in CS2007 (Countryside Survey 2007) for habitat and linear features, implemented via CS Surveyor in ArcMap.
- Focuses on recording habitat extents and changes to enable country- and UK-wide reporting and time-series analyses.
- Specifies data structures (areas, lines, points) and the workflow for editing, change attribution, and provenance to support cross-square comparisons and national reporting.

## Woody Linear Features (WLFs) and attributes
- Core WLF attributes to capture:
  - Unnatural shape vs natural shape/line of stumps
  - Height categories of base canopy (e.g., <1 m, 1–2 m, 2–3 m, >3 m, with further subcategories)
  - Base height and canopy height thresholds
  - Species composition (e.g., mixed species, >50% hawthorn, >50% other)
  - Evidence of recent management (no recent management, newly planted, cutting, laying, coppicing)
  - Line of stumps (Yes/No)
  - Vertical gappiness (percent breaks from canopy to ground; e.g., <10%, 10–<25%, etc.)
  - Margin widths on left and right sides (distance categories)
  - Staked trees (Yes/No) and tree protectors (Yes/No)
- If any base height is >2 m, component woody species must be cut or trimmed to avoid natural shapes; record natural shape when appropriate.
- Aids in identifying sections with natural vs managed, and in differentiating WLF classifications (line of trees, belt, hedge, etc.) for BH/PH allocation.

## Line editing workflow (CS Surveyor) and tools
- Create New Line
  - Map scale must be 1:5000 or finer; minimum length 5.0 m; cannot cross itself; lines added one at a time; each new line starts with a single Unsurveyed/Missing Data event.
- Modify Line
  - Select line, edit vertices (insert, delete, move); end-point vertices shared with other lines are edited via Shared Node Modify.
  - Ensure topology integrity; edits must not create intersections with other revised lines.
- Shared Nodes
  - Modify by selecting a shared node (pink highlight); moving a node moves connected lines; preserves topology.
- Cut Line
  - Digitize a cut polygon along the line; display shows length to be cut and length to remain; execute Cut to apply.
- Copy Tool
  - Use features from other layers (e.g., OS Mastermap) to draft edit sketches; combine with Cut edits to refine results.
- Delete Line
  - Deletes lines only if all events have valid Reason for Change; map scale must be 1:5000 or less; one line at a time.
- Reshape Line
  - Create a reshape graphic along the line to redefine its path; must intersect the line at start and end; then apply to reshape.
- Reshape Following Copied Line
  - Use a copied feature to guide the reshape; the reshape graphic must intersect the line and any boundary features used.
- Checking Visit Status on Linear Features
  - Use Select By Attributes to filter Landscape Events by VISIT_STATUS; unvisited lines are highlighted for follow-up.
- Data integrity notes
  - Minimum line length constraints apply; shared-endpoints and topology must be preserved; lines cannot be edited in ways that create new intersections with other lines.
  - Loops in data may occur in certain squares and require targeted procedures (set change theme to Deleted Feature, Reason for Change: No Change, Visit Status: Completed; then delete and re-create as appropriate).

## Publishing edits and data provenance
- All edits are stored with attributes indicating change reason, provenance, and visit status to enable reproducibility and time-series analyses.
- The workflow emphasizes capturing change (real change vs. correction) rather than only static extents, with explicit justifications.

## Ponds and sampling
- CS2007 Pond Mapping: every square with ponds requires a dedicated recording sheet; one survey pond is selected for detailed condition assessment (randomly or by pre-selection with justification).
- Pond attributes include boundary delineation, water presence, and reasons for pond loss or creation; pond data is integrated into tablet and field sheets for freshwater surveyors.
- The process accommodates newly mapped or re-evaluated ponds and allows re-selection if conditions change.

## Data structure, themes, and coding
- Features are organized into themes and mapped as polygons (areas), lines (linear features), and points (point features) with habitat allocations (BH/PH) and relevant attributes.
- Woodlands and vegetation are classified via vegetation keys and woodland feature keys to guide BH/PH placement and to support cross-square comparisons.
- Historic data (CS1990/CS2000) are harmonized with CS2007 methods to maintain meaningful time-series analyses and baselines.
- Appendix content provides detailed code lists for various themes (Agriculture/Natural Vegetation, Boundaries, Forestry, Physiography, Structures, Inland water, etc.), including species, habitat types, and condition descriptors.

## Practical takeaways for analysts
- Expect a rich, multi-layered dataset: Broad Habitats, Priority Habitats, woodland types, physiography, boundaries, and detailed component attributes for woody linear features.
- Change interpretation is central: distinguish genuine ecological change from mapping corrections; document reasons for changes and any new baselines.
- Harmonize older CS data (1990/1998/CS1990, CS2000) with 2007 methods to enable robust time-series analyses.
- Pond mapping requires standardized data capture and a carefully selected survey pond for detailed condition assessment.
- Woodland and linear features require careful structural classification (woodland vs belt vs hedge) and associated management attributes to support habitat allocation at polygon and component levels.
- Analysts should leverage vegetation and woodland keys to ensure consistent BH/PH allocations and cross-square comparability for national reporting.