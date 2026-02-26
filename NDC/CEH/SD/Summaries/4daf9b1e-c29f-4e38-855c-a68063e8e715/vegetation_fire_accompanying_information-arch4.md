# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011

## Objective and study scope
- Aims:
  - Characterise wildfire effects on blanket bog plant communities immediately after the fire.
  - Compare vegetation communities and wildfire effects in open bog vs. near drains.
  - Determine long-term vegetation recovery using a chronosequence approach.
- Study area and timeline:
  - Four study sites: Bighouse (BH), Forsinard (FD), Croft 1 (CR), Shurrery/Dorrery (SH).
  - Fire history: the 2019 wildfires together with historic fires from 1997, 2000, and 2011.
  - Time-since-burn categories used for analyses: 1, 8, 20, and 38 years.
- Land ownership and habitat context:
  - Sites reflect different landholdings; efforts to sample areas representative of typical habitat (mire, blanket bog) and to align with National Vegetation Classification (NVC) frameworks.

## Sampling design and site structure
- Plots and replication:
  - 48 plots in total: four sites × four plot types × three replicates.
  - Plot types per site: burnt bog, burnt drain, unburnt bog, unburnt drain.
- Plot layout and within-plot sampling:
  - Burnt/unburnt bog plots are 5 ha each within a 125 m radius; drain plots are ~500 m long along a drain.
  - For each burnt bog plot, the nearest drain and the nearest unburnt bog area of similar slope/NVC are identified and sampled.
  - Replicates A-C exist for BH, FD, and CR; SH comprises three plots covering combined older fire areas.
- Quadrats and sampling points:
  - 356 quadrats surveyed (some duplication due to microtopography in 2019 sites).
  - Within each plot: five sampling points for bog plots (U1-U5) and five for drain plots (D1-D5).
  - Quadrat types per site: standard (ST), drain (DR), hummock (HU), hollow (HO) where applicable; older sites only have standard bog quadrats.
  - Each plot contains three bog quadrats (A-C) and associated 500 m drain segments near each bog plot.

## Field methods and data collected
- Quadrat setup and orientation:
  - 1 m x 1 m quadrats; left edge oriented north–south; located at GPS-confirmed points, north-facing view, marked with bamboo canes.
  - Drain quadrats located adjacent to drains, within ~10 cm of the drain wall.
- Data captured per quadrat:
  - Vegetation height: maximum and obscured height at three positions (centre, near end, far end) using a 1 m cane.
  - Microtopography: vertical height difference within a 1 m radius circle.
  - Ground cover: percent cover of plants, litter, bryophytes, rocks, bare peat, water, etc., with a 1–100% scale; layers for water and vegetation are recorded separately when pools are present.
  - Species data: total cover per species, dominant species at quadrat centre; taxonomic group codes used when species cannot be separated.
  - Special categories: dead vs burnt vegetation, litter, deer signs, seeds, seedlings (Sitka spruce, Lodgepole pine), and presence of water or pools.
  - Fire impact metrics (burnt plots at 2019 sites): Sphagnum discoloration and capitulum loss, non-Sphagnum moss damage, moss survival, dwarf shrub resprouting, ericaceous seedling frequency, field notes, and oblique photos.
- Data handling and recording:
  - Wildfire Vegetation recording forms used; daily field data scanned to PDFs; photos stored on Forsinard server; specimens kept for lab verification.
  - Data entry and quality checks performed by multiple staff; sums of covers checked for consistency; observer training conducted pre-field to reduce variability.

## Datasets and data structure
- Wildfire_vegetation_cover.csv:
  - 356 quadrats across 67 vegetation-related variables.
  - Key fields: PlotID, site, fire status (BB burnt bog, UB unburnt bog), Year-burnt, plot, Qtype, date, dominant species, multiple height metrics, height differences, cover codes for all recorded taxa, deer signs, seedlings, water; multiple layers (alive, dead, burnt) for cover codes.
- Wildfire_vegetation_fire_impact.csv:
  - 116 entries for burnt plots from the 2019 fire.
  - Columns include SPH_DIS, SPH_CAP_LOSS, NON_SPH_LOSS, MOSS_SURVIVAL, VEGE_RESPROUT, ERI_SEEDLING, FIELD_NOTES, site/plot identifiers, Qtype, and point numbers.
- Data governance:
  - Two datasets produced; metadata and coding aligned with Appendix 1 (field forms) and Appendix 2 (species codes); consistent with NVC-related terminology and fire impact protocols.

## Standards, procedures, and references
- Methodological framework:
  - Forest-to-Bog (F2B) vegetation recording method; aligns with National Vegetation Classification (NVC) standards (Averis et al. 2004; Rodwell 1991).
  - Fire impact measures follow Davies et al. (2016) protocols and NatureScot endorsements.
- Instruments and calibration:
  - Field equipment: GPS, marking canes, cable ties, compass, measurement sticks, spirit level, camera, field guides, and specimen envelopes.
  - Calibration and training performed pre-field to minimize observer bias in ground-cover estimates.

## Data management, limitations, and context for data leaders
- Data management:
  - Centralized digital storage, standardized data entry, and multi-person quality control.
  - Clear versioning of field forms and photos; reproducible data collection workflow for multi-site peatland studies.
- Limitations and context:
  - COVID-19 prevented the planned one-year post-fire repeat surveys, affecting timeline for recovery assessment.
  - Variation in drainage status and land management between sites (e.g., drained vs. blocked drains) offers a cross-site perspective on drainage influence on recovery.
- Relevance for data strategy:
  - Demonstrates end-to-end data lifecycle: design, sampling, data capture, coding, storage, and quality assurance.
  - Provides structured, codified datasets suitable for cross-site synthesis, meta-analysis, or integration with other peatland vegetation datasets.
  - Highlights the importance of metadata completeness, standardized taxon coding, and documentation to enable reuse by partners and future researchers.