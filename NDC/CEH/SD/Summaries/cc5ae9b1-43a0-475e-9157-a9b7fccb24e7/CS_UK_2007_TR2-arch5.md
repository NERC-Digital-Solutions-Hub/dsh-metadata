CS Technical Report No.2/07: Vegetation Plots Handbook

## Overview
- Defines standardized protocols for recording vegetation plots across Countryside Survey to enable long-term time-series (four surveys over ~29 years).
- Data focus: plot location, plot type, plot metadata, vegetation presence/cover, nested subplots (nests), photos, and maps.
- Data lifecycle: creation of new plots, relocation of existing plots, handling Not Found or replaced plots, and ongoing updates across surveys.
- Data governance alignment: aims to support discovery, reuse, and appropriate governance of large, heterogeneous plot datasets through consistent data capture and documentation.

## Data Model and Structure
- Core concepts:
  - Plots categorized by type (A, X, Y, U, H, D, S, W, R, V, M, B, L, etc.) with defined nesting where applicable (e.g., X plots contain nested 1–5 subplots; Y plots have nested components).
  - Each plot has identifiers: Square, Plot Type, Plot Number, and Plot ID (Square+Type+Number).
  - Metadata fields include header information (location, physical attributes), admin notes, and data quality status.
  - Vegetation data captured as Listed Species (presence and/or counts) and Selected Species (with nest tracking and % cover in predefined bands).
- Data capture artifacts:
  - Plot maps (paper and digital), plot photos, and GPS coordinates (where available).
  - VegPlots software is used for data entry; ArcMap is used for mapping and locating plots.
- Data quality and traceability:
  - Validation and save cycles, with red-highlighted missing fields during validation.
  - Distinct statuses for plots (Found, Not Found, New Plot, Not Appropriate, etc.).
  - Documentation of plot-level decisions (e.g., relocations, new plots, replacing unfound plots).

## Data Capture Workflow
- Preparation and mapping:
  - Access ArcMap plot location maps; use ArcMap and VegPlots integration to locate and record plots.
  - For X plots, five-sector overlay guides new plot placement; prior plots may be edited or redrawn if landscape features change.
- Field data collection:
  - Collect and minimize disturbance to vegetation; record general header data, plot description, vegetation height estimates (canopy, shrub, ground levels), and admin notes.
  - Capture plot photos with a reference that includes plot number/type; download photos to tablet storage.
  - Log GPS coordinates where available; stamp GPS location on ArcMap plot map during recording.
- Data entry in VegPlots:
  - Start from the Standard Recording screen, using the Plot ID from ArcMap.
  - Complete Header fields, then move to the Listed Species and Selected Species tabs to record species presence and % cover.
  - Regularly save and validate; unresolved fields trigger validation prompts.
  - After completion, download and store plot photos for relocation references; ensure files are organized per square.
- Plot maps and protocols:
  - Plot maps should be clear and precise; redraws or edits must be documented on the map with initials and date.
  - For new plots, ensure correct labeling to avoid treating them as repeats (e.g., Y plots labeled Y6, U plots U7, etc.).

## Plot Types: Key Protocols (summary)
- X PLOTS (Large, 200 m2; “Wally” plots)
  - Location near random points; 200 m2 square with nested 4 m2 central inner plot (nest 0–1; nests 2–5 for additional sampling).
  - Header includes Soil sample taken and Date; precise plotting and labeling required to avoid repeat plotting.
- Y PLOTS (Small, 2 m x 2 m; habitat patches)
  - Located in Priority Habitats (PH) or un-sampled habitat patches; multiple nests (0–5) recorded for nested sampling.
  - Priority Habitat designation recorded; Listed Species and Nested plots recorded with 5% cover bands.
- U PLOTS (Unenclosed broad habitats)
  - 2 m x 2 m plots; up to 10 per square; located across unenclosed broad habitats; nesting and data capture similar to X/Y.
- S/W PLOTS (Streamside / Waterside)
  - 10 m x 1 m plots placed along watercourses; header includes Stream type, Watercourse condition, Stream Width, Freeboard.
