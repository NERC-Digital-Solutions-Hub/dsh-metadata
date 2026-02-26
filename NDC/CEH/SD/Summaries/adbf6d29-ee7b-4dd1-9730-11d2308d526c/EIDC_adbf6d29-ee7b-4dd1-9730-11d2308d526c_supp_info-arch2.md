# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

- Purpose: Provide reproducible R code (PLSPM_invasion.R) and data (Plot_measured_data.csv) to analyze how fragmentation, disturbance, propagule pressure, soil characteristics, and native plant communities influence exotic plant invasions in forest remnants and continuous forest in Sabah, Borneo. This supports the findings reported in Waddell et al. (2020a) in Landscape Ecology.

## Study design and data sources

- Study scope: 47 plots across 17 sites ( Sabah, Malaysian Borneo), including 13 fragmented forest sites within RSPO-certified oil palm plantations and 4 continuous forest sites.
- Plot structure: Nested, circular plots (30 m radius; 0.28 ha) per site with variable replication (two plots in smaller remnants; up to three plots in larger ones).
- Size-class sampling: Four native plant size classes:
  - C1: Trees ≥25 cm DBH
  - C2: Trees 10–25 cm DBH
  - C3: Tree saplings 2–10 cm DBH
  - Q: Tree seedlings (<2 cm DBH) and ground vegetation
- Data collection focus: Abundance and richness of natives vs. exotics, plus phylogenetic diversity (Faith's PD) for native communities.
- Data sources for fragmentation and environment: Landscape context within a 2 km buffer around each plot; variables include forest area, edge density, time since fragmentation (years since oil palm planting), soil pH, available phosphorus, and topography (elevation, slope).

## Measured and latent variables

- Fragmentation: 
  - Area of non-forest in 2 km, edge density within 2 km, years since fragmentation.
- Disturbance: 
  - Number of large dipterocarps (>25 cm DBH), average wood density of trees (>10 cm DBH).
- Soil characteristics: 
  - Soil pH, available phosphorus (P).
- Propagule pressure: 
  - Exotic richness outside (in oil palm matrix) and exotic abundance (across transects outside).
- Native community metrics (alpha diversity, per plot; examined as total native community and by components):
  - Native genera richness, native abundance (total and by component), Faith's PD (phylogenetic diversity) for each native subset: total, adults, saplings, seedlings, ground vegetation.
- Exotic invasion metrics: 
  - Exotic genera richness, exotic abundance (per plot).
- Data transformations and preparation:
  - Variables centered and scaled (mean 0, variance 1); some transformed (log10, sqrt, ln+1) as per Table 1 in the document.
  - Edge density created as a derived variable: Edge.in.2km.buffer / Area.in.2km.buffer.
- Latent variable specification (PLS-PM):
  - Thoughtfully defined to reflect the hypothesized pathways among fragmentation, disturbance, soil characteristics, native community, propagule pressure, and invasion.

## Analytical approach and workflow

- Method: Partial Least Squares Path Modelling (PLS-PM) using the plspm R package.
- Model structure:
  - Inner (structural) model specifies connections among latent variables (as in Fig. 1).
  - Outer (measurement) model specifies which observed variables load onto which latent variables; variables organized into blocks and declared reflective or formative.
- Model fitting:
  - Initial full model fitted on the complete native community (all size classes).
  - Five additional models fitted for native components separately (adult trees, saplings, seedlings, ground vegetation).
  - All models tested in both directions for the native community ↔ invasion relationship due to uncertain directionality, resulting in 10 models total.
- Data preparation steps:
  - Created data_pls dataframe with selected variables.
  - Defined inner model (connection matrix) and outer model (blocks mapping to latent variables) and specified reflective vs formative nature.
- Model execution and assessment:
  - Run PLSPM: summary(pls2) to inspect model.
  - Evaluate measurement model reliability and validity:
    - Convergent validity: AVE > 0.50
    - Indicator reliability: standardized loadings > 0.70 (exceptions noted for one variable)
    - Internal consistency: Cronbach's alpha and composite reliability > 0.70
    - Discriminant validity: assessed via cross-loadings and Fornell-Larcker criterion (AVE square root > inter-construct correlations)
  - Evaluate structural model:
    - Coefficient of determination (R2) thresholds to gauge explanatory power (weak/moderate/substantial)
    - Goodness of Fit (GoF) as the geometric mean of average communality and average R2
- Model refinement:
  - Stepwise removal of nonsignificant paths (P < 0.05) from the full specification to final, significant model(s).
  - Final pathway visualization (plot(pls2)) with standardized path coefficients.
- Inference:
  - Two-sided p-values for path coefficients estimated via 10,000 bootstrap resamples.
  - Bootstrap conducted at the site level (to account for site-level clustering, since site identity cannot be a random effect in plspm).

## Data preparation and structure details

- Data frame structure (data_pls) includes:
  - Site, Plot, Non.forest, Edge.density, Age, Dips (large dipterocarps), WD (wood density), pH, Avail.P, Total.richness, Total.PD, Outside.rich, Outside.abun, Exotic.abundance, Exotic.richness
- Inner model and blocks:
  - Latent variable connections specified in triangular matrix form (pathway) with connections among Fragmentation, Disturbance, Soil, Natives, Propagule Pressure, and Exotics.
- Data handling notes:
  - Variables renamed for brevity (e.g., Fragmentation.age → Age; Edge density derived as above).
  - All measured variables aligned with the measurement model described in the study’s Table 1.

## Validation and provenance

- Peer-reviewed foundation: Analyses implemented in this code underlie the published findings in Waddell et al. (2020a), Landscape Ecology.
- Quality checks: Code author-validated for correctness; peer-reviewed publication confirms methodological soundness.
- Data provenance:
  - Plot-level vegetation data collected in 2017 across 47 plots, with accompanying site metadata and environmental measurements.
  - Related vegetation and habitat data published in Waddell et al. (2020a) and data records in Waddell et al. (2020b).

## Study area and sampling specifics

- Location: Sabah, Malaysian Borneo.
- Site types:
  - Fragmented forest remnants within RSPO-certified oil palm plantations (n=13 sites)
  - Continuous forest sites (n=4)
- Temporal window: Field sampling July–October 2017
- Plot design details:
  - C1 (≥25 cm DBH), C2 (10–25 cm DBH), C3 (2–10 cm DBH), Q (seedlings and ground vegetation)
  - Exotic species surveyed along two 100 m transects outside forest remnants to estimate propagule pressure
- Native diversity metrics:
  - Alpha diversity measures: observed genera richness; Faith’s PD
  - Phylogenetic data constructed using Phylomatic and APGIII supertree; branch lengths from Wikstrom et al. and calibrations via BladJ in Phylocom

## Output expectations for analysts monitoring the environment

- Reproducible analyses linking landscape structure, disturbance, soil properties, and biotic communities to exotic invasion in tropical forests.
- A suite of ten PLSPM models (full native community and four component datasets, bidirectional) enabling assessment of biotic resistance strength across native subsets.
- Explicit model evaluation criteria and stepwise refinement procedure to derive significant pathways, accompanied by plots of the final network and bootstrap-supported path coefficients.

## References and resources

- Core methodological references for PLSPM and validation (Chin 1998; Sanchez 2013; Sanchez & Trinchera 2012)
- Foundational data and software packages (plspm, Phylomatic, picante, BIOMASS, rgeos, raster, GoF considerations)
- Related data sources and broader study context (Waddell et al. 2020a; Waddell et al. 2020b; RSPO guidelines; related phylogenetic resources)