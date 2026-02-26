# Global dilution factors estimates

- Purpose and scope
  - Global dilution factors (DFs) are used to estimate concentrations of chemicals entering freshwaters from domestic wastewater (e.g., pharmaceuticals, household cleaners) after human use.
  - The dataset captures temporal and spatial variability of DFs worldwide at 0.5-degree resolution and includes long-term annual and monthly DF grids.

- Methodology
  - Global applicability: designed to function across countries, even where river flow data or wastewater effluent data are scarce.
  - Wastewater effluents: derived from national per-capita domestic water use estimates and gridded population.
  - River flows: monthly and annual flows estimated by accumulating runoff based on topographically derived flow directions.

- Data format and contents
  - Stored as raster grids in ASCII format, compatible with most GIS software.
  - Files included:
    - 1 annual dilution factor file: df_annual.asc
    - 12 monthly dilution factor files: df_monthly_xx.asc (xx = month)

- Intended audience and use
  - Aims to support an international community (decision makers, pharmaceutical companies) in assessing relative exposure to down-the-drain chemicals in rivers.
  - Enables targeting of areas with potentially higher risk based on dilution factors.

- Access, documentation, and provenance
  - Method and data described in open-access publication: Keller et al. 2014, Environmental Toxicology and Chemistry.
  - DOI: 10.1002/etc.2441; NORA link: http://nora.nerc.ac.uk/504561/
  - Data format (ASCII rasters) ensures easy integration into GIS workflows.

- Considerations for data leaders
  - Data quality and standards: designed to function where data are sparse; documentation linked to a peer-reviewed method.
  - Discoverability and metadata: dataset is linked to open literature and provided as clearly named ASCII raster files for annual and monthly analyses.
  - Potential limitations: global coverage may reflect varying data availability; ongoing validation and updates would enhance reliability.
  - Collaboration and reuse: suitable for cross-sector use (policy, environment, industry) to assess exposure and prioritize monitoring or mitigation efforts.