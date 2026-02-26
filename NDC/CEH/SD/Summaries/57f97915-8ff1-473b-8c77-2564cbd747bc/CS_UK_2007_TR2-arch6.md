# CS Technical Report No.2/07: Vegetation Plots Handbook

## Overview and Purpose
- Documents the Countryside Survey vegetation plot methodology used to record plant species presence and abundance in various plot types.
- Enables a globally unique, long-term dataset to document vegetation change over time (four survey points over 29 years).
- Data collection relies on VegPlots software, ArcMap GIS, and digital photos, with GPS support to aid plot relocation.
- Emphasizes repeatability, data quality, and the ability to compare plots across survey rounds.

## Plot Types and Sampling Design
- A plots (Areal): 100 m by 1 m, located adjacent to boundary plots; central 4x1 m nest 0 is used for detailed recording; up to 5 A plots per square.
- X plots (Large, Wally plots): 200 m2 square (approx. 14.14 m on a side) with nested subplots (nest 0: inner 4 m2; nest 1: central 4 m2; nests 2–5: outer) for comprehensive species recording; includes random placement in new squares and special placement rules when crossing features.
- Y plots (Small, Habitat plots): 2 m x 2 m plots (Y1–Y5) placed in habitat types not well represented by other plots or in Priority Habitats; multiple nests and nesting strategy to capture habitat variation.
- U plots (Unenclosed): 2 m x 2 m plots (U1–U10) in unenclosed Broad Habitats; up to 10 per square, allocated based on habitat extent and grid stratification.
- M plots (Margins): 2 m x 2 m plots to record arable field margins associated with margins options and cross-compliance margins; placed to measure margin beyond cross-compliance strip.
- L/H/D/A/B/R/V/S/W plots: Various linear and boundary plots
  - H plots (hedgerows): 10 m x 1 m along hedgerows; located on the nearest hedgerow to associated X plots.
  - D plots (Diversity): Hedgerow diversity plots, 30 m long by 1 m wide, within or alongside hedgerows.
  - S/W plots (Streamside/Waterside): 10 m x 1 m along watercourses; located near water features; header captures stream type and watercourse condition.
  - R/V plots (Roadside/Verge): 10 m x 1 m along roadsides or verges; header captures road type.
  - B plots (Boundary): Boundary plots associated with 200 m plots; 1 m width along the boundary edge; used to prioritize boundary features.
  - A plots (Arable Field Margin) and M plots are linked to B plots for margin measurements.
- List of plot types to be recorded per square is defined; new plots may be added for changes in land use or habitat, with specific naming and placement rules.

## Data Capture, Tools, and Workflow
- VegPlots software: standard data entry form with tabs for Headers, Listed Species, Selected Species, and administrative details.
- ArcMap integration: plots are located on the GIS map; new plots are saved in ArcMap and then entered in VegPlots.
- Tablet-based data collection: data entered on tablets (two possible datasets, labeled A and B to avoid overwriting when two teams record simultaneously).
- Plot header data includes relocation status, plate detection, plot ID, slope, aspect, shade, photos, and plot map status.
- Vegetation height is captured at canopy, shrub, and ground levels with categorical height bands.
- Species data: two main layers
  - Listed species: predefined lists by group (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Unidentified species) with tick boxes.
  - Selected species: each identified species added as a record with nest number and estimated cover; cover is recorded in 1% steps initially, then 5% bands; total cover across nested plots is tracked.
- Nested plots (especially X plots) require careful recording across nests 0–5 to reflect multi-scale sampling within the 200 m2 plot.
- Validation and saving: use Save, Validate, and Exit; validation highlights missing fields; must validate before changing the plot or exiting.
- Photos: take new photos at each plot to aid relocation and illustrate changes; photos should include plot number and type; download photos to tablet during or after fieldwork.
- Plot maps: draw and annotate maps with measurements and bearings; where necessary, edits to existing maps should be marked as “edited” or “redrawn” with initials and date.
- Randomization and habitat allocation: Y plots in Priority Habitats may be allocated randomly using a tablet random number generator; X plots use a five-sector overlay to determine feasible new locations when positioning new plots.

## Plot Location, Relocation, and GPS Logging
- Plot relocation uses ArcMap maps, plot photos, and reference features to re-find plots; moving plots is allowed only for landscape shifts, not for GPS positions.
- GPS logging: even when non-differential GPS is used, surveyors should log coordinates for plots in ArcMap, stamping GPS locations within the plot map and labeling with plot type and number.
- Not Found or replacement plots: if relocation fails, record as Not Found and create a New Plot (Replacement or New feature/Land cover) as appropriate.
- Specific rules exist for relocating each plot type (A, B, D, H, S/W, R/V, X, Y, U, M, etc.) to minimize bias and ensure comparability with historical data.
- Five-sector overlay: used for X plots to determine whether a new plot position can be recorded in the same square when land-use or habitat changes occur.

## Plot Maps, Documentation, and Protocols
- Plot maps are critical data products; maps should be clear, precise, and include reference measurements and compass bearings.
- If an existing map is adequate, indicate NO action; otherwise, mark as Edited or Redrawn with clear annotations.
- New plots must be sketched and labelled with square, plot type, and plot number; for new squares, anchor plots with measured distances and bearings to nearby reference features.
- Plot types have specific documentation templates and drawing requirements (e.g., 100 m edges for arable margins, 200 m2 for X plots, 30 m lengths for D plots, etc.).
- The Plot Map Protocol emphasizes clarity, reproducibility, and the use of measurements and compass bearings to locate plots accurately.

## Data Model, Quality, and Taxonomic Details
- Aggregations/Combinations: some taxa are difficult to separate; when uncertain, use taxonomic combinations (e.g., Cardamine hirsuta/flexuosa) to stay consistent with prior surveys; use that combination only when the separate name is not unequivocally identified.
- Bryophytes and Lichens: only bryophytes and lichens in the provided lists are recorded, with individual cover values.
- Sphagna (Sphagnum): detailed sub-categories for color/texture and form (green/thin, red/thin, fat forms) are specified for standardized recording.
- Woody species: for woody species, record presence and cover (including climbing species) but not non-woody components.
- Tends toward standardized, repeatable sampling across plots and years to facilitate long-term trend analysis.

## Special Procedures and Considerations
- Plot density and spacing: ensure appropriate spacing and avoid overlap between linear plots; boundary plots take precedence over other linear plots unless specific exceptions apply.
- Replacement plots: when a plot cannot be found or habitat has changed, re-position in a nearby, appropriate habitat area, with notes on the change.
- Location logic by plot type: detailed procedures govern how to locate X, Y, U, M, H, D, S/W, R/V, B, and A plots, including how to handle hedgerows, streams, margins, and arable fields.
- Data integrity: frequent data saves, validation, and photo documentation are essential; maintain backup copies and ensure data are not overwritten by simultaneous entries on multiple tablets.
- Timing and logistics: fieldwork may involve multiple tablets; coordination is needed to avoid data overwrites and ensure consistent dataset naming and storage.

## Data Outputs, Archiving, and Access
- The handbook describes the in-field data capture process and the structure of the VegPlots database and associated ArcMap data.
- Outputs include plot-level species lists, nested species and cover data, plot header information, and GPS-labeled plot locations, all enabling longitudinal analysis of vegetation change.
- The document concludes with administrative details, copyright, and contact information for the Countryside Survey project office.