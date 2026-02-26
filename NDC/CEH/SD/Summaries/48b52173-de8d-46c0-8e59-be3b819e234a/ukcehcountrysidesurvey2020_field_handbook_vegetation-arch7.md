# VEGETATION PLOTS FIELD HANDBOOK: UK-SCaPE 2020

## Overview
- Field protocol for UK-SCaPE 2020 focusing on vegetation plots to quantify changes in the countryside with high spatial precision.
- Data collected include plot header information, plot-specific details, photos, sketch maps, and detailed vegetation data.
- Data collection uses ESRI Survey123 (Vegplots) and Collector apps; paper plot maps used for relocation and as backups; digital copies available on tablets.

## Plot Types, Layouts and Spatial Data Model
- Two plot sizes:
  - 200 m² VEGETATION PLOT (X plot) with nested 1 m² and larger nest structures along diagonals.
  - 2 m × 2 m SOIL plot (XX plot) nested within the larger plot.
- Nest structure for 200 m² plots:
  - Nest 0 through Nest 5, increasing from inner 1 m × 1 m to the full 14.14 m × 14.14 m area.
  - Species data entered per nest with cumulative cover estimates; bryophytes limited to common soil bryophytes.
- Plot location and geometry:
  - X plots are positioned at five predetermined random points inside a square; GPS coordinates captured at the south corner of the plot when possible.
  - If relocation is uncertain, plots may be recorded as Found, Not Found, New Plot (Replacement for unfound plot), or New Plot (New feature/Land cover).
  - Plot markers include aluminium plates or wooden stakes to aid relocation; metal detectors provided.
  - For arable fields, plots are positioned 12 m into the crop to minimize edge effects.
- Plot relocation and mapping:
  - Plot relocation relies on GPS, sketch maps, and photographs; travel to locate plots using the Collector map and plot symbol.
  - If a prior plot cannot be satisfactorily relocated, record as Not Found and create a new plot.
  - Five-sector overlay (XPlotSectors) used to identify new feasible locations when land permits.
- Plot header and map data:
  - Plot header includes square, plot type (X or XX), plot number, plot ID, surveyors, slope, aspect, location, and photos.
  - Plot maps: Plot Map drawn/edited/redrawn; GPS location captured; notes describe disturbances or reasons for not recording.
- Plot documentation:
  - Plot Photo Protocol: 2–3 photos to aid relocation, with a weatherwriter label showing plot type and number; photos should show unique nearby features.
  - Plot Sketch Map Protocol: precise, measured sketches with GPS readouts, north arrow, and clear labeling (Square, Plot number, date, surveyors).
- Data capture flow (GIS-friendly):
  - Use Collector to navigate to a plot and open the Survey123 form for data entry.
  - Header (page 1) → Plot header and relocation info; Page 2 → Plot-specific headers; Page 3 → Vegetation/Soil data (Nest data).

## Data Entry Details and Species Recording
- Page 3 data structure:
  -VEGETATION SQUARES (ground flora) or SOILS SQUARES (ground flora in 2×2 m nest).
  -Nested nest structure for vegetation: presence/absence and percent cover for major vascular plants plus six additional categories (litter, wood, rock, bare ground, water, bryophytes).
- Nest-specific recording:
  - Nest 0: presence/absence and initial cover for all vascular plants; total cover estimated to ~100%.
  - Nest 1–Nest 5: additional species found as nests are expanded; total cover estimates updated for each nest.
- Bryophytes and lichens:
  - Recorded selectively (mosses listed in Appendix IV and Bryophyte lists); prioritise vascular plants and overall total bryophyte cover.
- Data cleanliness:
  - The software allows blank or duplicate entries; reviewers must ensure no erroneous blanks/duplicates remain.
- Aggregations/Combinations:
  - Some taxa are combined (e.g., Cardamine hirsuta/flexuosa) when species-level separation is not reliable; invasive uprooting is discouraged.

## Habitat Classification and Descriptions
- Broad Habitat categories (for GIS tagging and BAP reporting) include:
  - Broadleaved Mixed and Yew Woodland, Coniferous Woodland Broad Habitat, Boundary/Linear Features, Arable & Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Water, Montane Broad Habitat, Inland Rock, Urban, Supra-Littoral Rock, and various Priority Habitats (e.g., Limestone pavement, Inland rock outcrops, Sand dunes, Saltmarsh, Reedbed).
- Habitat assignment:
  - Based on plant composition, discrete polygons, and plotted vegetation; Priority Habitats nested within Broad Habitats.
  - Annexed habitat descriptions and NVC associations guide consistent habitat allocation.
- Special notes:
  - Clear guidance on how to record habitats after disturbances (e.g., post-felling conifer areas may become heathland or remain coniferous woodland depending on vegetation cover).

## Data Submission, QA and Data Management
- Online submission when online; offline capability with Drafts/Outbox/Sent status:
  - Send Now for immediate central database submission; Copy to new survey for edit capability after submission.
  - If offline or mid-survey, data saved in Drafts or Outbox.
  - Auto-save reduces data loss if a device crashes.
- QA considerations:
  - Ensure all essential fields are completed before submission.
  - Verify relocation status and document reasons for non-recording.
  - Relocation accuracy is acceptable within reasonable errors, especially in homogeneous habitats; higher caution in heterogeneous landscapes.
- Data architecture and accessibility:
  - Central database stores plots, nest-level vegetation data, plot headers, sketch maps, and photos.
  - Survey123/Collector integration provides a GIS-friendly data capture workflow.
- Appendices and tools:
  - Appendix I: Generic references for Collector and Survey123 installation and usage.
  - Appendix II: Random number table (for random X plot positioning).
  - Appendix III: Plot types recorded in previous surveys (to maintain comparability).
  - Appendix IV: Habitat descriptions (to support Broad/Priority Habitat classification).

## Practical GIS-Focused Notes for Implementation
- Data interoperability:
  - Plot data integrates with GIS in terms of polygon geometry (1 km square extents) and nested nest coordinates for 200 m² plots.
  - Attribute schema should capture: square, plot_type, plot_number, plot_id, surveyors, slope, aspect, location, relocation_status, plot_map_status, habitat_code (Broad/PH), nest-level species lists, cover values, bryophyte indicators, incident notes, photos/sketch map references.
- Data quality gates:
  - Validate total cover sums per nest and per plot.
  - Enforce species lists with auto-complete and a fallback for “Other” entries to maintain data capture continuity.
- GPS and offline workflows:
  - Leverage offline GPS where available; ensure synchronization when online for central submission.
  - Use Location Averaging and multiple basemaps to improve georeferencing accuracy when re-finding plots.
- Documentation alignment:
  - Habitat codes and descriptions align with JNCC and NVC frameworks; ensure GIS users map polygons to corresponding Broad/PH categories.
- User guidance:
  - Follow Plot Photo and Plot Sketch Map protocols to maximize repeatability of plot relocation.
  - When in doubt about relocation, document rationale in Notes and mark the plot as Not Found if necessary.

## References and Appendices (for GIS teams)
- Appendix I: Collector & Survey123 – generic reference guides and app usage flows.
- Appendix II: Random numbers between 0 and 1 (for random X-plot placement).
- Appendix III: Plot types recorded in previous surveys (structure and naming, e.g., X plots, soil plots, boundary plots).
- Appendix IV: Habitat descriptions and Priority Habitat details (extensive glossaries and classifications).