# Detailed methodology for host species models:

- Objective
  - Develop a model to estimate the abundance of host plant species across heathland and woodland habitats in Scotland.
  - Address data challenges including overdispersion, unequal numbers of quadrats per site, and interval-censored percent cover data derived from DOMIN class intervals.

- Modelling approach and rationale
  - Initial attempt: inflated beta distribution with presence/absence for interval data failed to reliably estimate random effects (site and quadrat level).
  - Adopted a logit-normal model structured as a generalized linear mixed model (GLMM) for logit-transformed proportions.
  - Implemented a two-phase (two-stage) modelling framework:
    - Phase 1: model presence/absence using an overdispersed binomial GLMM.
    - Phase 2: conditional on presence, model abundance (percent cover) using a logit-normal model.
  - Both phases are fit within a Bayesian framework to accommodate interval censoring of latent true percent cover.

- Data structure and components
  - data: quadrats nested within survey sites; each quadrat has presence/absence and, if present, a measured (latent) percent cover.
  - Observations:
    - y_ij indicates zero cover (0) or non-zero cover (1) for quadrat j in site i (presence model).
    - For non-zero cases, the latent percent cover is treated with a second model.
  - Covariates: site-level predictors x_i influence presence and abundance.

- Phase 1: Presence model (binary data)
  - Model specification (conceptual):
    - Presence probability p_ij depends on site covariates and random effects.
    - Includes a site random effect (g_i) to capture unaccounted for site-level variation.
    - Includes an individual/quadrat random effect (h_ij) to capture overdispersion among quadrats within a site.
  - Distributional assumptions:
    - Quadrats are treated as conditionally independent given random effects.
    - Random effects: g_i ~ Normal(0, σ_g^2), h_ij ~ Normal(0, σ_h^2).

- Phase 2: Abundance model (conditional on presence)
  - Model specification (conceptual):
    - Among sites/quadrat combinations predicted to have presence, model the proportion cover z_ij.
    - z_ij follows a logit-normal distribution with latent mean μ and variance σ^2.
    - Includes covariates and random effects at site and quadrat levels.
  - Latent variable formulation:
    - logit(z_ij) = α + b_i x_i + γ_i + ε_ij
    - Random effects: γ_i ~ Normal(0, σ_γ^2) (site), ε_ij ~ Normal(0, σ_ε^2) (quadrat within site).
  - Interval censoring:
    - Proportions z_ij are not observed exactly but are known to lie within DOMIN class interval bounds.
    - A latent variable framework enforces z_ij to lie within these bounds, propagating uncertainty through the model.

- Bayesian framework and uncertainty
  - Using Bayesian inference allows explicit handling of latent variables and interval-censored data.
  - Uncertainty from both stages (presence and abundance) and from censoring is propagated to final estimates.
  - Different environmental covariates can influence presence and abundance independently, enabling flexible ecological inference.

- Data governance and practical implications for data leaders
  - Demonstrates robust handling of imperfect, censored ecological data without relying on potentially problematic inflated-beta approaches.
  - Highlights the value of hierarchical modelling to separate detection/presence from abundance, improving interpretability for decision-making.
  - Emphasizes the importance of documenting data intervals, metadata (e.g., DOMIN class definitions), and uncertainty to support reproducibility.
  - Provides a scalable, transparent framework that can be integrated with additional data sources and covariates to inform management and conservation strategies.