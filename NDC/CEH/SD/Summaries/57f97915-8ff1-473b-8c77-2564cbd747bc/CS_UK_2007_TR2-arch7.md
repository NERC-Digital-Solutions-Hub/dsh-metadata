# CS Technical Report No.2/07: Vegetation Plots Handbook v1.0

## Overview
- Standardized field manual for recording vegetation plots across Countryside Survey, enabling four longitudinal surveys over 29 years.
- Combines GIS-enabled map-based plotting (ArcMap) with tablet-based data capture (VegPlots) to log plot locations, descriptions, and species data.
- Emphasizes repeatability (re-finding plots via relocation aids, photos, and Maps) and consistent data standards across plot types.

## GIS and Data Workflow
- Plot locations and maps are managed in ArcMap; VegPlots provides the standard recording interface for each plot.
- Data and backups stored on tablets with explicit directory structures (e.g., C:\CEH\ square numbers\Field_Data\, New_Plot_Photos, 2007_plotmaps, plot_photos, New Plot Photos).
- Two tablets per team (A and B) may be used; datasets must be labeled to avoid overwriting (VegetationPlotsA.mdb vs VegetationPlotsB.mdb).
- Plot maps must be drawn, edited, and/or redrawn as needed; map edits require clear annotation (edited/redrawn) and pencil-based edits for photocopies.
- GPS logging: surveyors stamp GPS coordinates on the ArcMap plot location map and label each plot with square, plot type, and plot number; use tablet GPS to assist relocation, though non-differential GPS is the baseline.

## Plot Relocation and New Plot Protocols (GIS-Focused)
- Relocation relies on a combination of ArcMap plot maps, plot photos, and land features to find or reposition plots; precision is judged by surveyors in context.
- If a plot cannot be relocated satisfactorily, record as Not Found and create a New Plot (Replacement for unfound plot) or New Plot (New feature/Land cover).
- New plots must be marked with permanent markers (metal plates or wooden stakes) and linked to the correct plot type and square in ArcMap.
- Plot relocation decisions influence downstream data analysis (e.g., whether a plot is treated as a repeat or a new feature).

## Plot Types and GIS Layouts
- X PLOTS – LARGE, MAIN OR "WALLY" PLOTS (X1–X5)
  - 200 m² square with nested 1 m² plots; random locations guided by ArcMap points; fixed diagonals for layout; mark with metal plates near the south corner.
  - In new squares, random locations are selected with five sectors overlay; not overlapped with other plots.
- Y PLOTS – SMALL, TARGETED HABITAT PLOTS (Y1–Y5)
  - 2 m × 2 m plots in habitats not well represented by other plots; priority habitats may trigger additional Y plots.
  - Nested sampling within 1 m² nests and central 4 m² nest; total cover estimated for whole 200 m².
- U PLOTS – UNENCLOSED PLOTS (U1–U10)
  - 2 m × 2 m plots in unenclosed broad habitats; allocation based on proportion of unenclosed habitat within the square using grids; up to 10 per square.
  - Replacement plots use same basis as originals; grids and centroids guide placement.
- S/W PLOTS – STREAMSIDE PLOTS (S1–S2, W1–W3)
  - Linear plots along water features; 10 m long by 1 m wide; positioned to reflect normal water edge position.
  - Replacement plots must be placed near previous locations; ensure not within 10 m of other plots on the same feature.
- R/V PLOTS – ROADSIDE AND VERGE PLOTS (R1–R2, V1–V3)
  - 10 m long by 1 m wide along road verges; edge starts at soil/edge of tarmac; verges must be at least 1 m wide.
  - Placement can require crossing to the other side of the road if necessary; keep record of side used.
- A PLOTS – ARABLE FIELD MARGIN PLOTS
  - 100 m long by 1 m wide, located adjacent to arable margins; center aligned with B plot; up to 5 A plots per square.
  - Outer 1 m margin width sampled; central 4 × 1 m nests capture height and species data.
