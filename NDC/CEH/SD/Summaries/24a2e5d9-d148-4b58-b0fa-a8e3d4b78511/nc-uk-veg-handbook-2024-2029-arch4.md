# UKCEH Countryside Survey: Field Handbook 2024-2029

- Long-term vegetation survey designed to quantify countryside changes with high spatial and temporal precision using repeatable plot-based data.
- Data collected to support analysis by habitat type and landscape location, enabling trend assessment over decades.

## Data system and aims for leadership

- Emphasizes end-to-end data capture, from plot positioning to species presence and cover, photos, and sketch maps, to ensure repeatability and re-foundability.
- Centralized data pipeline: field data via mobile apps (FieldMaps and Survey123) feeding into a central database with offline-capable workflows.
- Data products are intended to meet user needs through careful metadata, documentation, and the ability to update and re-record plots across time.
- Encourages establishing a robust data asset with discoverability (digital and paper plot maps), versioning, and clear provenance (plot IDs, dates, surveyors).

## Data capture workflow and platforms

- Field data collection relies on ESRI FieldMaps to navigate to plots and Survey123 to enter data.
- Offline capability recommended; offline sync and subsequent online submission to a central database.
- Plot records begin with header information, proceed to plot-type-specific headers, then detailed vegetation data.
- Plot relocation and re-finding are core to the workflow, supported by GPS points, sketch maps, and multiple plot photos.
- Data submission:
  - Online: Use Send Now for direct upload to central database.
  - Offline: Save as Drafts/Outbox and submit later; auto-save protects against data loss.
  - Edits require creating a new survey copy when resubmitting.

## Plot types and data structure

- X plots (200 m2): Nested nests (Nest 0 to Nest 5) enumerating vascular plants with presence/absence and % cover, plus non-vascular components (litter, rock, bare ground, etc.). Nest 0 is the innermost 1x1 m area; nests progressively cover the full 14.14 x 14.14 m plot.
- Linear plots: B (Boundary), H (Hedgerow), S (Streamside), R (Roadside) plots; located along linear features and recorded in half of the squares that contain such plots.
- For each plot type, standard header fields include site name, recorders, slope, aspect, location, and date; scaling of vegetation height across canopy, shrub, and ground layers.
- X plots require soil sampling data in the header; field-specific soil sampling procedures are described in separate manuals.
- Species data: comprehensive drop-down lists with autotype support; if unidentified, use “Other” with a free-text entry; covers recorded in 5% increments; total covers may exceed 100% due to layering.
- Bryophytes and lichens: limited to listed mosses and bryophyte/lichen taxa; emphasis remains on vascular plant identification to maximize data utility.
- Plot-specific information includes relocation status (Found, Not Found, New Plot, Not appropriate, Access Denied, Too Dangerous) and notes explaining disturbances or reasons for non-recording.

## Metadata, quality, and validation

- Plot metadata (square, plot type, plot number, GPS coordinates, date, surveyors) are captured and used to generate a unique Plot ID (Square + Plot Type + Plot Number).
- Plot relocation rules govern when a plot is considered Found vs Not Found; relocation decisions balance relocation error with habitat stability and comparability over time.
- Sketch maps and photos accompany plots to aid re-finding in subsequent surveys; maps can be edited/redrawn with clear annotations when necessary.
- Quality controls include:
  - Mandatory fields prior to submission.
  - Alerts if essential data are missing.
  - Guidance to avoid uprooting invasive species; prioritize photo documentation for unidentified taxa.
- Documentation includes appendices with generic FieldMaps & Survey123 usage and random-number references to support random plot placement.

## Data governance, access, and lifecycle

- Data are managed centrally, with clear rules for submitting, drafting, and resubmitting surveys for data integrity and traceability.
- Plot IDs and metadata provide reproducibility and traceable lineage across survey cycles.
- Paper plot maps remain available for ease of use, with digital copies accessible via SharePoint or offline apps.
- Data provenance emphasizes retaining information about why plots were moved, lost, or deemed non-appropriate, to contextualize time-series analyses.

## Platforms, tools, and practical considerations

- FieldMaps and Survey123 are the primary tools for field data collection, with offline synchronization recommended.
- The FieldMaps interface supports map layers, basemaps, GPS accuracy indicators, and various plan views needed for precise plot relocation.
- Survey123 provides modular surveys with multi-page data entry, drafts/outbox management, and features to set default dates, scan barcodes, and capture photo/video evidence.
- Appendix guidance covers installation, usage, and common questions (e.g., GPS accuracy, offline work, and data restoration).

## End-to-end data lifecycle and reuse

- Data entered in the field flow into a central database, enabling long-term trend analyses and cross-square comparisons.
- Data are designed for iterative improvement: plots can be re-recorded, edited, or relocated with clear documentation of changes.
- The structure supports downstream analyses by habitat type and landscape location, facilitating policy- and planning-relevant insights.

## Key challenges and considerations for Data Leaders

- Data granularity and consistency: nested X plots and multiple plot types require rigorous standardization of protocols and metadata to ensure comparability over decades.
- Data access barriers and permission management: some plots may be inaccessible; decisions about recording and documentation in such cases must be explicit and traceable.
- Data quality variability: coordinates, plot maps, and photos must be sufficient to re-find plots; physical markers (plates/stakes) may be buried or displaced over time.
- Metadata richness vs. field practicality: comprehensive header and plot-specific data improve discovery and reuse but increase field workload; balanced design is essential.
- Coordination and standards: consistent taxonomy, taxon aggregation (e.g., certain species combinations), and bryophyte recording rules support cross-study comparability but require ongoing training and QA.

## Appendices at a glance

- Appendix 1: FieldMaps & Survey123 setup and generic notes, including app components, GPS location considerations, and how to access and manage surveys, maps, and basemaps.
- Appendix 2: Random numbers between 0 and 1, supporting random plot allocation and methodological transparency.

- Contact and repository details for UKCEH Countryside Survey field operations are provided for further guidance and support.