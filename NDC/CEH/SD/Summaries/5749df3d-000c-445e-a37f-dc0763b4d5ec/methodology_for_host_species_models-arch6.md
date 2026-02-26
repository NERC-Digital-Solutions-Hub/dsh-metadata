# Detailed methodology for host species models:

- Objective
  - Develop a model to estimate the abundance of host species across heathland and woodland habitats in Scotland, addressing overdispersion, unequal numbers of quadrats per site, and uncertainty in true percent cover due to interval-censored DOMIN class data.

- Modelling framework
  - Two-phase, generalized linear mixed model (GLMM) approach structured within a Bayesian framework.
  - Phase 1 models presence/absence; Phase 2 models abundance given presence.
  - Enables environmental covariates to influence presence and abundance independently and accommodates latent variables and data uncertainty.

- Phase 1: Presence/absence
  - Binary outcome for species i at site j across quadrats (y_ij): zero cover or non-zero cover.
  - Overdispersed binomial GLMM:
    - logit(p_ij) = a + b_i x_i + g_i + h_ij
    - g_i ~ Normal(0, sigma_g^2) is a site-level random effect.
    - h_ij ~ Normal(0, sigma_h^2) is a quadrat-level random effect (within-site overdispersion).
  - Accounts for unobserved heterogeneity between sites and among quadrats.

- Phase 2: Abundance given presence
  - For sites predicted to have presence, model the percent cover z_ij of species i (non-zero cases).
  - Logit-normal model:
    - logit(z_ij) = alpha + b_i x_i + gamma_i + epsilon_ij
    - z_ij ~ LogitNormal(mu, sigma^2) with mu = alpha + b_i x_i + gamma_i + epsilon_ij
    - gamma_i ~ Normal(0, sigma_gamma^2) is a site-level random effect.
    - epsilon_ij ~ Normal(0, sigma_eps^2) is a quadrat-level random effect.
  - Z_ij represents the proportion of cover; true values are latent due to interval censoring.

- Data handling and latent variables
  - DOMIN class intervals provide bounds for the true percent cover; z_ij is treated as a latent variable constrained within these bounds.
  - Interval censoring is explicitly incorporated in the Bayesian framework.

- Random effects and dependency structure
  - Both phases include site-level and quadrat-level random effects to capture unaccounted variation.
  - Assumes independence between quadrats and sites within each phase.

- Covariates and modelling independence
  - Covariates x_i (site-level predictors) influence presence and abundance.
  - Different covariates can affect presence and abundance independently, allowing flexible ecological interpretation.

- Bayesian estimation
  - The entire two-phase model is fit within a Bayesian framework to coherently propagate uncertainty from latent variables and interval censoring through to final estimates.