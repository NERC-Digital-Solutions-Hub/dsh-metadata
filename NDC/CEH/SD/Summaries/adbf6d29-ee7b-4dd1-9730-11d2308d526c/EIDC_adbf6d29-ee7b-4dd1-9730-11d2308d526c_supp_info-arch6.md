# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Overview
- Provides supporting information for the R code PLSPM_invasion.R used in Waddell et al. (2020a) to analyze exotic plant invasions.
- Primary data: Plot_measured_data.csv; analyses reproduce partial least squares path models (PLS-PM) via the plspm package.
- Objective: assess relative influence of fragmentation, forest disturbance, propagule pressure, soil characteristics, and native community composition on exotic invasions in fragmented forest remnants and continuous forest sites.

## Data and study design
- Study design: nested plot design across 47 plots in 17 sites in Sabah, Malaysian Borneo; 13 fragmented/remnant sites in RSPO-certified oil palm landscapes and 4 continuous forest sites (>1 million ha).
- Data types:
  - Plant surveys: adults (≥25 cm DBH), saplings (10–25 cm), seedlings (2–10 cm), and ground vegetation; exotic species richness and exotic stem abundance recorded.
  - Native community: alpha diversity measures including observed native genus richness and Faith's phylogenetic diversity (PD), calculated per plot for total native community and for each native component (adult trees, saplings, seedlings, ground vegetation).
  - Habitat and landscape: fragmentation metrics (area of forest/non-forest within 2 km, edge density), time since fragmentation (years since first oil palm planting 1991–2009), local disturbance indicators (Dipterocarpaceae large stems; average wood density), propagule pressure proxies (exotic richness and abundance outside remnants along two 100 m transects).
  - Soil characteristics: soil pH and available phosphorus (P) from five 20 cm cores per plot.
- Data structure: 47 rows (plots) with site and plot identifiers and a comprehensive set of measured variables described in Table 1.

## Variables and transformations
- Measured/derived variables include:
  - Fragmentation: Non-forest area within 2 km; forest area within 2 km; edge density index; fragmentation age.
  - Disturbance: Number of large Dipterocarpaceae stems; mean wood density (>10 cm DBH).
  - Soil: pH (logged), available phosphorus (P) (logged).
  - Propagule pressure: exotic richness outside; exotic abundance outside.
  - Native community measures: total native richness, total native PD, native adult tree richness/stems/PD, native sapling richness/stems/PD, native seedling richness/stems/PD, native ground vegetation richness/stems/PD.
  - Invasion: exotic richness and exotic abundance (within plots).
- Data preparation:
  - All measured variables centered and scaled (mean 0, variance 1).
  - Variables renamed to shorten names (e.g., Fragmentation.age -> Age; Non.forest -> Non.forest).
  - New variable Edge.density = Edge.in.2km.buffer / Area.in.2km.buffer.
  - Dataframes created to assemble variables for model input.

## Analytical approach
- Modeling framework: partial least squares path modelling (PLS-PM) using the plspm R package.
- Model structure:
  - Inner model specifies connections between latent variables (Frag, Dist, Soil, Natives, Prop, Exotics) as depicted in Fig. 1 of the accompanying material.
  - Measured variables are assigned to latent variables via blocks; latent variables can be reflective or formative.
  - Two directional tests for the relationship between native community and invasion: Native -> Invasion and Invasion -> Native.
- Model types:
  - Full dataset model using total native community as a single latent variable plus the four native components (adult trees, saplings, seedlings, ground vegetation) run in separate variants.
  - Ten total models: one full native model plus nine component-based models (full native, plus four native components each tested in both directions).
- Data preparation steps in code:
  - Create data_pls dataframe with Site, Plot, Non.forest, Edge.density, Age, Dips, WD, pH, Avail.P, Total.richness, Total.PD, Outside.rich, Outside.abun, Exotic.abundance, Exotic.richness.
  - Construct path matrix (inner model) and define blocks linking measured variables to latent variables.
  - Execute PLSPM model and summarize results.
