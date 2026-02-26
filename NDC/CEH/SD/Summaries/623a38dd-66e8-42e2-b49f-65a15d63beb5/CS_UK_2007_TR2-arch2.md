# CS Technical Report No.2/07: Vegetation Plots Handbook

- A comprehensive guide for recording vegetation data across standardized plot types to document long-term environmental change.
- Enables consistent four-point surveys over the last 29 years, creating a globally unique time-series dataset of vegetation composition and habitat change.
- Data are collected from established plot types, logged via forms-based Vegplots software on tablets, and stored with accompanying maps and photos for repeatability and scrutiny.

## Objectives and Data Outputs

- Capture general plot information, species presence and cover, and plot-specific descriptors to enable temporal analysis of environmental health and habitat change.
- Produce standardized outputs (datasets, plots, maps, and photos) suitable for policy and health assessments over time.
- Ensure datasets are stored and accessible through appropriate portals, enabling reuse and integration with other environmental data.

## Data Collection Workflow and Tools

- Establish and maintain plots using predefined protocols; relocate, add, or replace plots as land use changes or new habitat types are encountered.
- Primary data capture tools:
  - Vegplots forms-based software on tablets for standardized data entry.
  - ArcMap GIS for plot location mapping and integration with Vegplots.
  - Digital plot photos captured at each survey for relocation and trend illustration.
- Data entry sequence:
  - Locate plot in ArcMap, open Vegplots and begin standard recording.
  - Use headers, listed species, and selected species tabs to capture data.
  - Validate data and save frequently to minimize data loss; back-up procedures described.
- Data management:
  - Two tablets may be used per team; datasets must be labeled A or B to prevent overwriting when uploading.
  - Plot maps, GPS coordinates, and photos are stored in designated directories and backed up.

## Plot Relocation, New Plots, and Movement

- Plot relocation:
  - Use ArcMap and plot photos to re-find previously recorded plots; relocate with caution to avoid misclassification of habitat type.
  - If relocation is not feasible, record as Not Found or replace with a new plot, with appropriate designations.
- Adding new plots:
  - New plots arise from missing plots, new land-use features, or new plot types (e.g., M, Y, etc.).
  - New plots must be clearly identified and properly mapped to avoid treating as repeats.
- Plot movement:
  - If landscape features shift, plots can be moved on the GIS map, but not based on GPS alone.
- Plot IDs and labeling:
  - New plots receive new identifiers (e.g., Y6, U7) to avoid confusion with historical repeats.
  - ArcMap map editing requires saving edits to make newly positioned plots available for Vegplots.

## GPS and Location Logging

- GPS data logging:
  - Tablets provide non-differential GPS; use GPS as an aid alongside maps and photos.
  - Surveyors stamp and label GPS locations on the map with plot type and plot number.
- Location accuracy:
  - Relocation judgments are made by surveyors, balancing homogeneity of habitat and risk of misclassification; documented in the header.

## Plot Types and Layouts

- X PLOTS – LARGE, MAIN or “WALLY” PLOTS (X1–X5)
  - 200 m2 plots (14.14 m square) with nested subplots (1 m2 nest inside a 4 m2 nest; inner / outer nests 0–5).
  - Random sampling of common vegetation types; vertical/horizontal alignment with reference to nearby features.
  - Marked with metal plates or stakes; use random points for new placements in new squares; five-sector overlay guides feasibility in certain sectors.
- Y PLOTS – SMALL, TARGETED OR HABITAT PLOTS (Y1–Y5)
  - 2 m x 2 m plots placed in interesting habitats or Priority Habitats (PH) not well represented by other plots.
  - Nest scheme similar to X plots (Nest 0 through Nest 4) with multi-nest data collection and central nest for total cover.
  - PH identification required; random selection of patches when multiple PH areas exist.
- U PLOTS – UNENCLOSED PLOTS (U1–U10)
  - 2 m x 2 m plots in unenclosed broad habitats; up to 10 per square based on habitat extent.
  - Placement guided by broad habitat mapping; relocation assessed case-by-case due to relocation difficulty.
- A PLOTS – ARABLE FIELD MARGIN PLOTS (A1–A3)
  - Located adjacent to boundary features bordering arable fields; up to 5 plots per square.
  - 100 m long x 1 m wide plots with the outer 1 m in the arable field; central nest (nest 0) and secondary nest (nest 1) data captured.
- M PLOTS – MARGINS (M1–M4/5)
  - 2 m x 2 m plots recording margins associated with B plots (hedges, boundaries) and various margin types (grass margins, wildflower mixes, etc.).
  - Placement away from edge to ensure margin measurement accuracy; margins extend outward in defined intervals.
