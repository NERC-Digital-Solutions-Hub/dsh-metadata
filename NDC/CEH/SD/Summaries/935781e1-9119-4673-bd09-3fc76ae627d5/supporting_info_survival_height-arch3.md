# The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- Purpose and scope
  - A dataset accompanying Banin LF et al. 2023 to evaluate planted-tree survival and growth in tropical/sub-tropical Asian forests and inform policy decisions on monitoring approaches.
  - Geographic focus: South and Southeast Asia; habitat types include mineral soils and tropical peat swamp forests.
  - Scope of data: 151 studies, 176 restoration sites, 2,477 cases (a species at a site with a treatment), 625 species (252 genera; 81 families); 108 mineral-soil sites and 68 peat-swamp sites.
  - Outputs include survival data (for 148 sites, 207,224 trees) and height growth data (136 sites, 102,412 trees); median site richness is low (typically 1–3 species per site).

- Data sources and coverage
  - Systematic literature search up to May 15, 2021 using Web of Science; inclusion of regional/non-ISI journals; supplement with peat-swamp studies and unpublished grey literature via FOR-RESTOR partners.
  - Seedling dataset augmented with 43 peat-swamp studies and 7 grey datasets; includes data from 176 restoration sites and 221,199 planted trees in total.
  - Excludes studies focused only on natural regeneration, nurseries/greenhouses, or final census dates less than six months after planting.
  - Data licensing: wood density trait data released under CC license; broader datasets housed in the Environmental Information Data Centre (EIDC) with some climate/soil data requiring separate access/download due to licensing.

- Planting data and variables
  - Planting cases: survival (counts/proportions at census intervals) and growth (height, diameter, biomass) with time since planting; cases grouped by site, species, and treatment; replication handled to create comparable cases.
  - Disturbance history prior to restoration: six categories (logging, agriculture, plantation, fire, mining, draining; the last applies to peat swamp forests).
  - Current site condition categories: plantation enrichment, forest enrichment, open degraded (sites can span multiple conditions).
  - Restoration purpose classifications (Table S2 in the supplement): ranging from forestry/commercial to ecological restoration, experimental, land reclamation, and unspecified.
  - Restoration treatments alongside planting (Table S3): removal of competition, fertilisation, protection, shading, water regulation, soil preparation; many cases reported no additional restoration beyond planting.
  - Species and planting design: up to 625 species; if unspecified, treated as mixed planting; nurse plants and canopy considerations were used to classify site types (plantation enrichment vs open degraded).
  - Seedling traits: wood density from global databases (World Flora Online/Flora Malesiana; genus/family-level data when species-level density not available); data allow trait-based analyses of growth/survival.
  - Seedling planting metrics: number planted and monitored; planting density; height at planting; replanting events (nine studies replanted; mortality data treated with censoring where appropriate).

- Biophysical and climatic context
  - Biophysical data extracted from global datasets for each site: WorldClim (2.5-minute resolution, 1970–2000 means) for elevation, mean annual temperature, and precipitation; dry-season precipitation used due to high correlation with total annual precipitation.
  - Soil classification distinguished as mineral soil vs peat swamp forest (Harmonized World Soil Database); soil properties not used directly in analyses due to misclassification issues at peat sites.
  - Data integration relies on GIS-processed climate/soil data; licensing restricts reuse within the repository, but the analysis code handles these inputs.

- Growth and mortality analyses: methods and modeling
  - Mortality analysis
    - Time points standardized to six intervals: about 1, 2, 3, 4 years; 5–10 years; and >10 years after planting.
    - Generalized linear mixed models (GLMMs) with binomial error and complementary log-log link; random effects for site, species, and site-species; observation-level random effect for overdispersion.
    - Fixed effects include: mean annual temperature, dry-season precipitation, elevation; forest type; forest condition; species richness of planting; wood density; interactions between wood density and forest type/condition.
    - Model selection via information-theoretic approach (MuMIn dredge); variables with importance >0.8 included in final model; model diagnostics with DHARMa; marginal and conditional R2 reported; ICC used to assess random effects.
    - Additional analyses tested planting density and mean height at planting on mortality at 1–2 years in open degraded and forest-enriched habitats.

  - Growth rate analysis (AGR)
    - Growth measured as annual size-standardised growth rate (AGR) to account for size-dependence; analyzes cases with four or more height censuses using linear, exponential, and Gompertz growth forms.
    - Model selection via AIC; AGRs computed at reference heights of 100, 200, and 300 cm, within observed height ranges; time-to-reach height derived from inverse growth functions to calculate AGR.
    - Linear mixed models (ln-transformed AGR) with fixed effects mirroring mortality models (climate, forest type, forest condition, planting diversity, wood density) and random effects (site and species as appropriate).
    - Uncertainty propagation through simulation and delta-method standard errors; assessment of within- vs between-combination uncertainty (ICC-like metric); sensitivity analyses to evaluate impact of AGR uncertainty on model results.

- Tools, replication, and data handling
  - Data extraction and verification: numerical data captured from papers; figures digitized with WebPlotDigitizer; cross-checks by multiple researchers.
  - Growth and mortality analyses implemented in R:
    - Mortality: glmmTMB (binomial, cloglog link); model selection with MuMIn; diagnostics with DHARMa; marginal effects with ggeffects.
    - Growth: lme4 for linear mixed models; model selection with MuMIn; uncertainty propagated via simulation.
  - Data structure and sharing
    - Output comprises site-species-treatment units (cases) with associated measurements (survival counts, heights, census timings, planting and nursery metadata, disturbance history, restoration methods, species richness, wood density).
    - Data and wood density trait values are available in the EIDC under Creative Commons licensing; climate/soil inputs require separate access due to licensing.

- Practical implications for monitoring frameworks
  - Demonstrates how to harmonize heterogeneous restoration datasets across multiple sites and years into standardized mortality and growth metrics.
  - Highlights the importance of: consistent time-point definitions, metadata on disturbance history and restoration methods, and trait data (wood density) for trait-mediated analyses.
  - Provides a model-based approach to attribute variation in survival and growth to environmental context, site condition, and management actions (e.g., competition removal, fertilisation, protection).
  - Emphasizes handling of data gaps and uncertainties, including data licensing constraints and cross-site comparability, through standardized methods and uncertainty propagation.

- Challenges and data governance insights
  - Key barriers identified for monitoring frameworks:
    - Lack of data and data of sufficient quality; inconsistent metadata; data silos within/between organizations.
    data-sharing barriers due to openness requirements; timeliness of access; metadata gaps; data transformation burdens.
  Emphasizes the need for robust data governance, metadata standards, and open, interoperable datasets to support policy evaluation and decision-making.

- Related materials and references
  - Main publication: Banin LF, Raine EH et al. 2023. The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.
  - Data and trait sources: WorldClim, Harmonised World Soil Database, World Flora Online, Flora Malesiana, Plants of the World Online, and the global wood density database.
  - Analytical tools: glmmTMB, MuMIn, DHARMa, ggeffects; WebPlotDigitizer; BIOMASS R package for biomass-related traits.