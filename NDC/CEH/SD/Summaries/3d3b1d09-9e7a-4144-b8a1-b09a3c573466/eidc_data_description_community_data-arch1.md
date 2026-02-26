# The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- Purpose and scope
  - A data-rich synthesis accompanying Banin et al. (2023) that enables analysis of restoration outcomes in tropical and sub-tropical Asian forests.
  - Focuses on plot-level structure, carbon density (biomass), and tree biodiversity (species richness) from forest restoration sites in South and Southeast Asia.
  - Includes active restoration (seedling planting) and natural regeneration plots, with some old-growth reference plots and repeated measures.
  - Data collected up to May 2021 from 11 sites affected by prior disturbance (degradation or clearance) and compiled from published studies, grey literature, and co-authors’ contributions.
  - Dataset and accompanying code are designed to support comparisons of restoration approaches, track recovery over time, and reproduce analyses from the linked publication.

- Data content and structure
  - Core data described in three main datasets plus coordinates and supporting information:
    - df_restoration_response_LRR.csv: restoration response metrics comparing active vs natural regeneration, including time since restoration and disturbance, basal area (BA), species diversity (d), aboveground carbon density (ABC), plot areas, and counts of plots.
    - df_basalarea_timeseries.csv: longitudinal data per plot with restoration type, plot area, tree density, basal area, survey year, and time since restoration/disturbance; includes repeated measures identifiers.
    - df_recovery_completeness.csv: recovery completeness data including old-growth comparison plots (BA_og, d_og, ABC_og) alongside restoration plots, with time and plot metadata.
    - df_coords.csv: site coordinates (latitude/longitude) and area metrics for actively restored and naturally regenerating plots.
  - Supporting files:
    - script_community_analyses.R: R script to run three community-level analyses and generate three graphs plus a map corresponding to Figure 4 in the publication.
    - Supporting_info_community_analysis.docx: details on data collation, data collection methods, and analysis assumptions as reported in Banin et al. (2023).
  - Data fields (highlights):
    - Study identifiers, plot IDs for naturally regenerating and actively restored plots, time since restoration/disturbance, plot areas, tree densities, basal area (BA), aboveground carbon density (ABC), species richness (d), and counts of plots.
    - Time data includes r_duration (restoration duration) and d_duration (disturbance duration), with a d_estimated flag for cases where disturbance timing was inferred.

- Sites, scale, and restoration types
  - 11 sites across South and Southeast Asia.
  - Disturbance-led degradation with subsequent restoration efforts.
  - Two restoration modalities analyzed:
    - Active restoration: plantings of seedlings.
    - Passive/natural regeneration: no seedling planting.
  - Some plots include old-growth forest data for reference and/or repeat measurements over time to assess recovery trajectories.

- Time coverage and data quality considerations
  - Data up to May 2021; includes time since restoration and time since disturbance for many plots.
  - d_estimated flag indicates when the time since disturbance was inferred rather than directly reported.
  - Protocols for data collation follow Banin et al. (2023) and its electronic supplementary materials, with attention to data collection methods and analysis assumptions.
  - Coordinate and area data enable spatial analyses and aggregation across plot counts and areas.

- Intended use and methodological context
  - Enables cross-site comparisons of restoration outcomes for structure (basal area), carbon density (ABC), and biodiversity (tree species richness).
  - Supports replication and extension of Banin et al. (2023) analyses, including community-level analyses and mapping of restoration effects.
  - Facilitates transparency by providing the analysis code and detailed data provenance, aiding reproducibility and discovery of the underlying data sources.

- Provenance and citations
  - Data accompany Banin L.F. et al. (2023) The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests.
  - Dataset citation provided alongside the publication citation (NERC-Environmental Information Data Centre) to accompany the formal article.