# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011.

## Overview and Aim
- Reports on wildfire effects on blanket bog vegetation across Flow Country, Scotland, focusing on autumn 2019 after May 2019 wildfires and prior historic fires (1997, 2000, 2011).
- Aims:
  - Characterise immediate wildfire effects on the blanket bog plant community.
  - Compare vegetation in open ground vs. drains (burnt and unburnt contexts).
  - Assess long-term vegetation recovery using a chronosequence approach.

## Study Context and Sites
- Area: Flow Country peatlands (wet heath and blanket bog) impacted by a ~60 km2 wildfire in spring 2019.
- Four study sites within SAC/landholdings:
  - Bighouse Estate (BH)
  - Forsinard NNR (FD)
  - Croft #1 (CR)
  - Shurrery & Dorrery (SH)
- Historical fires included: 2011 (Croft 1), ~2000 Shurrery, 1997 Dorrery; some older sites excluded from sampling due to habitat differences.
- Sampling design reflects land ownership and habitat similarity to 2019 fire areas, with emphasis on mire vegetation and exclusion of non-mire habitats (e.g., bog pools, mineral soil grasslands).

## Sampling Design and Plots
- Four sites x 4 plot types x 3 replicates = 48 plots in total:
  - Burnt bog plots (B)
  - Unburnt bog plots (U)
  - Burnt drain plots (DR)
  - Unburnt drain plots (UR)
- Plot layout and sizes:
  - Burnt/unburnt bog plots: 5 ha each, mapped as 125 m radius circles.
  - Drain plots: 500 m sections along drains, nearest to corresponding bog plots.
- Plot allocation per site:
  - BH, FD: three bog plots per site center within randomised 1 km squares.
  - CR: three bog plots chosen to match habitat; SH: one bog plot per fire area (from 1997 and 2000).
- Replicates per plot: A, B, C within each site and plot type.
- Total quadrats:
  - 356 quadrats surveyed (4 sites × 4 plot types × 3 replicates × 5 sampling points; plus variations for hummock/hollow replication at BH/FD).
- Timeframe: September–December 2019 (COVID-19 interrupted planned 2020 repeat survey).

## Quadrat Design and Field Measurements
- Quadrat size and placement:
  - Standard 1 m × 1 m quadrats; oriented north-south with GPS localization.
  - Drain quadrats placed adjacent to drains, within 10 cm of the drain wall.
  - Hummock (HU) and hollow (HO) quadrats used for BH/FD; ST quadrats used for all sites (CR/SH did not use HU/HO except in BH/FD).
- Sampling within each plot:
  - 3 quadrat types in BH/FD: ST (standard), HU, HO; plus DR (drain) quadrats along drains.
  - CR/SH: ST and DR only.
  - Five sampling points per plot (U for bog plots; D for drain plots).
- Data recorded per quadrat:
  - Vegetation height: maximum height and obscured height at three transect points (centre, bottom, far end).
  - Microtopography: vertical height difference within a 1 m radius.
  - Ground cover: percent cover of vegetation, litter, moss, bryophytes, water, bare ground, brash, seedlings, needles, fungi, dung, etc.
  - Species data: total percent cover per taxon; dominant species at the quadrat centre; various lumping rules for mosses and other taxa when species-level identification was not possible.
  - Fire impact metrics (for burnt plots): Sphagnum discoloration, capitulum loss, moss scorch, moss survival, dwarf shrub resprouting, ericaceous seedling frequency.
  - Additional notes: litter, deer signs, water depth, depth of pools, presence of seedlings, and presence of trees and seedlings.
- Photography: oblique photographs of each quadrat; photos of the recording form for documentation.

## Data Capture, Storage, and QA
- Field data handling:
  - Field recording forms used (Wildfire Vegetation recording forms) with detailed metadata (date, site, plot, Qtype, etc.).
  - All forms scanned to PDF; photos renamed and stored on the Forsinard server; shared with partners as needed.
- Data entry and quality assurance:
  - Data entry by Field Officer with support from ERI Technician; two-person QA to check dataset integrity.
  - Consistency checks on total cover sums (expected 85–150%, some >150% in specific quadrats due to overlapping layers like Sphagnum and water).
- Datasets produced:
  - Wildfire_vegetation_cover.csv: 356 quadrats, 67 vegetation/related variables (cover and structure data).
  - Wildfire_vegetation_fire_impact.csv: 116 burnt-quadrat entries (2019 fire) focusing on fire impact metrics (Sphagnum damage, moss survival, seedling frequency, etc.) plus field notes.

## Data Standards, Codes, and Documentation
- Vegetation classification:
  - Field methods aligned with Forest to Bog (F2B) procedures; NVC-based mire definitions used to identify target communities (blanket mires, raised/valley mires; exclusions noted for bog pools, springs, fens, and mineral soils).
- Taxonomic coding:
  - Detailed Appendix 2 code list for species and categories (e.g., Agrostis sp., Dicranoids, Sphagnum spp., ericoids, mosses, lichens, etc.).
  - Special handling for taxa not identifiable to species-level; lumping rules for mosses, grasses, sundews, etc.
  - Distinctions for live, dead, and burnt plant material (BURNT vs. DEAD) with responses for depth and water presence.
- Metadata and structure:
  - Key identifiers: PlotID (site, replicate, burn status), plot type (BB/UB etc.), Qtype, year since burn (YR-burnt), sample point (O1–O5, D1–D5).
  - Datasets capture both cover data (percent cover, dominant species) and fire impact indicators (Sphagnum indicators, moss survival, re-sprouting, seedling frequency).

## Calibration and Training
- Field calibration:
  - Pre-field training to standardize how ground cover percentages and vegetation categories are estimated, aiming to minimize observer variation.
- Documentation and traceability:
  - Recording forms, code lists, and appendices provide a transparent trail for dataset interpretation and reuse.

## Practical Implications for Data Stewardship
- Demonstrates end-to-end data governance in a field ecology project:
  - Clear dataset definitions, field protocols, and coding schemes enabling discoverability and reuse.
  - Inclusion of both structure (cover/height) and condition (fire impact) data across multiple sites and historical contexts.
  - Robust QA steps and documentation to ensure data quality and reliability for downstream analyses.
- Data storage and sharing practices:
  - Local storage on a dedicated Forsinard server with partner sharing; datasets prepared for potential deposition in data portals or catalogues.
- Reuse considerations:
  - Datasets include rich metadata (site codes, plot types, burn status, year since fire) and a comprehensive species code table, facilitating comparative studies and meta-analyses across peatland fires and chronosequences.
- Limitations and caveats:
  - COVID-19 disrupted planned repeat survey (2020) to assess one-year post-fire recovery; older sites have some differences in habitat and plot design quality due to site history.
  - Some plots (CR/SH) had more limited quadrat types, while BH/FD included hummock/hollow measurements, affecting cross-site comparability.

## Key Takeaways for Data Stewards
- Emphasize standardized metadata, consistent coding, and robust QA to ensure long-term usability of ecological survey data.
- Maintain detailed documentation of site selection rationale, plot design, and measurement protocols to support reproducibility.
- Ensure data storage practices support accessibility to partners and potential portal deposition, with clear versioning and data provenance.
- Plan for future updates and repeat measurements to extend chronosequences, while documenting any deviations or constraints (e.g., pandemic impacts).