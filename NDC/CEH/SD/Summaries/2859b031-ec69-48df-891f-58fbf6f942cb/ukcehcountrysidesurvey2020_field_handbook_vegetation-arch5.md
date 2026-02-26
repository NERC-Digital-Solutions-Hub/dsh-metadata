# UKCEH Countryside Survey 2021

## Overview
- Vegetation field protocol handbook for the summer 2021 survey (UK-SCaPE / UKCEH Countryside Survey).
- Purpose: record vegetation presence, abundance and plot context to quantify countryside changes with high precision.
- Data collection relies on digital tools (ESRI Collector and Survey123) to enable relocation, data capture, and integration into a central database.
- Long-term value hinges on consistent plotting, relocation aids (sketch maps, photos), and thorough metadata.

## Data Collection Framework
- Plot types and sizes
  - VEGETATION SQUARE (200 m2 plot) with nested 1 m2 to 4 m2 subplots (Nest 0 to Nest 5).
  - SOIL SQUARE (2x2 m) nested within the 200 m2 plot for soil-focused data.
- Plot relocation and documentation
  - Each plot requires relocation aids: plot maps, GPS geopoints, sketch maps, and plot photos.
  - Plots are often revisited; in cases where relocation is not reliable, records may be flagged as Not Found or New Plot (Replacement/New feature).
  - Metal plates or stakes mark historic X plots (some may be buried or moved; detectors provided).
- Data entry workflow
  - Collector app for plot navigation; Survey123 for data entry.
  - Start from a map, then open relevant survey form; if editing an existing plot, use the prescribed workflow to avoid duplicating data.
  - For new plots, manual entry of header details is required.
- Plot header and relocation data (Page 1)
  - Includes square, plot type, plot number, Plot ID, surveyors, location, slope/aspect, photos.
  - Relocation status options: Found, New Plot (Replacement), New Plot (New feature/Land cover), Not appropriate, Access Denied, Too Dangerous.
  - Location coordinates captured automatically via offline GPS; if online, user confirms accuracy on a map.
  - Broad Habitat (BH) and Priority Habitat (PH) selections at both plot level and wider polygon contexts.
  - Notes for disturbances, soil samples, or unidentified species; tree disease indicators if applicable.
  - Plot Map: whether a plot map was drawn, edited, or redrawn; updates documented.
- Vegetation and soil measurement data (Page 2-3)
  - Vegetation height categories for canopy, shrub, and ground layers.
  - Plot-level and nest-level species recording (Nest 0 to Nest 5 for 200 m2 plots; Nest 1+ for the 4 m2 soil plots); comprehensive but prioritizing major vascular plants.
  - Use of auto-complete and “Other” options for unlisted species; ability to attach photos of unidentified species.
  - Total cover estimation per species, including six extra ground/structure categories (litter, wood, rock, bare ground, water, bryophytes); total covers should sum near 100% or more in layered vegetation.
  - Special bryophyte and lichen guidance; limited focus on common bryophytes (Sphagnum categories listed) with priority on vascular plants.
- Data submission and integrity
  - Online submission via Send Now; offline draft/outbox workflow supports continued data entry; auto-save minimizes data loss.
  - Copy-to-new-survey requirement for edits; notes must indicate correct version when resubmitting.
  - QA prompts to ensure required fields are completed prior to submission.

## Data Standards and Metadata
- Plot and nested structure
  - 200 m2 X plots with nested nests (Nest 0-5) for vegetation; 4 m2 nests for soil plots; 2x2 m soil nests within X plots.
  - Nest-specific species presence and cover data; total cover per species captured for each nest.
- Identifiers and traceability
  - Plot ID constructed from Square, Plot Type, and Plot Number (auto-generated or manual entry when new).
  - GPS coordinates, photos, and sketch maps linked to each plot to enable repeat visits.
- Habitat classification
  - Use of Broad Habitat (BH) and Priority Habitat (PH) codes at both plot and polygon levels.
  - Appendix IV provides habitat descriptions and a structured habitat key for consistent classification.
- Species handling and data integrity
  - Taxonomic aggregations used when species-level identification is unreliable (e.g., Cardamine hirsuta/flexuosa).
  - Warnings against uprooting invasive species; photos recommended when uncertain.
  - Documentation of entry issues (blank fields, duplicates) to maintain data QA.
