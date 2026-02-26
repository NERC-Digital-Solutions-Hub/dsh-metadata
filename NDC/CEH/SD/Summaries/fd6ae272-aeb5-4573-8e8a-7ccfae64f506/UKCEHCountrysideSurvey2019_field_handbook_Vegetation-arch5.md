# UK-SCAPE Field Survey Field Handbook 2019

## Overview
- Field protocol for recording vegetation plots across UK-SCAPE projects.
- Uses ESRI Collector and Survey123 apps to standardize data capture and storage.
- Two plot sizes: 200 m² vegetation plots (X plots) and 4 m² soil/vegetation plots (sub-nests within X plots).
- Repeated plots traced back to 1978; data enable quantification of vegetation change by habitat and location.
- Data intended for centralised storage (Vegplots) with emphasis on metadata, traceability, and future re-use.

## Data Governance and Standards
- Unique identifiers: Square, Plot Type (X or XX), Plot Number, Plot ID (Square + Plot Type + Plot Number).
- Comprehensive header metadata per plot: site name, recorders, slope, aspect, location, photos; plot maps (paper and digital), and plot sketches.
- Data types: presence/absence and cover percentages across nested plots; multiple species lists with auto-type entries; total cover targets (approximately 100% in nests).
- Taxonomic handling: preference for species-level identification; predefined aggregations for difficult taxa; explicit guidance on bryophytes (mosses, lichens) and Sphagnum categories.
- Data quality and integrity: QA prompts in Survey123; warnings about blank or duplicate entries; requirement to record plots even when inaccessible; notes on disturbances and non-appropriate plots.
- Data sharing and updates: support for offline data entry with later syncing; explicit submission workflows to a central Vegplots database; process for resubmitting edited or corrected surveys.
- Documentation and provenance: detailed appendices with software tools (Collector & Survey123) and workflows to ensure reproducibility.

## Data Collection Workflow
- Data collection tools:
  - Collector app for navigating to plots and initiating data entry.
  - Survey123 for plot data forms (header, plot-specific headers, and vegetation data).
- Plot entry sequence:
  - 2.3 Plot Recording in Veg Plots: minimize disturbance; record header, relocation status, and vegetation data.
  - 2.3.1 Plot header information (Page 1): pre-filled fields when re-recording; manual entry for new plots; geopoint capture with GPS.
  - Plot relocation options: Found, Not Found, New Plot (Replacement), New Plot (New feature), Not appropriate, Access Denied, Too Dangerous; notes on relocation accuracy and disturbance.
  - Geopoint capture: offline GPS when available; online basemaps to check accuracy; multiple location methods (location panel and full-screen map).
  - 2.3.1.1 Rules for plot relocation: land access checks; habitat broad/wide polygon classifications; priority habitats; tree disease indicators; relocation rules to minimize habitat misclassification.
- Plot design and placement:
  - 3 Plot types: Areal plots (200 m²) and Soil plots (4 m² nests within the 200 m² plot).
  - 3.1 X Plots (X1–X5): five predetermined random positions per square; nested 200 m² vegetation squares with 2 m × 2 m soil squares.
  - 3.1.1 Locating X plots: use random point maps; avoid crossing features; relocation plates (where present) and their recovery challenges; sea/inland water or unsafe land may require relocating to available land within the same sector.
  - 4 m² X plots: orientation and placement rules for arable and non-arable contexts.
  - 200 m² X plots: bordered by diagonal strings; nested subplots identified as nests 0–5; precise placement guidance for Nest 0 through Nest 5.
  - Plot maps: use of provided sketch maps; if maps are inadequate, indicate edits or redraws; photographing updated maps.
- Species data collection:
  - Nest 0 (innermost 1 m² area within Nest 0 for vascular plants plus bryophyte categories).
  - Nest 1 and subsequent nests: additional species in progressively larger nested areas; note when species appear only in nests beyond Nest 0.
  - 4 m² soil plots have similar species recording with full cover assessments.
- Data entry and validation:
  - Auto-type species lists; free-text “Other” entries for unidentified species with later identification recommended.
  - Covers recorded to the nearest 5% and must sum to ~100% for each nest (or higher in layered vegetation).
  - Summary of species at page bottom; warnings about blank or duplicate entries.
- Completing and submitting data:
  - Online submission via “Send Now” when online and survey is complete.
  - Offline submission via “Send Later”; drafts and outbox functionality; ability to resend and annotate correct version notes.
  - Auto-save features reduce data loss during interruptions.

## Plot Management and Metadata
- Plot headers include location, site, plot type, square, plot number, and Plot ID; GPS/geopoint data captured for repeatability.
- Plot relocation documentation emphasizes the use of photos, sketch maps, and GPS to refind plots in subsequent surveys.
- Plot maps and sketch maps are essential data products; edits are allowed with explicit notation (Edited/Redrawn) and clear provenance.
- Disturbance notes: capture reasons for plot loss (e.g., mowing, burning, inundation) and disturbance type in the Notes field.

## Data Quality Assurance and Documentation
- Repeated plots necessitate careful documentation of relocation accuracy and habitat context to avoid misinterpretation of vegetation change.
- Bryophyte data are constrained to a listed Moss/Lichen set; total bryophyte and Sphagnum measurements prioritized over exhaustive species-level identifications.
- Aggregations/combinations are allowed for troublesome taxa to preserve comparability with historical data.
- Users are urged not to uproot invasive species and to rely on photographic evidence for unidentified species to avoid altering species richness.

## Data Submission, Access, and Update Protocols
- Online and offline data submission workflows ensure data are stored centrally and can be revisited for QA checks or updates.
- “Copy to new survey” is necessary to enable editing after submission; resubmissions should include notes about which version is correct.
- Drafts, Outbox, and Sent sections manage survey lifecycle; “Submit” actions trigger central database updates.
- Data records, including plot IDs and nest-level species data, are designed for long-term discoverability and re-use.

## Appendices and Tools
- Appendix 1 – COLLECTOR & SURVEY123: installation guidance, app components, GPS and map functions, My Surveys, Download Surveys, and detailed app usage (Map, Collect, Basemaps, Location Accuracy, Favorites, Settings, etc.).
- Appendix 2 – Random numbers between 0 and 1: example datasets illustrating randomized plot allocations or sampling processes used in field protocols.

## Support and Contacts
- CEH Lancaster and CEH Edinburgh offices listed with addresses and contact details for project support and coordination.

## Data Steward Takeaways
- The Handbook provides a robust framework for data governance: consistent plot identifiers, comprehensive header metadata, standardized data capture workflows, and explicit data submission processes.
- Metadata, provenance, and traceability are embedded through relocation protocols, plot maps, photos, and sketch maps.
- Data quality is maintained via nested, hierarchical species recording, predefined taxonomic aggregations, and explicit QA prompts.
- Offline-first data collection supports resilience in field conditions, with clear pathways to update and share data centrally.