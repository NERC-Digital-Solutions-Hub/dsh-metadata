# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Describes methodology and digital tooling for Countryside Survey 2007 (CS2007) to map habitats and landscape features across 1 km squares.
  - Aims to report land cover change by Broad Habitats (BHs) and Priority Habitats (PHs), with detailed attention to unenclosed uplands and Wales squares.
  - Builds on CS2000/CS1990 methods, introducing full digital data collection and a unified GIS model for square-level features.

- Data model and workflow
  - Square-based, fully digital mapping using CS Surveyor (ArcMap extension) to edit Areas (polygons), Lines (linear features), and Points (points).
  - Data organized around BHs and PHs with detailed component-level attributes; supports recording genuine change versus error corrections.
  - Focus on producing time-series data suitable for policy-relevant monitoring and long-term trend analysis.
  - Emphasis on change attribution, metadata, and openness to support auditing and reuse.

- Key classification and change attribution
  - Vegetation and woodland keys determine BH/PH allocations; PHs nest within BHs where applicable.
  - Change attribution categories include REAL change, ERROR change, and NEW BASELINE (habitat subdivision or reclassification).

- Field mapping system and minimum criteria
  - MMU (minimum mapping unit) set at 0.25 ha; mapping prioritizes extent and change over ultra-high geolocation precision.
  - Workflow supports creating, splitting, merging, updating, and copying polygons; lines and points edited with an audit trail of changes.
  - Data governance and metadata requirements integrated to ensure traceability and reproducibility.

- Woody Linear Features (WLFs): attributes and interpretation
  - Unnatural shape vs natural shape distinctions; key attributes include:
    - Height categories (e.g., <1 m, 1–2 m, 2–3 m, >3 m; with notes on canopy base height)
    - Base height (canopy base), species composition, and dominance (>50% hawthorn or other)
    - Evidence of recent management (e.g., newly planted, flailed/coppiced, laying)
    - Line of stumps (Yes/No)
    - Vertical gappiness (percent breaks from canopy to ground)
    - Margins (left and right), presence of staked trees, tree protectors
    - Classification into woody line types: belts, lines, clumps; management history and DBH details
  - Guidance includes examples and imagery to aid distinction between unnatural and natural shapes, and notes that some sections may be recorded as “WLF natural shape” when appropriate.
  - Special terms: earth banks and other linear features may be recorded as part of the same linear feature.

- Field editing tasks and procedures (Lines)
  - Create New Line: add lines at or below 1:5000 scale, minimum length 5.0 m, lines cannot cross themselves; a new line starts with an Unsurveyed/Missing Data event.
  - Modify Line: edit geometry via vertices; manage end nodes (shared nodes) carefully; ensure edits do not create invalid intersections.
  - Shared Nodes: modify intersections of multiple lines; movement propagates to connected lines; ensure edits preserve topology.
  - Cut Line: digitize a cut polygon along a line to remove a segment; visualize cut length versus remaining length.
  - Copy Tool: use existing landscape features to build a cut sketch; combine with other features to refine edits.
  - Delete Line: delete lines only when all events have valid Reason for Change; cannot delete if any event lacks justification.
  - Reshape Line: reshape by drawing an edit sketch that intersects the target line; allow follow-line edits to align with boundaries or nearby features.
  - Reshape Line (Follow Copied Line): move a line to follow a copied boundary or landscape area feature; requires a valid intersecting graphic.
  - Validation: scale and length constraints enforced; shared-node edits require careful handling to avoid new intersections.

- Checking visit status and data integrity
  - Visit status for linear features tracked via an attributes-based selection workflow; unvisited lines highlighted for follow-up.
  - Loops in data (loops of linear features) flagged as corrupted; instructions provided to mark loops as Deleted Feature, complete changes, and reinstate lines with correct attributes.

- Ponds and water body mapping
  - CS2007 Pond Mapping: map ponds with a standard definition (area thresholds and water presence; typically >4 months of water per year).
  - Pond Recording Sheet and survey pond selection: one survey pond per square chosen randomly (or preselected if still valid) for detailed condition assessment.
  - Guidance on identifying ponds under dry conditions, distinguishing ponds from ditches/streams, and boundary delineation in fen/marsh/bog contexts.

- Data quality, metadata, and governance
  - Public sharing of underlying data and metadata can be a barrier; emphasis on quality assurance, cleaning, and transparent reporting of data sources and changes.
  - Documentation requires consistent metadata and openness at the data source to support reuse and auditing.
  - Need for standardized, auditable data models to support policy scrutiny, with processes to manage data gaps, organizational silos, data transformations, and clear communication of complex habitat-change findings.

- Practical guidance and historical context
  - Use of mosaics and partial areas when habitats blend or MMU criteria are not met for discrete polygons.
  - Orchard and non-native species considerations integrated into BH/PH attributes where relevant.
  - Non-native species are recorded to provide habitat context and potential management implications.

- Appendices and legacy datasets (CS2000/CS1990)
  - References to CS1990 and CS2000 themes, code sheets, and universal codes; descriptions of how attributes were recorded historically.
  - Examples of old field assessment materials and mapping approaches to inform current methods and comparability over time.
  - Appendix material includes maps, code sheets, pond forms, and veteran-tree girth guidance for related datasets.

- Core monitoring framework considerations (summary relevance)
  - The handbook provides a standardized, auditable approach to collecting, managing, and sharing environmental health monitoring data.
  - It addresses data gaps, governance, and data transformation needs while enabling clear communication of habitat-change findings.
  - Emphasizes governance processes, metadata quality, openness, and consistent classification schemes to support policy evaluation and decision-making.