# Trait filtering during exotic plant invasion of tropical rainforest remnants along a disturbance gradient

## Overview and aim for monitoring frameworks
- Provides a dataset and methodological blueprint to monitor herbivory and related plant traits of an invasive exotic (Clidemia hirta) and native congeneric shrubs (Melastoma spp.) across a disturbance gradient in Sabah, Malaysian Borneo.
- Designed to inform policy-relevant monitoring of invasion dynamics, herbivory pressure, and associated habitat factors along the forest–oil palm landscape continuum.
- Data support assessment of how disturbance (edge versus interior, canopy cover) influences invasion success, herbivore interactions, and potential impacts on native flora.

## Study design and data structure
- Location: 21 forest sites within RSPO-certified oil palm landscapes in Sabah; forest remnants with varying disturbance prior to plantation development.
- Sampling design: two 100 m transects per site (forest edge vs. forest interior); 39 transects in total (one interior transect excluded due to steepness; two interior transects lacked suitable C. hirta).
- Taxa: exotic Clidemia hirta and native Melastoma spp. (primarily M. malabathricum); presence of Melastoma proximate to focal C. hirta plants documented.
- Within-transect sampling: up to 10 C. hirta individuals per transect; nearest Melastoma individual surveyed when present.
- Datasets available: three CSV files
  - herbivory_habitat.csv: herbivory measurements for exotic and native plants plus local habitat variables
  - SLA.csv: leaf area and Specific Leaf Area (SLA) measurements
  - herbivory_local.csv: plant-by-plant herbivory measurements and contextual metadata

## Measurements and key variables
- Herbivory measurements
  - Herbivory occurrence: proportion of leaves damaged per plant (0–100)
  - Herbivory intensity: approximate damaged leaf area per four sampled leaves, scored by eye from scanned leaf images and converted to a continuous percentage (categories <10% subdivided; midpoints used for analysis)
  - Target: cross-species comparison of damage patterns between exotic and native plants
- Reproductive metrics
  - Number of reproductive organs (buds, flowers, immature fruits, ripe fruits) per plant for C. hirta and Melastoma spp.
- Habitat and microhabitat variables
  - Habitat type: forest edge vs. disturbed forest interior
  - Canopy cover: measured along transects with a densiometer (five points per transect; multiple measurements per point)
  - Light proxy: local canopy measures nearest to focal plant
  - Plant and neighborhood context: plant size (total leaves per plant), local density of C. hirta (presence in 5 m radius, across 10 2 m² sections), distance to nearest Melastoma plant, presence/absence and density metrics for transect
- Specific Leaf Area (SLA) and leaf traits
  - SLA measured for C. hirta across four habitat types (Oil palm, Forest–oil palm edge, Disturbed forest, Intact forest)
  - Leaf area for four leaves per plant; plant-level SLA derived from leaf measurements
- Dataset structure and coding
  - herbivory_habitat.csv includes per-plant herbivory metrics and plant traits
  - herbivory_local.csv links focal plants to site, transect, and local context with detailed codes (e.g., Clidemia_plant_code, Melastoma_plant_code)
  - SLA.csv links plant-level SLA and leaf-area measurements to habitat type and site
- Data units and interpretation
  - Occurrence: proportion (0–1 or 0–100%) of damaged leaves
  - Intensity: estimated percentage area removed or damaged per leaf, treated as a continuous variable
  - Canopy cover: percent (%) as a climate/light proxy

## Data collection methods and quality control
- Standardized field protocols followed; measurements conducted by consistent personnel to reduce observer bias
  - Herbivory intensity judged by eye from scanned leaves within six hours of collection
  - Densiometer readings taken by the same observer across all sites
- Data processing
  - Leaf area via Leafscan app; leaves dried at 60°C for weight-based SLA calculations
  - Reproductive organs counted in the field
- Quality assurance
  - Explicit documentation of methods, site codes, and variable definitions
  - Data checked for errors; provenance and references documented for traceability
- Data provenance
  - Ground-truthed within Sabah, Malaysian Borneo, as part of broader Waddell et al. studies
  - Related datasets and raw data available via EIDC (with cited studies: Waddell et al. 2020a, 2020b)

## Site context and ecological framing
- Landscape setting: oil palm-dominated landscapes with embedded rainforest remnants
- Conservation context: most forest remnants designated as High Conservation Value (HCV) areas; prior logging history likely between 1991–2009
- Gradient of disturbance: from highly disturbed forest edges to regenerating interior forest, enabling analysis of disturbance-driven variation in herbivory and plant traits
- Species context
  - Clidemia hirta is a highly invasive Melastomataceae species
  - Native comparison: Melastoma spp. (predominantly Melastoma malabathricum) used to benchmark native herbivory responses

## Data use, applications, and policy relevance for monitoring frameworks
- Enables monitoring of invasion traits and their interaction with disturbance and light environment
- Supports assessment of herbivory pressures as a component of ecosystem health within managed landscapes
- Facilitates cross-site comparisons of exotic-native interactions under varying canopy and edge effects
- Provides standardized trait data (SLA, leaf area) linked to habitat context for monitoring resilience and recovery in tropic forest remnants

## Limitations and challenges to consider
- Species identification uncertainty: Melastoma spp. field-level identification limited; most likely M. malabathricum but not conclusively distinguished
- Interior forest sampling: some interior transects lacked sufficient C. hirta, and one interior transect was inaccessible due to steepness
- Herbivory measurement: by-eye intensity scoring introduces subjectivity, though consistency across measures mitigates bias
- Spatial and temporal scope: single time window (March–April 2019); limited to 21 sites and specific disturbance gradient
- Generalizability: findings specific to Sabah’s oil palm–remnant landscapes; caution when extrapolating to other tropical regions

## Governance, access, and reproducibility considerations for monitoring teams
- Data accessibility: multiple CSV files with clear variable definitions; raw data and related materials available via the Environmental Information Data Centre (EIDC)
- Documentation: comprehensive method descriptions, unit definitions, and coding schemes included to support reproducibility
- Integration potential: data can be combined with other forest disturbance and invasion datasets to inform broader monitoring frameworks and policy evaluations
- Data provenance and references: well-documented study context and bibliographic references to support policy-linked analyses

## References and provenance
- Waddell, E. H., Chapman, D. S., Hill, J. K., et al. (2020a). Trait filtering during exotic plant invasion of tropical rainforest remnants along a disturbance gradient.
- Waddell, E. H., Chapman, D. S., Hill, J. K., et al. (2020b). Occurrence of exotic plant species in oil palm dominated landscapes with embedded rainforest remnants in Sabah, Malaysian Borneo, 2019. NERC Environmental Information Data Centre.
- Related methodological references for SLA and herbivory measurement standards as cited in the dataset documentation.