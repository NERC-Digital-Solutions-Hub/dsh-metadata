# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Overview
  - Countryside Survey 2007 (CS2007) maps habitats and landscape features across 1 km squares using digital GIS data.
  - Integrates six themes into a single editable digital map; reports habitat change by Broad Habitats (BH) and Priority Habitats (PH).
  - Emphasizes collecting more detailed habitat data, including upland unenclosed habitats, with PH mapping alongside BH mapping.
  - Fieldwork focuses on change detection, data quality, and consistent standards; spatial accuracy secondary to correct habitat attribution and extent.

- Data model and classifications
  - Broad Habitats (BH) group major landscape/habitat types (e.g., BH1 Broadleaved Woodland, BH2 Coniferous Woodland, BH4 Arable and Horticulture, BH5–BH18 various grasslands, BH21 Littoral/Sea, etc.).
  - Priority Habitats (PH) nest within BHs; post-survey GIS masks help define upland/lowland ranges and ensure consistent PH extents.
  - Woodland types/features are coded separately (e.g., Belt of Trees, Clump of Trees, Woodland/Forest) with primary/secondary attributes and can be assigned at polygon and component levels.

- Vegetation, woodland and WLF (Woody Linear Features) attributes
  - Vegetation Key links stands to BHs/PHs; supports PH identification and correct BH allocation.
  - Woodland types key classifies canopy structure (trees, belts, clumps, lines, scattered trees) for BH/PH allocation and secondary attributes.
  - For unenclosed habitats, record detailed vegetation attributes (species, coverage, indicator species) to support PH identification and habitat-change interpretation.
  - WLF data fields (from the example) include:
    - Unnatural shape/Line of stumps
    - Height categories (e.g., <1m, 1–2m, 2–3m, >3m; base canopy height)
    - Species composition (e.g., mixed species; >50% hawthorn)
    - Evidence of management (recent management, newly planted, cutting, laying or coppicing)
    - Line of stumps (Yes/No)
    - Vertical gappiness (% breaks from canopy to ground) with categories
    - Margins (Left/Right) width categories
    - Staked trees (Yes/No)
    - Tree protectors (Yes/No)
  - Note: If >2m height, check that woody species are cut or trimmed to avoid natural shape; record as WLF natural shape if appropriate.
  - Visual examples provided to aid coding and interpretation.

- Pond mapping
  - All ponds in a square must be identified; data collected on a Pond Mapping form.
  - One survey pond per square is selected randomly from mapped ponds; winter water level and vegetation cues define boundaries.
  - Distinguish ponds from ditches, flushes, and dammed streams; record pond attributes and any pond-sampling information.

- Data collection, change reporting and time-series
  - All habitat and feature mapping is digital; record genuine change vs. mis-recording (REAL change vs. ERROR change).
  - Change rules differ for enclosed (lowland) vs unenclosed (upland) habitats; integrates 1998 CS data and 1990 CS data where available to support change decisions.
  - Unenclosed habitats may require back-correction of 1998 mappings due to improved vegetation detail and data processing.

- GIS workflow, system and editing
  - CS Surveyor: ArcMap extension for on-tablet data capture, editing, and change logging.
  - Data model comprises three layers: Areas (polygons), Lines (linear features with events), and Points (point features with components).
  - Editing constraints: scale <= 1:5000; Minimum Mapping Unit (MMU) is 1/25 ha (400 m2); polygons smaller than MMU not mapped unless part of a larger feature; lines must be at least 5.0 m long; lines cannot cross themselves.
  - End-session vs. save-session emphasizes regular saving; do not exit without saving.
  - Editing operations:
    - Create, modify, copy, split, merge areas; update area boundaries; mandatory fields completed.
    - Points: manage attributes for individual trees, standing water bodies, ponds, etc.; a point may have multiple components.
    - Lines: edit Woody Linear Features (WLFs) and other edges; events along lines (fences, hedges, banks, ditches) each with attributes and lengths; lines can be copied, cut, reshaped, or deleted with validation.
    - Shared nodes: modify intersections where lines share endpoints; changes propagate to connected lines; avoid creating intersections that violate topology.
    - Cut Line: define cut polygons along a line to reduce its length; results shown graphically during editing.
    - Reshape Line: adjust line shapes via edit sketches; ensure resulting edits meet minimum length constraints and do not create invalid topology.
    - Copy Tool: use features from other layers (e.g., OS Mastermap) to assist in accurate cut-line edits.
    - Delete Line: delete lines only when all events have valid Change-for-Reason values; scale must be <= 1:5000; single-line deletions.
  - Line events and attributes: each event along a line has its own attributes and length; multiple events can be edited or copied.
  - Validation and checks: unvisited linear features highlighted; status checks and loop/consistency notes for data quality (loops may require special handling if corrupt).

- Practical guidelines and rules for GIS specialists
  - If a polygon contains continuous woodland cover, assign BH/PH accordingly, regardless of other components.
  - MMU enforcement: 1/25 ha; polygons below MMU mapped only if part of a larger feature; mosaics described as component-level percentages summing to 100%.
  - Orchards: record traditional orchards as PH where appropriate; classify under Agriculture/Crops; include Orchard attribute for curtilage contexts.
  - Non-native/invasive species: record notable species within habitat polygons.
  - Output aims: provide country-wide and UK-wide reporting by BH/PH with detailed habitat attributes, change data, and woodland structure; supports time-series analyses and policy-oriented reporting; designed to ensure consistent GIS-based habitat mapping and editing practices.
  - Documentation supports field staff and GIS technicians in data capture, quality control, and the interplay between vegetation keys, BHs, and PHs.

- Quick reference highlights
  - MMU: 1/25 ha; polygon-based mapping; lines/points used when features exceed MMU thresholds.
  - Woodland mapping: two primary tools:
    - Vegetation key for BH/PH allocation linked to stands.
    - Woodland types key for structure-based attribute assignment.
  - Pond mapping: mandatory workflow with a dedicated pond recording sheet and a pre-defined selection process for survey pond.
  - Time-series focus: CS Surveyor workflow emphasizes tracking, validation, and correction of prior data to maintain a consistent time-series.

- Appendix and context (high-level)
  - CS2007 themes and CS1990/CS1990 CS2000 context provide historical codes and structures for cross-walks, with extensive code lists and data sheets to support attribute coding and change interpretation.
  - Supplementary materials cover pond sheets, field assessment references, and veteran-tree girth guidelines in separate appendices for detailed coding and interpretation where relevant.