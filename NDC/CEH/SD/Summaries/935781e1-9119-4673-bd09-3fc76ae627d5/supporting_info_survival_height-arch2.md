# The road to recovery: A synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- Purpose
  - A dataset and synthesis accompanying Banin et al. (2023) to evaluate planted-tree survival and growth across forest restoration efforts in tropical and sub-tropical Asia.
  - Aims to enable standardized, time-aware assessment of environmental health and restoration policy performance.

-Scope and data sources
  - Systematic literature search up to May 15, 2021; English-language studies from South and Southeast Asia (tropical and subtropical moist/dry broadleaf forests).
  - Unit of analysis: planting cases (site, species, treatment, time since planting); includes both published and grey/unpublished data via FOR-RESTOR partners.
  - Datasets: seedling dataset with 176 restoration sites, 2,477 cases, 221,199 trees; 148 sites with survival data; 136 sites with height data; 625 species (252 genera, 81 families).
  - Peat swamp and mineral soil forests included; 68 peat swamp sites and 108 mineral soil sites.
  - Supplementary data: 43 additional peat-swamp studies; 7 partner datasets; Table S1 documents unpublished datasets.

- Data collection and processing
  - Inclusion criteria: planted trees with survival data (counts/percent surviving) and/or size growth (height/diameter/biomass) in field conditions; exclude greenhouse/nursery and studies focused on natural regeneration alone.
  - Data extraction: numerical values or digitized from figures (WebPlotDigitizer); cross-validated by multiple authors.
  - Taxonomy: species names checked against World Flora Online, Flora Malesiana, Plants of the World Online; non-native single-species focus excluded.
  - Biophysical covariates: climate and soils obtained from external datasets (WorldClim 2 at 2.5 arc-min; Harmonized World Soil Database). Note: soil data not used in final analyses due to misclassification; forest type (peat swamp vs mineral soil) used instead. Climate data averaged 1970–2000.
  - Measures recorded per case: disturbance history, restoration aim, site condition prior to planting, restoration methods, planting density, seed source, duration, taxonomic data, numbers planted/monitored, seedling height/diameter, census times, survival.
  - Replanting: nine studies included replanting; to avoid bias, survival data treated to exclude replanting beyond two months after initial planting (with one exception).

- Disturbance, site condition and restoration classification
  - Disturbance types prior to restoration (six categories): logging, agriculture, plantation, fire, mining, draining (peat-swamp only).
  - Current site condition (three categories): plantation enrichment, forest enrichment, open degraded (can be mixed within a site).
  - Restoration purpose (eight classifications; Table S2): forestry (commercial), forestry + NTFP, forestry + ecological restoration, experimental, land reclamation (mining), unspecified, etc.
  - Restoration treatments alongside planting (Table S3): removal of competition, fertilisation, protection, shading, water regulation, soil preparation, and cases with no reported restoration activities beyond planting.

- Planting and species data
  - Species richness per site recorded; when not stated, assumed mixed-planting design using the paper’s total number of species.
  - Seedling characteristics: height at planting when available; if not, height within 3 months of planting used as proxy.
  - Growth metric: height used as primary growth measure due to reporting frequency across studies.
  - Seedling counts: documented or inferred when missing, with proportional allocation across species where needed.
  - Seedling survival: calculated per census as number surviving = survival proportion × number monitored.

- Functional traits and supplementary data
  - Wood density for tested species drawn from global wood density databases; values assigned at species, genus, or family level as available (phylogenetically conserved in tropical Asia).
  - Wood density data licensed via CC and stored with the dataset in EIDC.

- Mortality analyses (Section 4)
  - Modeling approach: generalized linear mixed effects models (GLMM) with binomial error and complementary log-log link, at standardized time points (1, 2, 3, 4 years; 5–10 years; >10 years after planting).
  - Random effects: site, species, species within-site; observation-level random effect for overdispersion.
  - Fixed effects: mean annual temperature, dry-season precipitation, elevation; forest type; forest condition; species richness; wood density; interactions between wood density and forest type/condition.
  - Model selection: information-theoretic approach using dredge (MuMIn); top models with ∆AIC < 2; variables with importance > 0.8 carried into final models.
  - Additional analyses: separate models for planting density and initial height effects on mortality at 1–2 years in open degraded vs forest enrichment habitats.
  - Diagnostics and outputs: DHARMa residual diagnostics; marginal and conditional R2; intra-class correlations (ICC) for random effects.

- Growth rate analyses (Section 5)
  - Objective: estimate annual size-standardised height growth rates (AGR) across varying initial seedling sizes and census intervals.
  - Growth modeling: for each treatment–species–site with ≥4 height censuses, compare linear, exponential, and Gompertz growth forms; select best by AIC.
  - AGR calculations: at reference heights of 100, 200, and 300 cm (within data range); compute time to reach height h via inverse growth function; derive annual growth rate g(t).
  - Statistical modeling: ln-transformed AGRs modeled with linear mixed models; fixed effects similar to mortality (climate, forest type, forest condition, species richness, wood density; interactions with wood density).
  - Random effects: site and species (crossed) as appropriate; model selection via MuMIn with ∆AIC < 2; variables with importance > 0.8 used in final model.
  - Uncertainty assessment: delta-method standard errors for AGR; quantify within- vs between-combination uncertainty (ICC-like metric); simulation-based sensitivity analysis (500 simulated datasets × 1000 model runs) to assess impact on regression estimates.
  - Outputs: AGR estimates and uncertainty; evaluation of robustness of results to AGR estimation uncertainty.

- Practical implications for environmental monitoring
  - Provides standardized, time-adjusted metrics (mortality timepoints; AGR at common heights) to compare restoration outcomes across sites and regimes.
  - Enables assessment of how disturbance history, forest type, planting diversity, and wood density influence survival and growth.
  - Supports data-driven decisions on species selection, planting density, and maintenance practices in different habitat conditions.

- Data access, limitations and notes
  - Data licensing: climate and soil datasets require separate download; not included directly in the EIDC repository.
  - Some data derived from figures; potential measurement uncertainty.
  - Variability in census intervals and site conditions; mixed disturbances and canopy statuses within sites.
  - Peat swamp misclassifications in soil data; forest-type dichotomy used instead.
  - Replanting data treated cautiously to avoid bias in survival analyses.

- Tools and references
  - Statistical tools: glmmTMB (mortality), lme4 (AGR), MuMIn (model selection), DHARMa (diagnostics), ggeffects (marginal effects).
  - R scripts referenced: script_SynthesisAnalysis_MortalityModels.R, height_ASGR_nlms.R, script_SynthesisAnalysis_ASGR_MEMs.R.
  - Key sources: Banin et al. 2023; WorldClim; Harmonized World Soil Database; World Flora Online; Flora Malesiana; Plants of the World Online; WebPlotDigitizer.