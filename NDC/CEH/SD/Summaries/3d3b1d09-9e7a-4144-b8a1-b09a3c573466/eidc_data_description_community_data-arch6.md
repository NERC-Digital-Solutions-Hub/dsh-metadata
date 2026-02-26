# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- A dataset accompanying Banin et al. 2023, synthesizing outcomes from forest restoration in tropical and subtropical Asian forests.
- Contains plot-level data on forest structure, aboveground carbon density (biomass), and tree species richness from restoration sites in South and Southeast Asia.
- Represents 11 sites with disturbance-driven degradation; includes both actively restored plots and naturally regenerating plots, with some old-growth reference plots and repeat measurements.
- Data compiled up to May 2021 from published studies, grey literature, and contributions from co-authors.
- Includes the code used for analyses to compare outcomes of different restoration approaches.

## Data contents and structure
- Files included:
  - script_community_analyses.R: R script to run three community-level analyses, generate three graphs, and create a map corresponding to Figure 4 in the associated paper.
  - df_restoration_response_LRR.csv: dataset for restoration response analysis (log response ratio in community metrics).
  - df_basalarea_timeseries.csv: dataset for basal area time series analysis.
  - df_recovery_completeness.csv: dataset for recovery completeness analysis, including old-growth reference data.
  - df_coords.csv: site coordinates.
  - Supporting_info_community_analysis.docx: details on data collation, collection methods, and analysis assumptions from the sources in the analysis.
- Data coverage:
  - Plot-level censuses for structure, biomass (aboveground carbon density), and biodiversity (tree species richness).
  - Comparisons across restoration types (actively restored vs naturally regenerating) with some old-growth references and repeated measures over time.

## Datasets and key variables
- df_restoration_response_LRR.csv
  - Study, nr_site (natural regeneration plot ID), a_site (actively restored plot ID)
  - r_duration, d_duration (years since restoration/disturbance)
  - d_estimated (Y/N if timing was estimated)
  - BA_r, BA_nr (basal area for restored vs natural plots)
  - d_r, d_nr (tree species richness)
  - ABC_r, ABC_nr (aboveground carbon density)
  - plot_ha, np_nr, np_r (plot area and counts)
  - area_nr, area_r (total area for each restoration type)

- df_basalarea_timeseries.csv
  - Study, rest (active vs passive restoration), id (plot identifier)
  - rest_date, plot_area
  - tree_dens, basal_area
  - survey, time_since_rest, time_since_dist, n_plot

- df_recovery_completeness.csv
  - Study, rest, id, rest_date, plot_area
  - tree_dens, basal_area, ABC (aboveground carbon density)
  - survey, time_since_rest, time_since_dist, n_plot
  - BA_og, d_og, ABC_og (old-growth comparison metrics)

- df_coords.csv
  - study, lat_d/lat_m/lat_s/lat_ns, lon_d/lon_m/lon_s/lon_e
  - area_a (active restoration area), area_nr (natural regeneration area)

- Supporting_info_community_analysis.docx
  - Details on data collation, data sources, and analysis methods as reported in Banin et al. (2023)

## Provenance and scope
- Based on 11 sites with disturbance-induced forest degradation, incorporating both active restoration and natural regeneration plots.
- Some datasets include old-growth reference plots for comparative context and repeat measurements over time.
- Data collection and compilation followed protocols described in Banin, Raine et al. (2023) main text and electronic supplementary material.

## Usage and analyses
- The accompanying code enables replication of the three community-level analyses and generation of associated visualizations and maps.
- Data support comparative evaluation of restoration strategies (active vs natural regeneration) in terms of structure, carbon density, and biodiversity recovery.

## Access and data notes
- Data are structured for cross-site comparison and potential integration with other sources through consistent identifiers (study, plot IDs, restoration type).
- Units:
  - Basal area (m2 per plot or per hectare where indicated)
  - Aboveground carbon density (Mg C/ha)
  - Species richness (count)
  - Time variables in years
- Coordinates provided to enable spatial mapping of sites.

## Citations and reuse
- Please cite the dataset alongside the associated publication:
  - Banin LF, Raine EH, et al. 2023. Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia. NERC-Environmental Information Data Centre.
  - And the publication: Banin LF, Raine EH et al. 2023. The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.