- M PLOTS – MARGIN PLOTS
  - 2 m × 2 m plots to quantify arable field margins; margin widths typically around 6 m; up to 3 per field depending on margins present.
  - Mark centers at specified offsets from hedge or boundary to avoid overlap with B plots.
- H PLOTS – HEDGEROW PLOTS (H1–H2)
  - Linear 10 m × 1 m plots along hedgerows; positioned to the left of the hedge center, extending into the field.
  - Maintain minimum 10 m distance from boundaries/B plots; if hedges disappear, locate on nearest remaining hedge and rename (H3, H4, etc.).
- D PLOTS – HEDGEROW DIVERSITY PLOTS (D1–D10)
  - 30 m long plots sampling woody diversity in Woody Linear Features; extensive header data capturing modal height, width, gaps, management history, etc.
  - Detailed measurements on structure and presence of woody species; invasive species and woody taxa targeted.
- B PLOTS – BOUNDARY PLOTS (B1–B5)
  - Boundary plots along 200 m plots; located at boundary closest to X plots; record boundary type and distance from centre.
  - If boundary changes, relocate to new nearest boundary with rules prioritizing dominant vertical feature.
  - A plots may be placed where margins exist adjacent to boundaries; boundary geometry governs layout.
- A PLOTS – ARABLE FIELD MARGIN PLOTS (continued)
  - Arable margins associated with B plots; A plots measure distance from centre of boundary feature and sample central 4 × 1 m nest (nest 0) plus nest 1 in the inner 4 m².
- LATERAL PLOTS – ADDITIONAL NOTES
  - All plot types include detailed nesting, coverage estimation rules, and nested sampling specifics (e.g., 1 m, 4 m, 2 m nests) where described.

## Data Capture and Field Protocols (GIS-Relevant)
- Header data captures: plot relocation status, slope/aspect/shade, photos, plot map status, and admin notes.
- Vegetation height: modal height for canopy, shrub, and ground levels; categorized into specified bins.
- Listed vs Selected Species: multi-tab species lists (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens); nested plots’ caps and cover categories (1% then 5% bands); avoid double counting overcanopy material.
- Selected Species: grow a species nest list with estimated total cover; ability to delete rows; validation ensures consistency across partners.
- Combined taxa: where species separation is difficult, use predefined combinations to maintain consistency (e.g., Cardamine hirsuta/flexuosa).
- Bryophytes and Lichens: limited to listed taxa with individual covers; detailed sphagnum classifications included for Sphagnum groups.
- Validation workflow: Save regularly; Validate to highlight missing fields; ensure plot data are finalized before exiting to avoid data loss.
- Photos and mapping: all plots should have location photos linked to the plot; photos aid relocation and trend illustration; download photos to the tablet storage after each survey.

## Plot Mapping Protocols
- Plot maps should be clear, precise, and usable; in upland areas, reference bearings from skyline features are permissible.
- Maps may include multiple plots on a single map if co-located; inadequate maps can be edited (pencil) or redrawn with measurements and bearings.
- For new plots or relocated plots, a sketch map with distances and bearings must accompany the GIS data.
- A five-sector overlay (for X plots) guides new X plot allocations in new 1 km squares.

## Practical Notes for GIS Practitioners
- Consistent naming and versioning of datasets on tablets prevent overwriting (A vs B datasets).
- ArcMap and VegPlots integration requires careful syncing to maintain plot identity (Plot ID = Square + Plot Type + Plot Number).
- Data quality control is embedded: red highlights identify missing header fields; red circles with exclamation marks flag missing data in Selected Species.
- Plot maps and photos are essential metadata for repeatability and long-term change analysis.

## Endnotes
- The document provides a comprehensive, GIS-centric methodology for planning, locating, recording, and validating vegetation plots across diverse habitats and landscape features.
- It emphasizes repeatability, standardized data capture, and robust GIS integration to support long-term ecological monitoring and analysis.