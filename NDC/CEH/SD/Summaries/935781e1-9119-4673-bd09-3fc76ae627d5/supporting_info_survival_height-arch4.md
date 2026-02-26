# The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- Scope and purpose
  - Compiles and analyzes planted tree survival and growth across restoration efforts in tropical/sub-tropical Asia (South and Southeast Asia), including peat swamp and mineral soils.
  - Aims to understand how planting outcomes relate to disturbance history, current site condition, and restoration practices to support data-driven restoration decisions.

- Data scope and scale
  - Seedling dataset includes 151 studies, 176 restoration sites, 2,477 cases (a species at a site with a given treatment and time).
  - 625 tree species (252 genera, 81 families) planted; taxonomic names verified against World Flora Online, Flora Malesiana, and Plants of the World Online.
  - Sites: 148 with survival data (207,224 trees) and 136 with height growth data (102,412 trees).
  - Habitat types: 108 sites on mineral soils; 68 tropical peat swamp forest sites.
  - Gap and diversity: median planting species per site is 3 (range 1–49); includes both monocultures and mixed plantings.

- Data sources and data sharing
  - Data drawn from published studies and grey/unpublished datasets via FOR-RESTOR network partners.
  - Wood density data compiled from global databases to test trait-based effects; shared under Creative Commons via the EIDC repository.
  - Climate and soil variables sourced from external global datasets (WorldClim; Harmonized World Soil Database) and are processed separately due to licensing.

- Data curation and classification
  - Seedling-focused: excluded greenhouse/nursery studies and studies lacking sufficient post-plant census data (minimum six months after planting).
  - Disturbance history categories before restoration: logging, agriculture, plantation, fire, mining, draining (peat swamp only).
  - Current site condition categories: plantation enrichment, forest enrichment, open degraded.
  - Restoration purpose categories (eight classifications) to capture aims (e.g., ecological restoration, forestry, experimental).
  - Restoration methods catalogued (seven categories): removal of competition, fertilisation, protection, shading, water regulation, soil preparation, and cases with no restoration beyond planting.

- Seedling planting data and metrics
  - Recorded: number of seedlings planted and monitored, planting density, planting species richness, seed sources, census times, survival outcomes, and growth measures (with height as the primary growth metric when possible).
  - Height at planting captured when available; otherwise approximated from early census data.
  - Replanting: noted in nine studies; to avoid bias, survival data from replanting beyond two months post-planting were excluded.

- Analytical approach and models
  - Mortality analyses
    - Time-standardized points (1, 2, 3, 4 years; 5–10 years; >10 years) with generalized linear mixed models (binomial, cloglog link).
    - Random effects: site, species, species-within-site; observation-level random effect for overdispersion.
    - Fixed effects: climatic variables (mean annual temperature, dry-season precipitation), forest type, forest condition, species richness, wood density; interaction terms for wood density with forest type/condition.
    - Model selection via information-theoretic approach (AIC) with multi-model inference; identification of consistently important variables (importance > 0.8).

  - Growth rate analyses (annual size-standardised height growth rates, AGR)
    - Analyzed for cases with four or more height censuses using linear, exponential, and Gompertz growth forms.
    - Selected best-fitting growth model by AIC; computed AGR at reference heights (100, 200, 300 cm) only when within data range.
    - AGRs log-transformed and modeled with linear mixed models; fixed effects similar to mortality models; random effects site and species as appropriate.
    - Uncertainty propagation through delta-method standard errors, simulations, and sensitivity analyses to assess impact on model outputs.

- Key data-derived variables and trait integration
  - Wood density used to explore functional-trait effects on survival and growth; values assigned at species, genus, or family level when species-level data were scarce; most data were phylogenetically conserved traits within tropical Asia.
  - Ancillary predictors extracted from global datasets for site-specific biophysical context (altitude, temperature, precipitation, dry-season metrics).

- Data access and governance
  - Datasets and wood density values available in the Environmental Information Data Centre (EIDC) under open licenses.
  - Some climate and soil datasets are not included in the repository due to licensing; users must process these separately to run accompanying analyses.

- Practical implications for data leaders
  - Demonstrates how to harmonize heterogeneous restoration studies into a coherent, scalable dataset.
  - Highlights the importance of rigorous taxonomic verification, clear taxonomy standards, and metadata practices to enable cross-study comparisons.
  - Shows value of cross-institution networks (FOR-RESTOR) in pooling data, sharing tools, and building a community of practice for restoration analytics.

- Limitations and challenges (as identified)
  - Fragmented data with varying reporting standards; gaps in site biophysical metadata; potential access barriers (paywalls) and data availability constraints.
  - Heterogeneity in disturbance histories, restoration aims, and planting designs requiring careful standardization and robust modeling approaches.

- Overall contribution
  - Provides a large, curated, and well-documented seedling dataset linking survival and growth outcomes to disturbance history, restoration methods, and site context across tropical and subtropical Asian forests.
  - Enables evidence-based assessment of restoration effectiveness and supports data-driven decision-making for policy and practice in forest restoration.