- Documentation and provenance
  - Plot photos, sketch maps, and weather/wildlife notes support re-finding and context.
  - Versioned documentation with Change Log (Version History) to track updates across iterations.

## Plot Types, Layouts, and Relocation Rules
- X plots (200 m2 vegetation plots) and X plots (4 m2 soil plots)
  - Five predetermined random positions per square; relocation logic ensures plots remain representative and comparable over time.
  - If cross features (e.g., edges) place plots, adjust to maintain comparability and minimize edge effects.
  - If a plot lies in an unsuitable area (water, urban, etc.), relocate within same sector or mark as Not appropriate.
- Layout guidance
  - 200 m2 plot oriented on north-south and east-west axes; diagonal strings mark nested subsites.
  - Nest 0 located within outer boundary; nest 1-5 expand outward; nest 0 counts as the innermost sub-plot.
  - Nest-specific sampling: Nest 0 capture initial presence and total cover; Nest 1 and subsequent nests add new species absent in previous nests.
- 4 m2 soil plots
  - Nested within the X plots; similar data capture but focused on soil quadrats; total covers recorded including soil-specific categories.
- Special cases and amendments
  - If a previous plot cannot be relocated satisfactorily, record as Not Found and create a new plot; relocation error tolerance depends on habitat heterogeneity.
  - For arable fields or crops, 2x2 m plots are estimated rather than precisely measured, with careful boundary management.

## Appendices and Habitat Descriptions
- Appendix I: Collector & Survey123 Generic Reference Guides
  - Installation and usage guidance for Collector and Survey123 apps.
  - Data management workflows, including Map gallery navigation, My Surveys, Drafts, Outbox, and Sent statuses.
  - Offline/online data handling, basemaps, and GPS considerations.
- Appendix II: Random Numbers
  - Random number table for reference (0-1) used in field procedures.
- Appendix III: Plot Types by Square (previous surveys)
  - Historical breakdown of plot types (Areal, X Large, X Small, Soil, etc.).
- Appendix IV: Habitat Descriptions and Priority Habitat Key
  - Detailed broad habitat categories (e.g., Broadleaved mixed and yew woodland, Coniferous woodland, Arable and Horticulture, Various grasslands, Bracken, Heaths, Fens/Marsh/Swamp, Bog, Urban, Supra-Littoral habitats, Inland rock, Montane, etc.).
  - Priority habitat notes (limestone pavement, inland rock outcrop, scree, calcareous/acid grasslands, reedbeds, bogs, standing water, urban, montane, etc.).
  - Guidance on assigning patches to Broad and Priority Habitats for BAP reporting; habitat allocation aids consistency across surveys.
- Habitat key notes
  - Clear guidance on how to record current habitats (e.g., post-clearing, clearfelling, or ongoing forestry cycles) to reflect present conditions rather than future expectations.
  - Distinctions between habitats and land-use designations to avoid misclassification.

## Governance, Quality, and Change Management
- Version history and revisions
  - Documented version updates (e.g., front-page date changes; training alignment) to maintain audit trails.
- Data stewardship considerations
  - Emphasis on data discoverability and usability through standardized metadata, plot-level and nest-level structures, and consistent habitat classifications.
  - The protocol’s design supports long-term re-sampling and comparability across survey years via relocation aids, standardized forms, and explicit data entry rules.
- Challenges addressed
  - Incomplete user needs: mitigated by explicit relocation procedures, metadata richness (photos, sketches), and clear outcomes for not-found plots.
  - Interoperability: standardized BH/PH codes, nested plot structure, and centralized digital workflow (Collector + Survey123) to harmonize data across teams and years.
  - Large datasets: structured nest-based data and defined fields to optimize data capture and QA while enabling scalable storage and retrieval.

## Relevance for Data Stewards
- The UKCEH Countryside Survey 2021 protocol provides a comprehensive, standardized framework for collecting, curating, and sharing vegetation plot data.
- It emphasizes robust metadata (plot identity, location, habitat context, relocation status), traceability (sketch maps, photos, Plot ID), and data quality controls (mandatory fields, nest-level extraction, avoidance of duplicates/blank entries).
- The documentation supports reproducibility, data governance, and long-term data sharing across organizations, with explicit guidance on data lifecycle (offline work, submission, versioning) and habitat classification for consistent analyses.