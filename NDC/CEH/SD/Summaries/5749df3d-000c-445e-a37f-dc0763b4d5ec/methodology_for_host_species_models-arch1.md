# Detailed methodology for host species models:

## Purpose and context
- Develop a model to estimate the abundance of host species across heathland and woodland habitats in Scotland.
- Address challenges: overdispersion due to many absences, unequal numbers of quadrats per NVC site, and latent true percent cover arising from unequal DOMIN class intervals.
- Previous approach (inflated beta with binomial presence/absence) could not reliably estimate random site and quadrat-level effects within a single framework.

## Overall modeling approach
- Two-phase GLMM framework within a Bayesian setting to handle interval censoring of latent percent cover.
- Phase 1 models presence/absence; Phase 2 models abundance (percent cover) conditional on presence.
- Allows environmental covariates to influence presence and abundance independently.
- Random effects capture unobserved between-site and between-quadrat variation.

## Phase 1: presence/absence model
- Data: y_ij indicates whether quadrat j within site i has zero cover (y_ij = 0) or non-zero cover (y_ij > 0); there are n1 zero-quadrats and n2 non-zero quadrats.
- Model: y_ij follows a Bernoulli/binomial structure with probability p_ij for presence of the species.
- Link and fixed effects: logit(p_ij) = a + b_i x_i + g_i + h_ij
  - a: overall intercept
  - x_i: predictors associated with site i (covariates)
  - g_i: site-level random effect to capture between-site variation (g_i ~ Normal(0, σ_g^2))
  - h_ij: quadrat-level random effect to capture within-site overdispersion (h_ij ~ Normal(0, σ_h^2))
- Notes: Assumes independence between quadrats and sites; accounts for unobserved heterogeneity with random effects.

## Phase 2: abundance model (given presence)
- Condition: Only consider sites/quadrats where presence was predicted (non-zero cover).
- Data: z_ij is the proportion of cover for the non-zero quadrats; these proportions are interval-censored within DOMIN class intervals.
- Latent variable handling: z_ij is modeled as a latent variable constrained to lie within the observed interval bounds.
- Model: z_ij follows a logit-normal distribution with fixed and random effects.
  - logit(z_ij) = α + b_i x_i + γ_i + ε_ij
    - α: intercept for abundance
    - b_i x_i: covariate effects (potentially different from presence phase)
    - γ_i: site-level random effect (γ_i ~ Normal(0, σ_γ^2))
    - ε_ij: quadrat-level random effect (ε_ij ~ Normal(0, σ_ε^2))
- Notes: γ_i and ε_ij capture unobserved site and quadrat-level variation in abundance beyond presence probability.

## Data structure and assumptions
- There is a clear separation between the presence process and the abundance process.
- Random effects account for unobserved heterogeneity at both the site and quadrat levels in both phases.
- Covariates can have distinct influences on presence versus abundance.
- Interval censoring from DOMIN class intervals is incorporated via latent z_ij in the abundance model.

## Bayesian implementation and uncertainty
- Both phases are fit within a Bayesian framework to propagate uncertainty from interval-censored latent variables and random effects.
- This framework enables coherent inference on presence probabilities and conditional abundances across sites and quadrats.

## Implications and outcomes
- The two-phase approach accommodates overdispersion, unequal sampling across sites, and latent measurement uncertainty.
- Provides insight into where host species are likely present and, when present, how abundant they are across different habitats in Scotland.
- Enhances the ability to inform ecological decisions with a model that distinctly handles presence and abundance, while properly accounting for hierarchical data structure.