# Overview

- Aim and scope
  - Document and quantify herbivory occurrence and intensity on exotic Clidemia hirta and native Melastoma spp. across two 100 m transects per site, at 21 forest sites within RSPO-certified oil palm landscapes in Sabah, Malaysian Borneo.
  - Also measure reproductive organs per plant and local habitat variables to understand drivers of herbivory.
  - Data are prepared to support GIS-based analysis and map-like visualization of spatial patterns across a disturbance gradient.

- Data files and content
  - herbivory_habitat.csv: herbivory measurements for C. hirta and Melastoma spp., plus local habitat variables.
  - SLA.csv: leaf area and Specific Leaf Area (SLA) measurements for C. hirta across habitats.
  - herbivory_local.csv: plant- and site-level details for each focal plant and nearby Melastoma (per transect).
  - Note: In addition to per-plant herbivory data, records include reproductive metrics and proximity to native confamilars.

- Study area and sampling design
  - 21 forest sites within oil palm landscapes in Sabah; sites vary in canopy structure due to prior disturbance and logging.
  - Two forest habitats surveyed per site: forest edge (disturbed) and forest interior ( regenerating, downstream from disturbance).
  - 39 transects total (two per site when possible; some interior transects unusable or lacking sufficient C. hirta).
  - On each transect: up to ten C. hirta plants; nearest Melastoma plant (<10 m) surveyed when present.
  - Plants selected were >30 cm tall to ensure sufficient leaf material for herbivory assessment.

- Measurements and variables
  - Herbivory occurrence: proportion of leaves damaged per plant (0–100).
  - Herbivory intensity: estimated percent area damaged per leaf, using the four newest leaves; categorized in 0%, 0–2%, 2–5%, 5–10% ranges with midpoints used for analysis.
  - Reproductive metrics: number of reproductive organs per plant (buds/flowers/immature and ripe fruits); measured for both exotic and native species.
  - Habitat and light proxies: distance to nearest Melastoma plant; local canopy cover; canopy cover along transects (five points per transect, 20 m intervals); light level proxy from canopy measures.
  - Planting context and densities: C. hirta plant size (total leaves), local density of C. hirta (within 5 m of focal plant), and transect-wide density (presence in 1 m sections along transect).
  - Specific Leaf Area (SLA): measured in four habitats (Oil palm, Forest-oil palm edge, Disturbed forest, Intact forest); leaf area per leaf (cm2) and leaf dry weight (g) used to compute SLA (cm2 g-1).
  - Data collection notes: measurements of herbivory intensity were performed by a single observer to minimize bias; leaf scans used for calibration but intensity scored by eye.

- Spatial and temporal context
  - Fieldwork conducted in March–April 2019.
  - Transects span a disturbance gradient from forest edge to interior to capture variation in light and plant-herbivore interactions.
  - Geography anchored in Sabah, with maps and references to forest cover data (CIFOR) and RSPO landscape context.

- Data quality and provenance
  - Methodology aligned with established protocols; consistent observer for canopy-densiometer readings; single observer for herbivory intensity to reduce bias.
  - Explicit notes on data caveats, such as uncertain Melastoma identifications (Melastoma spp. vs. M. malabathricum) and the mismatch between some plant codes across files.
  - Raw data linked to related datasets (Waddell et al. 2020a,b) and stored in the Environmental Information Data Centre (EIDC).

- GIS relevance and potential uses
  - Enables spatial visualization of herbivory patterns across a disturbance gradient in oil palm landscapes.
  - Facilitates integration with land-cover layers (e.g., forest remnants, oil palm extent) and canopy cover maps for habitat suitability and light-availability analyses.
  - Supports analyses of biotic interactions (invasive exotic vs. native congeners) in relation to habitat structure, canopy cover, and plant density.
  - Data can be joined by site code, habitat type, transect, and plant code to produce map-based summaries and landscape-scale models.

- Limitations and considerations for mapping
  - Some interior transects lacked suitable C. hirta or had steep terrain, potentially biasing interior representation.
  - Melastoma identification at the species level is uncertain; most are likely M. malabathricum but not confirmed morphologically or genetically.
  - Plant-code mappings differ between herbivory_habitat.csv and SLA.csv, requiring careful cross-referencing when linking datasets.

- References and data access
  - Data and related studies cited include Waddell et al. (2020a, 2020b) and broader literature on herbivory measurement and plant traits.
  - Raw canopy and density data originate from Waddell et al. (2020a); primary data metadata and holdings available via EIDC (Waddell et al. 2020b).