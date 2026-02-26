# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

- Purpose and scope
  - Provides Standardised Precipitation Index (SPI) time series for Integrated Hydrological Units (IHU) groups in the UK, covering 1862–2015.
  - SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18 and 24 months, with calculations performed for each of the twelve calendar months.
  - Aims to support drought monitoring and contribute to a drought portal to enable area-based drought analysis via SPI aggregates over IHU groups.

- Key differences from the previous version
  - Underlying rainfall data shifted from CEH-GEAR to Met Office 5 km rainfall grids.
  - Monthly rainfall data for 1960–2000 updated due to localised issues; new monthly grids derived from daily grids (1960–2000) and added rescues (1862–1909).
  - Accumulation period 9 months added in version 2.
  - Methodology for SPI calculation remains the same, but data sources and input grids changed.

- Data and context
  - SPI is derived from the cumulative probability of precipitation for a given location and accumulation period.
  - Data sources include:
    - Met Office 5 km monthly rainfall grids (historic and rescues).
    - IHU groups (UK hydrological reference units) as spatial framework.
  - The dataset is produced as part of two projects:
    - DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) – international, Belmont Forum funding.
    - Historic Droughts – UK-focused, NERC funding, part of the Drought and Water Scarcity Programme.
  - The Historic Droughts Inventory complements the SPI dataset by providing hydro-meteorological timelines and reference to past droughts from diverse sources (newspaper reports, legislation, agricultural media, oral histories) to support cross-sector understanding of drought drivers and impacts.

- Data processing and methodology
  - SPI calculation follows McKee et al. (1993); for each location and month end, SPI is computed for the 7 accumulation periods.
  - A gamma distribution is fitted to each time series using L-moments to estimate parameters (via a modified R SCI package).
  - Transformation to a standard normal distribution yields SPIs with mean 0 and SD 1; SPIs are truncated at +/-5 to handle extremes.
  - Standard reference period for fitting the gamma distribution is 1961–2010.
  - Acknowledges that gamma may not be the best fit in all UK cases; alternative distributions (e.g., Pearson type 3, Tweedie) could be used in future versions if justified.
  - Serial correlation considerations:
    - For longer accumulation periods (e.g., 18, 24 months), overlapping data create autocorrelation.
    - While SPIs per calendar month are independent under the method, concatenated monthly SPIs are often autocorrelated; use appropriate methods if doing trend analyses.

- Data format and structure
  - File format: CSV.
  - Structure includes 10 columns:
    - RID (row identifier)
    - POLYGONID (IHU group ID)
    - THEDATETIME (date/time end of the accumulation period)
    - Columns 4–10: SPI values for the seven accumulation periods across the twelve calendar months (described as different temporal aggregations of SPI).
  - SPI values are normal scores (mean 0, SD 1), without units, bounded approximately within -5 to +5; -9999 denotes No Data.

- Data quality, metadata and governance
  - Metadata gaps historically present; the project team mitigates this by contacting data originators and documenting data sources and processing steps.
  - Data governance considerations include openness, reproducibility, and clear attribution of data sources and processing methods.
  - The dataset is designed to be integrated into a CEH droughts portal and used for cross-cutting drought monitoring and planning; openness and data sharing are important for policy and stakeholder use.

- Motivation for policymakers and monitoring authors
  - Aggregating SPI over IHU groups enables drought analysis within specific areas of interest, aiding regional water resource management and drought preparedness.
  - Provides a common, comparable reference for multi-sector policy planning, water supply management, agriculture, and regulatory decisions.
  - Enables assessment of drought severity and duration across multiple time scales, informing decision-making about interventions, resource allocation, and risk management.

- Acknowledgements and references
  - Joint output of the DrIVER and Historic Droughts projects, with contributions and datasets supported by NERC and related research initiatives.
  - References to methodological and data sources include foundational SPI literature, ENC/UK hydro datasets, and related drought indicators research.