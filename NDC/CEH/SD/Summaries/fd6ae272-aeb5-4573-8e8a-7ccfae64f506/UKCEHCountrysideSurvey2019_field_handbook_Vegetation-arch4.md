# UK-SCAPE Field Survey Field Handbook 2019

- Purpose: Provide standardized procedures for recording vegetation plots across the UK-SCAPE project to quantify changes in vegetation over time, with an emphasis on repeatability, data quality, and metadata.
- Scope: Field protocol for vegetation plots using two plot sizes (Areal X plots of 200 m2 and 2x2 m soil plots), nesting of sampling within X plots, plot relocation, photography, and associated metadata.
- Data architecture: Data collected digitally via ESRI Collector and Survey123, with paper plot maps as backups; central Vegplots database stores header information, species presence/absence, cover, and relocation status.
- Timeframe and tradition: Many plots are repeat visits since 1978; emphasis on re-finding exact locations using GPS, sketch maps, and photographs.

## Data collection framework

- Plot types and sizes
  - 200 m2 X plots (VEGETATION): nested sampling across five expanding nests (Nest 0 to Nest 5) with cumulative species lists and cover estimates.
  - 2x2 m soil squares (SOIL): smaller nested plots recording ground flora with total cover estimates.
- Data to collect per plot
  - Header information: site name, recorder, slope, aspect, location, photos, plot type, square, plot number, plot ID.
  - Plot relocation status: Found, Not Found, New Plot (replacement for unfound), New Plot (new feature/land cover), Not appropriate, Access Denied, Too Dangerous.
  - Location data: geopoint (GPS), with accuracy, basemaps, and optional manual adjustments via full-screen map.
  - Plot description: slope, aspect, shade, whether plot map was drawn, and notes.
  - Vegetation height estimates for canopy, shrub, and ground layers.
  - Photos: two to three per plot to aid relocation and illustrate change.
  - Plot sketches: hand-drawn maps on waterproof sheets; GPS point marked; photos of sketches uploaded.
- Nest-based species recording
  - Nest 0: inner 2x2 m, species list with presence and estimated cover; total cover accounting for multiple life forms and substrates.
  - Nest 1–Nest 5: successive enlargements; additional species recorded if present; if absent in a nest, indicate accordingly.
  - Data entry includes an “Other” option for unidentified species with later replacement when identified.
- Taxa considerations
  - Emphasis on vascular plants; bryophytes and lichens recorded only from approved lists with predefined moss categories and bryophyte aggregation rules.
  - Aggregations/combinations used for difficult-to-separate taxa (e.g., Cardamine hirsuta/flexuosa) with preference for specific identifications when possible.
  - Prohibition on uprooting invasive species to avoid altering species richness; photos recommended for unidentified taxa.

## Plot relocation and metadata management

- Plot markers and relocation aids
  - Original plots marked with metal plates or wooden stakes; markers may be buried or displaced; metal detectors provided.
  - If plate cannot be detected within 5–10 minutes, relocate using sketch map and photos; label as Not Found if relocation is not reliable.
- Relocation rules
  - Consider land access and habitat context; document broad habitat (BH) and priority habitat (PH) for both plot and wider polygon.
  - Record disturbance and rationale in plot notes if relocation is poor or plot is no longer appropriate.
  - When access changes between surveys (refused land vs now accessible), prioritize repeat plots; add new plots only if time permits.
  - Inconsistent past plots kept if oldest known position can be re-found to maximize interval between surveys.
- Geopoint and accuracy
  - GPS coordinates captured at plot corners; use automatic geopoint with optional offline GPS; full-screen map available for precise adjustments.
  - Location averaging and multiple basemaps available for improved accuracy; document any relocation uncertainties.

## Field data collection workflow and tools

- Devices and apps
  - Collector for navigation to plots and initial map; Survey123 for form-based data entry (plot header, nest data, species, and photos).
  - Paper plots and sketch maps retained for backup and validation.
- Data entry flow
  - Navigate to plot in Collector; select plot symbol to open data entry form in Survey123.
  - For existing plots, do not re-enter data via the same path—use dedicated open/edit workflow per instructions.
  - On new plots or edits, begin with general header information, then proceed to plot-specific headers, and finally nest/species data.
- Plot recording and sections
  - Page 1: Plot header information (site, recorder, location, slope, etc.); initial relocation options.
  - Page 2: Plot-specific header information (varies by plot type; soils sampling guidance in separate handbook).
  - Page 3: Vegetation data entry (Nest 0 – Nest 5 for 200 m2 plots; 4 m2 for soil plots).
  - Plot photos: capture 2–3 images; ensure plot number and type are visible; indicate direction on sketch map.
- Data submission and integrity
  - Online submission via Send Now; offline mode saves to Drafts/Outbox; auto-save protects mid-survey loss.
  - If resubmitting, create a new survey copy to allow editing; include notes on version differences.
  - Completed data is uploaded to the Vegplots central database; incomplete entries trigger reminders before submission.

## Plot types and layout details

- X Plots (X1–X5)
  - Five predetermined random positions per square; arrangements include a 200 m2 vegetation nest and a 2x2 m soil nest.
  - Areal 200 m2 plots laid out with diagonals and colored strings to mark nested areas; inner nests defined with precise markers and diagonal references.
  - 4 m2 X plots oriented north-south or east-west; small, easily markable layout with precise corner references.
- Layout specifics
  - 200 m2 plots use central post and diagonal strings; nest 0 begins at inner corner, with subsequent nests expanding outward.
  - For arable land, plots are offset to avoid edge effects; when land is inaccessible or unsafe, random land selection within the same sector is used.
  - PLOT IDs and markers reflect square, plot type, and number; metal plates or stakes recorded for repeat plots when found.
- Species data collection within nests
  - Nest 0: presence list + covers for all vascular plants plus defined categories (litter, wood, rock, bare ground, water, bryophytes).
  - Nest 1–Nest 5: additional species recorded and assigned to correct nest; accumulation of species across nests provides a comprehensive vegetation snapshot.

## Species data collection and quality assurances

- Data entry approach
  - Use auto-type dropdowns to facilitate rapid data entry; unknowns captured via Other with free-text fields for later identification.
  - Total cover estimates aligned to the nest area; total cover may exceed 100% in layered vegetation (especially in habitats with tall layers).
- Bryophytes and lichens
  - Recording limited to listed mosses, lichens, and liverworts per Vegplots appendix; prioritize vascular plants but ensure bryophyte data contributes to total bryophyte cover.
  - Sphagnum categories and representative moss lists provided for consistency; full species identification not required in all cases.
- Aggregations and caution
  - Certain species are recorded as combinations when precise identification is difficult; use specific combinations only when unequivocal identification is not possible.

## Appendices and resources

- Appendix 1 – COLLECTOR & SURVEY123: installation and generic notes for both apps; operational tips for map navigation, data collection, and common GPS questions.
- Appendix 2 – Random numbers between 0 and 1: sample datasets to aid random point selection or stratification processes.
- Regional and organizational contacts: CEH and Environment Centre Wales offices with contact details for Lancaster and Edinburgh hubs.

## Endnotes: governance, accessibility, and subsequent use

- Data governance
  - Central Vegplots database stores plot-level data, species presence/cover, and relocation metadata to enable long-term analysis and trend assessment.
  - Photographs, plot sketches, and relocation notes support traceability and reproducibility for future surveys.
- Data accessibility and continuity
  - Protocols emphasize co-ownership and confirmation of user needs; data products should be discoverable and updatable through ongoing collaboration within the data community.
  - Emphasis on standardization to facilitate cross-square comparisons and integration with broader habitat and landscape data.