# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

- Objective: Compare structure, biomass and biodiversity between naturally regenerating forests and actively planted restoration plots across tropical and subtropical Asian forests; assess recovery relative to old-growth references.

- Data scope and sources:
  - Literature search up to May 15, 2021; screened 373 papers.
  - Included data from 13 landscapes (across South and Southeast Asia) with 451 plots totaling 91.6 ha.
  - Data supplemented by unpublished FOR-RESTOR collaboration data.
  - Plot histories cover 0–50 years since disturbance and 0–30 years since planting.

- Data elements captured:
  - Site condition, disturbance type and intensity, time since disturbance, time since planting, census date.
  - Restoration type (active planting vs natural regeneration) and forest structure metrics (basal area, above-ground carbon density) and tree biodiversity (tree species richness).

- Data extraction and processing:
  - Paired actively restored and naturally regenerating plots within studies that share similar time since disturbance and disturbance intensity.
  - Excluded plots where disturbance types were not comparable between treatment groups.
  - Disturbance categories defined (e.g., logging, agriculture, plantation, fire, mining, drainage); multiple logging strategies grouped together.
  - Site conditions categorized as Plantation, Forest, or Open.
  - Handling of incomplete census data: census date assumed to be two years prior to publication in two cases.
  - Exclusions: some papers removed to ensure comparability (e.g., natives planted into exotic plantations).

- Metrics and data structure:
  - Primary metrics: above-ground carbon density, basal area, and tree species richness.
  - Data prepared and summarized in supplementary tables (Tables 1–2 detail processing; Tables S4–S5 present study-level and plot-level data; Table S10 documents analyses).

- Analytical approaches:
  - Three analyses implemented to compare restoration outcomes:
    1) Actively restored vs naturally regenerating plot pairs using restoration response log-ratio for each metric; linear mixed-effects models with mean time since disturbance as fixed effect; study as random effect; area-weighted.
    2) Basal area change over time between restoration types, compared to old-growth references; linear mixed-effects model with restoration type and time since disturbance; plot as random effect; area-weighted.
    3) Recovery completeness relative to old-growth for each metric; log-response ratio with time since disturbance and restoration type as fixed effects; study as random factor; area-weighted.
  - Old-growth benchmarks included where available (seven studies with old-growth references).
  - Analyses conducted in R (versions 4.0.4 and 4.1.0).

- Software and reproducibility:
  - Analyses performed in R; results compiled into supplementary materials (S4, S5, S10).

- Outputs and datasets:
  - Community-level synthesis of actively restored vs natural regeneration plots across multiple landscapes.
  - Summary statistics and plot pairings documented; includes old-growth comparisons and restoration completeness assessments.

- Data quality, limitations and challenges:
  - Heterogeneity in time since disturbance, disturbance intensity, plot sizes and census timing across studies.
  - Some metrics limited to single time points or lacked complete data across all studies, reducing comparability for certain analyses.
  - Several datasets excluded to preserve comparability (e.g., certain native vs exotic planting cases; plots with incomparable disturbance histories).

- Relevance for environmental monitoring and policy:
  - Provides standardized, cross-study comparisons of forest structure, carbon storage and biodiversity under different restoration strategies.
  - Facilitates monitoring of carbon recovery trajectories and biodiversity outcomes in restoration programs.
  - Supports data-driven decision-making by enabling integration with monitoring portals and broader environmental health assessments.
  - Demonstrates best practices in data verification, quality assurance, cleaning, transformation and archiving for monitoring datasets.