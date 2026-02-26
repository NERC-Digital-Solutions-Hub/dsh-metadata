# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011.

## Aim
- Characterise wildfire effects on blanket bog plant communities immediately after fire.
- Compare vegetation communities and wildfire effects in open ground and near drains.
- Determine long-term vegetation recovery post-wildfire using a chronosequence approach.

## Study area and sampling design
- Location: Flow Country peatlands, Caithness and Sutherland, Scotland; extensive blanket bog within the SAC.
- Sites: four study sites defined by landholding/area:
  - BH: Bighouse Estate (2019 burn area)
  - FD: Forsinard (2019 burn area)
  - CR: Croft #1 (2011 burn area)
  - SH: Shurrery & Dorrery (1997-2000 burns)
- Plot design:
  - 48 plots in total (4 sites × 4 plot types × 3 replicates)
  - Plot types per site: burnt bog, unburnt bog, burnt drain, unburnt drain
  - Burnt bog plots sized ~5 ha; drain plots ~500 m along a drain adjoining the bog plot
  - For BH, FD, CR: three burnt bog plots per site chosen within areas; for SH: one central burnt bog plot per fire area
  - Drain plots defined as nearest drain to each burnt bog plot; not necessarily within the same 1 km square
- Replication and sampling units:
  - 356 quadrats surveyed in total (with some duplication in ST when on hummock/hollow)
  - 4 sites × 3 plots per site × 3 plot types × 5 sample points per quadrat × 4 quadrat types (ST, DR, HU, HO in some sites)

## Field methods and measurements
- Quadrat setup:
  - 1 m × 1 m quadrats; orientation fixed with south edge to the left when viewed from the south
  - Quadrat types:
    - ST: standard open bog quadrat
    - DR: drain quadrat (along drain)
    - HU: hummock quadrat (near a hummock)
    - HO: hollow quadrat (near a hollow)
- Plot and point layout:
  - Burnt bog plots included at 3 random centers per BH/FD; SH had fixed central plots
  - 5 sample points per bog plot (U1–U5) on open bog
  - 5 sample points per drain plot (D1–D5) along 500 m drain length
- Data collected per quadrat:
  - Vegetation cover and species present (F2B method; also total cover scores)
  - Vegetation height: maximum and obscured height at three positions along the central axis
  - Microtopography: vertical height difference within a 1 m radius
  - Hummock–hollow vertical height difference (for FD and BH)
  - Ground cover by category (live plants, dead, litter, moss, algae, water, bare peat/rock, needles, brash, seedlings, deer signs, fungi, etc.)
  - Deer presence and pellet diameters; water presence and depth; seedling counts (Sitka spruce, Lodgepole pine)
  - Dominant species at quadrat centre and near the base of the cane
  - Fire impact measures for burnt plots (per Davies et al. 2016): Sphagnum discoloration and capitulum loss, non-Sphagnum moss scorch, moss survival, dwarf shrub vegetative resprouting, ericaceous seedling frequency
  - Oblique photographs of each quadrat and recording form
- Species coding and categorisation:
  - Full species data collected; when not identifiable to species, lumped into codes (e.g., Dicranoids for certain mosses, Hypnum spp., Agrostis sp., etc.)
  - Various broad categories captured (lichens, liverworts, algae, fungi, needles, brash, bare peat/rock, water layers, etc.)
- Data capture and quality:
  - Recording forms scanned; data entered and quality checked by two individuals
  - Field training conducted to standardise ground-cover estimates
  - Total cover checks to identify inconsistencies (e.g., sums outside plausible ranges)

## Data and datasets
- Dataset 1: Wildfire_vegetation_cover.csv
  - 356 quadrats × 67 vegetation, litter, algae, fungi, lichen, and rock/soil/water variables
  - Key fields: PlotID, site, fire status (BB/Burnt Bog or UB/Unburnt Bog), Yr-burnt, no (point number), Qtype, date, Dominant species, height metrics, Height_diff, Deer_print, Dm_large, Dm_small, Seedlings, various cover codes (appendix 2)
- Dataset 2: Wildfire_vegetation_fire_impact.csv
  - 116 entries from burnt plots of the 2019 fire
  - Key fields: SITE (Forsinard or Bighouse), PlotID, No (point), Qtype, SPH_DIS, SPH_CAP_LOSS, NON_SPH_LOSS, MOSS_SURVIVAL, VEGE_RESPROUT, ERI_SEEDLING, FIELD_NOTES
- Data handling:
  - Two datasets produced: one covering all quadrats with vegetation cover; one focused on fire impact measures for burnt plots
  - Datasets stored on Forsinard server; associated metadata and codes provided in appendices

## Data handling, quality control and SOPs
- Methods align with Forest to Bog (F2B) vegetation recording; complemented by NVC guidelines for upland vegetation classification
- Fire impact measurements follow Davies et al. (2016) protocols for standard, hummock, and hollow quadrats
- Calibration and consistency:
  - Pre-field training to harmonise cover estimates and taxon identification
  - Data validation including checks on total cover consistency
- Documentation and storage:
  - Field forms scanned to PDF; photos renamed and stored; specimens identified with lab assistance as needed

## Key notes and limitations
- Recovery assessment limited by COVID-19: planned repeat surveys a year after fire were not completed
- Observational data involve some subjective elements (e.g., cover estimates), mitigated by training
- Older fire sites (CR and SH) have habitat similarities but differ in drainage and land management history
- Data include comprehensive coding for species and functional groups to enable cross-site comparisons and modelling

## Appendices and codes
- Appendix 2 provides a comprehensive coding key for species and functional groups used in the quadrats (e.g., Agrostis sp., Sphagnum spp., ericads, mosses, liverworts, lichens, and various substrate layers)