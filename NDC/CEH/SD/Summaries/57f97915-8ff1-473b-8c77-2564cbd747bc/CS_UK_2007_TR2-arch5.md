# CS Technical Report No.2/07: Vegetation Plots Handbook

## Overview
- A comprehensive methodology for recording vegetation presence, abundance, and plot characteristics across long-term Countryside Survey plots.
- Data collection is digital (VegPlots) and GIS-enabled (ArcMap), enabling repeatable relocation of plots and consistent data capture across survey squares.
- Aims to support data governance, discoverability, and re-use by ensuring standardized data structures, metadata, and provenance.

## Data model and structure
- Plot-centric data captured via VegPlots software, integrated with ArcMap plot maps.
- Core identifiers:
  - Square, Plot Type (A, B, D, H, M, R, S, U, V, W, X, Y), Plot Number, Plot ID (Square + Type + Number).
- Metadata and headers:
  - Plot relocation status, plate detection, plot description (slope, aspect, shade), photos, plot maps (drawn/edited/redrawn), admin (surveyor initials, plot completion status), and notes.
- Vegetation data:
  - Listed species: multi-group lists (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Crops, Unidentified); selection via checkboxes; spatially nested plots (Nest 0, Nest 1, etc).
  - Selected species: cumulative list with estimated total cover (in 1% and 5% bands) per plot and per nested nest; prevent double-counting overlapping canopies.
  - Final cover estimates for all species in the 200 m2 plot (including nested plots).
- Plot recording sections:
  - Header (plot relocation, plate status, plot ID, description, photos, plot map status).
  - Plot-specific header information (varies by plot type).
  - Admin, Notes, and Plot-specific fields (e.g., Priority Habitat for Y plots, Priority Habitat field; boundary or land-use related data for other plots).
- Plot types and data scope (high-level):
  - X plots: Large 200 m2 random samples with nested 1 m2, 4 m2 nests; detailed nested recording.
  - Y plots: Small 2 m x 2 m plots targeting habitats and Priority Habitats not well represented.
  - U plots: Unenclosed Broad Habitats; up to 10 plots per square with proportional allocation across habitats.
  - A plots: Arable field margins adjacent to boundary features; presence and 4x1 m subset recording.
  - M plots: Margins associated with arable fields (new 2007 focus); measure margin vegetation beyond cross-compliance strip.
  - H plots: Hedgerow, linear 10 x 1 m plots; relocation rules when hedges disappear or shift.
  - D plots: Hedgerow diversity; comprehensive woody species metrics across 30 m length.
  - S/W plots: Streamside and waterside plots; 10 m x 1 m; stream/watercourse context and width data.
  - R/V plots: Roadside and Verge plots; location relative to road verge; linear layout.
  - B plots: Boundary plots (5 x 200 m2 plots per square); derived from boundary features (hedges, walls, fences, etc.).
  - X plots (Wally/Large): 200 m2 plots with five nested scales (including 1 m2 nests); random placement with edge handling near features.
- Special data handling:
  - Bryophytes and lichens limited to listed taxa only.
  - Taxonomic aggregations used when species identification is uncertain (e.g., Cardamine hirsuta/flexuosa).
  - Sphagnum species classified by green/thin vs red/thin forms; detailed schematic illustrations provided.

## Data collection workflow
- Pre-field planning:
  - Use ArcMap plot location maps and prior plots to guide relocation or new plot placement.
  - Determine which plot types are needed in a square based on habitat coverage and survey history.
- In-field data capture:
  - Data entered on tablets using VegPlots; plot positions linked to ArcMap maps.
  - GPS coordinates logged for plots to aid future relocation (non-differential GPS on tablets).
  - Plot photos collected to assist relocation and illustrate vegetation change over time.
  - Plot maps drawn, edited, or redrawn as needed; new plots sketched with measured references.
