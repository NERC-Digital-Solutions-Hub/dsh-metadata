# CS Technical Report No.2/07: Vegetation Plots Handbook v1.0

- The document is a comprehensive, field-ready protocol for recording vegetation presence and abundance across a wide range of plot types as part of Countryside Survey 2007, enabling repeated, four-point change documentation over 29 years.
- It integrates paper and digital data capture via VegPlots on tablets, with spatial context provided by ArcMap plot maps, plot photos, and tablet-stored plot maps/photos for relocation and verification.
- Data collection emphasizes consistency, traceability, and metadata: each plot has header information, plot maps, photos, and a nested data structure for species and cover.

## Workflow and Data Management

- Plot relocation and new plot procedures are tightly linked to ArcMap and VegPlots, with back-up maps/photos stored on tablets and in paper form.
- Surveyors log GPS coordinates during recording, and, where possible, use historical GPS outlines to aid relocation.
- Plot data entry starts by locating the plot in ArcMap, then launching VegPlots to record data on a Standard Recording screen; plots are identified by a unique Plot ID (Square + Plot Type + Plot Number).
- Data validation is required before exiting a plot; missing fields are highlighted, and photos should be re-taken if relocation proves difficult.
- Multiple tablets can be used per square (A or B datasets) as long as data are kept separate to avoid overwriting; data are stored in VegPlots.mdb (or VegetationPlotsA.mdb / VegetationPlotsB.mdb) and uploaded per training instructions.
- Plot maps must be precise, especially when new plots are added; edited/redrawn maps must be clearly annotated.

## Plot Recording and Header Structure

- Header information covers relocation status, plate detection, GPS labeling, plot description (slope, aspect, shade, photos, and map status), vegetation height in three strata, and admin notes.
- The system distinguishes between:
  - Plot relocation outcomes (Found, Not Found, New Plot, New Feature/Land Cover, Not Appropriate, Access Denied, etc.)
  - Plate status (plate detected, buried plate, no plate)
  - Administrative notes and plot completion status
- The Nested/Selected Species structure records all identified species, their nest location, and estimated total cover in percentage bands (1% initial, then 5% bands); species lists can include unidentified records for later identification.

## Plot Types and Protocols (per square)

- X PLOTS – LARGE, MAIN OR “WALLY” PLOTS (X1–X5)
  - 200 m² plots with nested 4 m² inner plots; built to sample common vegetation types.
  - Located using random points; if crossing a feature, place at vegetated land with a 3 m minimum buffer from the edge.
  - Marked with plates or stakes; precise placement governed by a five-sector overlay when locating new plots.
  - Not found plots and new plots require careful handling; replacement plots are positioned within the same habitat area where possible.

- Y PLOTS – SMALL, TARGETED HABITAT PLOTS (Y1–Y5)
  - 2 m × 2 m plots placed in habitat patches not well represented by others, including Priority Habitats (PH) when applicable.
  - Nested structure (nest 0 = 1 m²? central 4 m² nest; nest 1 onwards for additional sampling).
  - Priority Habitat field recorded; habitat patches chosen randomly among patches of the same PH when multiple patches exist.

- U PLOTS – UNENCLOSED PLOTS (U1–U10)
  - 2 m × 2 m plots placed in unenclosed Broad Habitats; up to 10 per square, allocated according to habitat extent.
  - Location uses a grid/fishnet approach to ensure representation proportional to habitat area; new plots placed in the center of gravity if “hit” points are too small.
  - Relocation is challenging; careful judgement to ensure plots remain representative of the habitat type.

- LAYOUT FOR STREAMSIDE AND VERGE PLOTS
  - S PLOTS – STREAMSIDE; W PLOTS – WATERWAYS; linear plots alongside watercourses
  - Each is 10 m long by 1 m wide; position relative to water boundary and reference features; replacement plots positioned close to prior locations when features persist.
  - Only permanent water features included; proximity to existing Boundary plots (B plots) is minimized (no part of a streamside plot within 10 m of a Boundary plot).

- R PLOTS – ROADSIDE AND VERVE PLOTS (R1–R2) and V PLOTS – VERGE
  - 10 m long by 1 m wide, located along road verges or roadside features; edge defined by the interface with soil and infrastructure; placement may require side changes if road layout changes.

