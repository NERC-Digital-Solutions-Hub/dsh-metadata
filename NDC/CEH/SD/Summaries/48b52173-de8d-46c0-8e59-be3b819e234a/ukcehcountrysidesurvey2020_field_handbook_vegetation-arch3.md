# VEGETATION PLOTS FIELD HANDBOOK: UK-SCaPE 2020

- Purpose and scope
  - Field protocol for recording vegetation presence, abundance, and habitat context to quantify changes in the countryside over time.
  - Aims to support monitoring frameworks by providing standardized data for policy scrutiny, evaluation, and future decisions.
  - Emphasizes repeatability, data provenance, and clear communication of methods and results.

- Relevance to monitoring frameworks
  - Establishes a standardized, time-series capable data collection structure (plots, nests, and habitat classifications).
  - Uses explicit relocation, metadata, and data quality controls to support data governance and comparability.
  - Integrates field data collection with digital tools to improve data accessibility, transparency, and dissemination.

- Data collection architecture
  - Plot types and nesting
    - X plots: 200 m² vegetation plots (14.14 x 14.14 m) with nested subplots (Nest 0 to Nest 5) for progressively larger photograph/record coverage.
    - XX plots: 2x2 m soil plots nested within the larger plot.
    - Nest scheme: Nest 0 (inner 1x1 m), Nest 1 (2x2 m), expanding outward through Nest 5 to cover the full 200 m².
  - Data capture tools
    - ESRI Collector for plotting and navigation.
    - ESRI Survey123 for entering plot data via structured forms.
    - Digital plot maps complemented by paper sketches for relocation.
  - Data fields and structure
    - Plot header information: square, plot type, plot number, plot ID, surveyors, location, slope, aspect, photos.
    - Plot relocation data: Found, Not Found, New Plot (Replacement/New feature), Not appropriate, Access Denied, Too Dangerous; notes on disturbance and relocation accuracy.
    - Plot maps and photos: mandatory for relocation; photos highlight distinctive nearby features to aid relocation.
    - Plot specifics: header fields per plot type (vegetation vs. soil) with relevant sampling guidance.
    - Species data: nested nests with presence/absence and percent cover; bryophyte priority lists; ability to enter “Other” species or unknowns with photos.
    - Abundance estimates: total cover per species across nests; guidance to sum to around 100% (allowing layered vegetation).
  - Documentation and output
    - Plot sketch maps with GPS point, bearings, and distances; field notes on disturbance and land use changes.
    - Plot photos annotated with plot number/type; directions recorded on sketch maps.

- Plot relocation and positioning
  - Positioning methods
    - GPS geopoint captured (prefer offline GPS); if online, map aids aid accuracy verification.
    - South corner GPS reading for X plots; specific corner reference for 2x2 m soil plots.
    - Sketch maps and photos used to re-find plots across surveys.
  - Relocation rules and judgement
    - Found: location close to previous position; minor relocation error acceptable in homogeneous habitats.
    - Not Found / New Plot: when relocation cannot be confidently confirmed; document disturbance and rationale.
    - Field constraints: land access, habitat change, or safety considerations may necessitate plot non-recording or relocation adjustments.
  - Sector-based relocation (X plots)
    - Five-sector overlay guides new X plot placement when land is scarce; avoid edge effects in arable fields by placing plots 12 m from edges.
  - Documentation of mapping changes
    - Edited/Redrawn maps recorded with explicit notes and dates; ensures transparency about map quality and changes.

- Data entry workflow and quality control
  - Nest-based species recording
    - Nest 0: record presence in the innermost 1x1 m; assign initial total cover across nests.
    - Nest 1: record additional species within the 2x2 m nest; flag species newly appearing in nest 1.
    - Nests 2–5: progressively search outward; record new species only if present; indicate when no additional species are found.
    - Bryophytes and lichens: limited to listed species; focus on total bryophyte cover and key Sphagnum categories.
  - Species data entry and validation
    - Use auto-type dropdowns; enter “Other” for unknowns with free-text entry; photos can be taken for later identification.
    - Ensure total cover per species is entered for all nests; watch for blank or duplicate entries.
  - Plot descriptions and habitat context
    - Record slope, aspect, shade, plot map status (drawn/edited/redrawn), and contextual notes.
  - Data submission and management
    - Online submission via Survey123 when connected; offline mode supports Drafts and Outbox with later submission.
    - Auto-save safeguards; ability to resend and track versions using “Copy to new survey” to enable edits.
  - Data governance and sharing
    - Requires recording plots and underlying data (plus photos and sketch maps) to support reproducibility and transparency.
    - Provides explicit guidance on data handling, quality assurance, and documentation to facilitate reuse and verification.

- Plot types, layout, and field protocols
  - 200 m² vegetation plots (VEGETATION) and 4 m² soil plots (SOIL)
  - Layout and measurement guidance for setting out nests and marker strings; diagonal layout for full X plot with nested perimeters.
  - Edge effects and land-use considerations: move plots to avoid crop damage; ensure plots remain within square boundaries when possible.
  - Handling of inaccessible or unsafe plots: document disturbance or decide not to record certain plots.
  - Habitat mapping and broad/narrow habitat context
    - Uses a comprehensive habitat classification framework (Broad Habitats and Priority Habitats) with detailed definitions and examples.
    - Habitat allocation supports downstream analyses and policy-relevant reporting (e.g., BAP reporting).

- Appendix and reference materials (supporting monitoring framework design)
  - Appendix I: Collector & Survey123 generic reference guides (installation, workflow, and feature usage)
  - Appendix II: Random numbers table (site selection / randomization context)
  - Appendix III: Plot types recorded in prior surveys (historical context and continuity)
  - Appendix IV: Habitat descriptions and priority habitat guidance (broad and detailed habitat classifications)
  - Notable content
    - Detailed bryophyte list and Sphagnum categorization to standardize mosses/lichens data collection.
    - Explicit guidance on not uprooting invasive species to maintain data integrity and comparability.

- Challenges and considerations for monitoring framework authors
  - Data availability and metadata
    - Requires robust metadata surrounding plots, dates, observers, and movement; potential barriers include data sharing constraints and comprehensive metadata requirements.
  - Data integration and governance
    - Standardized data formats (Survey123/Collector outputs) support integration into central monitoring systems; explicit data provenance and versioning improve governance.
  - Data quality and consistency
    - Nested plot design (Nest 0–5) and standardized species lists support comparability across surveys and years; QA checks catch missing fields and potential entry errors.
  - Access and reuse
    - Emphasis on sharing underlying data (and plots) to support transparency; design considerations to minimize barriers while protecting sensitive information.
  - Practical considerations
    - Use of mobile apps enables offline data capture and synchronization; relocation challenges require sound field judgment and clear documentation.

- End notes
  - The Vegetation Plots Field Handbook provides a comprehensive, time-series-oriented protocol for consistent vegetation monitoring, with explicit methods to improve data quality, relocation reliability, metadata capture, and governance aligned with monitoring framework needs.