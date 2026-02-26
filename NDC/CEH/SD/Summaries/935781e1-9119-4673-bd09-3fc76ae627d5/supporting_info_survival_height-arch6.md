# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Overview
- A dataset accompanying Banin et al. (2023) synthesizing outcomes from forest restoration in tropical and sub-tropical Asian forests.
- Focuses on planted tree survival and height/growth to enable cross-site comparisons and data-driven restoration insights.
- Based on 151 studies, 176 restoration sites, and 2,477 planting cases, spanning South and Southeast Asia (including peat swamp and mineral soils).

## Data scope and sources
- Literature coverage: systematic Web of Science search up to May 15, 2021; English-language studies; additional peat swamp studies read in Indonesian; includes 43 unpublished studies and grey literature via FOR-RESTOR partners.
- Seedling dataset: 176 sites, 221,199 trees; 148 sites with survival data; 136 sites with height growth data; 625 species (252 genera, 81 families).
- Soil/site context: 108 mineral-soil sites and 68 tropical peat swamp forest sites.
- Data sharing: datasets stored in the Environmental Information Data Centre (EIDC) under creative commons; wood density data linked from the Global Wood Density Database and provided in the dataset.
- Data and code availability: accompanying R scripts for analyses; climate and soil data not embedded in the repository and must be downloaded separately to reproduce analyses.

## Variables captured and data processing
- Planting and outcomes: number of seedlings planted, number monitored, survival counts, census times, height and/or diameter measurements, and growth (when available).
- Site and disturbance context: disturbance type (logging, agriculture, plantation, fire, mining, draining), current site condition (plantation enrichment, forest enrichment, open degraded), restoration purpose, and planting density.
- Planting design: species richness per treatment, seed source, and whether nurse plants were used.
- Ancillary data: species taxonomic names standardized to World Flora Online; loss of non-native monocultures; height recorded at planting when possible; replanting occurrences recorded and treated separately.
- Biophysical covariates: climate (mean annual temperature, dry-season precipitation) and elevation drawn from WorldClim datasets (averaged 1970–2000); soil type dichotomy (peat swamp vs mineral soil); soil data not included in the public dataset due to licensing.
- Functional traits: wood density for tested species drawn from the Global Wood Density Database; values assigned at species, genus, or family level when necessary.

## Planting cases, disturbance, and site condition classifications
- Disturbance types: six categories (logging, agriculture, plantation, fire, mining, draining); some sites contain mixed disturbances.
- Current condition categories: plantation enrichment, forest enrichment, open degraded (sites may have more than one condition).
- Treatment classification: restoration methods alongside planting categorized into seven types (see below).
- Restoration purpose classifications: eight categories (e.g., forestry, forestry and ecological restoration, experimental, land reclamation, and unspecified), enabling analysis of aims across studies.

## Restoration treatments and species information
- Restoration establishment/maintenance methods (examples): removal of competition (weeding, climber cutting, girdling), fertilisation, protection (fire breaks, fencing, guards), shading (nursery shade), water regulation (irrigation, drainage), soil preparation; some cases report no additional restoration beyond planting.
- Species diversity: mixed planting considered when multiple species were planted; taxonomic checks ensured accurate naming; single-species non-native sites excluded.
- Species and genera: dominant taxa included Shorea balangeran, Dyera polyphylla, Shorea leprosula, Shorea parvifolia, Shorea ovalis; genera-rich et al. across Dipterocarpaceae and related groups.
- Functional traits: wood density used to explore trait-driven survival/growth; values distributed across species/genus/family due to data availability.

## Seedling data and replanting
- Replanting: nine studies replanted seedlings (typically 1 week to 2 months after initial planting); some second-season replanting; to avoid bias, replanting data beyond 2 months were excluded from survival analyses.
- Seedling size: height at planting recorded when available; otherwise inferred from early census data or site-level averages.
- Data handling: where exact counts were missing, imputation rules (percentiles, proportional allocations across species) were applied to preserve comparability.

## Mortality analyses
- Modeling approach: generalized linear mixed effects models (GLMMs) with binomial error and a complementary log-log link.
- Time points: standardised intervals at 1, 2, 3, 4 years, 5–10 years, and >10 years after planting to accommodate heterogeneous census intervals.
- Random effects: site, species, and species-within-site (plus an observation-level random effect for overdispersion).
- Fixed effects and interactions: mean annual temperature, dry-season precipitation, elevation; forest type; forest condition; species richness of plantings; wood density; interaction terms between wood density and forest type/condition.
- Model selection and diagnostics: information-theoretic approach (MuMIn/dredge) to identify top models (ΔAIC < 2); variables with importance >0.8 retained in final models; additional models examining planting density and initial height for early mortality in open degraded vs forest enrichment habitats; diagnostic checks with DHARMa; marginal and conditional R2 values; ICC to assess random-effects contribution.

## Growth rate analyses
- Growth metric: annual size-standardised growth rate (AGR) derived from height data, acknowledging size-dependence of growth.
- Model forms: linear, exponential, and Gompertz growth curves f(t); selection by AIC, with preference for simpler models if ΔAIC < 2; reference heights chosen at 100, 200, and 300 cm (within observed ranges).
- AGR calculation: time to reach reference heights from the inverse growth function; AGRs computed as height change over time around the reference height.
- Statistical modeling: ln-transformed AGRs modeled with linear mixed models; fixed effects mirror mortality models; random effects include site and species (crossed where appropriate).
- Model selection and uncertainty: similar multi-model inference (MuMIn); propagation of uncertainty from growth curve fits via simulation; delta-method-based standard errors for AGR; comparison of within- vs between-combination uncertainty; simulation-based sensitivity analysis (500 datasets, 1000 models) showing robust results.
- Uncertainty interpretation: findings suggest within-combination uncertainty is low relative to between-combination variation, implying limited impact on final model outcomes.

## Data availability and usage notes
- Dataset scale and content: 176 restoration sites, 221,199 trees; 148 survival data sites; 136 height-growth data sites; 625 planted species (252 genera, 81 families).
- Top species and diversity: Shorea balangeran, Dyera polyphylla, Shorea leprosula, Shorea parvifolia, Shorea ovalis; dominant genera include Shorea, Hopea, Dipterocarpus, Dryobalanops, and Dyera.
- Wood density: species- and genus-level assignments based on global density data; density values are phylogenetically conserved in tropical Asia.
- Reproducibility: analyses are described with explicit scripts (Mortality: script_SynthesisAnalysis_MortalityModels.R; Growth: height_ASGR_nlms.R and related utilities); results and uncertainty analyses are documented in supporting materials of Banin et al. (2023).
- Data licensing and use: CC-licensed dataset; climate/soil data require separate download to reproduce statistical analyses; users can build dashboards or data products to compare drivers of survival and growth across restoration contexts.

Key takeaways for data-support use
- The dataset enables cross-site meta-analyses of survival and growth drivers in tropical/sub-tropical forest restoration across Asia.
- It supports testing how disturbance history, current forest condition, planting diversity, and wood density interact with climate and site type to influence outcomes.
- The accompanying code and methodological transparency allow replication, uncertainty assessment, and development of data products (dashboards, decision-support tools) for practitioners and policymakers.