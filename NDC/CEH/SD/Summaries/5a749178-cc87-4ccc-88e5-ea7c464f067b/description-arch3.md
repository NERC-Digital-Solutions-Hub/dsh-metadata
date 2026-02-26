# Data description Beech tree ring data from hot and dry European distribution edges, 2019

- Objective: Utilize the relationship between European Beech tree growth and environmental factors, including climate, to monitor and forecast drought-related declines in forest growth across Europe. Growth is measured as inter-annual ring width (dendroecology).

- Scope and sampling strategy:
  - 12 site samples collected in late 2019 across Bulgaria, Albania, Kosovo, and Spain.
  - Sites chosen to capture hot/dry conditions at the southern/eastern edges of Beech distribution; cores target lower elevational limits.
  - Metadata for sites provided in site_meta.csv (latitude, longitude, elevation, nearest town).

- Field and laboratory methods:
  - At least 15 standard canopy-level trees per site; two cores per tree.
  - Cores processed with standard dendrochronology procedures: air-dried, mounted, sanded (grits 80 → 1200).
  - Cores scanned at 2400 PPI for CDendro measurements with 0.01 mm precision.
  - Cross-dating performed virtually and statistically; COFECH used for cross-dating quality control.

- Data files and structure:
  - 12 site-specific measurement files (named by site IDs) containing ring width measurements for each core.
  - Each file: year as first column; subsequent columns are ring width measurements (mm) for individual cores.
  - Tree core IDs: combination of site ID and tree ID; two cores per tree labeled with 'a' and 'b'.
  - Missing values indicated as NA; measurement resolution 0.01 mm.

- Quality and governance considerations:
  - Cross-dating quality verified via COFECH, ensuring accuracy of annual growth signals.
  - Metadata availability supports data provenance and comparability across sites.
  - Discussion of data sharing: adding metadata and publicly sharing underlying data are acknowledged as potential barriers; highlighting the importance of data governance, openness, and standardized documentation for use in monitoring frameworks.

- Relevance for monitoring frameworks:
  - Provides a multi-site, tree-level time series of growth that can be linked to climate and drought indicators.
  - Enables modelling of drought impact on Beech growth, trend analysis, and forecasting, informing policy decisions related to forest health and adaptation strategies.

- Limitations and considerations for users:
  - Geographic coverage limited to 4 countries, with potential gaps in other regions.
  - Data gaps or missing years in individual cores may exist (NA values).
  - Requires integration with climate data and careful metadata management to ensure comparability and reproducibility across sites.