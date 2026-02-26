# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia.

## Overview
- Dataset accompanying Banin LF, Raine EH et al. (2023) "The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests" (Philosophical Transactions of the Royal Society B).
- Contains plot-level data on forest structure, aboveground carbon density (ABC) and tree species richness from forest restoration sites in South and Southeast Asia.
- Timeframe: censuses conducted up to May 2021; compiled from published studies, grey literature, and data from co-authors.
- Scope: 11 sites where disturbance led to forest clearance or degradation; includes plots with active restoration (seedling planting) and natural regeneration (no planting); some sites provide old-growth reference plots and repeat measurements over time.
- Purpose: to support analysis of restoration outcomes and provide the code and data needed to reproduce analyses.

## What the dataset contains
- Data and code used for analyses in Banin et al. 2023.
- Data collation and analysis protocols align with the main text and electronic supplementary material of Banin et al. (2023).

## Files contained
- script_community_analyses.R
  - R script to run three community-level analyses and produce three figures/maps included in Banin et al. (2023) Figure 4.
- df_restoration_response_LRR.csv
  - Restoration response dataset.
  - Key fields: study, nr_site (naturally regenerating plots), a_site (actively restored plots), r_duration, d_duration, d_estimated, BA_r, BA_nr, d_r, d_nr, ABC_r, ABC_nr, plot_ha, np_nr, np_r, area_nr, area_r.
- df_basalarea_timeseries.csv
  - Basal area time series dataset.
  - Key fields: study, rest (active vs passive), id (plot identifier over time), rest_date, plot_area, tree_dens, basal_area, survey, time_since_rest, time_since_dist, n_plot.
- df_recovery_completeness.csv
  - Recovery completeness dataset including old-growth comparisons.
  - Key fields: study, rest, id, rest_date, plot_area, tree_dens, basal_area, ABC, survey, time_since_rest, time_since_dist, n_plot, BA_og, d_og, ABC_og.
- df_coords.csv
  - Site coordinates and area metrics.
  - Key fields: study, lat_d, lat_m, lat_s, lat_ns, lon_d, lon_m, lon_s, lon_e, area_a, area_nr.
- Supporting_info_community_analysis.docx
  - Details on data collation, assumptions, data collection and analysis methods as reported in Banin et al. (2023).

## Key variables and measures
- Structural metrics: basal area (BA; m2 per plot) for actively restored vs naturally regenerating plots; plot-level BA differences across restoration types and time.
- Biomass and carbon: aboveground carbon density (ABC; Mg C per ha) for restoration types and comparisons with old-growth references.
- Biodiversity: tree species richness (d_r, d_nr; number of tree species) within plots and restoration types.
- Temporal trajectory: time since restoration (r_duration) and time since disturbance (d_duration) to assess recovery dynamics.
- Spatial scale: plot-level data with per-plot and per-site aggregations; total area for restoration types (area_r, area_nr).
- Longitudinal aspect: repeated measures over time in df_basalarea_timeseries.csv and df_recovery_completeness.csv (id tracks plots across surveys).

## Geographic and temporal scope
- Regions: South and Southeast Asia.
- Sites: 11 sites included, focusing on areas where disturbance led to forest degradation or clearance.
- Temporal span: data up to May 2021, with multiple time points and potential old-growth references for comparison.

## Data provenance and protocols
- Data collated from published papers, grey literature, and inputs from co-authors.
- Followed protocols described in Banin, Raine et al. (2023) main text and electronic supplementary material; missing data addressed per Appendix 2 of the same publication.
- Documentation provides details on data collection methods, assumptions, and analysis approaches (see Supporting_info_community_analysis.docx).

## Data usage and reproducibility
- Includes complete analysis script and datasets to reproduce the three community-level analyses and associated figures/maps.
- Emphasizes transparent data sharing of underlying datasets and the code used for analyses, enabling replication of restoration outcome comparisons between active restoration and natural regeneration, as well as with old-growth references.

## Relevance for monitoring frameworks
- Provides standardized restoration metrics (BA, ABC, tree species richness) across restoration approaches and time since restoration, aiding policy evaluation and decision-making.
- Enables comparison of active vs natural restoration trajectories and assessment against old-growth benchmarks.
- Rich metadata and accompanying documentation support data governance, quality checks, and reproducibility—key considerations for monitoring frameworks.
- Highlights practical data challenges (metadata quality, data access, harmonization across sources) and the importance of clear protocols and open data practices for effective monitoring.