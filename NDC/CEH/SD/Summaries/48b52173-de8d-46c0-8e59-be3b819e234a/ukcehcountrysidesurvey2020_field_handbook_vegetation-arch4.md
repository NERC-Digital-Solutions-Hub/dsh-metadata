# VEGETATION PLOTS FIELD HANDBOOK: UK-SCaPE 2020

## Overview
- Field protocol handbook for summer 2020 vegetation surveys (UK-SCaPE).
- Objective: standardised data collection to quantify vegetation change with precise, repeatable plot relocations.
- Data capture primarily digital via ESRI Survey123 (Vegplots) and Collector; paper plot maps provided as fallback.
- Data cover: plot header, relocation status, GPS/geometrics, plot photos, sketch maps, and detailed vegetation data across nested plots.

## Data Collection Workflow
- Distinguishes between new plots and repeated plots; emphasis on re-finding exact locations over time.
- Plot relocation decisions include: Found, Not Found, New Plot (Replacement for unfound), New Plot (New feature/Land cover), Not appropriate, Access Denied, Too Dangerous.
- For repeat plots, precise location is described with GPS, sketch maps, and photographs; metal plates or stakes mark locations where present.
- If relocation cannot be satisfactory, record as Not Found and create a new plot; allow relocation error where vegetation is homogeneous but be conservative in heterogeneous areas.
- New plots are allocated randomly within squares, excluding urban/inaccessible areas; five-sector overlay guides new X plot placements in scarce land.
- Data capture flow: Collector to locate plot → Survey123 forms for header and plot data → nested nest data entry (Nest 0 to Nest 5 for 200 m² vegetation plots; 2x2 m soil plots) → photos and sketch maps → data submission (online or offline with Drafts/Outbox/Sent).

## Data Model and Fields
- Plot header information (Page 1): square number, plot type (X = 200 m² or XX = 2×2 m), plot number, automatically generated Plot ID, surveyors.
- Plot relocation status (Page 1): Found, Not Found, New Plot etc.; notes on disturbance; geopoint captured (offline GPS if available).
- Plot data pages (Page 2 & 3):
  - Page 2: Plot-specific headers relevant to plot type (e.g., soil sampling details for XX plots; soil/peat depth guidance in separate handbooks).
  - Page 3: Vegetation data for nests:
    - Nest 0: presence/absence and % cover for vascular plants plus six extra categories; nested 1 m² (Nest 0) within the 200 m² X plot.
    - Nest 1–Nest 5: sequentially larger nests; species found in an inner nest may also be present in outer nests; total cover estimates provided per species across all nests.
    - Bryophytes and lichens: recorded with limited scope (only listed mosses/lichens per appendix; total bryophyte cover prioritized).
- Species entry:
  - Use dropdowns with auto-type suggestions; “Other” option for unidentified species (free text or photo), with later replacement once identified.
  - Total cover per species across all nests; ensure totals align with the recording rules (may allow slight over- or under-estimation due to layering).
- Plot photos and sketch maps:
  - Plot photos (2–3 per plot) to aid relocation; photos must show plot number/type and reference features.
  - Plot sketch maps: precise, measured drawings with GPS point, bearings, and reference features; north arrow included.

## Plot Types and Layout
- X Plots (200 m² vegetation plots): nested 14.14 m square with five nests (Nest 0–Nest 5) enabling presence/abundance records across progressively larger areas.
  - Nest 0: 1 m² inner area; Nest 1: 2×2 m; Nest 2: 4×4 m; Nest 3–5 expand accordingly to cover full 14.14 m square.
  - Location and orientation: GPS read at the south corner; plot strings/diagrams oriented NS/EW; diagonal strings used to mark nests.
- Soil Squares (2×2 m) nested within X plots for soil vegetation sampling.
- New plots have random allocation within square boundaries; in arable fields, placement starts 12 m into the crop to minimize edge effects.
- Plot layout specifics (dimensions, diagonals, and nesting) are described in detail for accurate replication and cross-survey comparability.

## Location, Relocation, and Verification Protocols
- Relocation relies on GPS geopoints, plot maps, and photos; metal plates or stakes aid relocation in many cases.
- If a reliable relocation is not possible within a reasonable time (5–10 minutes, or longer in difficult terrain), mark as Not Found and document rationale.
- If a previous plot area was refused access and later becomes accessible, prioritise repeating prior plots; add new plots only if time permits.
- In homogeneous vegetation, relocation error up to 10–20 m may be acceptable; in heterogeneous vegetation, smaller relocation errors are essential to ensure habitat type consistency.
- For arable habitats, new plots are placed 12 m into fields away from edges; if land is unfit for plot placement, do not record the plot.

## Data Quality, Validation, and Submissions
- Built-in validation checks require essential fields before submission.
- Online submission via Send Now is possible when data are complete; offline option Save Drafts/Outbox to complete later; resending creates a new survey instance for edits.
- Auto-save protects against data loss if the device crashes.
- Data management emphasizes not uprooting invasive species; photos and uncertain identifications are preferred for later confirmation.

## Habitat Classification and Taxa
- Broad Habitat and Priority Habitat assignments guide biodiversity summarisation and reporting.
- Key Broad Habitats include: Broadleaved Mixed and Yew Woodland, Coniferous Woodland, Boundary/Linear Features, Arable & Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Montane, Inland Rock, Urban, and others (with detailed descriptions and NVC associations).
- Priority Habitats include limestone pavement, inland rock outcrops, screes, calcareous/acid grasslands, dunes, reedbeds, fen communities, moorland, and urban priority types; habitat descriptions provide criteria for assignment and context for BAP reporting.
- Bryophytes and lichens: recording limited to listed mosses/lichens and total bryophyte cover; substantial emphasis on vascular plants for ecological interpretation.
- Aggregations/Combinations: where species-level identification is uncertain, recorded as amalgamated taxa to maintain consistency with previous surveys.

## Tools, Apps, and Technical Guidance
- Primary tools: Collector (ArcGIS) for navigation and plot localization; Survey123 for data forms and submission.
- Map and GPS guidance: use My Location, accuracy indicators, and alternative basemaps; GPS accuracy informs readiness for data capture.
- Offline workflows: surveys saved as Drafts or Outbox; online submission recommended when possible.
- Appendix I–II provide practical references for installation and random-number usage; Appendix III lists plot types previously recorded; Appendix IV contains habitat descriptions.

## Practical Considerations and Tips
- Metal plates may be buried or displaced; use metal detectors and multiple evidence sources (maps, photos) to confirm relocation.
- When a plot cannot be relocated precisely, ensure notes explain the uncertainty and potential impact on data interpretation.
- Avoid uprooting plants; use photos or labeling for later identification where possible.
- Documentation consistency is critical: always record and attach plot maps, photos, and clear notes about disturbances or land-use changes.

## Appendices and Reference Material
- Appendix I: Collector & Survey123 generic reference guides (installation, navigation, and data management).
- Appendix II: Random numbers table (0–1) for sampling allocation.
- Appendix III: Plot types recorded in each square across surveys.
- Appendix IV: Habitat descriptions and the vegetation key for Broad and Priority Habitats.