- H PLOTS – HEDGEROW PLOTS (H1–H2)
  - Linear 10 m x 1 m plots along hedgerows; relocation to nearby hedges if original feature disappears.
  - Data include vegetation presence, all listed species, and habitat-related notes; spacing requirements relative to B plots.
- D PLOTS – HEDGEROW DIVERSITY PLOTS (D1–D10)
  - 30 m long plots along woody linear features to capture woody species diversity, structure, gaps, and disturbance.
  - Detailed header fields cover modal height, width, gappiness, historic management, and presence of invasive or notable species.
- S/W PLOTS – STREAMSIDE AND WATERSIDE PLOTS (S1–S2, W1–W3)
  - Linear plots along clean, permanent watercourses; inclusion criteria consider water depth, flood status, and proximity to boundaries.
  - 10 m long x 1 m wide; records cover stream type, width, watercourse condition, and presence of listed species.
- R/V PLOTS – ROADSIDE AND VERGE PLOTS (R1–R2, V1–V3)
  - Linear plots along roadsides and verges; placed near the X plots while respecting safety and habitat integrity.
  - Road type and verge characteristics documented; species lists recorded with cover estimates.

## Data Collected per Plot

- Header information:
  - Plot identification (Square, Plot Type, Plot Number, Plot ID)
  - Relocation status (Found, Not Found, New Plot, Replacements, Not Appropriate, Access Denied, etc.)
  - Plot description (slope, aspect, shade, photos, plot map status)
  - Vegetation height across canopy, shrub, and ground layers
  - Admin details (surveyors, initials, completion status, validation)
  - Notes on plot loss, relocation challenges, and non-viable plots
- Listed species and Selected species:
  - Nested plots capture species in each nest; presence/absence and 5% cover bands (1% increments for initial entries)
  - Comprehensive species lists by group (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody species, Mosses/Lichens)
  - Unidentified species handling (A–C, D–Z entries for later identification)
  - Totals and cross-checking to prevent over- or underestimation of cover
- Plots’ nested structure and Nest fields:
  - Nest 0, Nest 1, ... up to Nest 5 for X plots; nest allocation guides cover calculations for total plot cover

## Data Quality, Validation, and Output

- Validation workflow:
  - Use Validate to highlight missing fields; color-coded prompts indicate incomplete data
  - Save frequently; exit prompts require prior validation
- Plot completion and relocation notes:
  - Explicit handling of “Not Found,” “New Plot,” “Replacement,” “Not Appropriate,” and “Too Dangerous” cases
  - Plot photos are required or strongly encouraged to aid future relocation
- Data storage and sharing:
  - Vegplots data stored as local databases (e.g., VegPlot s.mdb/A and VegPlotsA.mdb) with scanning and uploading procedures
  - Photos organized in dedicated folders; periodic data uploads to central portals as per project guidelines

## Plot Maps and Documentation

- Plot maps are essential; new maps must be clear, precise, and include measurements and bearings
- If pre-existing map data are inadequate, editors should annotate maps (Edited/Redrawn) and re-submit with updated measurements
- Sketch maps are used for new plots or relocated plots, clearly labeled with square and plot identifiers
- Plot type-specific maps and locations rely on ArcMap overlays and ArcGIS-based workflows; back-up maps retained

## Taxonomy, Aggregations, and Special Considerations

- Aggregations:
  - Certain species are grouped into combinations where accurate separation is difficult; use combined taxa where necessary
- Bryophytes and Lichens:
  - Only bryophytes and lichens on the specified list are recorded, with respective covers
- Sphagnum:
  - Detailed sub-typing of Sphagnum mosses used for consistent identification
- Habitat-specific considerations:
  - Priority Habitat (PH) tagging for Y plots in 2007; habitat-specific selection and randomization for Y plots
  - Boundary, hedgerow, streams, and verge interactions define how other plots are positioned and recorded

## Accessibility and Data Sharing Implications for Analysts

- Emphasizes the value of well-documented plots for cross-survey analysis and integration with other data sources.
- Encourages sharing underlying data and metadata to enable broader scrutiny of environmental health and policy performance.
- Provides a structured, repeatable data capture framework enabling robust longitudinal environmental assessments.

## Context and Funding

- Countryside Survey (CS) 2007 edition; funded by a partnership led by NERC and Defra
- Publication intended to standardize long-term vegetation Monitoring and facilitate data-driven environmental health assessments