- R/V PLOTS (Roadside and Verge)
  - 10 m x 1 m plots along verges; header includes Road type; recording follows same nesting and species procedures.
- A PLOTs (Arable field margins)
  - 100 m x 1 m plots along arable field margins adjacent to B plots; central 4x1 m nesting within the margins; presence and 4x1 m cover data collected.
- M PLOTS (Margins)
  - 2 m x 2 m plots measuring margins beyond cross-compliance strips; multiple margins per field; nest structure recorded; margin vegetation presence recorded.
- H PLOTS (Hedgerow)
  - 10 m x 1 m plots along hedges; centered on hedge with 1 m extending into field; distance to crop centre captured.
- D PLOTS (Hedgerow diversity)
  - 30 m long plots along woody linear features; extensive header data on modal height, width, gappiness, historic management, canopy structure, and presence of invasive/woody elements.
- S1/W2 and R1/V2
  - Additional streamside and roadside variants with specific layout rules and header fields.

## Data Quality, Validation, and Documentation
- Validation rules:
  - Header and Selected Species fields must be complete; missing data flagged for correction.
  - Ensure non-double counting of overlapped canopy layers; total cover can exceed 100% due to multi-layered vegetation.
- Data completeness:
  - Photos and plot maps are essential for relocation and trend illustration; new photos recommended for each plot location.
  - Documentation of reasons for Not Found or Not Appropriate recordings; free-text Notes (max 250 chars) capture context.
- Documentation of lineage:
  - All plots have an audit trail: plot type, number, square, and final status; any edits to maps or relocation should be annotated.

## Metadata, Provenance, Storage, and Sharing
- Data storage and organization:
  - Primary data captured in VegPlots (mdb-based database) on tablets; ArcMap provides spatial context and plot maps.
  - Two datasets per team (A and B tablets) to prevent overwriting; data naming conventions include suffixes (e.g., VegetationPlotsA.mdb).
  - Plot IDs are designed to remain stable across surveys; new plots get unique identifiers to avoid confusion with repeats.
- Documentation and access:
  - Training and protocols accompany dataset collection; plotting and data uploading processes are described to support integration into data portals.
  - Data sharing aims align with the long-term, discoverable, and reusable dataset goals, supported by explicit metadata and structured data capture.

## Challenges and Considerations for Data Stewards
- Completeness and timeliness:
  - Incomplete understanding of user needs (e.g., which plots to prioritize) and delays in locating plots or acquiring new plots.
- System diversity and interoperability:
  - Multiple plot types with varied data fields and nesting require careful mapping to a consistent data model; older GPS data may be less precise.
- Time-series continuity:
  - Maintaining consistency in plot placement, labeling, and nesting across surveys is crucial for valid time-series analyses.
- Large datasets and manual processes:
  - Handling many plots across diverse habitats, large table-like datasets, and image/photo management demands robust data governance and storage solutions.
- Documentation of decisions:
  - Clear notes on plot relocation decisions, new feature insertions, and rationale for Not Found or Not Appropriate statuses are essential for future analysts.

## Governance Implications and Recommendations
- Enforce a unified data model:
  - Maintain consistent identifiers (Square, Plot Type, Plot Number, Plot ID) and standardized header/species fields across all plot types.
- Require complete metadata and provenance:
  - Capture GPS context, plot maps status (Drawn/Edited/Redrawn), photo references, and relocation rationale as part of the core metadata.
- Strengthen data quality controls:
  - Implement mandatory validation steps at data entry, with automated checks for nested plot consistency, non-overlapping linear plots, and reasonable cover sums.
- Support data lifecycle management:
  - Establish clear processes for creating new plots, replacing unfound plots, and retiring outdated plots, with transparent versioning.
- Facilitate data sharing and discovery:
  - Maintain accessible data schemas and documentation to enable reuse by researchers and data stewards; ensure data uploads to portals follow defined conventions.
- Plan for interoperability:
  - Map the VegPlots/ArcMap data structures to common biodiversity data standards where possible to improve interoperability and future integration.