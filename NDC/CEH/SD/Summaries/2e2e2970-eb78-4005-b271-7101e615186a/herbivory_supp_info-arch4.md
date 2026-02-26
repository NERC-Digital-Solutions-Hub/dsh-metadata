# Occurrence of exotic plant species in oil palm dominated landscapes with embedded rainforest remnants in Sabah, Malaysian Borneo, 2019

## Overview of the study
- Assess herbivory occurrence and intensity on the invasive Clidemia hirta and native Melastoma spp. across two 100 m transects per site (forest edge and disturbed forest interior) at 21 forest sites in Sabah, Malaysian Borneo.
- Sites are forest remnants within RSPO-certified oil palm plantations; surveys conducted in March–April 2019.
- Additional data collected on reproductive organs per plant and local habitat variables to contextualize herbivory patterns.
- Data are provided in three CSV files (see table 1): herbivory_habitat.csv, herbivory_local.csv, and SLA.csv.

## Data assets (files and contents)
- herbivory_habitat.csv
  - Herbivory measurements for exotic Clidemia hirta and native Melastoma spp., plus surrounding local habitat variables.
  - Includes herbivory occurrence (proportion of damaged leaves) and herbivory intensity (estimated % area damaged per leaf, per leaf 1–4, averaged per plant).
  - Reproductive organs per plant measured for comparison between species.
- herbivory_local.csv
  - One row per focal Clidemia hirta plant and nearest Melastoma spp. plant (if present) with detailed per-plant herbivory data and local context.
  - Variables include survey date, site code, habitat, exact transect position, local densities, canopy cover, presence of Clidemia/Melastoma, leaves counts, damage counts, per-leaf intensities, reproduction status, and proximities between focal and nearby Melastoma.
- SLA.csv
  - Specific Leaf Area (SLA) measurements for Clidemia hirta across four habitats representing a disturbance gradient: Oil palm, Forest-oil palm edge, Disturbed forest, Intact forest.
  - Includes leaf area measurements, total leaf area/weight, and mean SLA per plant.
- Additional notes
  - Data link to broader datasets for canopy cover and density from Waddell et al. (2020a, 2020b) and contextual landscape data (RSPO certification, plantation contexts).

## Study design and sampling
- Sites: 21 forest remnants within oil-palm dominated landscapes; sites vary in canopy cover and disturbance, with sizes ranging from 3.25 to 1375 ha; sites >1 km apart to avoid spatial autocorrelation.
- Transects: two per site in different forest habitats—forest edge (FE) and forest interior (FI). FI transects located on average 53 m from the nearest edge.
- Sampling: up to 10 Clidemia hirta plants per 100 m transect were surveyed; nearest Melastoma spp. plant (<10 m) also surveyed when present.
- Plant selection: only plants >30 cm tall selected to ensure multiple fully developed leaves for herbivory assessment.
- Habitat gradient: transects chosen to span light availability and disturbance gradients, capturing potential effects on herbivore communities.

## Measurements and variables
- Herbivory
  - Occurrence: proportion of leaves damaged per plant (0–100%).
  - Intensity: estimated % leaf area removed/damaged for four fully expanded leaves per plant, recorded by eye from scanned leaf images and categorized into <10% ranges (0%, 0–2%, 2–5%, 5–10%); middle values used for continuous analysis.
- Reproductive output: number of reproductive organs (buds, flowers, immature fruits, ripe fruits) per plant for both Clidemia hirta and Melastoma spp.
- Local context variables
  - Distance to nearest Melastoma plant, presence/absence of Melastoma within 10 m, shortest distance to confamiliar Melastoma.
  - Habitat type (Forest edge vs. Disturbed forest) and local canopy cover.
  - Light proxy: canopy cover at multiple transect points; plant-level light estimation via nearest or adjacent canopy readings.
  - Clidemia hirta biology: plant size (total leaves), local density of Clidemia hirta within 5 m (derived from 1 m segments along transect).
  - Disturbance level: edge vs interior; canopy cover variations.
- SLA and leaf traits
  - SLA.csv includes leaf area measurements for four leaves per plant, total leaf area/weight, and mean SLA to compare functional trait variation across habitats.

## Data collection quality and provenance
- Protocols align with established methods; same observer conducted canopy measurements and one observer performed all by-eye herbivory scoring to reduce bias.
- Data quality checks performed to minimize errors; detailed metadata included to support reproducibility and reuse.
- Land-use and landscape context documented (RSPO standards, plantation history), with references to related datasets (Waddell et al. 2020a, 2020b) for raw canopy and density data.

## Units, metadata, and accessibility
- Herbivory occurrence: expressed as a proportion (0–1) or 0–100% in data descriptors.
- Herbivory intensity: percentage damage per leaf (0–100%), treated as a continuous variable after mid-point assignment for categorized data.
- Canopy cover: measured as percent canopy cover using a densiometer.
- SLA and leaf area: standard plant-trait units (cm2 for area, g for weight, and cm2 g−1 for SLA).
- Site and plant identifiers encoded consistently (e.g., site codes and plant codes) to enable cross-file joins.
- Raw data referenced to external datasets and are described for discoverability through EIDC (Environmental Information Data Centre) with links to Waddell et al. (2020a,b).

## Considerations for data use and governance (Data Leaders perspective)
- Comprehensive data schema across three CSV files enables cross-linking of herbivory metrics, local context, and leaf traits for multi-level analyses.
- Clear documentation of measurement methods, units, observer consistency, and data quality supports trust and reuse across teams and networks.
- Identifiable site-level and transect-level metadata facilitate integration with broader landscape and biodiversity datasets, supporting scalable data governance and collaboration with partners.
- Potential use cases include assessing how disturbance gradients influence herbivory patterns between an invasive species and native congeners, and linking herbivory to leaf traits (SLA) and reproductive output.
- Data availability notes highlight provenance and linkage to larger data infrastructures (RSPO context, EIDC), important for data sharing policies, licensing, and discoverability.