- Relocation and new plots:
  - Plots can be relocated if landscape features align; otherwise, Not Found or New Plot (Replacement for unfound plot) or New Plot (New feature/Land cover).
  - For new X plots or re-allocations due to land-use changes, exact positioning follows defined rules (e.g., edge distances, random-sector placement).
  - Plot maps and sketches maintained as part of the dataset; edited/redrawn status recorded.
- Data entry and validation:
  - VegPlots: start by selecting the plot on ArcMap; navigate to Standard Recording for the plot.
  - Headers populated (Square, Plot Type, Plot Number, Plot ID); Nest field defaults; subsequently complete data entry.
  - Validate data to highlight missing fields (Red flags); save frequently; mandatory data validated before leaving a plot.
  - Selected Species loaded as nested records; covers captured per nest; totals checked for consistency.
- Post-recording and archival:
  - New photos downloaded to tablet storage; photos linked to plot entries; photos accompany relocation evidence.
  - Plot maps saved and annotated; maps may be edited or redrawn if landscape has changed.
  - Storage paths referenced (e.g., New_Plot_Photos on tablet, VegPlots data in local .mdb).

## Quality assurance, provenance, and governance
- Data quality controls:
  - Regular validation within VegPlots to identify missing or inconsistent fields.
  - Avoidance of double-counting across nested plots; clear rules for partial canopies and bare ground.
  - Consistency checks across nested plots and species lists; cap on total cover categories to maintain ecological plausibility.
- Provenance and traceability:
  - Plot IDs capture source square and historical sequence; changes to location or plots are documented via relocation status and map edits.
  - Admin and Notes fields capture context for why plots were lost, displaced, or deemed inappropriate.
  - All changes to plot maps are annotated (Edited/Redrawn) and linked to the plot’s ArcMap entry.
- Data consolidation and dissemination:
  - Data are designed for longitudinal analyses across multiple survey rounds, enabling trend assessment in vegetation change and habitat representation.
  - Clear taxonomy and aggregation rules facilitate comparability with past surveys and consistent reporting.

## Practical considerations for data stewardship
- Standardization:
  - Maintain consistent naming conventions for plots and nests; enforce plot IDs (Square + Type + Number) to prevent duplicates.
  - Adhere to predefined plot types, their sizes, and layout rules to ensure comparability across squares and years.
- Metadata completeness:
  - Ensure header fields, plot descriptions, species lists, and nested plot data are recorded for every plot entry.
  - Capture context on habitat type, measurement methods, and any deviations (e.g., when a plot is not found or relocated).
- Accessibility and storage:
  - Data captured in VegPlots.mdb (and VegPlotsA.mdb when multiple tablets are used) with ArcMap integration for GIS context.
  - Photos stored in structured directories on tablets; ensure consistent linking to plot entries.
- Change management and updates:
  - When landscape changes, document rationale and methods for new plot placement or relocation, including map sketches and coordinates.
  - Maintain historical plots where possible to preserve time series, while allowing new plots where necessary.

## Quick reference: key plot types and purposes
- X plots: Large random 200 m2 plots with nested 1 m2 and 4 m2 nests; primary random sample across habitat types.
- Y plots: Small 2 m x 2 m plots targeting under-sampled habitats and Priority Habitats.
- U plots: Unenclosed broad habitats; up to 10 per square, allocated by habitat area.
- A plots: Arable field margins adjacent to boundaries; focus on field-edge biodiversity.
- M plots: Margin plots measuring margins beyond cross-compliance strips.
- H plots: Hedgerow plots; linear 10 x 1 m along hedgerows.
- D plots: Hedgerow diversity; woody species within hedgerow features.
- S/W plots: Streamside and waterside plots along permanent watercourses.
- R/V plots: Roadside and verge plots along transport routes.
- B plots: Boundary plots at 200 m2 scale along field boundaries.
- A, H, D, S/W, R/V combinations involve detailed measurements of structure, height, width, and gappiness to characterize woody and herbaceous components.