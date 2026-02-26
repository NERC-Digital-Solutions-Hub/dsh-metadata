# GLASTIR MONITORING & EVALUATION PROGRAMME VEGETATION AND SOIL FIELD HANDBOOK

## Overview and purpose
- Field protocol handbook for the Glastir Monitoring and Evaluation Project (GMEP) to quantify landscape and habitat changes in Welsh 1km squares.
- Establishes repeatable, fixed-point data collection for vegetation and soil across multiple years, enabling time-series analysis tied to Glastir options.
- Emphasizes data discovery, usability, and governance through standardized data capture, documentation, and metadata.

## Data capture systems and standards
- Data collection via a forms-based software tool called Vegplots, integrated with ArcMap (VegPlotsWelsh.mxd).
- Data captured on tablets with digital photos, sketch maps, and drag-and-drop plot positioning; paper maps used as backups.
- GPS stamping (preferably differential GPS via Trimble) required for precise plot locations; ARCMAP layers and Vegplots data entry are tightly linked.
- Heavy emphasis on documentation per plot: header information, plot relocation notes, photos, and sketch maps for re-finding plots in future surveys.
- Metadata and data provenance enforced through explicit entries (plot type, plot number, nest, validation status, etc.) and a strong QA workflow.

## Plot allocation and survey design
- Plots are allocated within each 1km square to target different habitat types and Glastir option groups (enclosed vs unenclosed habitats, hedgerows, streams, margins, etc.).
- Plot calculator and proportional sampling: number and type of plots (in-option vs out-of-option) are determined after habitat mapping and option area estimation.
- A single square contains multiple plot types (X, Y, U, B, A, M, H, D, S/W, P, etc.), each with defined placement rules relative to features (random points, boundaries, hedges, watercourses, etc.).
- X plots provide the core random locations; other plot types are projected from X plots or placed to optimize sampling of Glastir option groups; occasional uncoupling from X plots is allowed to avoid sampling bias.
- Special attention to Countryside Survey repeat squares and time-series continuity, including notes on revisiting fixed plots and handling land access changes.

## Plot types and layout (high-level)
- X plots: 4 m2 (woodland exceptions: 200 m2 in woodland or Countryside Survey contexts); located at five random positions per square; used to anchor subsequent plots.
- Y plots: 2 m x 2 m; sampled in enclosed habitats and Priority Habitats (PH); positioned after habitat mapping.
- U plots: 2 m x 2 m; sample unenclosed broad habitats; number and placement depend on the proportion of unenclosed habitat in the square.
- B plots: Boundary plots along boundaries (5 per square); positioned at the X plot boundary with 1 m width.
- A plots: Arable field margin plots (100 m x 1 m); associated with B plots in-option/out-of-option logic.
- M plots: Margin plots (2 m x 2 m) sampling arable margins; coupled with A plots where margins exist.
- H plots: Hedgerow plots (10 m x 1 m) on hedges; sampling hedgerows with careful handling of options.
- D plots: Hedgerow diversity plots (30 m x 1 m) sampling hedgerows with diverse structure and canopy characteristics; nested data include trees/shrubs, gappiness, and invasive species presence.
- S/W plots: Streamside plots (10 m x 1 m) sampling along watercourses; S plots are near two X plots; W plots sample additional watercourse types; RHS coordination described.
- P plots: Perpendicular plots (up to 5) aligned upslope from S/W plots to capture riparian margins and buffer-zone variation; nesting within P plots helps manage within-plot diversity.
- Plot placement rules account for option in/out status, proximity constraints (e.g., no two plots too close on the same feature), and practical constraints (land access, safety, and habitat characteristics).

## Data entry workflow and validation
- Plot creation begins in ArcMap; plots are then recorded in VegPlots on the tablet with a mapped plot ID (Square + Plot Type + Plot Number).
- Vegplots interface includes:
  - Headers: relocation status, slope, aspect, shade, photos, and plot map status.
  - Vegetation height categories and nested plots where applicable.
  - Listed species by groups (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Crops, Unidentified).
  - Selected species: add species with corresponding nest, and enter % cover in 5% bands; caution to avoid double counting.
  - Validation: a Validate step highlights missing fields (red) and incomplete species data; data must be saved and validated before exiting.
