# Detailed methodology for host species models:

- Context and purpose
  - Develop a model to estimate the abundance of host species across heathland and woodland habitats in Scotland.
  - Address data challenges: overdispersion from many absences, unequal numbers of quadrats per NVC site, and latent true percent cover due to DOMIN class interval structure.
  - Provide a framework where environmental covariates can differently influence presence and abundance, aiding monitoring and decision-making.

- Modelling approach
  - Two-phase modeling within a Bayesian generalized linear mixed-model (GLMM) framework.
  - Phase 1 focuses on presence/absence; Phase 2 focuses on abundance given presence.
  - Treats latent variables and interval censoring explicitly to reflect data limitations.

- Phase 1: presence/absence model
  - Outcome: whether species i is present at site j across quadrats (zero vs non-zero cover).
  - Model type: overdispersed binomial GLMM.
  - Structure:
    - Probability of presence p_ij' modeled on the logit scale.
    - Fixed effects: site-level predictors x_i with coefficients b_i.
    - Random effects: site-level g_i and quadrat-level h_ij to capture unobserved variation between sites and among quadrats within a site.
  - Assumptions:
    - Independence between quadrats and sites.
    - Random effects modeled as Normal distributions with respective variances (σ_g^2, σ_h^2).

- Phase 2: abundance given presence
  - Conditioned on presence (non-zero cover), model the observed percent cover z_ij.
  - Model type: logit-normal GLMM for proportions, with latent interval-censoring to reflect DOMIN class intervals.
  - Structure:
    - For non-zero cases, z_ij is modeled via a logit-normal distribution with mean μ and variance σ^2.
    - Fixed effects: site-level predictors x_i with coefficients b_i (same predictors as Phase 1, but potentially different influence).
    - Random effects: site-level γ_i and quadrat-level ε_ij to capture unobserved variation between sites and among quadrats within a site.
  - Latent variable and censoring:
    - z_ij is not observed exactly but is known to lie within the DOMIN class interval bounds.
    - A latent variable framework ties z_ij to the interval-censored data, enabling proper estimation under censoring.

- Data- and model-driven decisions
  - The inflated/beta approach to model plant cover was not reliable for estimating random effects; thus the logit-normal GLMM approach was chosen.
  - The model accommodates different environmental covariates influencing presence and abundance separately, enabling nuanced interpretation for monitoring and policy evaluation.

- Bayesian framework and inference
  - Both phases are fit in a Bayesian context to handle latent variables and interval censoring effectively.
  - Random effects capture unobserved heterogeneity across sites and quadrats, improving uncertainty quantification and interpretability for management decisions.

- Relevance to environmental monitoring
  - Provides a rigorous, hierarchical method to derive presence/absence and abundance metrics from imperfect field data.
  - Addresses common monitoring data issues: missing data, unequal sampling, data censorship, and data governance considerations through transparent modeling of uncertainty.
  - Produces indicators that can inform policy decisions by separating occupancy dynamics from abundance dynamics and by clearly quantifying site- and quadrat-level variability.