- B PLOTS – BOUNDARY PLOTS (B1–B5)
  - Located at the boundary marker of 200 m plots in enclosed land; precedence over other linear plots when adjacent to a boundary.
  - Recording involves distance to ploughed edge, boundary type, and boundary feature characteristics.

- A PLOH PLOTS – HEDGEROW PLOTS (H1–H2)
  - Linear 10 m × 1 m plots along hedgerows; relocated along hedges if the original hedge changes or disappears; typically placed to the left of the hedge as viewed from the field.

- D PLOTS – HEDGEROW DIVERSITY PLOTS (D1–D10)
  - 30 m long by 1 m wide; baseline data on woody species diversity and hedgerow condition, including gappiness, canopy structure, and historic management indicators.
  - Extensive header metrics cover height, width, vertical gappiness, presence of managed trees, and invasive species presence.

- S/W / A / M / H / D – Taxa and habitat specifics
  - Bryophytes and lichens are sampled from the prescribed lists; certain taxa combinations are used when species identification is uncertain.
  - Sphagna (Moss species) have a detailed sub-classification for green/thin and red/thin forms.

- A PLOTS – ARABLE FIELD MARGINS (A1–A3)
  - Arable field margins (100 m × 1 m) located along boundaries adjacent to arable land; nest 0 (central 4 × 1 m) for cover and nest 1 for presence only; extent from hedge center outward to avoid edge effects.

- M PLOTS – MARGINS (M4+5)
  - Margins associated with cross-compliance or arable margins; 2 × 2 m plots with 6 m margin widths, arranged to measure margins beyond the hedge edge with specified distances from the center.

- A LAYOUT AND MAXIMUMS
  - Maximum plots per square vary by type (e.g., up to 5 X plots; up to 10 U plots; up to 5 A plots; up to 3 M plots per square depending on margins).

## Species Recording and Taxonomy

- A single, unified approach to species presence and cover; considerations for combinations where taxa are difficult to separate (e.g., Cardamine hirsuta/flexuosa).
- Bryophytes and lichens are recorded using the designated lists; other bryophytes/lichens outside these lists are not recorded.
- Invasive species, including several Acquisitions (e.g., Fallopia spp., Heracleum mantegazzianum, Impatiens glandulifera), are specifically tracked with presence/absence in D plots.
- Nested plots (for X plots) require careful accounting of species across nests, with total cover calculated across the entire 200 m² plot.

## Data Quality, Validation, and Special Considerations

- Plot relocation accuracy is prioritized; if relocation cannot be confidently achieved, plots are recorded as Not Found and may be replaced with new plots, with clear documentation on relocation limitations.
- Data validation highlights missing fields; photos associated with plots are used to aid relocation and document changes across surveys.
- Plot maps must be drawn carefully, with references to distant landscape features permitted when necessary; maps may be edited or redrawn if landscape features have changed.
- The five-sector overlay is used to determine feasible Y/X plot allocations and to guide the placement of new X plots when there are constraints.
- Aggregations and combinations: when species cannot be separated confidently, combinations from the BRC list are used for consistency across surveys.
- Data outputs emphasize discoverability and reuse: plots and datasets are logged with metadata, and field data entry is designed to be reproducible and traceable across survey cycles.

## Plot Photos, Maps, and Documentation

- Plot relocation uses a combination of ArcMap plot maps, plot photos, and on-tablet digital plot maps for robust relocation and re-identification in future surveys.
- All plot photos are recorded to facilitate relocation and trend analysis, with guidelines for consistent phrasing (e.g., include plot number and type on each photo).

## Additional Information

- The document provides detailed protocols for each plot type, including dimensions, nest structure, placement rules, and data fields to be completed within VegPlots.
- It includes figures and tables guiding layout (e.g., plot geometries, five-sector overlay, grid-based allocation for U plots, and B/W/R/V/A plot configurations).
- It concludes with copyright,Disclaimer, and contact information for Countryside Survey/CEH.

- Overall, the Vegetation Plots Handbook provides a standardized, data-rich framework for capturing long-term vegetation data across a diverse set of plot types, balancing precise field geometry with flexible relocation and combination strategies to sustain a coherent, comparable time series.