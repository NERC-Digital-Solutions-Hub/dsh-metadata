# Detailed methodology for host species models:

- Objective and context
  - Develop a model to estimate the abundance of host species across heathland and woodland habitats in Scotland.
  - Address overdispersion, unequal numbers of quadrats per site, and uncertainty about true percent cover due to interval-censored DOMIN class data.
  - Use a two-phase, Bayesian GLMM approach with latent variables to enable mapping and spatial interpretation.

- Modelling framework
  - Data structure: observations across sites (i) and quadrats (j) with presence/absence and partially observed abundance (percent cover) data; DOMIN class intervals provide interval bounds for true cover.
  - Two-phase model enables environmental covariates to influence presence and abundance independently.
  - Bayesian framework used to handle latent variables and interval censoring, providing full posterior uncertainty for GIS outputs.

- Phase 1: Presence/absence (overdispersed binomial GLMM)
  - Response: presence vs. absence of species in each quadrat (y_ij).
  - Link and linear predictor: logit(p_ij') = intercept + site effects + quadrat effects + covariates for site i.
  - Random effects: a site-level random effect g_i to capture unobserved site variation and a quadrat-level random effect h_ij to capture extra variation among quadrats within a site (overdispersion).
  - Purpose: estimate the probability of occurrence while accounting for between-site and within-site heterogeneity.

- Phase 2: Abundance given presence (logit-normal model)
  - Applicable only where the species is predicted present at a site.
  - Response: latent proportions z_ij representing percent cover for non-zero quadrats.
  - Latent modeling: z_ij is treated as logit-normally distributed with bounds from DOMIN class intervals (interval-censored).
  - Link and linear predictor: logit(z_ij) = intercept + site covariates + site random effect γ_i + quadrat random effect ε_ij.
  - Random effects: a site-level effect γ_i and a quadrat-level effect ε_ij to capture unobserved variation among sites and among quadrats at the same site.
  - Purpose: estimate abundance (percent cover) conditional on presence, while honoring interval-censored data.

- Handling uncertainty and data challenges
  - Interval censoring: true cover z_ij is unobserved but constrained within DOMIN interval bounds; latent variable approach accommodates this in the Bayesian framework.
  - Separate covariate effects: environmental covariates can differently influence presence and abundance.
  - Choice of distribution: replacing inflated beta with a logit-normal GLMM addresses estimation issues for random effects and residual variation.

- Data requirements and GIS outputs
  - Requires site-level covariates and per-quadrat presence/absence data with DOMIN interval bounds for percent cover.
  - Outputs suitable for mapping: predicted presence probability at quadrat/site level and predicted (latent) abundance where present.
  - Enables spatial visualization across heathland and woodland habitats with quantified uncertainty (credible intervals) from the Bayesian fit.

- Assumptions and considerations
  - Independence assumptions: quadrats are independent given site effects; sites are independent.
  - Random effects capture unobserved heterogeneity at both site and quadrat levels.
  - The approach reconciles data limitations (unequal quadrat numbers, zero-inflation, interval-censored data) to produce robust, map-ready estimates.