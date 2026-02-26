# Plant species cover and vegetation damage from burnt and unburnt areas of the Flow Country, Scotland, autumn 2019, following wildfires in May 2019 and nearby historic wildfire sites from the years 1997, 2000 and 2011.

- Purpose and scope
  - GIS-focused vegetation survey assessing burn effects on blanket bog mire communities and short- to medium-term recovery.
  - Four study areas capture both burnt and unburnt conditions, with a chronosequence including historic fires (1997, 2000, 2011) and the 2019 wildfire.

- Study area and fire history
  - Location: Flow Country peatlands, Caithness and Sutherland, northern Scotland.
  - 2019 wildfire burnt ~60 km2 of wet heath and blanket bog within a 4000 km2 peatland area.
  - Historic fire references: 1997, 2000, 2011 (mapped areas provided).

- Sampling design and plot layout
  - Four study sites: BH (Bighouse Estate), FD (Forsinard), CR (Croft #1), SH (Shurrery & Dorrery).
  - For each site: four plot types (burnt bog, burnt drain, unburnt bog, unburnt drain) with three replicates (A-C).
  - Total plots: 48 (4 sites × 4 plot types × 3 replicates).
  - Within each plot: 5 sampling points for bog plots; 5 sampling points along the 500 m drain for drain plots.
  - Plot boundaries: 125 m radius for bog plots; 500 m length for drain plots; adjustments made to remain within blanket bog habitat.
  - Burnt vs unburnt sampling: burnt bog plots centered within 1 km square; drain plots defined relative to corresponding burnt bog plots.

- Field quadrats and data collection
  - Quadrat size: 1 m × 1 m; standard, hummock (HU), hollow (HO) quadrats; drain quadrats (DR) placed adjacent to drains.
  - 356 quadrats surveyed in autumn 2019 (Sept–Dec); COVID-19 prevented planned repeat survey in 2020.
  - Data capture: vegetation height (max and obscured) at three points (A, C, F positions within quadrat); microtopography; ground cover by category (plants, litter, moss, rock, water, etc.).
  - Sampling points: five per bog plot (O1–O5 or U1–U5) and five along each drain section (D1–D5).
  - Additional measurements: dominant species at quadrat center, water depth, presence of standing water, deer signs, seedlings (Sitka spruce, Lodgepole pine), and other structural/fire-impact indicators.

- Vegetation and fire-impact measurements
  - Forest-to-Bog (F2B) method used to record vegetation and total cover; taxa coded with a predefined list (Appendix 2).
  - Fire impact metrics (for burnt plots, following Davies et al. 2016): Sphagnum discoloration and capitulum loss; non-Sphagnum moss scorch; moss survival; dwarf shrub resprouting; ericaceous seedling frequency.
  - Additional field notes and oblique photographs of each quadrat.
  - Burnt plots include “burnt” vs “unburnt” designations; replicated in data fields.

- Species coding and data structure
  - Two primary datasets:
    - Wildfire_vegetation_cover.csv: 356 quadrats × 67 vegetation, litter, algae, fungi, lichen, rock/soil/water variables.
    - Wildfire_vegetation_fire_impact.csv: 116 burnt bog quadrats with fire-specific metrics.
  - Key fields include: PlotID, site, plot (A–C), fire status (BB/UB), YR-burnt (years since fire), Qtype (ST/DR/HO/HU), date, dominant species, height measurements (A/C/F), height differences, cover codes (Appendix 2), water and seedling data, and fire-impact indicators.
  - Dominant species and cover values can sum beyond 100% due to overlapping vegetation layers; some categories are aggregated (e.g., moss groupings) to facilitate field identification.

- Data handling, storage, and quality control
  - Field forms and photos scanned and stored on Forsinard server; specimens identified with lab support.
  - Data entry and quality checks performed by field staff; totals checked for consistency (cover sums typically 85–150%, with some >150% genuine in dense understories or water-heavy plots).
  - Observation calibration: pre-field field training to reduce observer bias in cover estimation.

- GIS-ready outputs and applicability
  - Spatially explicit design: four sites, 48 plots, and 356 quadrats with precise GPS-backed locations and transect/drain geometry.
  - Rich attribute schema enabling map-based visualization of:
    - Burn extent and burn status by site and plot type.
    - Vegetation composition and dominant species per quadrat.
    - Fire impacts on Sphagnum and other mosses, as well as shrub regeneration.
    - Drain condition (blocked vs open) and its relation to burn effects.
  - Suitable for integrating with National Vegetation Classification (NVC) layers and peatland habitat maps; supports analyses of short- to medium-term recovery and habitat change following wildfire.

- References and methodologies
  - Field methods align with Forest-to-Bog (F2B) vegetation recording practices and NVC survey guidance.
  - Fire impact measures reference Davies et al. (2016) supplementary materials.
  - Basis for data collection, plotting, and species coding relies on standard botanical keys and field guides.

- Notes on limitations and context
  - The 2020 repeat survey could not be completed due to the COVID-19 pandemic.
  - Some older fire sites (CR and SH) had fewer burn replicates; older patches are clustered geographically near 2019 burn areas.
  - Data capture acknowledges species identification challenges in the field; lab verification is used where necessary.