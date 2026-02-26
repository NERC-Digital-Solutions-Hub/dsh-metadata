# SEOSAW Field Manual

## Executive snapshot
- A field protocol for establishing and maintaining long-term plots across savannas, woodlands, and forests in southern Africa.
- Emphasizes standardized data collection, metadata, and compatible data sheets to enable cross-site and global comparisons.
- Recommends digital data capture (Android tablets with ODK) and Excel sheets, plus GIS and drone tools to improve plot placement, measurement accuracy, and data integration.
- Provides detailed procedures for plot design, stem-level measurements, marking, species identification, height estimation, regeneration monitoring, and plot re-measurement at ~5-year intervals.

## Data governance, standards, and lifecycle
- Central goal: ensure data are consistent, interoperable, and reusable for long-term analyses and cross-site comparisons.
- Data are organized around two core datasets:
  - Plot-level metadata (design, location, environment, land use, management, and protocol details).
  - Stem-level data (individual stems, bases, and associated attributes such as species, diameter, POM, status, and recruitment).
- Key data practices:
  - Use standardized plot data sheets and stem data sheets; treat every row as a record for easy cleaning and analysis.
  - Do not reuse tag numbers; maintain stable base IDs to track stem lineage across censuses.
  - Capture both live and dead stems, including fallen and resprouting stems; record missing stems with careful verification (topkill vs mislocation).
  - Collect and store vouchers for species identification; attach or bury tags to minimize disturbance; photograph living and herbarium specimens when possible.
  - Maintain a clear data provenance trail (authors, PI, institution, contact details) and align with Nagoya protocol requirements for international transfer of specimens.
- Data capture and integration:
  - Field data entry via Android tablets using the SEOSAW data sheets; later consolidation into standardized datasets for analysis.
  - Include geometry, coordinates, slope, aspect, and altitude in plot metadata to enable slope-adjusted area calculations and cross-site alignment.
  - Ensure consistency in units and measurement definitions (e.g., POM = 1.3 m or 0.3 m, diameter to 0.1 cm precision).

## Plot design and establishment (workflow)
- Location criteria:
  - Plots placed in homogenous soils and land-use history areas; informed consent obtained from landowners and users.
  - Prefer long-term access and institutional support; avoid areas likely to be permanently converted; random or stratified random placement within strata.
- Plot shape and size:
  - 0.25, 0.5, or 1.0 ha plots; 1.0 ha squares preferred; shape options include circle, square, or rectangle.
  - For slope, record slope, aspect, and corner altitudes to allow planar-area calculations later.
  - Begin with random points using GIS; reserve extra points as backups.
- Location technology and tools:
  - Use GIS for randomization; tablet GPS for field placement; drones (e.g., DJI) to assess suitability and reduce field effort; drone photogrammetry (Pix4D, Metashape) for post-processing are recommended with appropriate hardware.
- Plot marking and visibility:
  - Mark plot corners or center with durable markers (concrete posts, steel droppers, or cryptic marking when necessary); ensure markers withstand field conditions and re-measurement needs.

## What to measure and how (core data)
- 5.1 Tree stems (minimum dataset):
  - Measure all stems that meet inclusion criteria (base ≥ 50% inside plot and diameter threshold ≥ 5 cm or 10 cm; dead and fallen stems included if contiguous with base).
  - Assign Tag ID or Stem ID; record species (morphospecies acceptable when needed); note Alive/Dead status and cause; indicate Standing/Fallen; record if damaged, broken, or on termite mounds; optional spatial position coordinates; optional height measurements.
  - For climbers, measure at multiple points if applicable to enable cross-site comparisons.
- 5.2 Diameter and Point of Measurement (POM):
  - Measure DBH at default or adjusted POM (1.3 m standard; 0.3 m alternative if necessary).
  - Record exact POM height and adjust if needed due to deformities, buttresses, forked stems, or leaning trees.
  - Use diameter tape for ≥5 cm; calipers for smaller stems; document half-diameter methods when full round measurement isn’t possible.
  - For large trees, note “large tree” in notes to reduce data-entry errors.
- 5.3 Marking and mapping:
  - Tag stems with metal tags or painted numbers; place tag 20 cm above POM on the stem to ease relocation; alternative: bury tag at base if tagging is problematic.
  - Map stem locations within plots (10 m strips for coordinates; or center-based measurements for circular plots); consider differential GPS as an option with caveats.
- 5.4 Damage and status:
  - Record cut/broken height, cambial exposure, presence of bracket fungus, and whether the stem has fallen; if not rooted in soil, it’s not part of stem inventory (record as woody debris instead).
- 5.5 Alive/Dead status and topkill:
  - Classify stems as Alive or Topkilled (no life signs above POM); document cause of death and decay class where possible.
  - Use standard codes for mode (U, P, S, etc.) and causes (human, elephant, fire, etc.); record notes to aid interpretation.
- 5.6 Species identification:
  - Identify stems to species or morphospecies; collect vouchers when possible and work with botanists; store vouchers in appropriate herbaria; photos of living material and dried specimens are valuable.
- 5.7 Height:
  - Height estimation can be derived via site-specific height-diameter relationships or quick field methods (trigonometry, angle measurement) when direct height is impractical.
- 5.8 Stems on termite mounds:
  - Note if stems are on termite mounds as they influence species composition.
- 5.9 Data recording:
  - Use separate data sheets to record live stems, topkilled stems, new recruits, and stumps.

## Small stems, stumps, and coarse woody debris
- Small stems:
  - Poles (5–10 cm DBH), saplings, and seedlings included in optional subsampling (2 m x 50 m transects).
- Stumps:
  - Record diameter at top, height, diameter at 0.3 m above base, decay class, and species; note cause of break if relevant.
- Coarse woody debris:
  - Measure along cross transects, recording diameter at intersection, length, decay class, and species where possible; estimate density, volume, and biomass using standard equations.

## Plot re-measurement and longitudinal data management
- Re-measure approximately every 5 years; begin with a shorter initial cadence to resolve census errors and improve species identifications.
- Data integrity:
  - Revisit previous census data; include all prior measurements on the new datasheet to enable straightforward cleaning and analysis.
  - Use a recruit sheet for new stems; ensure tag numbers are never reused; track base IDs for recruits and resprouting.
  - If a stem dies, record alive/dead in subsequent censuses to avoid premature removal; if a stem is dead in two censuses, it can be removed from later field sheets.
- Demographic processes:
  - Track recruitment, resprouting, and topkill; maintain base IDs to link new recruits to their potential parent stems.
- Relocation:
  - Re-marker or relocate stems using POM references; if POM deteriorates, document and adjust with a new POM while preserving measurement continuity.

## Annexes and templates
- Annex 1: Plot data sheet (plot-level metadata: design, location, environment, land use, protection status, etc.).
- Annex 2: Stem data sheet (stem-level records: tag, base ID, species, POM, DBH, Alive/Dead, stem status, height, method, notes).
- Tools: Data entry templates, data sheets, and example data structures are available on the SEOSAW website; field data can be captured with open data kit forms and Excel sheets.