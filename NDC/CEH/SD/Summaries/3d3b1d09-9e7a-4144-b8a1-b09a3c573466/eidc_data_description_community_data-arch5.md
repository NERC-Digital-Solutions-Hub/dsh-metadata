# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

## Overview
- Dataset accompanying Banin et al. 2023, The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests.
- Contains plot-level measurements of forest structure, aboveground carbon density (biomass), and tree species richness from forest restoration sites in South and Southeast Asia.
- Covers 11 sites where disturbance led to forest clearance or degradation; includes active restoration (seedling planting) and natural regeneration; some sites include old-growth reference plots and repeated measures.
- Data up to May 2021, compiled from published studies, grey literature, and co-authors; follows protocols from Banin et al. (2023).
- Includes the code used to perform analyses described in the publication, enabling reproducibility.

## Contents and data structure
Files included and purposes:
- script_community_analyses.R — R script to run three community-level analyses, produce three graphs, and generate the map for Figure 4 (Banin et al. 2023).
- df_restoration_response_LRR.csv — dataset for restoration response analysis (active vs natural regeneration) with area, carbon density, diversity metrics, and plot counts.
- df_basalarea_timeseries.csv — dataset for basal area time series by plot, restoration type, and survey year; includes time since restoration/disturbance.
- df_recovery_completeness.csv — dataset for recovery completeness analysis, including old-growth references (BA_og, d_og, ABC_og) and time since restoration/disturbance.
- df_coords.csv — site coordinates (lat/long) and plot area breakdowns by restoration type.
- Supporting_info_community_analysis.docx — details on data collation methods, assumptions, data collection and analysis methods as reported in Banin et al. (2023).
- df_restoration_response_LRR, df_basalarea_timeseries, df_recovery_completeness, df_coords include structured fields as described below.

## Data scope and provenance
- Sites: 11 forest restoration sites in South and Southeast Asia.
- Data types: structure (tree density, basal area), biomass/carbon density (ABC), and biodiversity (tree species richness).
- Restoration types: actively restored plots (seedling planting) and naturally regenerating plots (no planting).
- References: data collated from published papers, grey literature, and co-authors; original data sources cited in the accompanying documentation and Banin et al. (2023) main text and supplement.
- Timeframe: censuses up to May 2021; some sites include old-growth reference plots and repeat measurements over time.

## Variables and data structure (high-level)
- df_restoration_response_LRR.csv
  - study, nr_site (natural regeneration plot ID), a_site (actively restored plot ID)
  - r_duration, d_duration (years since restoration/disturbance)
  - d_estimated (Y/N for estimated disturbance time)
  - BA_r, BA_nr (basal area for restored vs natural plots)
  - d_r, d_nr (tree species richness)
  - ABC_r, ABC_nr (aboveground carbon density)
  - plot_ha, np_nr, np_r (plot areas and counts)
  - area_nr, area_r (total area for each restoration type)
- df_basalarea_timeseries.csv
  - study, rest (restoration type: active or passive), id (plot identifier), rest_date (year of restoration)
  - plot_area, tree_dens, basal_area, survey (year of survey)
  - time_since_rest, time_since_dist, n_plot
- df_recovery_completeness.csv
  - study, rest, id, rest_date, plot_area, tree_dens, basal_area, ABC, survey
  - time_since_rest, time_since_dist, n_plot
  - BA_og, d_og, ABC_og (old-growth references for comparison)
- df_coords.csv
  - study, lat_d/lat_m/lat_s/lat_ns, lon_d/lon_m/lon_s/lon_e (coordinates)
  - area_a (total actively restored area), area_nr (total naturally regenerating area)

## Data quality, methods and provenance
- Data collation and analysis follow the protocols described in Banin, Raine et al. 2023 (main text and electronic supplementary material) and cite original data sources accordingly.
- Data were quality assured, cleaned, and transformed for sharing; the accompanying code enables replication of the analyses and figures from the publication.
- Metadata captures study identifiers, plot IDs, restoration status, timing, and spatial context, facilitating traceability and reuse.

## Access, reuse, and citation
- Hosted in the NERC Environmental Information Data Centre (EIDC).
- Dataset should be cited alongside Banin et al. (2023) publication; explicit citation guidance is provided in the dataset documentation.
- Includes executable R code to reproduce analyses and figures, supporting transparency and reuse.

## Governance, stewardship and maintenance considerations
- Provenance: preserve links between dataset files and the original publications, supplementary materials, and co-authors to maintain traceability.
- Metadata completeness: ensure consistent field definitions across files (e.g., restoration type coding, time metrics, and units for basal area and carbon density).
- Versioning: track updates to data sources, especially if new data become available post-May 2021; record changes to variables or categorizations (e.g., restoration status, old-growth references).
- Interoperability: maintain clear variable names and units to facilitate integration with other forest restoration or ecosystem datasets.
- Licensing and access: confirm and document licensing terms to support data sharing beyond the original project; ensure citation requirements are clear for users.
- Data quality controls: periodically verify data integrity, especially for time-series panels and repeated-measure plots; monitor for inconsistencies in plot IDs or restoration classification.
- Updates and embargoes: define if and when new data will be released and under what conditions, including any embargo periods for ongoing projects.

## Limitations and caveats
- Timeframe limited to May 2021; newer data not included in the current release.
- Data are collated from multiple sources with varying methodologies; while harmonized, residual heterogeneity may affect cross-site comparability.
- Some time-since-disturbance estimates are inferred (d_estimated = Y), which may introduce uncertainty in timing across sites.
- Old-growth reference comparisons are included, but not uniformly distributed across all sites.

## Practical implications for dataset custodians
- Maintain and publish clear data dictionaries and methodological notes to support accurate interpretation.
- Ensure reproducible workflows by preserving the provided code and aligning future updates with the original protocols.
- Facilitate discoverability through consistent study identifiers, location data, and restoration-type classifications to enable cross-dataset comparisons.