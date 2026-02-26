# Overview

- Description: Data on herbivory occurrence and herbivory intensity of exotic Clidemia hirta and native Melastoma spp. across 21 forest sites in Sabah, Malaysian Borneo, alongside leaf trait data (Specific Leaf Area, SLA) for Clidemia hirta.
- Purpose: Assess herbivory patterns and potential differences between exotic and native taxa along disturbance gradients (forest edge vs interior) and varying canopy conditions.
- Data packaging: Three CSV data files are provided:
  - herbivory_habitat.csv – herbivory measurements for exotic and native plants, plus local habitat variables.
  - SLA.csv – leaf area and SLA measurements for exotic Clidemia hirta.
  - SLA.csv (continued) – additional SLA-related measurements and derived metrics.
- Study context: Conducted along two 100 m transects per site (forest edge and forest interior) across 21 sites within RSPO-certified oil palm landscapes in Sabah. Surveys occurred in March–April 2019.

## Dataset scope and purpose from a data stewardship viewpoint

- Facilitates cross-site comparisons of herbivory pressure on an invasive shrub versus native Melastoma spp. under different disturbance regimes.
- Captures both presence/absence of herbivory (occurrence) and extent of damage per leaf (intensity), enabling robust ecological analyses.
- Includes environmental and spatial context variables (canopy cover, distance to Melastoma, local density of Clidemia, transect habitat type) to support multi-variable modeling.

## Data files and structure

- herbivory_habitat.csv
  - Contains per-plant measurements for exotic Clidemia hirta and nearby native Melastoma spp. (if present).
  - Key measures:
    - Herbivory occurrence: proportion of damaged leaves per plant (0–100).
    - Herbivory intensity: estimated percentage area damaged per leaf (0–100, with categorization and mid-point values used for analysis).
    - Reproductive organs per plant for both species.
  - Additional plant and habitat context:
    - Plant size, canopy cover, distance to closest Melastoma, local confamiliar presence.
    - Habitat type (Forest edge vs Disturbed forest) and transect-level canopy data.
    - Local density metrics for Clidemia within 5 m of focal plant and transect-wide presence.
  - Identifying fields: site codes, transect identifiers, plant codes for Clidemia and Melastoma.
- SLA.csv
  - Measures leaf area and Specific Leaf Area (SLA) for Clidemia hirta plants.
  - Habitat gradient: Oil palm, Forest-oil palm edge, Disturbed forest, Intact forest.
  - Plant codes and leaf-level measurements (Leaf1–Leaf4 areas, total and mean SLA calculations, total leaf weight, etc.).
- Related notes
  - Some plant codes in herbivory_habitat.csv do not directly map to plant codes in SLA.csv; cross-dataset mapping should be handled carefully.
  - The SLA data include derived metrics (Total_leaf_area, Average_leaf_area, Total_leaf_weight, Mean_SLA) to support trait-based analyses.

## Study system and sampling design

- Species context
  - Exotic: Clidemia hirta (invasive shrub across tropics).
  - Native comparison: Melastoma spp. (primarily Melastoma malabathricum in the sampling area; field identification limited to morphological grouping).
- Site and transect layout
  - 21 forest sites within oil-palm landscapes; sites range from small to large (3.25–1375 ha) and are >1 km apart.
  - At each site, two 100 m transects:
    - Forest edge (disturbed forest–oil palm interface)
    - Forest interior (regenerating forest, ~53 m from edge)
  - Across sites, 39 transects were surveyed (not all inner transects usable due to steepness or absence of target plants).
- Sampling units
  - Up to 10 Clidemia hirta plants per transect were surveyed for herbivory; nearest Melastoma plant within 10 m if present also surveyed.
  - Plants selected were >30 cm tall to ensure sufficient leaves for herbivory assessment (median leaves per plant: ~19–22).

## Measurements and variables (highlights)

- Herbivory measurements
  - Occurrence: proportion of leaves damaged per plant.
  - Intensity: estimated percentage area damaged per leaf for four fully expanded leaves near the shoot apex; categorized into <10% increments with midpoints used for analysis.
  - Data collection method: “by eye” assessment performed by a single observer to reduce bias; leaf damage captured from high-resolution scans when possible, but by-eye method retained for efficiency and comparability.
- Reproductive fitness
  - Counts of buds, flowers, immature fruits, and ripe fruits per plant for both Clidemia hirta and Melastoma spp.
- Habitat and plant context variables
  - Canopy cover and light environment (via densiometer measurements along transects).
  - Local canopy estimates near each focal plant; transect-level mean canopy cover.
  - Local Clidemia density (presence in 5 m radius around focal plant) and total transect Clidemia density.
  - Distance to nearest Melastoma confamiliar plant; presence/absence of confamiliar near focal plant.
  - Habitat type (Forest edge vs Disturbed forest) and plant size (total leaves per plant).
- SLA and leaf traits
  - SLA measurements (mean and per-leaf values) across habitat types representing a disturbance gradient.
  - Leaf area for individual leaves, total leaf area, and leaf weight to support trait-based analyses.

## Data quality and metadata

- Quality control
  - Consistent observer for canopy/densiometer measurements (single observer).
  - Uniform “by eye” herbivory scoring performed by the same person to minimize observer bias.
  - Data checked for errors and validated against study protocols.
- Methodological notes
  - Herbivory defined broadly to include damage from insects, mammals, and pathogens when distinguishing causes is not feasible.
  - Intensity scoring used a standardized approach to handle a large dataset without image-processing complexity, with justification that the method yields comparable results to others in the literature.

## Access, provenance, and governance

- Provenance
  - Data collected in 2019 across 21 sites within Sabah, Malaysia, in oil palm landscapes with rainforest remnants.
  - Raw canopy data and other measurements align with Waddell et al. 2020a for canopy and density metrics; raw data available in the Environmental Information Data Centre (EIDC) under Waddell et al. 2020b.
- Access and use
  - Data are organized into CSV files suitable for re-use in meta-analyses and cross-site comparisons.
  - Clear field definitions and unit annotations (0–100 scales for herbivory metrics; percent for SLA and leaf area) support reproducibility.
- Data stewardship considerations
  - Mapping between Clidemia hirta plant codes and SLA plant codes requires careful handling due to non-direct correspondence.
  - Documentation provides explicit column definitions for survey date, site codes, transect type, and measurement details to enable accurate data integration and reuse.

## Practical implications for data governance and reuse

- Strengths for data stewards
  - Rich multi-site design across a disturbance gradient with both exotic and native comparisons.
  - Explicit measurement protocols and single-observer consistency for key variables reduce inter-observer variability.
  - Comprehensive metadata on habitat, canopy, density, and reproductive metrics enables robust ecological analyses and cross-study synthesis.
- Considerations and potential issues
  - Harmonization across datasets (herbivory_habitat.csv vs SLA.csv) requires careful mapping of plant codes and site identifiers.
  - Some taxonomic specificity (Melastoma spp. vs M. malabathricum) is broader due to field identification limitations; users should note potential species-level ambiguity.
  - Interoperability with external datasets may require alignment of habitat categorizations and measurement units.

## End-user recommendations for data stewards

- Ensure consistent cross-dataset linking keys (site_code, Plant_code) and document any mappings or ambiguities clearly in metadata.
- Maintain the single-observer approach for the key qualitative measurements (canopy, herbivory) or provide calibration notes if expanding to multiple observers.
- Preserve the explicit habitat gradient design (Oil palm, Forest-oil palm edge, Disturbed forest, Intact forest) to support gradient analyses.
- Provide a data dictionary with field-level definitions, units, and example rows to facilitate onboarding of new users and integration with other datasets.