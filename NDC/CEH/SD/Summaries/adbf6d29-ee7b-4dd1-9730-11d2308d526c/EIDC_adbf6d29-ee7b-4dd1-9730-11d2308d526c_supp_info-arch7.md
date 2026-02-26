# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Provides supporting information for reproducing analyses from Waddell et al. (2020a) using the R script PLSPM_invasion.R and Plot_measured_data.csv.
- examines how fragmentation, forest disturbance, propagule pressure, soil characteristics, and native plant communities influence exotic plant invasions in forest remnants and continuous forest in Sabah, Malaysian Borneo.
- tests bidirectional relationships between native community diversity and invasion across multiple native components (total native community and four size-class subgroups).

## Study area and sampling design (GIS-relevant)
- 47 plots across 17 sites: 13 fragmented forest remnants within RSPO-certified oil palm plantations and 4 continuous forest sites (>1 million ha).
- Plot design: nested, circular plots (30 m radius; 0.28 ha) with subplots for different native size classes (C1: 25+ cm DBH; C2: 10–25 cm; C3: 2–10 cm) and eight 1 m x 1 m quadrats (Q) for ground vegetation and seedlings.
- Locations span Sabah, elevation 42–267 m, and complete a broad fragmentation/disturbance gradient.

## Spatial variables and fragmentation metrics
- Fragmentation and edge metrics computed within a 2 km radius around each plot:
  - Area of forest and non-forest within 2 km buffer (m2).
  - Edge density: forest edge cells per forest area within the buffer (derived from 5x5 m raster cells).
  - Edge density proxy indicates degraded edge effects.
- Time since fragmentation: years since first planting of oil palm (1991–2009, calculated in 2018).
- Data sources: drone imagery from plantation managers (May–Nov 2016) used to quantify buffer habitat and edge metrics.

## Local disturbance and soil characteristics (GIS-linked)
- Disturbance proxies:
  - Number of large Dipterocarpaceae stems (>25 cm DBH).
  - Average wood density for trees >10 cm DBH (genus-level, from Global Wood Density Database).
- Soil variables (per plot, n=47):
  - Soil pH (average of five 20 cm cores).
  - Available phosphorus (P) (average of five 20 cm cores).
- Transformations applied: log10 for soil pH and phosphorus; (sqrt)*-1 and (log10)*-1 for certain disturbance-related metrics.

## Propagule pressure and invasion metrics
- Propagule pressure proxy:
  - Exotic richness (number of exotic genera) along two 100 m transects in the oil palm matrix.
  - Exotic abundance: number of transect sections with exotic species.
- Invasion measure:
  - Exotic stem abundance and exotic richness per plot (across two transects).

## Native community structure and phylogeny
- Native alpha diversity calculated per plot for total native community and separately for each size class:
  - Observed genus richness.
  - Faith's phylogenetic diversity (PD).
- Phylogeny constructed using Phylomatic with APGIII supertree; final dataset included 303 genera (two genera excluded due to absence from the supertree).
- Data preparation for phylogenetic metrics and diversity analyses performed in R.

## Data structure and variables (CSV fields)
- Core fields include:
  - Site_code, Site_plot_code, Forest_type
  - Latitude, Longitude, Elevation_masl, Plot coordinates
  - Non.forest in 2km, Area in 2km buffer, Edge in 2km buffer, Fragmentation age
  - Mean wd 10cm, Number of large dipterocarps
  - Outside.exotic richness, Outside.exotic abundance
  - Soil pH, Soil available P
  - Plot exotic abundance, Plot exotic richness
  - Total native richness, Total native stems, Total native phylo diversity
  - Native adult sapling/seedling richness, stems, phylo diversity
  - Native ground veg richness, stems, phylo diversity

## Analytical workflow (PLS-PM modeling)
- All measured variables are centered and scaled (z-scores) prior to modeling; specific transformations applied per Table 1.
- Data frames:
  - data_pls combines Site, Plot, and all measured variables; includes derived edge density.
- Modeling approach:
  - Construct inner model matrix (latent variable links) and a path matrix (which measured variables map to which latent variables), specifying reflective vs. formative relationships.
  - Fit a full PLS-PM model using plspm for the entire dataset (Native community + Invasion) and separate models for native adult trees, saplings, seedlings, and ground vegetation.
  - Test both directions of the native community -> invasion relationship and invasion -> native community relationship (10 models total).
  - Iteratively remove nonsignificant paths (P < 0.05) in a stepwise fashion to yield a final model with significant links.
- Model assessment:
  - Measurement model: assess convergent validity (AVE > 0.50), reliability (standardized loadings > 0.70; with some exceptions), internal consistency (Cronbach's alpha and composite reliability > 0.70), and discriminant validity (cross-loadings and Fornell-Larcker criterion).
  - Structural model: evaluate R2 for endogenous latent variables; interpret based on thresholds (weak/moderate/substantial); report Goodness-of-Fit (GoF) as the geometric mean of average communality and average R2.
- Outputs:
  - Final standardized path coefficients (via bootstrap with 10,000 iterations) and two-sided P-values, with bootstrapping conducted at the site level (to accommodate lack of random site effects in plspm).
  - Simple plots of the final pathway relationships (plot(pls2)).
  - The code and outputs replicate figures and results reported in Waddell et al. (2020a).

## Validation and quality control
- Analyses used in a peer-reviewed publication (Landscape Ecology, 2020a).
- Data collection followed established protocols with single-operator consistency to ensure quality.
- The code has undergone careful error-checking by authors and is documented for reproducibility.

## Data availability and references
- Primary dataset: Plot_measured_data.csv; vegetation data reported in Waddell et al. 2020b (NERC EIDC).
- Related tools and references include plspm (Sanchez & Trinchera), Phylomatic, picante, BIOMASS, and standard geospatial R packages for raster and geometry operations.