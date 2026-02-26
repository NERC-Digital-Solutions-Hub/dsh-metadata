# UKCEH Countryside Survey 2021

## Overview
- Vegetation field protocol handbook for the UK-SCaPE / UKCEH Countryside Survey (summer 2021).
- Defines standardized field data collection for vegetation plots to quantify countryside changes with high spatial precision.
- Emphasises map-based data capture, plot relocation, data quality assurance, and habitat classification for reporting.

## Plot types and sampling design
- Two plot sizes and types:
  - X plots (200 m² vegetation plots) with nested sub-squares (Nest 0 to Nest 5) for detailed species and cover data.
  - XX plots (4 m² soil plots) representing the smaller nested soil sampling unit.
- Nest structure:
  - 200 m² plot: nested data collection starting at Nest 0 (innermost 1 m² region) then expanding to larger nests up to 14.14 m × 14.14 m (200 m²).
  - 4 m² soil plots: data collected within Nest 1, recording species and cover for the smaller quadrat.
- Areal layout and markers:
  - X plots positioned at five predetermined random positions within a 1 km square; 2×2 m soil nests within each X plot.
  - GPS-based positioning at plot corners for reproducibility; metal plates or stakes (when present) used as relocation markers.

## Data collection workflow (GIS-enabled)
- Apps used: ESRI Collector and Survey123 (ArcGIS ecosystem) for map-based data entry and form-based data capture.
- Offline-first design with online submission:
  - Collect data via Collector to locate plots and launch Survey123 data entry forms.
  - Data can be saved offline as drafts and later sent when online.
  - “Copy to new survey” option required to enable editing of entries after submission.
- Navigation and data entry:
  - Plot navigation via a map, then launching forms for header information, plot-specific headers, and species data.
  - Plot relocation status tracked in the form (Found, Not Found, New Plot, Not Appropriate, Access Denied, Too Dangerous).
- Plot positioning and accuracy:
  - Geopoints captured automatically (offline GPS available); online mode offers an on-map accuracy check and basemaps.
  - Location averaging and accuracy thresholds used to ensure reliable coordinates.

## Plot relocation and positioning
- Relocation process:
  - If a prior plot cannot be relocated satisfactorily, mark as Not Found and create a new plot at a new location.
  - Allow relocation error in homogeneous vegetation; more caution in heterogeneous habitats.
  - Inaccessible or land-use changed plots may be recorded as Not Appropriate.
- Five-sector overlay:
  - Used to identify feasible new X-plot locations within a square when land is scarce.
  - Ensures new plots are placed away from sensitive features (e.g., crops) to avoid trampling effects.

## Plot recording details (headers, nesting, species)
- Plot header information (Page 1):
  - Square number, Plot Type (X = 200 m²; XX = 2×2 m), Plot Number, Plot ID (auto-generated), Surveyors, location details, slope, aspect, and photos.
  - Plot relocation status, notes on disturbances, and whether the plot map was drawn/edited/redrawn.
- Plot-specific headers (Page 2):
  - Plot-type-relevant fields (e.g., soil sampling data for X plots; soil sample status; scanning barcodes for soil samples).
  - Broad Habitat (BH) and Priority Habitat (PH) selections at both plot level and wider polygon level.
- Entering species (Nest 0–Nest 5 for 200 m² plots; Nest 1 for 4 m² soil plots):
  - Nested species lists with cumulative recording across nests (Nest 0 to Nest 5; Total Cover per species per nest).
  - Use of “Other” with free-text entry for unidentified species; option to attach a photo for later identification.
  - Bryophytes: recording limited to listed mosses and bryophytes as per protocol; focus on total bryophyte cover rather than exhaustive identification.
  - Areal spacing and nest-specific cover: hierarchical recording where Nest 0 captures base data and subsequent nests capture new species not present in earlier nests.
- Data quality:
  - The software validates required fields before submission; warnings appear if data are incomplete.
  - Note: blank or duplicate species entries may occur; operators must verify accuracy.

## Plot sketches and photos
- Plot sketch maps:
  - Essential for relocating plots in future surveys; drawn with measured distances, compass bearings, and GPS reference point.
  - North arrow required; clearly labeled with square and plot numbers; photos of maps can be taken after sketch completion.
  - If a sketch map is inadequate or changed, mark as Edited or Redrawn with initials and date.
- Plot photos protocol:
  - Two to three photos per plot location, focusing on nearby stable features to aid relocation (e.g., rock, tree, fence post).
  - Photos must show plot number and type; include orientation notes on the plot sketch map.

## Data submission and QA
- Submission options:
  - Online: Send Now to central database; Copy to new survey to enable later edits.
  - Offline: Drafts, Outbox (unsent), and Sent (submitted) available; auto-save protects in-crash scenarios.
- Quality assurance:
  - Software prompts remind users to complete missing fields before submission.
  - Data integrity is maintained through standardized field definitions (BH/PH, location accuracy, plot maps).

## Habitat classifications (Broad and Priority Habitats)
- Broad Habitat (BH) classifications:
  - Includes Broadleaved Mixed and Yew woodland, Coniferous woodland, Arable & Horticulture, Improved/Neutral grasses, Urban, Fen/Marsh/Swamp, Bog, Montane, Inland rock, Rivers/Water bodies, and more.
  - Examples provided for major woodland types (lowland mixed deciduous, upland oaks, wet woodland, upland birchwoods, etc.) and grassland types (improved, neutral, hay meadows) with National Vegetation Classification (NVC) references.
- Priority Habitat (PH) classifications:
  - Includes Limestone pavement, Inland rock outcrop and scree, Coastal cliffs, Sand dunes, Saltmarsh, Reedbeds, Purple moor grass and rush pastures, Bog species complexes, and Urban-related habitats.
  - Detailed descriptions guide assignment of polygon-level PH within Broad Habitats.
- Recording guidance:
  - Use BH/PH to classify plots and broader polygons (minimum mappable unit) for reporting (e.g., Biodiversity Action Plan, habitat inventories).
  - Special notes on recording managed landscapes (orchards, drained/feral areas) and responses to habitat changes (e.g., post-logging vegetation as Broad Habitat rather than coniferous woodland if conditions have altered).

## Appendices and practical references (GIS workflow aids)
- Appendix I: Collector & Survey123 generic reference guides (installation, map interactions, data collection paradigms).
- Appendix II: Random numbers between 0 and 1 (used for sampling processes and reproducibility).
- Appendix III: Plot types historically recorded in prior surveys (helps maintain consistency in long-term datasets).
- Appendix IV: Detailed habitat descriptions and PH/BH allocations to assist consistent GIS classification.