- Plot relocation and repeat survey procedures rely on a combination of GPS, sketch maps, and photos to re-find plots in future surveys.
- Special rules govern handling of unidentified species, amalgamated taxa (combinations), and bryophyte/lichen recording subsets.

## Metadata, photos, and GIS integration
- Plot photos are required for relocation and trend visualization; directional orientation and a north arrow are recorded on sketch maps.
- Landscape photography protocol recommends fixed-point, four-quadrant photos from X plots and, if possible, 360-degree panoramas; photos are stored on devices and later uploaded to designated folders.
- Central documentation includes:
  - Plot maps (sketch maps for relocation; paper maps retained; digital versions accessed via ArcMap).
  - Plot location data (GPS points, nest data, plot IDs) used for re-finding locations in subsequent surveys.
  - Photo labeling and directory structure (e.g., New_Photos folder, VegPlots folder) to maintain data traceability.
- Travel and logistics also call out data-related dependencies (e.g., GPS log setup, tablet software versions, data backups).

## Time series, repeat surveys, and legacy data
- Emphasizes continuity with historical data: Countryside Survey squares (appearing since 1978) revisited in 2016, extending a globally unique time series; prior cycles include 1990, 1998, 2007.
- Additional Note 5 provides guidance on tackling repeat 1km squares, including how to allocate plots as habitat and option statuses evolve over time.

## Soil sampling protocol and field equipment
- Soil sampling uses four cores per X-plot:
  - Core C (Chemistry): long black core, 15 cm depth target.
  - Core P (Physics): long white core, 15 cm depth target.
  - Core B (Biology): fauna-focused core, 15 cm depth target in a tin.
  - Core F (Fauna): fauna core, short white core, offset from center.
- Step-by-step preparation and handling instructions for mineral and organic soil types, core extraction, labeling, and packaging.
- Tin sample (Biology) collected via gouge auger: five samples, each recovered to 15 cm depth, then placed in a labeled screw-lid tin.
- Samples stored in a cool box and mailed to specified laboratories (Bangor for chemistry and physics cores; Lancaster for fauna cores) with strict mailing schedules (avoid Thursday/Friday or weekends).
- Documentation accompanies samples (bag labels, depth notes, and envelopes) to ensure traceability and proper chain-of-custody.

## Data governance, quality, and best practices
- Strong emphasis on data quality and reproducibility:
  - Avoid uprooting plants, prevent disturbance biases, and maintain consistent identification practices.
  - Use of nested plots and standardized cover estimates to minimize subjectivity.
  - Aggregations/combinations for difficult taxa to maintain consistency with historical data.
  - Bryophytes and lichens are recorded using a defined subset to maintain comparability.
  - Clear guidance on when plots should be treated as new, replaced, inaccessible, or not appropriate due to land-use changes.
- Important software notes and training considerations:
  - VegPlots software updates and known issues (e.g., dropdown responsiveness, autosave), with actions tracked in Additional Note 8.
  - GPS integration challenges and troubleshooting guidance for both internal and external GPS devices.
  - Documentation of center maps, plotting conventions, plastic markers, and Nest allocations to support repeatability.
- The Plot Calculator tool assists in translating square habitat mappings into plot numbers for each option group; guidance emphasizes sampling proportional to plot-able land and careful handling of mosaics and option overlaps.

## Challenges and considerations for data stewards
- Incomplete or evolving user needs and varying systems/formats across plots and habitats.
- Timely data acquisition from landowners and data creators; consistency across survey years.
- Interoperability of diverse data types (vegetation lists, cover estimates, nested plots, photos, GPS logs, sketch maps).
- Managing large data volumes, including high-resolution photos and GIS data, while preserving traceability and auditability.
- Ensuring documentation, version history, and QA workflows are maintained across years and survey teams.

## Endnotes and supplementary materials
- The document includes extensive Appendices and Note sections (e.g., Additional Note 4 on allocating plots to Glastir land, Additional Note 5 on repeat survey strategies, and detailed field methods for various plot types and soil sampling).
- Illustrative figures and tables accompany plot layouts and calculator workflows to support practical field implementation.
- An emphasis on clear, auditable data records to support landscape-scale analyses of Glastir impacts over time.