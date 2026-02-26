# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- Provides plot-scale data on forest structure, aboveground carbon density (biomass), and tree species richness from forest restoration sites in South and Southeast Asia.
- accompanies the publication on ecosystem restoration outcomes in tropical and subtropical Asian forests (Banin et al., 2023) and is archived in the NERC Environmental Information Data Centre.
- Includes data from 11 sites with disturbances that led to forest clearance or degradation; covers both active restoration (seedling planting) and natural regeneration; some sites include old-growth references and repeated measurements.
- Designed to support cross-site comparisons of restoration approaches and to enable transparency and reuse of the underlying data and analysis code.

## What the dataset contains
- Structure, carbon density (aboveground biomass), and biodiversity (tree species richness) metrics at plot level.
- Data up to May 2021, collated from published studies, grey literature, and contributions from co-authors.
- Information on both actively restored and naturally regenerating plots, plus references to old-growth comparison plots where available.
- Includes the analytical code used to reproduce the reported analyses and figures from Banin et al. (2023).

## Data files and contents
- script_community_analyses.R: R script to run the three community-level analyses and produce three graphs and a map included in Figure 4 of the publication.
- df_restoration_response_LRR.csv: restoration response data comparing active vs natural regeneration across plots/sites.
- df_basalarea_timeseries.csv: basal area time series data by plot, including restoration type, dates, and survey years.
- df_recovery_completeness.csv: recovery completeness data, including old-growth comparisons and time-since-restoration metrics.
- df_coords.csv: site coordinates (lat/long) and area information for active vs natural plots.
- Supporting_info_community_analysis.docx: methodological details on data collation, collection methods, and assumptions used in Banin, Raine et al. (2023).
- Note: The dataset also includes fields describing study identifiers, plot identifiers, time since restoration/disturbance, plot areas, tree densities, basal areas, aboveground carbon density (ABC), and counts of plots.

## Key variables and structure
- Study: short-title identifier for each study site.
- For each plot pair (active vs natural):
  - nr_site / a_site: natural regenerator and actively restored plot identifiers.
  - r_duration / d_duration: years since restoration and years since disturbance.
  - d_estimated: Y/N if disturbance timing was estimated due to missing data.
  - BA_r / BA_nr: basal area per plot for restored vs natural plots.
  - d_r / d_nr: tree species richness in restored vs natural plots.
  - ABC_r / ABC_nr: aboveground carbon density in restored vs natural plots.
  - plot_ha: plot area in hectares; area_nr / area_r: total areas of plots by restoration type.
  - np_nr / np_r: number of natural and restored plots.
- Time series data (df_basalarea_timeseries.csv):
  - rest: restoration type (active vs passive).
  - id: plot identifier for repeated measurements.
  - rest_date, survey: restoration date and survey year.
  - plot_area, tree_dens, basal_area: plot metrics.
  - time_since_rest / time_since_dist: time since restoration/disturbance.
  - time_series metadata: n_plot, etc.
- Recovery completeness data (df_recovery_completeness.csv):
  - Includes basal area, ABC, and other metrics with old-growth comparison plots (BA_og, d_og, ABC_og).
- Coordinates (df_coords.csv):
  - Study, latitude/longitude (degrees, minutes, seconds; N/S/E/W), area_a (active plot area), area_nr (natural plot area).

## Provenance and methods
- Data were compiled according to protocols described in Banin, Raine et al. (2023) and its electronic supplementary material.
- Sources include published papers, grey literature, and data contributions from co-authors.
- The codified analyses (three community-level analyses) and associated visuals (graphs and a map) are reproduced from Banin et al. (2023) using the included R script.

## How to use and cite
- Intended for analyzing and comparing outcomes of different restoration approaches (active vs natural regeneration) in tropical and subtropical Asian forests.
- Use the provided R script to reproduce the three community analyses and figures, and reference both the dataset and the Banin et al. (2023) publication.
- Citation guidance: Banin Lindsay F., Raine Elizabeth H., et al. 2023. Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia. NERC-Environmental Information Data Centre; accompanying publication: The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.

## Access, limitations and considerations
- Timeframe: data up to May 2021; some estimates (e.g., time since disturbance) may be inferred when data were missing.
- Heterogeneity: data come from multiple studies with potentially differing methodologies, sites, and plot designs; comparability is facilitated by standard protocols referenced in Banin et al. (2023).
- Old-growth comparisons provide context but may vary in sampling intensity and location relative to restoration plots.
- The dataset is designed to enable data sharing and reuse, with explicit documentation of methods, variables, and analytical steps.

## Practical takeaways for analysts
- Enables cross-site assessment of restoration outcomes in terms of structure (basal area), carbon density, and biodiversity (tree species richness).
- Supports analyses contrasting active restoration against natural regeneration, with longitudinal and cross-sectional perspectives.
- Provides ready-to-use data and reproducible analysis code to facilitate transparent monitoring and policy evaluation of forest restoration progress.