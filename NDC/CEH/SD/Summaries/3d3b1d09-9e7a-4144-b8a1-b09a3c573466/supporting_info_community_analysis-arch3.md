# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

- This document provides the supporting information for a dataset accompanying Banin, Raine et al. (2023) synthesizing restoration outcomes in tropical and subtropical Asian forests.
- Scope: 13 landscapes across multiple countries in South and Southeast Asia; total restored forest area of 91.6 ha across 451 plots; plots span 0 to 50 years since disturbance and 0 to 30 years since planting.
- Core metrics: plot-level measures of forest structure (basal area), above-ground carbon density, and tree species richness.
- Data sources: published studies identified via a Web of Science literature search and unpublished FOR-RESTOR data from collaborators; inclusion focused on plots with both natural regeneration and active restoration within the same landscape and surveyed at least once for the target metrics.
- Purpose for monitoring frameworks: standardize metrics and comparisons across studies to inform policy-relevant assessments of restoration effectiveness and carbon outcomes.

## Data collection and scope

- Literature search and data sources:
  - Web of Science query using keywords related to tree planting, restoration, and tropical forests, complemented by prior meta-analyses.
  - Up to May 15, 2021, with no publication-year restrictions.
  - Included unpublished data from FOR-RESTOR collaborators to broaden landscape coverage.
- Landscape and dataset characteristics:
  - 13 landscapes, 12 published studies plus one unpublished landscape provided by co-authors.
  - Combined data cover 451 plots totaling 91.6 ha of restored forest.
  - Monitoring coverage from 0 to 50 years since disturbance and 0 to 30 years since planting.
- Data extracted from studies:
  - Site condition, disturbance type, time since disturbance, time since planting, census date, restoration type, and community metrics (basal area, above-ground carbon density, tree species richness).

## Data extraction and processing

- Plot pairings and metrics:
  - Actively restored plots and naturally regenerating plots were paired within studies based on similar time since disturbance and disturbance intensity to enable fair comparisons.
  - When multiple censuses existed, the longest time since disturbance was used to maximize comparability; pseudo-replication was avoided by not reusing plots across pairings.
- Disturbance and site-condition classifications:
  - Disturbance classes included logging (clear fell, selective), agriculture, plantation, fire, mining, drainage.
  - Site conditions categorized as Plantation, Forest, or Open (with various understory types included in Open).
- Data inclusion/exclusion:
  - Excluded two papers where restoration plots were not directly comparable to natural regeneration (native seedlings into exotic plantations) despite otherwise fitting criteria.
  - Some papers required processing assumptions (e.g., time since disturbance vs. time since planting) and were documented in detail in Table 1 (Processing/assumptions) and Table 2 (Plot-level data aggregation).
- Data preparation notes:
  - Time since disturbance and time since planting were harmonized with study-specific notes (e.g., when exact census dates were missing, census dates were approximated relative to publication date).
  - Biomass to carbon conversions were applied where needed (e.g., using 47% carbon content for wood).

## Data analysis and metrics

- Analyses conducted:
  - Three primary analyses using the three metrics: above-ground carbon density, basal area, and tree species richness.
  - Analysis 1: Actively restored vs. naturally regenerating plot pairs using restoration response (log-response ratio) with linear mixed-effects models; study as a random effect; mean time since disturbance as a fixed effect; weighted by total surveyed plot area.
  - Analysis 2: Basal area change over time comparing actively restored and naturally regenerating plots to old-growth references; linear mixed-effects model with restoration type and time since disturbance as fixed effects and plot as a random effect (note: only three landscapes supported time-series change for this metric).
  - Analysis 3: Recovery completeness relative to old-growth references using a log-response ratio (recovery completeness) across the three metrics; linear mixed-effects model with study as a random effect and time since disturbance and restoration type as fixed effects; weighted by area.
- Data handling and robustness:
  - Longest available time-since-disturbance used for each plot pairing when multiple censuses existed.
  - Avoided overlapping use of plots across multiple pairings to reduce pseudo-replication.
  - Analyses performed in R (versions 4.0.4 and 4.1.0).
- Data tables and transparency:
  - Table S4 lists studies included in the community-level analyses and associated study-level notes.
  - Table S5 provides summary values (means and standard errors) for each study’s active restoration, natural regeneration, and old-growth references.
  - Table S10 reports the number of studies and plots used for each analysis and metric.

## Data governance and metadata considerations for monitoring frameworks

- Standardization and comparability:
  - Uses common metrics (basal area, above-ground carbon density, tree species richness) and a uniform effect size (log-response ratio) to harmonize disparate study methodologies.
  - Explicit plot-pairing criteria and time-matching approach enhance comparability across landscapes.
- Metadata and provenance:
  - Detailed processing notes and assumptions are documented (Table 1) to ensure reproducibility and auditability of the data synthesis.
  - Clear documentation of site condition classifications, disturbance types, and restoration categories supports metadata transparency.
- Data sharing and governance implications:
  - Inclusion of unpublished data demonstrates value of data sharing for comprehensive monitoring, while maintaining clear methodological traceability.
  - The approach highlights how to handle incomplete data (approximations for census timing, conversions) transparently, which is crucial for governance and policy interpretation.
- Limitations relevant for monitoring design:
  - Heterogeneity in plot sizes, census timing, and measurement methods across studies; some metrics were not available for all plots.
  - Some old-growth comparisons were incomplete or not measured across all landscapes, limiting the comparability of recovery completeness for certain metrics.
  - Time-since-disturbance and time-since-planting harmonization required study-specific assumptions, which should be captured in metadata when applying similar frameworks elsewhere.

## Practical implications and takeaways for monitoring framework authors

- Core lesson: to enable cross-study monitoring, researchers should target a consistent set of metrics (carbon density, basal area, species richness) and implement standardized effect-size approaches (log-response ratios) with appropriate random effects (e.g., study) and area-weighting.
- Robust data governance practices:
  - Maintain thorough processing notes and assumptions (as in Table 1) to ensure reproducibility when aggregating diverse datasets.
  - Document publication-status of data (published vs. unpublished) and provenance to enhance transparency and trust.
- Design considerations for monitoring programs:
  - Ensure plots have comparable disturbance histories or are carefully paired to minimize bias.
  - Collect comprehensive metadata (disturbance type, time since disturbance, time since restoration, census dates) to support future re-analyses.
  - Include old-growth reference data where possible to assess recovery completeness and inform targets for restoration policy.