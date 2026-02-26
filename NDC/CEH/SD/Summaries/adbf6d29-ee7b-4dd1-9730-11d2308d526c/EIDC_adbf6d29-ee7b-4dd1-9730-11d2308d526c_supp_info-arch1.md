# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

- Purpose and scope
  - Provides code and data to reproduce analyses in Waddell et al. (2020a) on how fragmentation, disturbance, propagule pressure, soil characteristics, and native plant community composition influence exotic plant invasions in fragmented vs. continuous forest in Sabah, Malaysian Borneo.
  - Code analyzes a plot-level data table (Plot_measured_data.csv) to assess relative influences using partial least squares path modeling (PLS-PM) with the plspm R package.

- Data and study design
  - Data source: plot-level vegetation and habitat measurements from 47 plots across 17 sites ( Sabah, Malaysia Borneo).
  - Landscape context: 13 fragmented forest sites within RSPO-certified oil palm plantations and 4 continuous forest sites for baseline comparison.
  - Sampling design: two to three circular plots per site (0.28 ha each), nested sampling across native size classes:
    - C1: large trees (≥25 cm DBH)
    - C2: small trees (10–25 cm DBH)
    - C3: tree saplings (2–10 cm DBH)
    - Q: tree seedlings and ground vegetation (1×1 m quadrats)
  - Exotics: recorded exotic richness and exotic stems to quantify invasion (inside plots and along two 100 m transects outside the forest remnants).

- Variables and measures
  - Fragmentation: area of non-forest and edge density within a 2 km buffer; time since fragmentation (years since first oil palm planting).
  - Disturbance: number of large Dipterocarpaceae stems; average wood density of trees >10 cm DBH.
  - Soil characteristics: soil pH; available phosphorus (P) in the top 20 cm.
  - Propagule pressure: exotic richness and exotic abundance along external transects (two 100 m transects).
  - Native community metrics (alpha diversity, per size class and total): observed native genus richness; Faith’s phylogenetic diversity (PD).
  - Phylogenetic data: a filtered 303-genus phylogeny used to calculate PD; data cleaned to genus level where needed.
  - Exotics: richness and abundance of exotic genera/species along transects and within plots.

- Data preparation and processing
  - Variables centered and scaled to mean 0 and variance 1 before PLSPM; some variables transformed to improve normality (e.g., log10, sqrt, and ln+1).
  - Variable renaming and creation of a compact data frame (data_pls) for model input, including an edge density variable computed from edge and area within the 2 km buffer.
  - Separate dataframes created for each native component (total native community, adult trees, saplings, seedlings, ground vegetation) to test whether biotic resistance varies by native group.
  - Latent variable structure defined via inner model matrix and a path matrix; variables assigned to latent blocks (reflective vs. formative).

- Analytical approach and models
  - Primary method: partial least squares path modeling (PLS-PM) using the plspm R package.
  - Model setup
    - Full dataset model: Native community → Invasion (and tested in the opposite direction as a sensitivity analysis); total of 10 models (full data plus four native components, each with both directional specifications).
    - Data preparation and model specification follow Sanchez (2013) conventions for PLSPM, including model validity and reliability checks.
  - Model specification steps
    - Inner model: latent variables connected as per hypothesized relationships (Frag/Dist/Soil/Natives/Prop/Exotics, with Invasion as a latent outcome).
    - Outer model (blocks): assign measured variables to the corresponding latent variables; define reflective vs. formative indicators.
    - Final model refinement: stepwise removal of nonsignificant terms (P < 0.05) to arrive at a significant, parsimonious network.
  - Model evaluation
    - Measurement model reliability and validity: AVE > 0.50; standardized loadings > 0.70 (except one exception: native abundance in total native and ground vegetation models).
    - Internal consistency: Cronbach’s Alpha and composite reliability (Dillon-Goldstein’s rho) > 0.70 for each latent variable.
    - Discriminant validity: cross-loadings checked; Fornell-Larcker criterion; square roots of AVE exceed correlations with other latent variables.
    - Structural model: R2 values for endogenous latent variables (weak <0.30, moderate 0.30–0.60, substantial >0.60; with some variants in the literature).
    - Global fit: Goodness-of-Fit (GoF) index; higher GoF indicates better fit (no strict universal threshold; used in context of published work).
  - Uncertainty estimation
    - Two-sided P-values for standardized path coefficients obtained via 10,000 bootstrap resamples.
    - Site effects addressed by bootstrap sampling at the site level (since random effects could not be included in plspm’s standard implementation).

- Outputs and reproducibility
  - The code reproduces the results reported in Waddell et al. (2020a), including the final path diagrams and the statistical assessments of model reliability and structural relationships.
  - Final visualization: a simple plot of the final pathway (standardized coefficients) is produced (plot(pls2)).
  - Validation and quality assurance
    - Code and analyses have undergone peer review and were accepted for publication in Landscape Ecology (Waddell et al., 2020a).
    - Authors performed thorough checks for errors and documented the validation process.

- File contents and access
  - PLSPM_invasion.R: R script implementing the PLSPM analyses, data preparation, model specification, bootstrapping, and plotting.
  - Plot_measured_data.csv: plot-level data used to run PLSPM_invasion.R (data structure described in the document with fields for Site, Plot, Forest_type, geographic and environmental variables, diversity metrics, and invasion metrics).
  - Additional context: Data and methods are aligned with Waddell et al. (2020a) and point to Waddell et al. (2020b) for full vegetation data; the project references extensive methodological guidance from Sanchez (2013) on PLSPM.

- Study context and limitations
  - Study spans fragmentation gradients in Sabah with both oil palm-fragmented remnants and continuous forest comparisons.
  - Data are plot-level and genus-level for certain taxa due to identification challenges in tropical forests.
  - Bootstrap approach accounts for site-level clustering, but the modeling framework uses PLS-PM, which has specific assumptions about latent variable formation and measurement models as outlined in the validation criteria.

- References and sources
  - Key methodological and contextual references include Sanchez (2013), Sanchez & Trinchera (2012), Chin (1998), Fornell & Larcker (1981), and domain-specific sources on tropical forest structure, soil chemistry, and phylogenetic diversity (Faith 1992; Phylomatic; picante; BIOMASS; Global Wood Density Database; RSPO guidelines, etc.).
  - Primary study: Waddell et al. (2020a) Landscape Ecology; data release: Waddell et al. (2020b) NERC Environmental Information Data Centre.