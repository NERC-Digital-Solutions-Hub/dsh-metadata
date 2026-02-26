# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011.

## Overview
- Investigates vegetation response to a 2019 wildfire across Flow Country peatlands, comparing burnt and unburnt areas and considering historical fires (1997, 2000, 2011).
- Employs a chronosequence approach to assess short-term effects and long-term recovery potential.

## Aims and scope
- Characterise wildfire effects on blanket bog plant communities immediately after fire.
- Compare vegetation between open ground and areas near drains.
- Determine long-term vegetation recovery using a chronosequence framework across multiple fire years.

## Study areas and experimental design
- Four study sites: Bighouse (BH), Forsinard (FD), Croft 1 (CR), Shurrery & Dorrery (SH).
- Within each site, four plot types: burnt bog (BB), burnt drain (DR), unburnt bog (UB), unburnt drain (UD).
- Plot structure: 48 plots total (4 sites × 4 types × 3 replicates); each plot contains five sampling points.
- Burnt bog plots are linked to the nearest drain plots (500 m drain segments); unburnt bog plots paired with comparable unburnt drains.
- Sampling focuses on mire vegetation (excluding non-mire NVC types and bog pools/springs).

## Sampling design and field plots
- Four sites, each with three replicate plots per type (A–C) and central random placement when possible.
- Burnt drain plots defined as 500 m drain segments nearest each burnt bog plot.
- Total of 48 plots and 356 quadrats surveyed (with some duplication in ST plots for BH and FD; later adjustments maintain dataset integrity).
- Plot types categories and replication lead to 240 quadrats for FD/BH and 120 for CR/SH, adjusted to 356 total due to field conditions.

## Field and sampling methods
- Vegetation sampling using 1 m × 1 m quadrats; standard orientation with the south edge as reference.
- For burnt bog plots, additional quad types: hummock (HU) and hollow (HO) quadrats; standard quadrats (ST) used across sites where applicable.
- Drain plots sampled along 500 m drain lengths with five points (D1–D5) spaced along the drain.
- For each quadrat, multiple data types recorded:
  - Dominant species and total percent cover for all taxa.
  - Maximum and obscured vegetation height at three positions (access end, centre, far end).
  - Microtopography and water depth; presence of standing/shallow/deep water.
  - Ground cover categories (bare peat/rock, litter, brash, dead vegetation, deer signs, fungi, seedlings, algae, lichens, etc.).
  - Specific fire impact measures for burnt plots (Sphagnum discoloration and capitulum loss, moss scorch/survival, dwarf shrub resprouting, ericaceous seedling frequency).
  - Oblique photographs of each quadrat and field notes.

## Data collection, handling and storage
- Field forms completed per quadrat using the Wildfire Vegetation recording form; data entered to two CSV datasets:
  - Wildfire_vegetation_cover.csv: 356 quadrats, 67 vegetation-related variables (covers, heights, species codes, dominants, etc.).
  - Wildfire_vegetation_fire_impact.csv: Burnt 2019 plots data (116 entries) focusing on fire impact metrics.
- Data captured with GPS, field maps, taxon codes, and standardized forms; specimens collected for lab verification.
- Post-field workflow included data entry, dual QA checks, and consistency verification of total cover sums.
- Data and images stored on Forsinard server and shared with partners as needed.

## Variables and data structure
- Primary identifiers: PlotID, site (BH, FD, SH, CR), plot (A–C), fire status (BB or UB), year since fire (YR-burnt), point number (O1–O5 or D1–D5), Qtype (ST, DR, HU, HO).
- Measurements per quadrat: dominant species, multiple height readings (Max_height and Obscured_height at A/C/F positions), Height_diff_max_min, Height_diff_hum_hol, ground cover percentages, presence of water, count of seedlings/deer signs, and other ecological indicators.
- Fire impact metrics for burnt plots: SPH_DIS, SPH_CAP_LOSS, NON_SPH_LOSS, MOSS_SURVIVAL, VEGE_RESPROUT, ERI_SEEDLING, FIELD_NOTES.
- Species and variables coded via Appendix 2 (extensive taxon coding and groupings).

## Calibration, quality assurance and governance
- Field calibration: pre-season training to reduce observer variability in cover estimation and species identification.
- Quality checks: cross-plot total cover validation (target 85–150%; some >150% legitimate due to overlapping canopies and water layers).
- Field documentation includes standardized recording forms, photographic evidence, and careful quadrat marking to minimize trampling and ensure replicability.
- Data governance considerations highlighted, including openness of underlying data and metadata concerns typical for monitoring frameworks.

## Fieldwork equipment and SOPs
- Required tools: GPS, printed maps, plant taxon codes, bamboo quadrat markers, cable ties, compasses, measuring sticks, spirit level, rulers, loupe, field guides, sample envelopes, cameras.
- SOPs followed:
  - Forest-to-Bog (F2B) vegetation recording methodology.
  - Davies et al. (2016) fire impact measurements for burnt plots (standard, hummock, hollow quadrats).
  - Alignment with National Vegetation Classification (NVC) guidance for mire communities.

## Relevance to monitoring framework authors
- Demonstrates a rigorous, standardized approach to long-term environmental health monitoring across multiple sites and fire histories.
- Highlights the importance of:
  - Clear experimental design enabling cross-site comparability.
  - Use of established vegetation classifications and field protocols.
  - Comprehensive data capture (cover, structure, microtopography, hydrology, and fire impacts).
  - Robust data handling, storage, QA, and governance, including plans for open data sharing and metadata quality.
- Outlines practical challenges many monitoring programs face:
  - Data gaps and access barriers (e.g., metadata quality, dataset fragmentation, need for originator data).
  - Siloed information within/between organizations.
  - Barriers to public data sharing and ensuring up-to-date datasets.
  - Impact of external factors such as COVID-19 on planned repeated measurements.

## Notes on limitations and constraints
- Planned repeat surveys to assess yearly recovery could not be completed due to COVID-19 restrictions.
- Some older fire areas had limited sampling in comparison with the 2019 fire, reflecting landownership and habitat differences.