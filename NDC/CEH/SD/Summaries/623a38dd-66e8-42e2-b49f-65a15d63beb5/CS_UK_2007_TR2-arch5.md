# CS Technical Report No.2/07: Vegetation Plots Handbook

- This document outlines the Countryside Survey methodology for recording plant species presence and abundance across a long-term time series of vegetation plots in the UK. It covers plot relocation, addition of new plots, data capture using VegPlots and ArcMap, GPS logging, photo protocols, plot maps, and detailed protocols for every plot type (X, Y, U, A, M, H, D, S/W, R/V, B). It emphasizes standardization, data provenance, and repeatability across surveys.

## Purpose and scope
- Long-term, repeatable recording of vegetation composition to document fine-scale changes over time.
- Four key data components per plot: header (metadata), plot description, vegetation height, and species data (listed and selected species with nested plots).
- Digital data capture introduced in 2007 via Vegplots; GIS context via ArcMap; photos used to aid relocation and illustrate trends.

## Data capture and storage systems
- Primary tools:
  - VegPlots software for standard recording (header, relocation, description, height, admin, notes, listed/selected species).
  - ArcMap GIS for plot location, mapping, and integration with VegPlots.
  - Tablet-based data entry with digital photos saved to tablet directories.
- Data storage and versioning:
  - VegPlots data stored in VegPlots.mdb; when two tablets are used for a square, data are saved as VegetationPlotsA.mdb (A or B suffix).
  - Plot maps, backup maps, and plot photos stored in predefined directories (e.g., C:\CEH\squareNumber\Field_Data, New_Plot_Photos, plot_photos, 2007_plotmaps).
- Data entry workflow:
  - Locate plot in ArcMap, open VegPlots for the relevant plot, validate data, save, and exit.
  - Photographs taken to aid relocation and illustrate vegetation change; photos labeled with plot number/type and stored for later reference.

## Plot relocation, addition, and movement
- Plot relocation
  - If a prior plot position cannot be relocated confidently, it is recorded as Not Found and a new plot is created.
  - If relocation is possible, use ArcMap and photos to guide relocation; do not alter GPS positions but adjust map position as needed.
- Adding new plots
  - Triggered by unfound plots, new land-use types, new squares, or new plot types (e.g., M plots).
  - New plots are marked with metal plates or wooden stakes; labeling follows plot-type-specific conventions (e.g., Y6, etc.).
- Moving plots
  - Plots can be moved on the ArcMap map if landscape features change; not a re-location of GPS data, but a map update to reflect the current position.

## GPS locations and plot logging
- In addition to historical differential GPS data, surveyors log GPS coordinates for all plots using tablet tools.
- GPS coordinates are recorded on the ArcMap plot map with a stamp/labeling approach to tie the GPS point to the plot type and number.
- Logging GPS helps ensure repeatability and improves relocation accuracy for future surveys.

## Plot types and data collected (summary of types and data focus)
- X plots (Large/Wally plots, 200 m2)
  - Random placement with multiple nested plots (1 m2 and inner 4 m2 nests).
  - Use ArcMap five-sector overlay to select new X plots; ensure cross-feature placement rules when crossing linear features.
  - Boundary rules and marking near edges; detailed layout and orientation aligned to cardinal axes.
- Y plots (Small, habitat-targeted, 2 m x 2 m)
  - Placed in habitats not well represented by other plots; include Priority Habitat (PH) mapping.
  - Nested sampling with inner 1 m2 nest and inner 4 m2 nest; progress through nests 0–4.
  - Record Priority Habitat selection and species presence across nests.
- U plots (Unenclosed plots, 2 m x 2 m)
  - Represent unenclosed broad habitats; up to 10 plots per square.
  - Locations determined via grid-based allocation across unenclosed habitat types; relocation guided by habitat representation.
- A plots (Arable field margins, 100 m x 1 m)
  - Located adjacent to boundary plots (B); margins extending outward from the boundary.
  - Widths and distances from center of boundary feature recorded; central 4 m2 nest in nest 0 for detailed cover data.
- M plots (Margins associated with arable fields)
  - 2 m x 2 m plots to measure margins beyond cross-compliance strips; up to 3 per field depending on margin widths.
  - Distances from boundary center recorded; vegetation forming tussocks noted.
- H plots (Hedgerows, 10 m x 1 m)
  - Placed along hedges, with 10 m separation from B plots; can relocate to a nearby hedge if the original disappeared.
- D plots (Hedgerow diversity, 30 m length)
  - Focus on woody species diversity and hedge condition; D1–D10 as appropriate.
  - Detailed header data on modal height, feature width, gappiness, presence of gaps, proximity to managed land, tree canopy characteristics, historical management signs, and invasive species presence.
- S/W plots (Streamside/waterside, 10 m x 1 m)
  - Placed along watercourses near where water reaches the shoreline in the dry/wet context.
  - Header captures stream type, watercourse condition, width, and freeboard; species data recorded.
