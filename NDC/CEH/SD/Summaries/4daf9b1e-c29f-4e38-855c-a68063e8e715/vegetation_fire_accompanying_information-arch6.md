# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011

- Background and aims
  - A wildfire in spring 2019 burnt about 60 km2 of wet heath and blanket bog in the Flow Country, Scotland.
  - The study site spans ca. 4000 km2 of blanket bog across Caithness and Sutherland; it includes diverse land uses (natural, drained, drained/afforested, peat cutting).
  - Objectives: characterize immediate wildfire effects on blanket bog vegetation, compare open ground vs. drains, and assess long-term vegetation recovery using a chronosequence approach that includes historic fires from 1997, 2000, and 2011.

- Study design and sites
  - Four study sites representing different landholdings and fire histories:
    - BH (Bighouse Estate, 2019 burn area)
    - FD (Forsinard, 2019 burn area)
    - CR (Croft 1, 2011 burn area)
    - SH (Shurrery/Dorrery, 1997–2000 burn areas)
  - At each site, four plot types within each of three replicates (A–C):
    - Burnt bog plots (BB)
    - Burnt drain plots
    - Unburnt bog plots
    - Unburnt drain plots
  - Total design includes 48 plots across four sites, with three plots per replicate in each plot type.

- Sampling framework and plot layout
  - Plot geometry:
    - Burnt and unburnt bog plots: each 5 ha, defined as a 125 m radius area, excluding non-mire habitat.
    - Burnt drain plots: a 500 m segment along the nearest drain to the corresponding bog plot.
  - Plot types per site: 3 bog plots per category per site, with drain plots linked to each bog plot.
  - Quadrats and sampling within plots:
    - 356 vegetation quadrats in total (combining standard 1 m x 1 m bog plots and drain plots; some duplication occurred for ST on hummock/hollow in BH/FD).
    - Within bog plots: three sub-plots A–C (centered randomly within burn area) for burnt/unburnt comparison.
    - Within drain plots: 5 sampling points along the 500 m drain length.
  - Quadrats and types:
    - Standard (ST), Drain (DR), Hummock (HU), Hollow (HO) quadrats; HS (hummock) and HO used only for the 2019 sites (BH/FD).
    - Burnt bog plots: standard approach plus hummock/hollow measurements in BH/FD.
  - Field timing: surveys conducted September–December 2019; planned 2020 repeat surveys delayed by COVID-19.

- Vegetation data collection and measurement
  - Data captured per quadrat:
    - Vegetation cover (0–100%), including mosses, bryophytes, vascular plants, litter, rock, and water layers.
    - Dominant species at the quadrat center.
    - Maximum and obscured vegetation heights at three positions along the quadrat (centre, bottom, far end).
    - Microtopography: vertical height difference within a 1 m radius around quadrat centre.
    - Ground/underwater conditions: presence and depth of standing water; deep water handled with “DWAT” coding where relevant.
    - For pools: total water cover calculated as sum of standing water layers.
    - Deer presence (prints) and dung diameter; seedling counts for Sitka spruce and Lodgepole pine.
    - Seedling counts for ericaceous species; presence of seedlings frequency categories.
  - Fire impact measures (only for burnt plots, following Davies et al., 2016 protocols):
    - Sphagnum damage: discoloration and capitulum loss.
    - Non-Sphagnum moss scorch/consumption.
    - Moss survival (green material).
    - Dwarf shrub resprouting.
    - Ericaceous seedling frequency.
  - Photography: oblique photo of each quadrat; photos linked to recording forms.
  - Taxonomic coding and data handling:
    - Field codes and taxa aligned with a predefined appendix (Appendix 2) for species grouping when species cannot be separated in the field.
    - Burnt vs. live vs. dead classification for vegetation (BURNT vs. DEAD) where applicable.
  - Data collection logistics:
    - GPS-defined quadrat locations; bamboo canes mark quadrat corners; cable ties identify standard quadrats.
    - Recording forms used (Wildfire Vegetation recording form) with site, plot, burn status, quadrat type, and point identifiers.

- Data management, storage and quality control
  - Field data and photographs stored on the Forsinard server; scanned forms and photos renamed and archived.
  - Data entry coordinated by Field Officer; QA performed by two individuals.
  - Post-entry checks included verifying total vegetation cover sums (expected 85–150%; some values >150% were genuine, especially where Sphagnum and water layers created high totals).

- Datasets produced
  - Wildfire_vegetation_cover.csv
    - Contains 356 quadrats across 4 sites, 3 replicates per site, 4 plot types, and 67 vegetation-related variables.
    - Key fields: PlotID, site, fire status, YR-burnt (years since burn), Qtype (ST, DR, HU, HO), date, dominant species, height metrics, height differences, coverage values for each taxon/lactor, deer/dung metrics, seedling counts, and canopy/water layers.
  - Wildfire_vegetation_fire_impact.csv
    - Contains 116 entries from burnt 2019 plots with fire-impact metrics: SPH_DIS, SPH_CAP_LOSS, NON_SPH_LOSS, MOSS_SURVIVAL, VEGE_RESPROUT, ERI_SEEDLING, plus FIELD_NOTES.

- Data interpretation and units
  - Vegetation cover values are percent-based across taxa; total covers may exceed 100% due to overlapping layers and multiple strata.
  - Height measurements are in centimeters; height differences quantify microtopography within and between hummock/hollow quadrats.
  - Fire impact metrics are percentage-based for various burn effects (discoloration, capitulum loss, moss scorch, etc.) and categorical/semi-quantitative measures (seedling frequency, resprouting).

- Standard operating practices and references
  - Field methods: Forest-to-Bog (F2B) vegetation recording approach; alignment with National Vegetation Classification (NVC) guidelines.
  - Fire impact methodology: Davies et al., 2016 protocols.
  - Calibration: field training conducted to minimize observer variability in cover estimation.

- Calibration, limitations, and notes for future use
  - Observer calibration helps reduce variability in cover estimates; acknowledges subjectivity in cover scoring.
  - COVID-19 interruption prevented planned 1-year post-fire resampling for the 2019 sites, limiting short-term recovery inferences for those plots.
  - The dataset structure provides a baseline for cross-site comparisons (different landholdings and drain statuses) and chronosequence analysis with older fires.

- Appendices and codes
  - Appendix 1: Example field recording sheet (structure of data entry: plot, quadrat type, height, cover, water, seedlings, etc.).
  - Appendix 2: Comprehensive codes for species and variables (extensive list covering mosses, Sphagnum species, bryophytes, grasses, shrubs, forbs, lichens, fungi, and other categories).