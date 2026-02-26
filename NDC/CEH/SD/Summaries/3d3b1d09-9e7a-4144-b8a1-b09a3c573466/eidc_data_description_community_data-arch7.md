# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- Dataset accompanying Banin LF et al. 2023: The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests.
- Contains plot-level data on forest structure, aboveground carbon density (biomass), and tree species richness from restoration sites in South and Southeast Asia.
- Covers both active restoration (planting) and natural regeneration (no planting), with some old-growth reference plots and repeat measures over time.
- Data collected up to May 2021 from 11 sites, sourced from published studies, grey literature, and co-authors.
- Includes the R code used for analyses and to generate figures/maps reported in the associated paper.

## What’s in the dataset
- Structure, biomass (carbon density), and biodiversity (tree species richness) data at the plot level from forest restoration sites.
- Comparison between actively restored and naturally regenerating plots, plus old-growth references for context.
- Time-series elements: repeated measures over time for some plots.
- Accompanying code used to perform community-level analyses and produce figures and a map.

## Data content and file descriptions
- script_community_analyses.R: R script to run three community-level analyses and produce three graphs and a map (as in Figure 4 of the paper).
- df_restoration_response_LRR.csv: Dataset for restoration response analysis; includes per-plot metrics and area summaries for active vs natural restoration.
  - Key fields: study, nr_site (natural regeneration), a_site (active restoration), r_duration, d_duration, d_estimated, BA_r, BA_nr, d_r, d_nr, ABC_r, ABC_nr, plot_ha, np_nr, np_r, area_nr, area_r.
- df_basalarea_timeseries.csv: Dataset for basal area time-series analysis.
  - Key fields: study, rest (active or passive), id, rest_date, plot_area, tree_dens, basal_area, survey, time_since_rest, time_since_dist, n_plot.
- df_recovery_completeness.csv: Dataset for recovery completeness analysis, including old-growth reference data.
  - Key fields: study, rest, id, rest_date, plot_area, tree_dens, basal_area, ABC, survey, time_since_rest, time_since_dist, n_plot, BA_og, d_og, ABC_og.
- df_coords.csv: Site coordinates and spatial context.
  - Key fields: study, lat_d, lat_m, lat_s, lat_ns, lon_d, lon_m, lon_s, lon_e, area_a, area_nr.
- Supporting_info_community_analysis.docx: Documentation on data collation, methods, and assumptions from the included papers and Banin et al. (2023).

## Variables and data points
- Structural and composition metrics per plot:
  - Basal area (BA) for actively restored vs naturally regenerating plots (m2 per plot).
  - Tree species diversity (d_r, d_nr), i.e., number of tree species per plot.
  - Aboveground carbon density (ABC) per plot (Mg C/ha).
  - Plot area (plot_ha) and counts of plots (np_nr, np_r).
- Temporal and restoration context:
  - Time since restoration (r_duration) and time since disturbance (d_duration).
  - Time markers for time-series analyses (survey year, time_since_rest, time_since_dist).
- Spatial context:
  - Site coordinates provided in degrees, minutes, seconds with hemispheric indicators.
  - Area metrics for actively restored vs naturally regenerating plot sets (area_r, area_nr).
- Old-growth comparison data (for recovery completeness analyses):
  - Basal area (BA_og) and species richness (d_og) for old-growth plots.
  - ABC for old-growth plots (ABC_og).

## Spatial and temporal coverage
- Geographic scope: Restoration sites across South and Southeast Asia.
- Temporal coverage: Plot-level data up to May 2021, with some repeat measures over time.

## Data provenance and quality
- Protocols followed as described in the main text and electronic supplementary material of Banin, Raine et al. (2023).
- Data collated from multiple sources: published studies, grey literature, and co-authors.
- Includes documentation on data collection, collation decisions, and analysis methods.

## How this supports GIS-focused work
- GIS-ready attributes for mapping: BA, ABC, species richness, plot size, restoration type (active vs natural), time since restoration/disturbance.
- Spatial coordinates enable mapping of site distributions and integration with other geospatial layers.
- Time-series data allow exploration of restoration trajectories across plots and sites.
- Old-growth references provide contextual baselines for spatial analyses and comparisons.

## How to cite and access
- Please cite Banin LF, Raine EH et al. (2023) The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests, and the accompanying dataset (NERC-Environmental Information Data Centre) as described in the dataset documentation.