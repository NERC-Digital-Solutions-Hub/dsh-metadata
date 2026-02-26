# Detailed methodology for host species models:

- Purpose
  - Develop a model to estimate the abundance of host species across heathland and woodland habitats in Scotland.
  - Address key data challenges: overdispersion from many absences, unequal numbers of quadrats per NVC survey site, and uncertainty in true percent cover due to interval-censored DOMIN class data.

- Modelling strategy
  - Two-phase, hierarchical approach embedded in a Bayesian framework.
    - Phase 1: model presence or absence (binary) of each host species at each site/quadrat.
    - Phase 2: conditional on presence, model the abundance as percent cover (a proportion).
  - This separation allows environmental covariates to influence presence and abundance independently.

- Phase 1 — presence/absence model
  - Model type: overdispersed binomial generalized linear mixed model (GLMM).
  - Data structure: for each site i and quadrat j, y_ij indicates zero cover (absent) or non-zero cover (present).
  - Random effects:
    - Site-level random effect (g_i) to capture unaccounted variation between sites.
    - Quadrat-level random effect (h_ij) to capture extra-binomial variation among quadrats at the same site.
  - Fixed effects: predictors x_i associated with site i.
  - Link function and linear predictor: use logit with parameters a, b_i, plus random effects g_i and h_ij, to model presence probability p_ij.

- Phase 2 — abundance model (given presence)
  - Model type: logit-normal GLMM for proportions, conditional on presence.
  - Data structure: consider only quadrats with non-zero cover (n_2 sites).
  - Latent variable handling: true proportion z_ij is interval-censored within the DOMIN class interval data.
  - Random effects:
    - Site-level random effect (γ_i) to account for between-site variation in abundance.
    - Quadrat-level random effect (ε_ij) to account for within-site, between-quadrat variation.
  - Distributional form:
    - z_ij follows a logit-normal distribution with mean μ and variance σ^2.
    - logit(z_ij) = α + b_i x_i + γ_i + ε_ij, with ε_ij ~ Normal(0, σ_ε^2).
  - Latent variable handling: z_ij is constrained to lie within the observed DOMIN interval bounds to reflect interval-censored data.

- Key methodological features
  - Bayesian inference is used to accommodate interval censoring of latent variables (true percent cover) and to propagate uncertainty through both modelling stages.
  - The model structure includes both site and quadrat random effects to capture hierarchical data and overdispersion.
  - Covariates can influence presence and abundance separately, enabling nuanced ecological interpretation.

- Data and assumptions
  - Data are hierarchical: quadrats nested within sites, with varying numbers of quadrats per site.
  - Assumptions include independence between quadrats and sites conditional on random effects, and separability of the presence and abundance processes.
  - The approach explicitly accommodates missing or interval-censored information about percent cover.

- Implications for environmental monitoring
  - Produces robust, uncertainty-aware estimates of host species abundance across different habitat types.
  - Handles common monitoring data issues (unbalanced sampling, overdispersion, censored measurements) within a coherent Bayesian framework.
  - Provides a principled basis for using environmental covariates to explain both occurrence and abundance, aiding habitat health assessments and policy-relevant monitoring over time.