- Model evaluation and refinement:
  - Measurement model (reliability and validity) checks:
    - Convergent validity: AVE > 0.50.
    - Reliability: standardized loadings > 0.70 (with noted exceptions).
    - Internal consistency: Cronbach’s alpha and composite reliability (Dillon-Goldstein’s rho) > 0.70.
    - Discriminant validity: cross-loadings appropriate; Fornell-Larcker criterion (AVE square root > correlations with other latent variables).
  - Structural model: assessed via R-squared (R2) for endogenous latent variables and Goodness-of-Fit (GoF).
  - Model refinement: start from full specification and remove non-significant paths (P < 0.05) stepwise; kept path matrices reflect these changes (e.g., specific loading patterns for Frag, Dist, Soil, Natives, Prop, Exotics).
  - Statistical inference: two-sided P-values for path coefficients obtained via 10,000 bootstrap iterations, using site-level bootstrap to account for the absence of site as a random effect.
- Outputs:
  - Final path diagrams (positive/negative standardized relationships) plotted via plot(pls2).
  - Summary outputs (summary(pls2)) including reliability/validity and structural relationships.
  - Reproduction guidance for figures from Waddell et al. (2020a) and related outputs.

## Validation and quality assurance
- Code and analyses have undergone peer review and are published in Landscape Ecology (Waddell et al., 2020a).
- Authors performed careful code checks and data quality control.
- Data collection followed established protocols with single observers for field surveys to minimize variation.

## How to reproduce and use
- Purpose: enables researchers to reproduce the PLS-PM analyses and explore how fragmentation, disturbance, soil attributes, propagule pressure, and native community structure relate to exotic invasion.
- Reproducibility features:
  - Clear data preparation steps (centering/scaling, renaming, edge-density calculation).
  - Explicit inner/outer model specification and sequential model fitting (full dataset and component-specific variants).
  - Bootstrap-based significance testing accommodating site-level sampling.
  - Detailed model evaluation criteria and stepwise refinement notes to replicate the final models.
- Outputs you can expect:
  - Final PLSPM model object (pls2) and bootstrap results.
  - Path diagrams and a quantitative summary of path coefficients, loadings, AVEs, reliability metrics, and R2/GoF values.
  - Documentation to recreate the figures used in the associated Landscape Ecology article.

## Study sites and data specifics
- Study sites: 17 sites across Sabah, Malaysia (July–October 2017).
- Plot design: 47 plots across 17 sites, with 2–3 plots per site; circular plots of 0.28 ha; nested sampling for different plant size classes.
- Fragmentation context: oil palm plantations (13 sites) with varying conservation values and disturbance histories; 4 continuous forest sites for baseline comparison.
- Key variables captured for analysis include fragmentation metrics, disturbance proxies, soil chemistry, propagule pressure indicators, and rich native/exotic plant community data.

## Data structure (columns)
- Site_code, Site_plot_code, Forest_type, Latitude, Longitude, Elevation_masl.
- Fragmentation and landscape: Amount of non-forest in 2km, Area in 2km buffer, Edge in 2km buffer, Fragmentation age.
- Native and disturbance: Mean wd 10cm, Number of large dipterocarps, Native and exotic richness/stems/PD across components, Plot exotic richness/abundance.
- Soil: Soil pH, Soil available P.
- Edited/derived: Edge density; transformed variants as needed for analysis.

## References
- Waddell et al. (2020a) Land-use change and propagule pressure promote plant invasions in tropical rainforest remnants. Landscape Ecology.
- Waddell et al. (2020b) Vegetation and habitat data for fragmented and continuous forest sites in Sabah, Malaysian Borneo, 2017. NERC EIDC.
- Foundational methodological references for PLS-PM and validation criteria (Sanchez 2013; Chin 1998; Fornell & Larcker 1981; related R packages plspm, phylocom, picante).