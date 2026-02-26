# CS Technical Report No.2/07: Vegetation Plots Handbook v1.0

- Purpose and scope
  - Establishes standardized, repeatable vegetation-plot methods to document plant presence and abundance across diverse plot types.
  - Enables large-scale, fine-grained change detection over time to inform policy, management decisions, and future monitoring.
  - Supports long-term time series by providing detailed relocation, data collection, and data-management protocols.

- Core approach to monitoring and data management
  - Combine field plots with GIS (ArcMap) and a forms-based digital tool (VegPlots) to capture consistent header, species, and plot data.
  - Emphasize repeatability: precise relocation (where possible) using plots, photos, maps, and GPS aids; document relocations and any changes.
  - Public data and metadata considerations: ensure data provenance, plot maps, photos, and underlying data are available for verification and reuse; specify when and how data can be shared.

- Plot relocation, addition, and lifecycle
  - Relocation: use ArcMap plot maps, plot photos, and instrumented marks to re-find plots; move only when relocation to the correct habitat is verifiable; do not relocate by GPS position alone.
  - Not Found vs New plots: if a plot cannot be relocated satisfactorily, record as Not Found or New Plot (Replacement for unfound plot) or New Plot (New feature/Land cover); maintain an audit trail of decisions.
  - Adding new plots: criteria include lost plots, new square survey requirements, land-use changes, or new habitat types; permanently mark new plots with metal plates or wooden stakes and label systematically to avoid duplication.
  - Plot labeling: new plots in a square must be labeled to avoid treating them as repeats (e.g., Y6, U7) except when a new feature necessitates it.

- Data capture workflow and tooling
  - VegPlots tablet software: start from a map-selected plot, then use VegPlots for standardized data entry; use the Validate, Save, and Exit workflow to ensure completeness.
  - Dual-tablet workflows: if two tablets are used per square, label datasets A or B (e.g., VegetationPlotsA.mdb, VegetationPlotsB.mdb) to prevent overwriting.
  - Plot headers and nests: main header information (plot location, type, slope, aspect, shade, photos, maps) and nested data (Listed Species, Selected Species) per plot type.
  - Photos and maps: take repeatable photos for relocation; download photos to a central New_Plot_Photos directory; maintain plot maps (paper and digital) with edits clearly marked (Edited, Redrawn).

- Plot types and their sampling design (summary)
  - X PLOTS – LARGE, MAIN OR WALLY PLOTS (X1–X5)
    - Size: 200 m² (approximately 14.14 m × 14.14 m); contains nested 1 m² to 4 m² subplots.
    - Purpose: random sample of common vegetation types; two to five nested subplots across the 200 m².
    - Locating: use random points; if crossing a feature, place on vegetated land with the boundary near field edges; record with a mismatch if necessary.
  - A PLOTS – ARABLE FIELD MARGIN PLOTS (A1–A3)
    - Location: adjacent to boundary plots bordering arable fields; maximum up to 5 per square.
    - Size: 100 m × 1 m (outermost cultivated metre) extending 50 m from the B plot center.
    - Data: nested nest 0 (inner 4 × 1 m) for cover and presence, nest 1 for presence only.
  - M PLOTS – MARGIN PLOTS (2 m × 2 m)
    - Purpose: assess margins related to cross-compliance and agri-environment schemes; margins typically up to 6 m wide.
    - Placement: to ensure margins beyond the cross-compliance strip are measured; multiple plots per square as margins extend.
  - H PLOTS – HEDGEROW PLOTS (H1–H2)
    - Type: linear 10 m × 1 m plots positioned along hedges; locate on the hedge with 1 m extending into the field.
  - D PLOTS – HEDGEROW DIVERSITY PLOTS (D1–D10)
    - Purpose: baseline woody species diversity and hedgerow condition; long 30 m plots with data on structure and gaps.
    - Header metrics include modal height, width, vertical gappiness, presence of lines of management, and invasive/broad woody characteristics; woody species presence and cover recorded.
  - S PLOTS / W PLOTS – STREAMSIDE PLOTS (S1–S2, W1–W3)
    - Location: along watercourses; 10 m plots with 1 m width extending landward from water edge.
    - Data: stream type, watercourse condition (dry/wet/flood), width, freeboard, and species presence/cover.
  - R PLOTS / V PLOTS – ROADSIDE AND VERGE PLOTS (R1–R2, V1–V3)
    - Location: along roadsides and verges; 10 m × 1 m plots starting at the interface of soil and tarmac (verges may be on either side of the road).
    - Data: road type, and species presence/cover.
  - U PLOTS – UNENCLOSED PLOTs (U1–U10)
    - Location: unenclosed broad habitats; two-by-two metre plots; up to 10 per square.
    - Allocation: based on extent of unenclosed habitat; random placement within broad habitat types using grid/overlay logic; relocation guidance depends on habitat persistence.
  - Y PLOTS – SMALL, TARGETED OR HABITAT PLOTS (Y1–Y5)
    - Location: 2 m × 2 m plots placed in habitat patches, including Priority Habitats (PH) not sampled by other plots.
    - PH assignments: up to 22 PH options; random selection among patches when multiple patches exist.
    - Nested sampling: nest 0 (1 m²) and central nest 1; cover estimates by nested 5% bands; total cover across nests aggregated.
  - LAYING OUT AND RELOCATION GUIDELINES
    - For all plot types, ensure minimum separation between plots on the same feature, avoid overlap between different plot types where specified, and measure true horizontal width when on slopes or banks.
    - Boundary features (hedges, fences, walls, ditches, grass strips, banks) guide placement and nesting.

- Species recording and data quality
  - Listed species: full vascular plant list with presence and cover estimates; certain bryophytes and lichens are included according to plot type.
  - Selected species: nest-based recording with presence/absence and percent cover (5% bands); supplements with BRC lists; avoid double counting overhangs or nested material.
  - Aggregations/combinations: some taxa are amalgamated (e.g., Cardamine hirsuta/flexuosa) when distinction is uncertain; use the separate or combined nomenclature as appropriate.
  - Data validation: regular saving, field validation, and red flags on missing fields; photos to illustrate plots; ensure all nest plots are accounted for and total cover is checked.

- Plot maps, documentation, and governance
  - Plot maps are essential for relocation; edits must be clearly recorded (Edited, Redrawn) with initials and date.
  - Sketch maps accompany new plot allocations, with measurements and compass bearings; if maps run out, continue on blank sheets with square/plot identifiers.
  - Documentation and data sharing: maintain traceable origins of plots, photos, and maps; data can be shared for research under the project’s governance; official guidance provided in the Countryside Survey program.

- Practical considerations and challenges
  - Data gaps and access: relocation can be difficult in older plots or where markers are buried or moved; precise relocation relies on a combination of maps, photos, and field judgment.
  - Habitat changes: land-use changes may necessitate introducing new plots or replacing plots; strict rules govern how to record replacements and new features.
  - Time and resource constraints: some plots (e.g., D plots in Scotland) may require adaptation; ensure time series consistency while acknowledging local variations.
  - Technical constraints: tablet-based data entry requires careful data management to avoid overwriting datasets when multiple devices are used.

- Outputs and intended use
  - The handbook provides a comprehensive, repeatable framework for collecting vegetation data that underpin long-term monitoring of environmental health and biodiversity.
  - Outputs include standardized plots, nested sampling data, species lists with cover, and plot-level metadata suitable for aggregation across time and space to inform environmental policy and management decisions.