- R/V plots (Roadside and Verge, 10 m x 1 m)
  - Placed along road verges or verge types; start at interface between soil and tarmac; verge width requirements apply.
  - Location and verge characteristics recorded; species data collected.
- B plots (Boundary plots, 200 m2)
  - Located at field boundaries, prioritizing boundary features; 1 m width along boundary.
  - Placement rules depend on dominant boundary feature; when multiple features exist, dominant feature governs layout.
  - Distance to boundary feature and boundary type recorded; species data collected.
- All plot types collect:
  - Header: plot relocation status, plate detection, plot ID, slope, aspect, shade, photos, plot map status.
  - List of species with nest structure and presence/cover.
  - Selected species tab to capture estimated total cover per species and per nested plot.
  - Admin notes, occupation of plots, and any validation notes or reasons for non-recording.

## Data entry, validation, and quality assurance
- Data entry
  - Begin by locating the plot in ArcMap, then open VegPlots to record data for the selected plot.
  - Use Nest fields for nested plots; enter percent cover using a 1% step with subsequent 5% categories; total cover should reflect nested plots without double counting.
- Validation and completeness
  - Use VegPlots Validate to highlight missing fields; red highlighting indicates required fields not completed.
  - Save frequently; complete all required fields before exiting the plot screen.
- Photo and map protocols
  - Take new photos of plot locations, aiming to replicate previous survey references as much as possible; attach to support relocation and trend analysis.
  - Download photos to tablet storage; manage camera memory by deleting already-uploaded photos.
  - Plot maps should be drawn or edited as needed; indicate map status in VegPlots (NO, Edited, Redrawn).
- Plot maps and documentation
  - Provide clear and precise plot maps; include measured distances and bearings; sketches for new plots are required where maps are not adequate.
  - For new X plots, five-sector overlay and random selection are used to ensure spatial representation.

## Data governance, metadata, and provenance
- Data structure and metadata
  - Data model includes: header, plot relocation, plot description, vegetation height, admin, notes, listed species, selected species (with nest associations), and per-plot plot type specifics.
  - Nested plots (e.g., X plots with nest 0–4) require careful recording of species and cover per nest.
  - Bryophytes and lichens are recorded only from the specified lists; other taxa are generally not recorded unless specified.
- Provenance and continuity
  - The time-series design requires consistent labeling and numbering across surveys (e.g., new Y plots labeled Y6, Y7, etc.; D plots renumbered as D11+ where needed).
  - When plots are moved or relocated, maintain linkage to the original plot identity, or appropriately replace with a new plot (Not Found → New Plot).
  - Replacement plots follow the same logic as the original allocation, preserving the time-series intent and habitat representation.
- Data accessibility and sharing
  - Data are designed for long-term discovery and reuse; metadata and schema are oriented toward comparability across years and squares.
  - Data are stored in standardized formats (VegPlots, ArcMap GIS) and are intended to be uploaded to relevant data portals.

## Particular challenges and data steward considerations
- Incomplete user needs and priorities
  - Balancing the need for comprehensive vegetation data with the complexity of many plot types and protocols.
- Timeliness of data
  - Timely data entry and uploading to ensure up-to-date time-series analyses.
- Data standardization across systems
  - Coordinating VegPlots with ArcMap, GPS logging, and photo management; avoiding data overwrite when using multiple tablets.
- Interoperability and formats
  - Working with many formats (digital forms, GIS shapefiles, and database tables) across different software ecosystems.
- Large datasets and legacy data
  - Managing large time-series datasets; maintaining compatibility with older data and potentially updating integration approaches as systems evolve.
- Non-interoperable or bespoke solutions
  - Acknowledging that some square-specific adjustments may be needed due to habitat types or survey history; ensuring documentation captures these deviations for future stewardship.

## Practical takeaways for data stewards
- Enforce standardized data capture and metadata across all plot types to ensure comparability over time.
- Maintain rigorous provenance: unique plot IDs, square, type, number, GPS coordinates, and map references; document any relocations or replacements clearly.
- Use VegPlots validation and mandatory fields to minimize missing data; enforce consistent nest structures and cover categories.
- Preserve both digital and paper artifacts: maps, photos, and back-ups; ensure clear directory structures and naming conventions.
- Plan for data sharing and long-term accessibility by documenting data dictionaries, plot schemas, and data flow from field to portal.

Appendix: Key storage and workflow references (high-level)
- Data and maps: VegPlots.mdb; optionally VegetationPlotsA.mdb for multi-table tablet usage.
- GIS: ArcMap plot location maps and VegPlots integration.
- Photos and maps: Directories such as C:\CEH\squareNumber\New_Plot_Photos, C:\CEH\squareNumber\FAB\2007_plotmaps, and plot_photos; New_Plot_Photos directory for tablet uploads.
- Plot naming conventions: New plots use type-based prefixes and sequential numbering (e.g., Y6, D11); sticky notes and sketch maps accompany newly positioned plots when needed.