# CS Technical Report No.2/07 Vegetation Plots Handbook

## Overview
- Describes standardized methods for recording plant species presence and abundance across diverse vegetation plots to maintain a long-term, globally unique dataset.
- Data collection combines GIS mapping (ArcMap), a forms-based VegPlots software, and digital photography to enable repeatable plot relocation and consistent data capture.
- Emphasizes plot relocation accuracy, metadata, and provenance to support four-point temporal change documentation over decades.

## Data Architecture and Standards

- Data sources and systems
  - ArcMap GIS plot maps and VegPlots software used for data capture.
  - Tablets and digital photos storage; central directories (e.g., C:\CEH\...), with planned data uploads and backups.
  - Plot maps (paper and digital) accompany relocation and data entry.
- Plot types and nested structure
  - X plots (Large, 200 m2) with nested nests (nest 0, 1, 2–5); primary sampling of common vegetation types.
  - Y plots (Small, 2 m x 2 m) for targeted habitats and Priority Habitats (PH).
  - U plots (Unenclosed Broad Habitats) 2 m x 2 m, up to 10 per square, allocated by habitat proportion.
  - A plots (Arable field margins) 100 m x 1 m along boundary, up to 5 per square.
  - M plots (Margins associated with A plots) 2 m x 2 m (new in 2007) to sample margin quality.
  - H plots (Hedgerow, 10 m x 1 m) and D plots (Hedgerow diversity, 30 m length) for woody features.
  - S/W plots (Streamside) and R/V plots (Roadside and Verge) for linear water-related and transport-edge habitats.
  - B plots (Boundary), 1 m width along boundaries for hedges, walls, fences, etc.
  - Lays out specific rules for each plot type to ensure representation and avoid duplication.
- Core data fields and data model
  - Headers: relocation status, plate detection, plot ID, date, slope, aspect, shade, photos, plot map status (drawn, edited, redrawn).
  - Plot description and environmental context (slope, aspect, shade, photos, plot maps).
  - Vegetation height categories (canopy, shrub, ground) in specified bands.
  - Admin: surveyor initials, plot completion status, notes.
  - Listed species: groups (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Crops, Unidentified); presence/absence data and order of entry.
  - Selected species: nested plotting data with nest-specific cover estimates in 1% then 5% bands; ability to delete rows; cross-checking cover with partners.
  - Nest and plot relationships for X plots, and 4x4 m nesting logic culminating in total cover estimates.
- Data quality and provenance
  - Data entry validated via VegPlots with red-highlighted missing fields; Save and Validate workflow to ensure completeness before exit.
  - Twin data streams: ArcMap location data linked to VegPlots entry; GPS coordinates logged in ArcMap for future relocation.
  - Photo protocol ensures reference visuals aid relocation and trend illustration.

## Data Lifecycle and Governance

- Data capture workflow
  - Establish ArcMap plot locations first; then open VegPlots for the relevant plot to enter data.
  - Use data validation and saving practices to avoid data loss; back-up exists via system.
  - Finalize and exit only after data validation; prevent overwriting by requiring validation before changing the plot.
- Plot creation and numbering
  - New plots must be uniquely labeled (e.g., Y6, U7) to avoid confusing repeats with new features.
  - When adding new plots due to relocation or habitat change, coordinate with mapping team.
- Relocation and data integrity
  - Plot relocation: move in ArcMap if landscape features shift; do not relocate by GPS position alone.
  - Not Found or New Plot scenarios documented for subsequent analysis; includes plate status, replacement IDs, and notes.
- GPS and location data
  - Log GPS coordinates for each plot during recording using tablet GPS; mark locations on the ArcMap plot map with stamps and labels.
  - Non-differential GPS used on tablets; historical differential GPS locations shown as outlines for reference.
- Plot records and data entry details
  - VegPlots header includes relocation outcomes, plate presence, plot IDs, and map-related fields.
  - List of species and selected species captured per nest; total cover estimates compiled after all nests are processed.
- Plot maps and field records
  - Plot maps can be NO Edited/Redrawn when suitable; edited maps require pencil edits with initials and date.
  - Sketch maps used for new or relocated plots, with measurements and bearings; maps must be clearly labeled with square, plot type, and number.
- Data quality controls
  - Validation highlights missing fields; users must resolve issues before exiting or changing plots.
  - Special caution for rare/uncommon habitats, and for species that are difficult to identify (use of amalgamated taxa when needed).

## Data Quality, Challenges, and Considerations

- Relocation accuracy
  - Some plots historically difficult to relocate; judgement about acceptable relocation error is required, especially for unique habitat plots.
- Data completeness
  - Some plot types have extensive header and nested data fields; ensuring complete entries across multiple nests is essential.
- Taxonomic considerations
  - Use of amalgamated taxa when exact identification is uncertain; ensure consistency with BRC lists and tablet drop-downs.
  Bryophytes and lichens are limited to the specified list; other bryophytes/lichens are not recorded.
- Access and data integration
  - Data exist in multiple formats (GIS maps, VegPlots database, photos). Harmonization relies on consistent IDs and linkage across systems.
- Practical field constraints
  - GPS and travel challenges, weather, and habitat accessibility influence relocation and sampling; protocols emphasize documentation and notes for interpretation.

## Access, Discoverability, and Reuse

- Data and artifacts
  - Plot location maps, VegPlots records, ArcMap files, and plot photos form an integrated data package per square.
  - Photos are downloaded to a dedicated folder on the tablet after each survey window; memory card management required to avoid overflow.
- Documentation and provenance
  - Detailed procedural guidance per plot type ensures repeatability and comparability across survey cycles.
  - Metadata includes date, location, plot type, nesting structure, sampling area, and habitat context.
- Governance and rights
  - Publication and reuse governed by NERC/Defra policy; proper attribution required for reproduced material.

## Key Implications for Data Leaders

- Establish robust data contracts and schemas
  - Maintain explicit data models for each plot type, including nested structures and temporal linkage.
  - Ensure unique, stable identifiers for plots across survey cycles; enforce naming conventions (e.g., Y6, U7) to prevent duplication.
- Integrate GIS and data capture systems
  - Seamless linkage between ArcMap plot maps and VegPlots data entry to preserve provenance and enable spatial analyses.
  - Maintain up-to-date, accurate plot relocation workflows and GPS logging to support longitudinal analyses.
- Enforce metadata and data quality controls
  - Standardized validation workflows, with red flags for incomplete fields; require complete validation before finalizing.
  - Document uncertainty and relocation confidence to support later data analyses and decision-making.
- Support data discoverability and reuse
  - Centralize plot data and associated assets (maps, photos) with clear directory structures and versioning.
  - Provide clear guidance for researchers on data access, licensing, and attribution, while preserving data integrity and rights.
- Prepare for long-term sustainability
  - Plan for data retention, migrations of file paths, and compatibility between VegPlots and GIS systems as technology evolves.
  - Build in governance for taxonomic harmonization, habitat classifications, and species aggregation to ensure comparability over time.