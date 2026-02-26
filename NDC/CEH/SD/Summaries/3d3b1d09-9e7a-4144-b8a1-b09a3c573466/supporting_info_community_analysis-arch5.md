# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Scope and purpose
- Compiles plot-level data to compare forest structure, biomass/carbon density, and tree diversity across restoration approaches.
- Covers restoration sites in South and Southeast Asia, including 13 landscapes and 91.6 ha across 451 plots.
- Time span: disturbances from 0 to ~50 years; planting/treatment up to ~30 years before surveys.
- Aims to support understanding of how actively restored forests compare with naturally regenerating and old-growth reference forests.

## Data sources and provenance
- Derived from published literature and unpublished collaborators within the FOR-RESTOR network.
- Systematic search of Web of Science; 373 papers screened; 12 landscapes used from 15 studies plus 2 co-authors contributed data; plus one additional unpublished landscape.
- Excluded studies where comparability between treated and naturally regenerating plots was not met (e.g., inappropriate disturbances, topsoil addition, or incompatible metrics).

## Data content and variables
- Extracted variables:
  - Site condition, disturbance type, time since disturbance, time since planting, census date, restoration type.
  - Metrics: basal area, above-ground carbon density, and tree species richness.
- Plot pairings: actively restored vs naturally regenerating plots paired by similar disturbance timelines; oldest census used when multiple censuses existed.
- Site condition categories at planting: Plantation, Forest, Open.
- Disturbance categories: logging, agriculture, plantation, fire, mining, drainage, etc.
- Exclusions: certain papers removed due to non-comparability; some papers included for completeness in tables.

## Data structure and processing
- Table 1 documents data processing and assumptions (e.g., time-since disturbance vs. time-since planting, plot pairings, conversions).
- Time-related data handling:
  - Where data were missing, approximations used (e.g., census assumed two years before publication; time since disturbance equated to time since planting in some cases).
  - Above-ground carbon densities converted from biomass using 47% C content.
- Table 2 lists plot pairings and the specific restoration vs natural regeneration comparisons.
- Data prepared to enable community-level analyses across studies, with explicit notes on processing decisions.

## Analytical approach (as basis for data interpretation)
- Three analyses conducted using log-response ratios:
  1) Active restoration vs natural regeneration (restoration response) for basal area, above-ground carbon density, and tree species richness.
  2) Basal-area change over time comparing restoration types (Act. vs Nat. regen vs old-growth references) with mixed-effects modeling.
  3) Recovery completeness relative to old-growth references for the three metrics.
- Models include fixed effects (e.g., time since disturbance, restoration type) and random effects (study) with area weighting; some random-effects structures simplified due to convergence or data constraints.
- Analyses implemented in R (versions 4.0.4 and 4.1.0).

## Data quality, limitations, and caveats
- Heterogeneity across studies in plot sizes, census timing, and measurement methods.
- Incomplete data and selective reporting in some studies; several metrics had data gaps limiting cross-study comparisons.
- Potential pseudo-replication mitigated by careful plot-level pairing; in a few cases, multiple pairings used data from the same plots.
- Several studies excluded from certain analyses due to comparability concerns (e.g., enrichment with exotic materials, or non-equivalent disturbance histories).

## Data access, sharing, and governance
- Primary data are documented in Tables S4, S5, and S10 of the supporting information; full provenance linked to underlying publications.
- Data include detailed methodological metadata and transformation notes to ensure reproducibility.
- Recommendations for data sharing: preserve source citations, provide stable identifiers for plots where possible, include data dictionary, and maintain versioned updates as new data become available.

## Data management and stewardship recommendations
- Adopt a formal metadata schema to capture:
  - Plot identifiers, coordinates (where allowed), study origin, restoration type, disturbance history, time metrics, and measurement units.
  - Data processing steps and all transformations (e.g., biomass-to-carbon conversion factors, time approximations).
- Standardize units and variable definitions across the dataset (e.g., basal area in m2/ha, above-ground carbon in Mg C/ha, tree species richness as number of species per plot).
- Maintain a data dictionary and data provenance log linking each plot-level entry to its source publication or dataset.
- Implement data versioning and changelogs to track updates from new landscapes or studies.
- Ensure appropriate licensing and access controls, including clear usage rights for unpublished FOR-RESTOR data.
- Consider adding coordinate- and plot-level privacy considerations if sharing publicly, with alternatives (e.g., aggregated or de-identified data) as needed.
- Provide reproducible analysis scripts (R code) and a clear workflow so future curators can reproduce the three analyses (restoration response, basal-area change over time, recovery to old-growth).

## Relevance to Data Stewards
- Demonstrates end-to-end data curation across multiple studies, including extraction, pairing, transformation, and multi-metric analysis.
- Highlights the importance of transparent processing decisions and documentation for cross-study comparability.
- Illustrates handling of incomplete data and the need for robust metadata to enable discovery, reuse, and governance of complex, harmonized ecological datasets.