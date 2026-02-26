# CS Technical Report No. 2/07: Vegetation Plots Handbook v1.0

## Purpose and Scope
- Establishes a globally unique, time-series dataset documenting vegetation change across four survey points over 29 years.
- Defines required data for each plot: header information, relocation/verification data, plot description, vegetation height, admin, notes, and plot-specific metadata.
- Provides a standardized workflow for plot recording, relocation, and data entry to enable repeatable sampling and robust analysis.

## Data Model and Schema
- Central data entry through VegPlots forms-based tool, integrated with GIS (ArcMap) plot maps.
- Data structure includes: 
  - Header (plot metadata such as plot number, type, height, location)
  - Plot relocation (status: Found, Not Found, New Plot, etc.)
  - Plot description (slope, aspect, shade, photos, plot maps)
  - Vegetation height (canopy, shrub, ground layers)
  - Admin (surveyors, completion status)
  - Notes (free text on relocation/conditions)
  - Plot-specific header information (type-dependent fields)
  - Listed species (taxonomy groups; presence/cover where applicable)
  - Selected species (Nest-based recording with % cover in 5% bands)
- Unique Plot IDs are constructed from Square, Plot Type, and Plot Number; new plots receive sequential numbering to avoid re-identification as repeats.
- Data integrity supported by validation steps and mandatory photo/maps for relocation and verification.

## Data Collection Tools and Workflow
- GIS-enabled ArcMap maps used for locating plots; VegPlots software used for field data entry.
- Tablets used for data capture; two tablets may be used per team with dataset differentiation (VegetationPlotsA.mdb vs VegetationPlotsB.mdb).
- Plot photos and plot maps are stored digitally on devices:
  - New Plot Photos directory (tablet)
  - 2007_plotmaps (GIS back-ups)
  - plot_photos (back-ups)
- GPS coordinates are logged for each plot to assist relocation in future surveys; GPS data is annotated on the ArcMap plot map after recording.
- Data entry flow:
  - Locate plot in ArcMap, open VegPlots, enter data, validate, save, and exit.
  - Photos of each plot location are taken and uploaded for future relocation references.
  - Plot maps are drawn or edited as needed and marked as Edited/Redrawn when new maps are created.

## Plot Types and Data Requirements
- X plots (Large, Wally) – 200 m2; random point samples across habitat types.
- Y plots – Small habitat-targeted plots (2 m x 2 m) positioned in Priority Habitats and other un-sampled areas.
- U plots – Unenclosed broad habitat plots (2 m x 2 m; up to 10 per square; representation across unenclosed habitat types).
- S/W plots – Streamside/waterside plots (linear, 10 m long; 1 m wide; along watercourses).
- R/V plots – Roadside and verge plots (linear; 10 m long; near roads/verges).
- A plots – Arable field margins (100 m x 1 m; margins adjacent to B plots).
- M plots – Margin plots (2 m x 2 m) for evaluating arable margins associated with B and A plots.
- H plots – Hedgerow plots (linear, 10 m x 1 m; along hedges).
- D plots – Hedgerow diversity plots (D1-D10) for woody species diversity and hedgerow condition.
- B plots – Boundary plots (linear along field boundaries; 200 m plot).
- A/Aplots-related details and nesting structure (nest 0, nest 1, etc.) used for nested species recording.
- Relevant header fields are plot-type dependent (e.g., soil sampling for X plots; priority habitat for Y plots; distance measures for A/M plots; stream type for S/W plots).

## Data Capture: Species, Cover, and Abundance
- Listed species: comprehensive lists by group (Common species, Grasses, Ferns, Forbs/Woody, Bryophytes/Lichens), with presence and, where applicable, % cover.
- Selected species: per plot, species are added to a growing nest-based list; cover estimates are entered in 5% bands (with a 1% minimum increment during entry).
- Nested plots (Nests) capture multi-scale sampling within X plots; total cover estimates cover the entire 200 m2 plot when applicable.
- Special attention to avoid double-counting and to consider overstory branches that project into plots.

## Plot Relocation, Verification, and Quality Assurance
- Relocation protocols emphasize minimizing disturbance while ensuring accurate relocation; note explicit criteria for “Not Found” vs “New Plot” vs “replacement” scenarios.
- Plot descriptions include physical site characteristics (slope, aspect, shade, photos, map status).
- Validation rules highlight missing fields; red/green cues in VegPlots guide data completion.
- Photos and map updates are essential for ensuring repeatability and for illustrating changes across surveys.

## Data Storage, Provenance, and Access
- Data stored in VegPlots database files on tablets; two-tablet workflow with clear naming conventions to prevent data overwrite.
- GIS integration ensures plotting accuracy and ease of locating plots across survey rounds.
- Physical and digital backups include paper maps, a 2007_plotmaps folder, and a dedicated New_Plot_Photos directory; photos must be downloaded to tablet storage regularly.
- Documentation and metadata accompany data collection, with versioning and cross-referencing to previous surveys.

## Governance, Standards, and Community Coordination
- The handbook defines standardized methods for plot layout, categorization, and data entry to support cross-square comparability and long-term time series.
- Encourages use of consistent naming, Nests, and plot types to maintain data continuity across survey cycles.
- The data protocol supports collaboration and data-sharing within the Countryside Survey network and with partner organizations, enabling a cohesive, community-driven dataset.

## Key Considerations for Data Leaders
- Time-series integrity: strict adherence to relocation, labeling, and nesting conventions to maintain comparability across surveys.
- Data standardization: uniform header metadata, species lists, cover categories, and plot-type rules to minimize interpretive variance.
- Data provenance: robust GIS and VegPlots linkage, with comprehensive photo/maps to enable replication and audit trails.
- Access and governance: clear data storage paths, versioning, and training (training course references) to ensure consistent usage and data quality across teams and squares.
- Data integration and sharing: structured data suitable for pooling with wider ecological datasets and networks of partners.