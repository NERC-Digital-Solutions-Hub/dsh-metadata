# Supporting documentation for R code to reproduce analyses of exotic plant invasion in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Purpose and scope
- Provides supporting information to reproduce analyses in Waddell et al. 2020a using PLSPM_invasion.R and Plot_measured_data.csv.
- Investigates relative influence of fragmentation, forest disturbance, propagule pressure, soil characteristics, and native community composition on exotic plant invasions in fragmented (oil palm–surrounded) versus continuous forest sites in Sabah, Malaysian Borneo.
- Tests both directions of the native community–invasion relationship (total and component-specific native communities).

## Study design and data sources
- 47 plots across 17 sites in Sabah (July–October 2017).
- Study design includes fragmented forest remnants in RSPO-certified oil palm landscapes (n=13 sites) and continuous, extensive logged/unlogged forest (n=4 sites).
- Nested plot sampling by size class:
  - C1: trees ≥25 cm DBH (adult trees)
  - C2: trees 10–25 cm DBH (tree saplings)
  - C3: tree saplings 2–10 cm DBH
  - Q: tree seedlings and ground vegetation in eight 1x1 m quadrats
- Exotic flora surveyed along two 100 m transects outside remnants (outside richness and abundance).

## Data and variables
- Data sources:
  - Plot_measured_data.csv: plot-level measurements for analysis.
  - PLSPM_invasion.R: R script used for analyses.
  - Full vegetation data: referenced in Waddell et al. 2020b.
- Key variable groups (Table 1 in the document):
  - Fragmentation: area of non-forest in 2 km; area in 2 km buffer; edge density; fragmentation age.
  - Disturbance: number of large dipterocarps; average wood density.
  - Soil characteristics: soil pH; available phosphorus (P).
  - Propagule pressure: exotic richness and exotic abundance outside the remnant.
  - Native community metrics (by size class and total): richness, abundance, and phylogenetic diversity (Faith's PD).
  - Exotics: richness and abundance (for context within plots).
- Transformations and data prep:
  - log10, natural log + 1, and sqrt transformations applied where appropriate.
  - Some variables multiplied by -1 to align latent variable interpretation.
  - Edge density calculated as Edge.in.2km.buffer / Area.in.2km.buffer.
  - All variables renamed to shorter object names for data frames (e.g., Fragmentation.age → Age).
- Data frame structure used for modeling:
  - data_pls <- data.frame('Site', 'Plot', 'Non.forest', 'Edge.density', 'Age', 'Dips', 'WD', 'pH', 'Avail.P', 'Total.richness', 'Total.PD', 'Outside.rich', 'Outside.abun', 'Exotic.abundance', 'Exotic.richness').

## Analysis workflow
- Modeling approach:
  - Partial Least Squares Path Modeling (PLS-PM) using the plspm R package.
  - Full model: latent variables for fragmentation, disturbance, soil, natives, propagule pressure, and exotics; two directions tested: Native community → Invasion and Invasion → Native community.
  - Four additional models: native adults, natives (saplings), natives (seedlings), natives (ground vegetation) tested separately.
- Model specification and execution:
  - Inner model matrix defines latent-variable connections; path matrix created and blocks assigned to measured variables; latent constructs specified as reflective or formative.
  - Models fitted on full dataset and then simplified by removing non-significant terms (P < 0.05) in a stepwise fashion.
  - Final outputs include a simple plot of the final pathway with standardized path coefficients.
- Model assessment and validation:
  - Measurement model reliability/validity:
    - Convergent validity: AVE > 0.50.
    - Indicator reliability: standardized loadings > 0.70 (with noted exception for native abundance in some models).
    - Internal consistency: Cronbach’s alpha and composite reliability > 0.70.
    - Discriminant validity: assessed via cross-loadings and Fornell-Larcker criterion (sqrt(AVE) greater than inter-construct correlations).
  - Structural model: assessed via R2 for endogenous latent variables and Goodness-of-Fit (GoF).
  - Statistical significance of path coefficients obtained via 10,000 bootstrap iterations; bootstrap samples drawn at the site level to account for the lack of a random effect in plspm.
- Reproducibility and validation:
  - Code has undergone peer review and is reported as accepted in Landscape Ecology (Waddell et al. 2020a); authors validated calculations and checked for errors.

## Data structure and quality control
- Study design details:
  - 47 plots across 17 sites; fragmentation gradient includes RSPO oil palm–surrounded remnants and continuous forest tracts.
  - Sampling paraphernalia includes 0.28 ha per site plot areas, nested size-class plots, and transects for exotics.
- Quality control measures:
  - Standardized field protocols; same observers conducted field surveys.
  - Data checked for errors; voucher specimens and botanical verification used for species identifications.
- Data provenance:
  - Fragmentation metrics derived from drone imagery (May–Nov 2016) for 2 km buffers.
  - Habitat and landscape variables calculated using R packages such as rgeos and raster; wood density derived from BIOMASS package using Global Wood Density Database.
  - Phylogenetic diversity calculated with Phylomatic and picante packages; phylogeny rooted with dated nodes.

## Reproducibility, data sharing, and references
- Data and code intended for download/reuse:
  - Plot_measured_data.csv and PLSPM_invasion.R accompany the study.
  - Full vegetation data described in Waddell et al. 2020b.
- Outputs align with results presented in Waddell et al. 2020a (Landscape Ecology).
- Methodological references and tools cited (PLS-PM methodology, bootstrap, phylogenetic analyses, soil chemistry methods, etc.) to support reproducibility.

## Data stewardship implications
- Provenance, context, and methodological metadata are thoroughly documented to support data reuse and audit trails.
- Clear variable definitions, transformations, and data processing steps enable consistent data governance and interoperability.
- The dataset structure and accompanying script provide a transparent workflow for replication, validation, and potential extension to similar ecological invasion studies.