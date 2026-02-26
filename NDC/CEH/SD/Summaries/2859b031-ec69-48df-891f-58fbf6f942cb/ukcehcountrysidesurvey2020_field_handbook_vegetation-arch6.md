# UKCEH Countryside Survey 2021

- A vegetation field protocol for the summer 2021 survey (UK-SCaPE / UKCEH Countryside Survey) detailing how to locate, record, and relocate vegetation plots to quantify vegetation change across the countryside.
- Uses digital data collection via ESRI Survey123 and Collector to enable self-serve data access, with paper plot maps and photos for relocation support.
- Covers plot setup, data entry, site/habitat classification, bryophyte recording limits, data submission, and appendices with technical guides.

## Key aims and data focus

- Record presence and abundance of plant species across nested plots to quantify changes by habitat type and location.
- Capture essential plot metadata (location, size, habitat context) and relocation aids (sketch maps, plot photos).
- Produce data products (dashboards, reports, charts) that enable end users to explore vegetation change over time.
- Promote consistent data quality and repeatability across survey rounds.

## Plot types and layouts

- X plots (200 m² vegetation plots) and XX plots (2×2 m soil plots nested within larger plots).
- Areal structure:
  - X plots: five predetermined random positions per square; nest 0 (innermost) to nest 5 (outermost) for vegetation.
  - Soil nests: 2×2 m inside the X plots to capture soil/ground flora.
- Layout specifics:
  - Nest 0: inner 1×1 m area within the 2×2 m nest; record species and their % cover.
  - Nests 1–5: progressively larger areas; record additional species not present in inner nests.
  - Total cover per species across all nests should sum to about 100% (or more in layered vegetation).
- Plot relocation and markers:
  - GPS readings, plot sketches, and associated photos used to relocate plots in future surveys.
  - Metal plates or stakes mark older plots; diligence required as markers may move or vanish.
  - If relocation confidence is too low, mark as Not Found and create a New Plot (Replacement or New feature) rather than a direct repeat.
- Location rules:
  - New plots can be placed in most vegetation except urban areas or restricted land; record location as accurately as possible.
  - In arable fields or crop margins, apply specific rules to minimize disturbance (e.g., start 12 m into crop; use drill lines).

## Data capture workflow and tools

- Apps and navigation:
  - ESRI Collector: to locate plots on a map and access related Survey123 forms.
  - ESRI Survey123: to enter plot header information and nested plot data.
- Plot recording pages and headers:
  - Page 1: Plot header information (site name, recorder, slope, aspect, location, photos, plot type, square, plot number, Plot ID).
  - Page 2: Plot-specific headers (relevant to X or XX plots; soil sampling fields for X plots).
  - Page 3: Vegetation/soil data entry (Nest 0 through Nest 5; species lists with auto-type selection; optional “Other” entries for unidentified species).
  - Plot photos protocol: two to three photos per plot, with clear reference to plot number and nearby landmarks to aid re-finding.
  - Plot sketch maps protocol: precise, measurement-based sketches with GPS point, north arrows, and clear labeling; can be drawn on paper or on tablet.
- Relocation nuances:
  - Plot Recorded options: Found, Not Found, New Plot (Replacement), New Plot (New feature/Land cover), Not appropriate, Access Denied, Too Dangerous.
  - If Found, allow small relocation error (10–20 m in homogeneous vegetation is acceptable); otherwise use Not Found and record reasoning in Notes.
  - For X plots crossing a linear feature, place the plot in vegetated land with the linear feature near the edge, maintaining a 12 m buffer where possible.
- Data entry specifics:
  - Nest data: record species on Nest 0; add additional species in subsequent nests if present.
  - Bryophytes: recording limited to a defined list; avoid uprooting; photos or “Other” entries for unidentified species.
  - Aggregations/Combinations: use aggregated taxa where precise ID is not possible; avoid uprooting invasive species; photograph when uncertain.
- Submission and data integrity:
  - Online: Use Send Now to push fully completed surveys to central database.
  - Offline: Save as Drafts/Outbox and resend when online.
  - Copy to new survey: required to enable edits; auto-save protects progress.

## Taxonomic scope and quality notes

- Vascular plants prioritized; bryophytes/Lichens listed in Appendix 4.2; detailed bryophyte lists provided but total sampling emphasizes major bryophytes and mosses within Vegplots guidelines.
- Unknown species: use “Other” with free-text or photo submission for later identification; re-check and replace with correct names when identified.
- Data integrity: current software permits blank or duplicate species entries; reviewers must verify accuracy and consistency across nests and totals.

## Habitat classification and habitat key (Appendix IV)

- Broad Habitat categories (examples):
  - Broadleaved Mixed and Yew Woodland, Coniferous Woodland, Wet Woodland, Lowland Mixed Deciduous, Upland Mixed Ashwoods, Upland Oakwood, Urban Broad Habitat.
  - Grassland types: Improved Grassland, Neutral Grassland, Lowland hay meadow, Upland hay meadow, Calcareous Grassland (lowland and upland), Acid Grassland (lowland and upland).
  - Specialized habitats: Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Water (rare for X plots), Montane Broad Habitat (Mountain heaths; priority habitat), Inland Rock (including screes and lime-rich outcrops).
  - Hydrological/shoreline habitats: Fen/Marsh/Swamp, Purple Moor Grass and Rush Pastures, Reedbeds, Saltmarsh, Sand Dune, Supra-Littoral Rock, Strandline vegetation.
- Priority habitats: limestone pavement, inland rock outcrop/scree, calcareous/mountain/peatland variants, purple moor grass and rush pastures, reedbeds, and other Annex 1/PH classifications.
- Habitat allocation guidance: assign Broad Habitat polygons first, then identify any Priority Habitat within (or nested within) those polygons; habitat descriptions link to National Vegetation Classification (NVC) communities and regional specificity.

## Appendices: technical references and guides

- Appendix I: Collector & Survey123
  - Installation, map use, GPS/location tips, My Surveys workflow, collecting, drafts, outbox, sent surveys, and basemap management.
  - Guidance on GPS accuracy indicators and troubleshooting.
- Appendix II: Random numbers between 0 and 1
  - Provided as generic references for sampling procedures.
- Appendix III: Plot types recorded in previous surveys
  - Details the historical plotting scheme (Areal, X plots, soil plots, and various managed/targeted habitats).
- Appendix IV: Habitat descriptions
  - Detailed criteria and example species for each Broad Habitat and Priority Habitat category (woodlands, grasslands, wetlands, urban, montane, inland rock, etc.).
  - Guidance on how to classify felled conifer areas and evolving habitat post-disturbance.

## Practical considerations and challenges

- Time invested in understanding the ask and data needs, especially when teams have patchy data or access issues.
- Handling patchy data, multiple data formats, and access across different systems.
- Communicating complex data clearly to end users and promoting outputs for broader reuse.
- Ensuring consistent relocation accuracy; deciding when a plot remains a valid repeat versus new feature due to habitat heterogeneity or land-use change.
- Data governance: clear audit trail via plot IDs, Rep IDs, relocation notes, and photos to support reproducibility and future QA checks.

## End-to-end takeaway for data-oriented use

- This protocol provides a comprehensive, repeatable framework to capture vegetation data at multiple spatial scales with robust relocation aids, enabling precise long-term monitoring.
- The data workflow supports offline and online collection, QA-friendly data structures, and clear pathways to publish data products and dashboards for stakeholders.
- The habitat key and appendices equip data supporters with the contextual metadata necessary to classify vegetation stands consistently across time and space.