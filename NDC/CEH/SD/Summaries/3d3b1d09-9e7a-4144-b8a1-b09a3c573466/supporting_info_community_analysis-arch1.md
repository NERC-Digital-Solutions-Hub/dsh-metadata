# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

- This document accompanies Banin, Raine et al. 2023 and outlines methods for accessing, collating, and analysing plot-level data on forest structure, carbon density, and tree species richness from restoration sites in tropical and subtropical Asian forests.
- Objective: compare actively restored forests with naturally regenerating forests to understand differences in structure, biomass, and biodiversity, and to relate restoration status to old-growth references.

## Data scope and sources

- Coverage: 13 landscapes across South and Southeast Asia (0–50 years since disturbance; 0–30 years since planting).
- Dataset size: 91.6 hectares across 451 plots.
- Data origins: 12 landscapes from 15 published studies plus additional unpublished FOR-RESTORO data; supplemented by collaborators’ data.
- Timeframe of monitoring: plots surveyed at multiple time points; where multiple censuses exist, the longest time since disturbance used for comparisons.
- Plot conditions and restoration categories:
  - Disturbance prior to restoration categorized as logging, agriculture, plantation, fire, mining, or drainage.
  - Site conditions at planting categorized as Plantation, Forest, or Open.
  - Excluded studies: two papers where treated and control plots were not directly comparable; other exclusions noted in processing tables.

## Data extraction and processing

- Extracted fields: site condition, disturbance type, time since disturbance, time since planting, census date, restoration type, and metrics (basal area, above-ground carbon density, tree species richness).
- Plot pairing: actively restored plots paired with naturally regenerating plots within the same study based on similar time since disturbance and disturbance intensity.
- Handling inconsistencies:
  - Where census dates were missing, estimates were made (often census 2 years before publication).
  - Converted biomass to carbon using wood carbon content of 47% (Martin & Thomas 2011).
  - Excluded incomparably disturbed plots or restoration treatments (e.g., certain enrichment projects where comparability was poor).
- Tables and processing notes:
  - Table 1 documents processing steps and study-specific assumptions.
  - Table 2 documents plot-level data used for community-level analysis.
  - Tables S4, S5 detail studies and site data; Table S10 summarizes analyses.

## Metrics and variables

- Primary metrics: above-ground carbon density (Mg C ha−1), basal area (m2 per plot), and tree species richness (species per plot).
- Time-related variables: time since disturbance, time since planting.
- Additional context: disturbance intensity, plot area, and census timing to support pairings and weighting in analyses.

## Analytical approach

- Analyses conducted in three complementary ways:
  1) Active restoration vs natural regeneration (plot-level pairing):
     - Use restoration response: log-response ratio of Active/ Natural for each metric.
     - Linear mixed effects models with fixed effect: mean time since disturbance; random effect: study; weights: total area surveyed.
     - Purpose: test whether restoration response differs from zero for each metric.
  2) Basal area change over time:
     - Compare basal area change over time between actively restored and naturally regenerating plots, relative to old-growth plots.
     - Model: basal area ~ restoration type * time since disturbance + (time since disturbance | plot); weights: plot area.
     - Limitation: random effects structure limited by only three landscapes; convergence issues prevented a more nested random effect.
  3) Recovery completeness vs old-growth reference:
     - Use recovery completeness: log-response ratio of Restored vs Old Growth for each metric.
     - Model: recovery rate ~ time since disturbance + restoration type; random effect: study; weights: area.
- Statistical environment: analyses conducted in R (versions 4.0.4 and 4.1.0).
- Data synthesis: three separate meta-analyses; studies and plots enumerated in Tables S4, S5, and S10.

## Key datasets and references

- Primary data synthesis draws on:
  - Banin et al. 2023 (synthesis paper).
  - Core studies in the companion tables (Asanok et al. 2013; Wei et al. 2013; Long et al. 2021; Jayawardhane & Gunaratne 2020; Osuri et al. 2019; Inada et al. 2017; Meng et al. 2014; Ruslandi et al. 2017; Philipson et al. 2020; Gustafsson et al. 2016; Khopai & Elliot 2003; Kamo et al. 2002/2008; among others).
- Old-growth references and comparators included where available (Table S5).

## Data availability and reproducibility

- Data and metadata are organised into:
  - Table 1: Processing and assumptions for data preparation.
  - Table 2: Plot-level data used in community-level analyses.
  - Table S4: Summary of studies included in restoration vs natural regeneration analyses.
  - Table S5: Summary data for old-growth comparisons.
  - Table S10: Counts of studies and plots per analysis.
- Analyses and code were performed in R, enabling reproduction and extension of the meta-analyses.
- The dataset supports cross-study comparisons of actively restored vs naturally regenerating plots and their relation to old-growth references, with explicit attention to time since disturbance and disturbance intensity.

## Limitations and considerations for analysts

- Heterogeneity: substantial variation in time since disturbance, disturbance intensity, plot sizes, and monitoring methods across studies.
- Missing data: several plots or metrics had incomplete reporting; processing involved assumptions and approximations (documented in Table 1).
- Comparability: some restoration types (e.g., enrichment in plantations) were excluded due to comparability concerns; results depend on the quality of plot pairings and the availability of long-term data.
- Spatial scale and local detail: while the synthesis covers 13 landscapes, local-scale data gaps remain a challenge for precise inference at smaller administrative or landscape units.

## Implications for data-driven decision-making

- The compiled dataset enables quantitative comparisons of restoration strategies and their effectiveness in restoring carbon, structure, and biodiversity across tropical and subtropical Asian forests.
- Methods support the development of predictive insights about carbon recovery trajectories and biodiversity gains associated with active restoration versus natural regeneration, with reference to old-growth baselines.
- By emphasizing explicit data provenance, metadata, and reproducibility, the work aligns with analytical best practices for policy-relevant ecological assessments.