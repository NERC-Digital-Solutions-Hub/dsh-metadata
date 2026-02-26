# Detailed methodology for host species models:

- Purpose and scope
  - Develop a model to estimate host species abundance across heathland and woodland habitats in Scotland.
  - Address data issues: overdispersion from many absences, unequal numbers of quadrats per NVC site, and latent true percent cover due to DOMIN class interval uncertainty.
  - Employ a two-phase, logit-normal GLMM framework within a Bayesian setting to handle interval censoring of latent proportions.

- Data structure and challenges
  - Data organized as quadrats within sites (NVC survey sites).
  - Presence/absence data is highly zero-inflated; the number of quadrats per site varies.
  - True percent cover is not directly observed because DOMIN class intervals provide only interval-censored bounds.

- Modeling framework (two-phase approach)
  - Phase 1: Model presence vs. absence using an overdispersed binomial GLMM.
  - Phase 2: Given presence, model the abundance (percent cover) with a logit-normal GLMM.
  - Covariates (x_i) can influence presence and abundance independently.

- Phase 1: Presence/absence (binomial GLMM)
  - Outcome: y_ij indicates zero cover (0) or non-zero cover (1) for quadrat j in site i.
  - Model structure: logit(p_ij') = a + b_i x_i + g_i + h_ij.
  - Random effects: 
    - Site effect g_i ~ Normal(0, sigma_g^2) to capture between-site variation.
    - Quadrat effect h_ij ~ Normal(0, sigma_h^2) to capture within-site overdispersion among quadrats.
  - Assumptions include independence between quadrats and sites.

- Phase 2: Abundance given presence (logit-normal GLMM)
  - Eligible quadrats: those predicted present (non-zero) at site i.
  - Outcome: z_ij is the proportion of cover for quadrat j within site i (non-zero cases).
  - Model structure: logit(z_ij) = alpha + b_i x_i + gamma_i + epsilon_ij.
  - Random effects:
    - Site effect gamma_i ~ Normal(0, sigma_gamma^2) to capture between-site variation in abundance.
    - Quadrat effect epsilon_ij ~ Normal(0, sigma_e^2) to capture within-site overdispersion among quadrats.
  - Latent, interval-censored nature: z_ij is not observed exactly but lies within DOMIN class interval bounds; a latent variable framework constrains z_ij within those bounds.

- Handling uncertainty and censoring
  - Interval censoring of the latent percent cover (true z_ij) is incorporated to reflect DOMIN class interval uncertainty.
  - Bayesian framework is used to accommodate latent variables and quantify uncertainty in both presence and abundance components.

- Random effects and hierarchical structure
  - Two-level hierarchy with sites and quadrats:
    - Stage 1 includes site (g_i) and quadrat (h_ij) random effects.
    - Stage 2 includes site (gamma_i) and quadrat (epsilon_ij) random effects.
  - This structure accounts for unobserved heterogeneity at both the site and quadrat levels, aiding robust estimation of presence and abundance.

- Bayesian inference and benefits
  - Fitting within a Bayesian framework allows:
    - Direct incorporation of interval-censored data for true percent cover.
    - Propagation of uncertainty from latent variables through to presence and abundance estimates.
    - Flexible estimation of random effects and variance components.

- Data governance implications for Data Stewards
  - Data quality and provenance
    - Document data collection design: number of quadrats per site, site selection, DOMIN class intervals, and covariates used.
    - Metadata should capture how presence/absence and abundance are derived, including interval-censoring rules and latent variable treatment.
  - Data standards and interoperability
    - Use consistent identifiers for sites, quadrats, and species.
    - Standardize variables for covariates (x_i) and ensure units are clear for reproducibility.
  - Uncertainty and transparency
    - Report uncertainty from both model stages and from latent z_ij; provide posterior distributions or credible intervals.
    - Clearly label and share the latent variable framework and censoring mechanics to enable reproducibility.
  - Data storage, access, and sharing
    - Store inputs (counts, interval bounds, covariates) and outputs (stage-1 and stage-2 parameter estimates) with versioning.
    - Ensure data portals support hierarchical model outputs and latent-variable annotations.
  - Data quality assurance
    - Validate data against field protocols (quadrats-per-site, presence/absence recording, DOMIN classifications).
    - Implement consistency checks for interval bounds and model-derived quantities (presence probabilities, latent z_ij values).
  - Operational considerations
    - Plan for data updates and re-fitting as new quadrats or sites are added; systems should accommodate updating random effects and posterior summaries.