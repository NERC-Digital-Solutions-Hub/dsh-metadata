# VEGETATION PLOTS FIELD HANDBOOK: UK-SCaPE 2020

## Purpose, scope and data governance context
- Provides standardized field protocols for recording vegetation plots across UK-SCaPE surveys.
- Data are collected digitally via ESRI Collector and Survey123 to support repeatability, plot relocation, and long-term change detection.
- Emphasizes the importance of accurate metadata, plot relocation evidence (GPS, sketch maps, photos), and consistent data entry to enable robust analysis and discovery by others.

## Data model and required metadata (key fields)
- Plot header information (Page 1):
  - Square (survey square number)
  - Plot Type (X = 200 m² or XX = 2×2 m)
  - Plot Number, Plot ID (auto-generated or manual)
  - Surveyors (names/initials)
- Plot relocation status and location:
  - Found, Not Found, New Plot (Replacement for unfound), New Plot (New feature/Land cover), Not appropriate, Access Denied, Too Dangerous
  - Geopoint (GPS) captured automatically; accuracy considerations described
- Plot description and contextual data:
  - Slope, Aspect, Shade, Plot Map drawn (Yes/No/Edit/Redrawn), Habitat classifications (Broad Habitat BH; Priority Habitat PH)
  - Notes (disturbances, soil notes, species updates)
- Plot map and photos:
  - Plot Sketch Map protocol and photographic documentation to aid relocation
- Plot-level data for vegetation or soils squares:
  - For vegetation squares: nested 200 m² structure with multiple nests (Nest 0–5)
  - For soils squares: 2×2 m plots within X plots
- Species data:
  - Nested recording of species by quadrat size; ability to record “Other” taxa with free text or photo for later identification
  - Abundance/percent cover estimates, with total cover aiming for 100% (or higher where layered)
- Bryophytes and lichens:
  - Recorded using predefined lists; priority on vascular plants but certain bryophytes/lichens are captured as specified
- Special notes on data integrity:
  - Include all plots in a square (even if inaccessible or refused)
  - Avoid uprooting invasive species; if identified, photograph or note rather than uproot

## Data collection workflow and tools
- Data entry workflow:
  - New plots or edits via Survey123; location navigation through Collector
  - Use of random X-plot points; relocation guidance to minimize disturbance
  - For new plots, start with header information; for repeats, use existing plot IDs and relocation options
- Plot relocation and evidence:
  - Use GPS, sketch maps, and nearby features (photos) to relocate; if unreliable, mark as Not Found and create a New Plot
  - Relocation decisions consider habitat homogeneity and potential misclassification risk
- Plot recording process:
  - Page structure: Plot header (Page 1), Plot-specific headers (Page 2), Vegetation/Soil data (Page 3)
  - Nested nest approach for 200 m² vegetation plots (Nest 0 to Nest 5) and 4 m² soil plots
  - Nest data: presence/absence and “Total Cover” per species; bryophyte handling limited to specified taxa
- Technical workflow and offline capability:
  - Survey123 supports offline data capture; data can be sent when online, with drafts/outbox/sent states for submission management
  - Auto-save and data recovery features reduce data loss during disruptions
- Location capture nuances:
  - GPS readings taken at specific plot corners; location averaging and accuracy controls described
  - Full map viewing and multiple basemaps available for navigation and precision

## Data quality assurance and validation
- Embedded QA checks in the data entry forms (e.g., required fields, consistency of plot IDs, and completeness of plot headers)
- Guidance to maintain data integrity:
  - Record disturbances and reasons for non-recordable plots in notes
  - Avoid duplicate or blank species entries; use “Other” options for unidentified taxa with follow-up
  - Document changes to plot maps (edited/redrawn) with clear annotations
- Protocols to minimize impact on vegetation while ensuring census quality
- Explicit guidance on bryophyte and lichen recording limits and prioritization of total bryophyte data over exhaustive identification

## Data storage, sharing, and access
- Central data repository:
  - Vegplots central database for plot-level data, species lists, and habitat classifications
  - Data exchanged via Survey123 and Collector; online submission or offline draft/outbox flow
- Data discoverability and provenance:
  - Plot IDs, surveyors, dates, locations, and method details are captured to support reproducibility
  - Plot photos, sketches, and map revisions serve as data provenance artifacts
- Data update and editing workflow:
  - Use “Copy to new survey” when resubmitting edited forms
  - Submissions tracked in Sent, Drafts, and Outbox; ability to resend corrected forms
- Data governance considerations:
  - Publication-ready data should maintain consistent taxonomy, nest structures, and habitat coding
  - Clear records of when plots were Found vs Not Found, and rationale for replacements

## Metadata standards and habitat classification
- Habitat classification framework:
  - Broad Habitat (BH) and Priority Habitat (PH) categories used to classify plots
  - Appendix IV and related sections provide detailed habitat descriptions and examples (e.g., Broadleaved Mixed and Yew Woodland, Calcareous/Acid Grasslands, Wet Woodland, Orchards, urban habitats, etc.)
- Taxonomic and data standardization:
  - Use of predefined species lists with auto-type search; subset of bryophytes/lichens as specified
  - Aggregation/combination rules for difficult taxa (e.g., Cardamine hirsuta/flexuosa) to maintain consistency with historical data
- Appendices and technical references:
  - Appendix I: Collector & Survey123 generic reference guides (installation, map/navigation features, and data management)
  - Appendix II: Random numbers table for sampling references
  - Appendix III: Plot type listings by square (historical context)
  - Appendix IV: Habitat descriptions (detailed broad and priority habitat guidance)

## Practical governance implications and recommendations for data stewards
- Enforce a published data schema:
  - Maintain uniform field names, allowed values, and validation rules across Survey123 forms
- Ensure complete data capture and traceability:
  - Require header data, relocation status, GIS coordinates, photos, and sketch maps for every plot
- Support reproducibility and discovery:
  - Preserve plot IDs, nesting structure for vegetation plots, and habitat classifications with clear provenance
- Manage data lifecycle and accessibility:
  - Clearly document offline-into-online data transfer processes, submission states, and update workflows
- Mitigate interoperability risks:
  - Align with standard botanical data practices, and provide guidelines for handling non-native or ambiguous taxa
- Address common Data Steward challenges:
  - Plan for incomplete user needs and varying systems by maintaining clear governance roles, data dictionaries, and training materials
  - Establish processes to handle large numbers of plots, outdated maps, and non-interoperable formats by documenting relocation criteria and map editing rules

## Appendices and references (for governance and implementation)
- Appendix I: Collector & Survey123 generic reference guides (installation, map workflow, and data capture)
- Appendix II: Random numbers between 0 and 1 (sampling reference material)
- Appendix III: Plot types recorded in each square (historical context)
- Appendix IV: Habitat descriptions and priority habitat guidance (broad/narrow habitat classifications)