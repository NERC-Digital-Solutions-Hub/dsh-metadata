CS Technical Report No.2/07 Vegetation Plots Handbook

## Overview

- Long-term Countryside Survey method for recording plant presence and abundance in vegetation plots of multiple types and sizes.
- Goal: enable large-scale, fine-grained change detection over time (four time points across 29 years).
- Data collection moved to digital forms in 2007 using Vegplots on tablets; photos captured per plot to aid relocation; plot maps used for relocation and recording.
- Integration with GIS: ArcMap plots and Vegplots database are closely linked to locate and record plots, with data entry centralized in Vegplots.

## Data collection workflow

- Determine “the ask” and data requirements; verify data availability and consult topic experts as needed.
- Use ArcMap plot maps and Vegplots tablet software to locate the target plot and record data.
- For relocation or non-detection, follow specific protocols to mark as Found, Not Found, New Plot (Replacement), or New Plot (New feature/Land cover).
- If using two tablets, distinguish datasets (VegetationPlotsA.mdb vs VegetationPlotsB.mdb) to avoid overwriting data; upload and merge per training guidance.
- Regular saving and validation steps to minimize data loss and highlight missing fields.

## Plot types and layout (summary)

- A plots: Areal plots; 100 x 1 m edge plots adjacent to arable boundaries; contain central 4 x 1 m nest with full cover data and nest 1 for additional data.
- X plots: Large 200 m² plots (Wally plots) with nested 4 m² and 1 m² subplots (nests 0–4) to capture common vegetation types; random-location with careful placement near on-site references.
- Y plots: Small 2 m x 2 m plots in habitat patches or Priority Habitats not well represented by other plots.
- U plots: Unenclosed broad habitats; 2 m x 2 m plots, up to 10 per square; allocated to represent unenclosed habitat types proportionally.
- M plots: Margin plots measuring arable field margins (6 m width, up to 3 per field); associated with B plots; measure margin vegetation.
- Lateral/linear plots:
  - H plots: Hedgerow plots (10 m x 1 m) along hedges.
  - D plots: Hedgerow diversity; longer 30 m plots with detailed woody feature metrics.
  - S plots: Streamside plots; W plots: waterside plots; R plots: roadside; V plots: verge; all 10 x 1 m when applicable.
- B plots: Boundary plots adjacent to field boundaries (hedges, fences, walls, ditches, etc.) used when a boundary feature defines the plot location.
- A plots (arable margins) and M plots (margins) are tied to B plots and measure vegetation beyond cross-compliance margins (M plots measures margins extending into the cropped area).
- Plot placement rules emphasize non-overlap, minimum distances (e.g., 10 m apart for linear plots of same type), and prioritization of dominant boundary features.

## Data capture and fields (VegPlots)

- Header data:
  - Plot relocation status (Found, Not Found, New Plot Replacement, New Plot New feature/Land cover, Not appropriate, No Longer Required, Access Denied, Too Dangerous).
  - Plate detected? (Yes/No/No (new plate buried)/No plate to find).
  - Plot ID: square, plot type, plot number, and a combined Plot ID.
  - Plot description: slope, aspect, shade, photos taken, plot map drawn/edited.
  - Admin: surveyor initials; whether plot completed; notes describing lost plots or reasons not recorded.
- Plot maps: new maps drawn or edited/redrawn; sketch maps for new locations and boundary features.
- Plot location and GPS:
  - GPS coordinates recorded for plots to aid future relocation; stamps and labels used to mark plot type and number on ArcMap.
  - For some plots, older non-differential GPS outlines may exist; current practice logs GPS coordinates on the ArcMap plot map.
- Photo protocol: take 1–2 repeatable photos per plot to aid relocation; photos labelled with plot type/number; download photos to a dedicated folder on the tablet; erase camera memory as needed during the survey.
- Plot description and nesting: lists of species (Listed Species and Selected Species) across nested plots; presence/absence and cover estimates recorded per species; total cover checks across nests.
- Nested plots and coverage:
  - X plots use nested 4 m² inner and surrounding nests (0–4) with 5% cover bands; total cover aggregated across nests.
  - Y plots and others record species presence per nest and aggregate totals where applicable.
- Aggregations/Taxa:
  - Some amalgamated taxa are used when species-level identification is uncertain; use combinations only when separate species identification is not possible.
- Bryophytes and lichens:
  - Only pre-defined bryophytes/lichens lists are recorded, with individual covers.
- Data validation:
  - Use Vegplots Validate to highlight missing fields; ensure header and Selected Species data are complete before finalizing.
- Data output:
  - Data stored in VegPlots MDB/ACE-style databases; linked to ArcMap for plot maps and relocation; outputs intended for long-term trend analysis and cross-time comparisons.

## Species data structure

- Listed Species: broad groupings and taxa across different species groups (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody species, Mosses/Lichens, etc.), with presence and cover data.
- Selected Species: per plot, as species are ticked in the lists; nest-based data entry for cover (5% bands) and overall total cover across the plot.
- Coverage rules:
  - Presence entries use 1% increments up to 5% increments; total cover may exceed 100% due to multiple layers but avoid double counting overlapping components.
  - Some species recorded as trees/shrubs with canopy overhanging plots are included with appropriate cover estimates.
  - Bare ground excludes leaf litter and rocks.

## Data quality and challenges (from the handbook perspective)

- Relocation accuracy: relocation relies on maps, photos, and GPS history; moving plots is allowed only within map-based references, not by GPS alone; not-found plots require careful documentation to avoid false repeats.
- Patchy data: long-running time series and patchy data across years; some squares may have missing plots or changed habitat types due to land-use changes.
- Data consistency: standardization across many plot types and nested data requires disciplined data entry and adherence to species lists and nest structures.
- Map quality: plot maps must be clear and usable; edited/redrawn maps require appropriate notation; new plots need unique labeling to prevent duplication.
- Data harmonization: combining outputs across different plot types and years requires careful handling of nested plots, habitat classifications, and taxonomic aggregations.

## Operational considerations for data use

- GIS-centric workflow: primary geospatial location, plot maps, and GPS coordinates drive data capture and subsequent analyses.
- Data provenance: every plot entry carries a square, plot type, plot number, and plot ID, ensuring traceability across surveys.
- Documentation: the handbook provides thorough protocols for each plot type, including placement rules, relocation procedures, and data fields essential for analysis.
- Long-term value: designed to produce a globally unique dataset enabling analysis of vegetation change over decades, with standardized data capture enabling cross-year comparisons.