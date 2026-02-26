# The road to recovery: A synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- A dataset accompanying Banin LF, Raine EH et al. (2023) synthesizes planted-tree survival, size/growth, and area-based forest structure/diversity metrics in tropical and subtropical Asia to understand restoration outcomes and drivers.

## Dataset scope and content
- Studies and sites
  - 151 studies; 176 restoration sites across South and Southeast Asia; 221,199 planted trees.
  - 176 sites defined as unique locations and/or planting episodes; 2,477 cases (a species at a site, with a treatment, established at a time).
  - 108 sites on mineral soils; 68 sites on tropical peat swamp forests.
- Planting outcomes tracked
  - Survival data: 148 sites reported survival (207,224 trees).
  - Height growth data: 136 sites reported height growth (102,412 trees).
  - Taxonomic breadth: 625 species (252 genera; 81 families) were planted; species richness per site typically low (median 3; range 1–49).
  - Most common taxa: Shorea balangeran, Dyera polyphylla, Shorea leprosula, Shorea parvifolia, Shorea ovalis.
  - Most common genera: Shorea, Hopea, Dipterocarpus, Dryobalanops, Dyera.
- Data scale and scope
  - Included both mineral soil forests and peat swamp sites; includes both field plantings and embedded restoration treatments; excludes nurseries/greenhouses and natural regeneration-only studies.

## Data sources, search strategy, and scope
- Literature search
  - Systematic search of Web of Science up to May 15, 2021; 427 references screened; 108 final studies included after screening.
  - Supplemented with 43 additional published studies from peat swamp sites and 7 unpublished datasets from FOR-RESTOR partners.
- Data extraction and validation
  - Extracted seedling-level data for survival and growth; digitized from figures when necessary (WebPlotDigitiser); data quality cross-checked by multiple researchers.
  - Seedling replanting and time-since-planting harmonized for comparability.

## Planting data, variables, and site characteristics
- Disturbance history prior to restoration
  - Classified disturbances into six types: logging, agriculture, plantation, fire, mining, draining (peat-swamp only).
- Current site condition classifications
  - Plantation enrichment (native trees under non-native/monoculture plantations)
  - Forest enrichment (areas with some tree cover)
  - Open degraded (no canopy; understory may exist)
- Restoration purpose classifications
  - Eight categories (e.g., forestry, forestry and NTFP, ecological restoration, experimental, land reclamation, unspecified)
- Restoration treatments alongside planting (seven categories)
  - Removal of competition, fertilisation, protection, shading, water regulation, soil preparation, and cases with no extra restoration activities beyond planting
- Planting design and management
  - Species richness and planting density recorded where possible; when not reported, site-wide averages or assumptions used to standardize across cases
- Seedling attributes
  - Height at planting when available; otherwise treated as planting-age equivalent if within three months of planting
  - Seedling counts planted and monitored; methods to infer counts when not explicitly reported
- Peat swamp vs mineral soils
  - Clear separation in site type; many peat sites required special handling due to differing hydrology and ecology

## Functional traits and species data
- Wood density
  - Wood density data drawn from global databases; assigned at species (most common), genus, or family level as needed
  - Used to explore trait-based drivers of survival and growth; data shared under open license with the dataset
- Replanting and data integrity
  - Nine studies included seedling replanting; careful treatment to avoid bias in survival estimates (e.g., excluding replants beyond two months after initial planting for survival analyses)

## Mortality analyses
- Analytical approach
  - Mortality modeled at standardized time points: 1, 2, 3, 4 years; 5–10 years; >10 years after planting.
  - Generalized linear mixed effects models with binomial error and complementary log-log link (glmmTMB), with random effects for site, species, and species-within-site; observation-level random effect for overdispersion.
- Fixed effects and interactions
  - Environmental/biophysical: mean annual temperature, dry-season precipitation, elevation
  - Forest context: forest type, forest condition
  - Planting context: species richness of plantings; wood density
  - Interactions: wood density × forest type; wood density × forest condition
- Model selection and diagnostics
  - Information-theoretic model selection (AIC) across fixed-effect combinations; retained top models (ΔAIC < 2)
  - Variables with importance > 0.8 included in final models
  - Additional analyses: effects of planting density and initial height on mortality in open degraded vs. forest-enriched habitats
  - Diagnostics: DHARMa; marginal and conditional R2; intra-class correlations (ICC) for random effects

## Growth rate analyses
- Size-standardised growth (AGR)
  - Height growth tracked across diverse census intervals; growth modeled as function of time with linear, exponential, and Gompertz forms
  - Best-fitting model chosen by AIC; three reference heights used for AGR: 100 cm, 200 cm, 300 cm (within observed range)
  - Time to reach reference heights derived from model inverses; AGR computed as growth between adjacent height bands
- Statistical modeling
  - AGRs ln-transformed and modeled with linear mixed models
  - Fixed effects: same structure as mortality models (climate, forest type, forest condition, species richness, wood density; interactions)
  - Random effects: site and species (and sometimes species-within-site or site-specific terms)
  - Model selection via MuMIn; top models assessed for variable importance (>0.8)
- Uncertainty and sensitivity
  - Uncertainty in AGR estimated with delta method; inspected within-case vs between-case variance (ICC-like measure)
  - Simulation-based sensitivity analysis to account for AGR uncertainty in mixed-model outputs; results indicated similar estimates to models ignoring AGR uncertainty, suggesting limited impact of curve-fitting uncertainty on final inferences

## Data sharing, accessibility, and licensing
- Data repository
  - Datasets stored and made discoverable via the Environmental Information Data Centre (EIDC)
  - Wood density data licensed for open use; accompanying analysis code relies on external datasets (WorldClim, Harmonized World Soil Database) not embedded in the repository
- Documentation and reproducibility
  - Detailed methodological notes, tables (S1–S7), and supplementary materials referenced; scripts and analyses designed for replication and extension

## Key takeaways for analysts and decision-makers
- Large, multi-site dataset enables cross-regional comparison of planted-tree survival and growth in tropical Asia, incorporating peat swamp and mineral soils.
- Data capture a wide range of disturbance histories, restoration aims, planting schemes, species mixes, and management treatments, allowing exploration of context-dependent drivers of mortality and growth.
- Wood density and forest context (type and condition) are integral in modeling mortality and growth dynamics, with interactions indicating trait-by-environment effects.
- Analyses explicitly address temporal heterogeneity in census intervals and account for uncertainty in growth-rate estimation, enhancing robustness of inferences.
- Data sharing through EIDC, with transparent metadata and lineage, supports reproducibility and future meta-analyses or policy-relevant assessments.

## Limitations and challenges for interpretation
- Heterogeneity across studies in design, reporting, and temporal resolution; missing soil- and microhabitat details for some sites.
- Soil data (where used) rely on global databases with acknowledged misclassifications at peat sites; final analyses emphasize forest-type dichotomies rather than detailed edaphic properties.
- Some data rely on grey literature or unpublished datasets; variability in data quality and completeness across sources.
- Extrapolation risks when applying trait-based insights (wood density) across diverse species and sites with limited sample sizes for some taxa.