# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Scope and purpose
- Supporting information for Banin et al. 2023 synthesis on ecosystem restoration outcomes in tropical and subtropical Asian forests.
- Provides plot-level data to compare naturally regenerating forests, actively restored (planted) forests, and old-growth references.
- Data enable assessment of structure (basal area), carbon density, and tree species richness across restoration scenarios.

## Data collection and scope
- Literature search focused on plot-level data to compare natural regeneration and planted restoration within the same landscape over similar times.
- Web of Science search up to May 15, 2021; screened 373 papers.
- Included data from 13 landscapes in total: data from 12 landscapes extracted from 15 studies, plus data from FOR-RESTOR collaborators (unpublished landscape), totaling 451 plots across 91.6 ha.
- Plots surveyed 0 to 50 years since disturbance and 0 to 30 years since planting.

## Data extraction and harmonization
- Extracted: site condition, disturbance type, time since disturbance, time since planting, census date, restoration type, and metrics (basal area, above-ground carbon density, tree species richness).
- Pairing of actively restored vs naturally regenerating plots based on similar time since disturbance and disturbance intensity.
- Classified pre-restoration disturbance into categories: logging, agriculture, plantation, fire, mining, drainage.
- Distinct site-condition categories at planting: Plantation, Forest, Open.
- Excluded certain studies where comparability was not achievable (e.g., native trees planted into exotic plantations) and any plots with incomparable disturbance histories.
- In some papers, census dates were missing; approximations were used (e.g., census two years before publication).

## Data processing and assumptions
- Detailed processing and assumptions documented (Tables 1 and 2 in the supplement) to prepare data for community-level analyses, including:
  - Time-since-disturbance vs. time-since-planting pairings.
  - Aggregation of multiple plots within a study when disturbance and restoration time were aligned.
  - Handling of varying plot sizes and census timings.
- Specific study-level decisions summarized in Table 1 (data preparation and assumptions) and Table 2 (plot-level data groupings).

## Analytical approaches
- Three main analyses conducted using the compiled data:
  1) Active restoration vs natural regeneration (restoration response)
     - Metric: log-response ratio of Active/Natural for each variable (above-ground carbon density, basal area, tree species richness).
     - Model: linear mixed-effects with mean time since disturbance as a fixed effect; study as a random factor; weighted by total area surveyed.
  2) Basal-area change over time
     - Compare change in basal area over time between restoration types against old-growth references.
     - Model: basal_area ~ restoration_type * time_since_disturbance + (time_since_disturbance|plot); weights by plot area.
     - Note: data limited to three landscapes; convergence issues prevented full random-effect nesting.
  3) Recovery completeness relative to old growth
     - Metric: log-response ratio of Restored/Natural vs Old Growth (recovery completeness) for each variable.
     - Model: recovery_complete ~ time_since_disturbance + restoration_type + (study as random factor); weighted by restored plot area.
- Analyses implemented in R (versions 4.0.4 and 4.1.0).

## Data structure and contents
- Metrics examined: basal area (m2 per plot), above-ground carbon density (Mg C ha-1), and tree species richness (plots).
- Landscapes include diverse site conditions: forested remnants, plantations, open areas, and various disturbance histories.
- Data tables (S4, S5, S10) provide study-level and plot-level summaries, with extensive documentation of which studies and plots contributed to each analysis.

## Data accessibility and supplementary materials
- Supplementary materials provide:
  - Table S4: Studies included in the restoration vs natural regeneration analyses.
  - Table S5: Study and plot-level data summaries for active restoration, natural regeneration, and old-growth references.
  - Table S10: Number of studies and plots per analysis, across categories (e.g., basal area, species richness, above-ground carbon density).
- References for the included studies span multiple datasets and restoration contexts (e.g., Philipson et al. 2020; Osuri et al. 2019; Inada et al. 2017; Wei et al. 2013; etc.).

## Software and reproducibility
- Analyses conducted in R; explicit versions cited (4.0.4 and 4.1.0) to support reproducibility.

## Limitations and considerations
- Variability across studies in time since disturbance, disturbance intensity, restoration duration, plot sizes, and census timing.
- Some data are missing or approximated (census dates, old-growth references) and were handled with documented assumptions.
- Only a subset of studies allowed multiple time-point comparisons; some analyses restricted by data availability (e.g., basal area change over time limited to three landscapes).
- Exclusion of certain datasets where comparability could not be established may bias broader inferences about restoration outcomes.