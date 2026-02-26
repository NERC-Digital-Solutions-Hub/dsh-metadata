# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- Synthesizes plot-level data to compare actively restored forests with naturally regenerating forests across 13 landscapes in tropical and subtropical Asia.
- Data originate from published studies and unpublished FOR-RESTOR collaborators, totaling 451 plots over 91.6 hectares.
- Plots span 0 to 50 years since disturbance and 0 to 30 years since planting.
- Focus metrics: basal area, above-ground carbon density, and tree species richness.

## Data Collected and Metadata
- Site information
  - Site condition at planting (Plantation, Forest, Open)
  - Disturbance type prior to restoration (logging, agriculture, plantation, fire, mining, drainage)
  - Time-related variables: time since disturbance, time since planting, census date (often approximated)
- Plot-level metrics
  - Basal area (m² per plot)
  - Above-ground carbon density (Mg C ha⁻¹)
  - Tree species richness (number of species per plot)
- Data sources
  - Published studies identified via Web of Science search
  - Unpublished data from collaborators in the FOR-RESTOR network
- Data scope
  - 91.6 ha across 451 plots
  - Plots surveyed 0–50 years post-disturbance; 0–30 years post-planting

## Data Processing and Harmonization
- Plot pairings
  - Actively restored plots paired with naturally regenerating plots within the same study based on similar time since disturbance
  - Exclusions applied where disturbance could not be meaningfully matched between paired plots
- Disturbance classification
  - Disturbances consolidated into categories (logging, agriculture, plantation, fire, mining, drainage)
  - Different logging strategies grouped as a single disturbance type
- Data adjustments and assumptions
  - When census timing was unclear, estimated census timing as two years before publication
  - Time since disturbance sometimes equated with time since planting when not specified
  - Several studies excluded if restoration and natural plots were not directly comparable
  - Two papers with native seedlings planted into exotic plantations excluded from certain analyses but listed in tables
- Documentation
  - Table 1 documents processing and assumptions per study
  - Table 2 lists plot-level data used in community-level analyses
  - Table S4 and Table S5 provide study-level summaries and mean values (with some entries missing)

## Analysis Approach
- Three main analyses (all using log-response ratios to standardize across studies)
  1) Actively restored vs naturally regenerating plot pairs
     - Restoration response m = ln(Active restoration_m / Natural regeneration_m)
     - Linear mixed effects models with mean time since disturbance as a fixed effect; study as a random effect; weights by total plot area
  2) Basal area change over time
     - Basal area ~ restoration type * time since disturbance + (time since disturbance | plot)
     - Weights by plot area; limited to datasets with temporal data
  3) Recovery completeness relative to old-growth reference
     - Recovery completeness m = ln(Restored_m / Old growth_m)
     - Linear mixed effects models with time since disturbance and restoration type as fixed effects; study as a random factor; area-weighted
- Metrics and data usage
  - Analyses performed for above-ground carbon density, basal area, and tree species richness
  - Some metrics had data from multiple censuses or only single time points, affecting inclusion in certain analyses
- Tools
  - All analyses conducted in R (versions 4.0.4 and 4.1.0)

## Data Provenance and Access
- Core reference dataset comes from Banin et al. 2023 (The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and subtropical Asian forests).
- Supporting materials and tables (Tables S4, S5, S10) provide detailed study-level data and methods.
- Key related sources include:
  - Science (Philipson et al. 2020) on active restoration accelerating carbon recovery
  - Gustafsson et al. (2016); Osuri et al. (2019); Inada et al. (2017); Hayward et al. (2021); and others
- Data are documented in supplementary material with explicit processing notes and exclusions to ensure transparency and replicability

## Data Quality and Gaps
- Heterogeneity across studies in plot size, census timing, disturbance history, and restoration practices
- Incomplete or approximated temporal data (e.g., census dates approximated; time since disturbance vs. planting not consistently reported)
- Occasional missing metrics (some studies report only subsets of basal area, carbon density, or species richness)
- Exclusions applied where comparability between active restoration and natural regeneration was not feasible
- Old-growth reference data available for several studies, but not all; some old-growth metrics are missing or not reported consistently

## Implications for Data Leaders
- Demonstrates a scalable approach to compiling, harmonizing, and analyzing cross-study ecological data to assess restoration outcomes
- Highlights the importance of:
  - Clear metadata standards (disturbance type, time since disturbance, time since planting, census timing)
  - Consistent measurement units and definitions for structure, carbon, and biodiversity metrics
  - Transparent documentation of processing decisions, assumptions, and exclusions
  - Collaborative data sharing (including unpublished datasets) to expand landscape coverage
- Useful blueprint for building a broader data architecture that integrates plot-level restoration data across networks, improves comparability, and supports evidence-based decision-making for restoration strategy and policy.