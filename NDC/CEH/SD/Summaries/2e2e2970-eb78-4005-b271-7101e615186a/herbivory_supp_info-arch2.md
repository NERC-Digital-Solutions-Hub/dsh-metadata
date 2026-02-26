# Overview

- Global aim: Provide standardized, comparable environmental data to monitor ecological health and policy performance over time, focusing on herbivory and related habitat variables across disturbance gradients.
- Context: 21 forest sites within RSPO-certified oil-palm landscapes in Sabah, Malaysian Borneo. Surveys conducted March–April 2019 across two habitat types per site (forest edge and forest interior) to span canopy-disturbance gradients.
- Data products: Three CSV data files describing herbivory, habitat context, and leaf traits (SLA).

## Data files and contents

- herbivory_habitat.csv
  - Measures for exotic Clidemia hirta and native Melastoma spp. across transects
  - Variables include herbivory occurrence (proportion of damaged leaves) and herbivory intensity (average percent leaf area damaged per leaf), plus local habitat variables
  - Reproductive metrics: number of reproductive organs per plant for both species
  - Habitat and plant context: canopy cover, distance to nearest Melastoma, local density of C. hirta, plant size, and presence/absence of C. hirta along transects
  - Transect and site identifiers, leaf damage per leaf (CH_L1…CH_L4), and average intensity per Clidemia plant
- SLA.csv
  - Specific Leaf Area and leaf area/weight data for exotic C. hirta
  - Plant-level data across four habitat types: Oil palm, Forest-oil palm edge, Disturbed forest, Intact forest
  - Columns include site code, plant code, leaf areas (Leaf1_area…Leaf4_area), total and mean leaf area and weight, and mean SLA
- SLA and herbivory metadata
  - Additional details linking C. hirta density, canopy cover measurements, and transect-level context
  - Notes that C. hirta density and canopy cover data originate from Waddell et al. 2020a; raw data available in EIDC (Waddell et al. 2020b)

## Study species and design

- Target species
  - Exotic Clidemia hirta (Melastomataceae): highly invasive; widespread in Sabah
  - Native Melastoma spp. (primarily M. malabathricum in the sampling area) used as a confamilial comparison
- Field design
  - 39 attempted transects (two per site, forest edge and interior; some interior transects excluded due to steepness or lack of target plants)
  - At each transect: up to 10 C. hirta plants surveyed; nearest Melastoma plant surveyed if present
  - Plant selection: >30 cm height to ensure multiple leaves for herbivory assessment
  - Leaf sampling for SLA and leaf area: 4 leaves per plant where possible, across habitat types

## Measurements and methods

- Herbivory definitions
  - Herbivory includes any leaf damage from insects, pathogens, mammals, etc.; not limited to a single herbivore group
- Herbivory occurrence
  - Proportion of leaves per plant that show damage (0–100%)
- Herbivory intensity
  - Scored visually from scanned leaves to nearest 10%; categories collapsed to midpoints (0, 1, 3.5, 7.5, 15, etc.) treated as continuous
  - Four fully expanded leaves per plant sampled; middle values used for analyses
- Reproductive metrics
  - Number of buds, flowers, immature fruits, and ripe fruits per plant
- Habitat and microhabitat variables
  - Canopy cover (via densiometer) at multiple points; local canopy as proxy for light
  - Light environment inferred from local canopy and transect position (forest edge vs interior)
- Spatial and community context
  - Distance to nearest Melastoma plant
  - Local density of C. hirta (presence in 5 m either side of focal plant, across ten 2 m2 sections)
  - Overall transect-level Clidemia density and total transect exposure
  - Presence/absence and proximity of native confamilar Melastoma spp. within 10 m
- Leaf trait measurements (SLA.csv)
  - Leaf area measurements for up to four leaves per plant
  - SLA derived from leaf area and oven-dry weight
  - Four habitat categories to represent disturbance gradient

## Data quality and control

- Consistency and bias reduction
  - All canopy measurements conducted by the same observer
  - Herbivory intensity assessed visually by the same observer to minimize cross-observer bias
- Methodological notes
  - By-eye herbivory intensity validated against alternative image-processing approaches in literature
  - Data follow established protocols and have undergone quality checks
- Limitations acknowledged
  - Intensity scoring relies on observer judgment
  - Only two disturbed habitat types surveyed extensively; very few closed-canopy intact forest transects were surveyed due to low C. hirta density in that habitat

## How this supports monitoring and policy analysis

- Standardized, repeatable measurements across multiple sites enable temporal and spatial comparisons of invasive plant interactions with herbivores and native flora
- Captures disturbance-gradient effects on herbivory and plant performance, informing assessments of invasive species impacts in production landscapes
- Provides linkage points for broader environmental monitoring:
  - Herbivory occurrence and intensity as ecological health indicators
  - Relationships between canopy disturbance, light regimes, and herbivore pressure
  - Reproductive fitness metrics to assess potential invasion dynamics over time
- Data accessibility and reuse
  - Data are organized in clearly defined CSV files with explicit metadata and column descriptions
  - Raw canopy and density data originate from prior research (Waddell et al. 2020a,b); broader datasets are available via EIDC
  - Comprehensive references accompany the data to support methodological transparency

## Practical considerations for analysts

- Data structure
  - herbivory_habitat.csv: per-plant measurements with plant-level and site-level context
  - SLA.csv: per-plant leaf-trait data across habitat types
- Potential analyses
  - Compare herbivory occurrence and intensity between exotic and native species across habitat types
  - Assess how canopy cover and light environment influence herbivory
  - Examine relationships between herbivory and reproductive output
  - Integrate SLA and leaf-area metrics to explore trait-mediated herbivory patterns
- Integration with other datasets
  - Datasets can be linked to RSPO-certified landscape context and other environmental monitoring outputs to evaluate policy effectiveness and restoration or conservation outcomes