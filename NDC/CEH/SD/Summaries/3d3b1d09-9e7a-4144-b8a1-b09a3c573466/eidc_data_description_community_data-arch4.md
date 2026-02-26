# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- Dataset accompanying Banin et al. (2023) on ecosystem restoration outcomes in tropical and sub-tropical Asian forests.
- Contains plot-level data on structure, biomass (carbon density), and biodiversity (tree species richness) from restoration sites in South and Southeast Asia.
- Covers forest inventory data up to May 2021, collated from published studies, grey literature, and co-authors.
- Includes both actively restored plots and naturally regenerating plots, with some old-growth references and repeat measures.
- Also provides code used to analyze the data and generate figures in the associated publication.

## Data scope and structure
- 11 sites where disturbance led to forest degradation or clearance.
- Both active restoration (planting) and natural regeneration plots were censused for structure, biomass, and/or biodiversity.
- Some sites include old-growth reference plots and/or repeat measurements over time.
- Data were assembled following the protocols in Banin, Raine et al. (2023) and cite the main publication alongside the dataset.
- Files included:
  - script_community_analyses.R: R script to run three community-level analyses and produce three graphs and a map (Figure 4) from Banin et al. (2023).
  - df_restoration_response_LRR.csv: restoration response analysis dataset.
  - df_basalarea_timeseries.csv: basal area time-series dataset.
  - df_recovery_completeness.csv: recovery completeness dataset (includes old-growth comparison data).
  - df_coords.csv: site coordinates.
  - Supporting_info_community_analysis.docx: details on data collation, data collection, and analysis methods.

## Key datasets and variables
- df_restoration_response_LRR
  - Study, nr_site (naturally regenerating plots), a_site (actively restored plots)
  - r_duration, d_duration (years since restoration/disturbance)
  - d_estimated (Y/N on whether time since disturbance was estimated)
  - BA_r, BA_nr (basal area for restored vs natural plots)
  - d_r, d_nr (tree species diversity in restored vs natural plots)
  - ABC_r, ABC_nr (aboveground carbon density in restored vs natural plots)
  - plot_ha (plot area), np_nr, np_r (numbers of plots)
  - area_nr, area_r (total area of naturally regenerating and restored plots)
- df_basalarea_timeseries
  - Study, rest (restoration type: active or passive), id (plot identifier across time)
  - rest_date (year of restoration), plot_area, tree_dens, basal_area
  - survey (year of survey), time_since_rest, time_since_dist
  - n_plot (number of plots in the time series)
- df_recovery_completeness
  - Study, rest, id, rest_date, plot_area, tree_dens, ABC, survey
  - time_since_rest, time_since_dist
  - n_plot
  - BA_og (basal area for old-growth comparison plots), d_og (species richness in old-growth plots)
  - ABC_og (aboveground carbon density for old-growth comparison plots)
- df_coords
  - study
  - lat_d, lat_m, lat_s, lat_ns (latitude in degrees/minutes/seconds and hemisphere)
  - lon_d, lon_m, lon_s, lon_e (longitude in degrees/minutes/seconds and hemisphere)
  - area_a (total area of actively restored plots), area_nr (total area of naturally regenerating plots)

## Data curation and methods
- Data compiled from published studies, grey literature, and co-authors.
- Followed protocols described in the Banin, Raine et al. (2023) main text and electronic supplementary material.
- Includes both active restoration and natural regeneration plots, with potential old-growth references for context.

## Usage focus for Data Leaders
- Supports evaluation and comparison of restoration approaches across multiple sites in Asia.
- Enables assessment of how restoration type influences structure (basal area), biomass (carbon density), and biodiversity (species richness) over time.
- Provides a reproducible codebase (R script) to reproduce analyses and visualizations from the associated publication.
- Useful for planning data collection, identifying data gaps, and coordinating cross-site data governance and metadata standards.

## Citation and access
- Dataset: Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia. NERC-Environmental Information Data Centre.
- Publication to cite alongside dataset: Banin LF, Raine EH et al. 2023. The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.
- Ensure citation of both the dataset and the associated publication per the provided references.