# The road to recovery: A synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

## Overview
- A dataset accompanying Banin LF et al. (2023) synthesizing planted-tree outcomes in tropical and subtropical Asian forests.
- Compiles planted tree survival and growth data (height, diameter, biomass) from landscapes across South and Southeast Asia.
- Final seedling dataset: 151 studies, 176 restoration sites, 2,477 cases (a species at a site with a given treatment, established at a given time).
- Surviving data: 148 sites with survival data (207,224 trees) and height-growth data from 136 sites (102,412 trees).
- Includes mineral soil and tropical peat swamp forest sites (108 and 68 sites, respectively).
- Species richness is generally low (median 3 species per site; up to 49 in some cases).
- Wood density traits are linked to species data; in total 625 tree species represented (252 genera, 81 families).
- Unpublished/grey literature contributions included via the FOR-RESTOR network.

## Data scope and geography
- Regions: South and Southeast Asia.
- Sites: 176 restoration sites across 221,199 planted trees.
- Data types:
  - Survival: numbers or proportions surviving at census intervals.
  - Growth: height (primary growth metric), with some studies reporting diameter/biomass.
- Biophysical context:
  - Climate variables derived from WorldClim (mean annual temperature, dry-season precipitation, elevation).
  - Soil context categorized as forest on mineral soil vs peat swamp forest (soil properties not used directly due to misclassification issues).

## Data collected and variables
- Disturbance history prior to restoration (six categories): logging, agriculture, plantation, fire, mining, draining (peat swamp only).
- Current site condition categories: plantation enrichment, forest enrichment, open degraded (can be multiple per site).
- Restoration purpose (eight classifications): forestry and related terms (commercial) to ecological restoration, experimental, land reclamation, and unspecified.
- Restoration treatments (alongside planting): seven categories including removal of competition, fertilisation, protection, shading, water regulation, soil preparation, and cases with no additional restoration activities.
- Planting details:
  - Species richness per site (within-treatment); cases with multiple species treated as mixed planting when not specified.
  - Seedling counts planted and monitored; density calculations when not all data provided.
  - Seed sources and planting ages; height at planting when available.
  - Replanting: nine studies reported replanting after initial death; data cleaned to avoid confounding survival estimates.
- Taxonomy and data quality:
  - Plant species names validated against World Flora Online; non-native single-species sites excluded.
  - Wood density values drawn from global databases and assigned at species, genus, or family level as appropriate.
- Geospatial and ancillary data:
  - Location data: country, coordinates, study year, region, disturbance type, restoration method, site condition, etc.
  - Biophysical at site level drawn from WorldClim (2.5-minute resolution, 1970–2000 means).
  - Soil/forest type classification (mineral soil vs peat swamp) used in analyses due to data limitations.
- Data extraction and validation:
  - Numerical data extracted from papers and figures (WebPlotDigitiser used where needed).
  - Independent checks performed for consistency.
  - Seedling replanting data treated to avoid biasing survival estimates.

## Mortality analyses
- Approach: separate generalized linear mixed effects models for standardized time points (1, 2, 3, 4 years; 5–10 years; >10 years after planting).
- Model: binomial data with a complementary log-log link; random effects for site, species, and site-species; observation-level random effect for overdispersion.
- Fixed effects tested:
  - Climate: mean annual temperature, dry-season precipitation, elevation (dry-season precipitation used due to high correlation with mean annual precipitation).
  - Forest type (mineral soil vs peat swamp) and forest condition (plantation enrichment, forest enrichment, open degraded).
  - Species richness of plantings and wood density; interaction terms wood density × forest type and wood density × forest condition.
  - Exposure to hazard (for longer-term analyses) as a covariate.
- Model selection:
  - Information-theoretic approach (AIC); multi-model inference to identify key variables (importance value >0.8).
  - Separate models to test effects of planting density and initial mean height on mortality at 1–2 years across habitat classes.
- Diagnostics: model checks with DHARMa; marginal and conditional R2; intra-class correlations to assess random-effect contributions.

## Growth rate analyses
- Metric: annual size-standardised growth rate (AGR) to account for size-dependent growth; analyzed separately for each treatment–species–site combination with at least four height censuses.
- Growth curve options:
  - Linear, Exponential, Gompertz. Selection via AIC (best fit chosen; simpler model preferred if ΔAIC < 2).
- AGR calculation:
  - AGRs estimated at reference heights of 100, 200, and 300 cm (within observed height range).
  - Time to reach reference height derived from inverse growth function; AGR computed as short-term rate around that height.
- Statistical modeling of AGR:
  - ln-transformed AGR modeled with linear mixed models.
  - Fixed effects mirrored mortality models: climate, forest type, forest condition, species richness, wood density; interactions as above.
  - Random effects: site and species (crossed); some growth models had site-only random effects.
- Uncertainty and robustness:
  - Delta-method used to derive standard errors for AGR; propagation of uncertainty via simulations to assess impact on model outputs.
  - Additional analysis comparing within-site–species–treatment uncertainty to between combinations; simulations (n=500 datasets) show similar parameter estimates, indicating limited influence of AGR estimation uncertainty on final results.

## Data outputs and key traits
- Planting scope:
  - 176 restoration sites; 221,199 trees planted; 625 species represented (252 genera; 81 families).
  - 148 sites reported survival data; 136 sites reported height growth data.
- Species and traits:
  - Most common species: Shorea balangeran, Dyera polyphylla, Shorea leprosula, Shorea parvifolia, Shorea ovalis.
  - Most common genera: Shorea, Hopea, Dipterocarpus, Dryobalanops, Dyera.
  - Wood density data linked to species; used as a functional trait to explore trait-based survival/growth patterns.
- Data products for GIS:
  - Case-level data linking site, species, treatment, and temporal census information.
  - Biophysical layers (from WorldClim) and forest type classifications at each site.
  - Site-condition, disturbance history, restoration methods, and planting-density variables.

## Data access and GIS applicability
- Access: data stored in the EIDC (Environment Information Data Centre) repository; wood density traits and ancillary data available under open licenses.
- GIS relevance:
  - Enables spatial analysis of survival and growth relative to climate, elevation, and dry-season precipitation.
  - Facilitates exploration of how peat swamp vs mineral soils influence restoration outcomes.
  - Supports mapping of disturbance context, restoration approaches, and site conditions to identify best-practice patterns.
  - Provides a rich trait-based layer (wood density) for linking species traits to spatial patterns of performance.
- Data limitations for GIS:
  - Soil properties not directly used due to misclassification; classification into peat vs mineral soil is a proxy.
  - Climate and soil datasets used in analysis must be downloaded separately by users due to licensing.
  - Heterogeneous census intervals across studies; aggregation and cross-site comparisons require careful standardization.

## Limitations and considerations for GIS analyses
- Heterogeneity across studies in census timing, planting densities, and reporting formats.
- Soil properties omitted due to data licensing and misclassification issues; physical soil maps may be needed for finer-scale analyses.
- Potential biases from study design (e.g., focus on certain habitat types or species) despite rigorous data curation.
- Reliance on global climate datasets (WorldClim) for site-level covariates; local climate nuances may affect fine-scale analyses.

## Practical GIS applications
- Map and compare survival rates at standardized time points across sites and forest types.
- Link mortality and AGR patterns to disturbance history and restoration methods to identify effective strategies.
- Overlay with climate and elevation to assess climate–growth/survival relationships at landscape scale.
- Integrate wood density and taxonomic data to explore trait-driven restoration outcomes and prioritize species for enrichment planting.
- Build predictive layers for planning restoration investments under varying climate and disturbance scenarios.