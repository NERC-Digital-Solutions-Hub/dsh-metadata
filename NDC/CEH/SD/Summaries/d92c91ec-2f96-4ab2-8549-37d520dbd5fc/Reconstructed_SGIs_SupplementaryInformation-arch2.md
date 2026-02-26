# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015) Bloomfield JP, Marchant BJ and Wang L

- Project context and aim
  - Part of the Historic Droughts project (2014–2018) to build a cross-disciplinary understanding of past UK droughts and improve tools for drought management.
  - SGI dataset contributes to the Historic Droughts Inventory, a knowledge base of past drought characteristics, impacts and responses.

- Dataset scope
  - 54 UK observation boreholes located on Principal Aquifers, with a focus on Chalk and other aquifers; majority in southern/eastern England.
  - Timespan: 1891–2015; monthly standardized groundwater levels (SGI).

- What SGI is
  - A standardized index of groundwater levels created by applying a non-parametric normal scores transform to reconstructed groundwater level data for each calendar month.
  - Includes probabilistic estimates for SGI being below key thresholds: Prob0 (SGI < 0), Prob1 (SGI < -1), Prob15 (SGI < -1.5), Prob2 (SGI < -2).
  - Drought definitions aligned with groundwater context: SGI ≤ 0 indicates groundwater drought; severe groundwater drought is SGI between -1.5 and -1.99; extreme drought is SGI ≤ -2.

- Data sources and reconstruction
  - Based on reconstructed groundwater level data prepared for the Historic Droughts Inventory (Bloomfield et al., 2018).
  - Reconstruction methodology builds on earlier work (Bloomfield and Marchant, 2013) and uses data rescue to extend records back to the 19th century.

- Standardization and uncertainty
  - Standardization method: month-by-month, using a rank-based inverse normal transform to produce SGI values.
  - Uncertainty quantified with Generalised Likelihood Uncertainty Estimation (GLUE); behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5) are used to derive SGI time series and associated exceedance probabilities.

- Data format and access
  - Datasets provided as CSV files (one per site) with headers:
    - Date (Year-Month-Day, first day of each month)
    - SGI (standardized groundwater level)
    - Prob0, Prob1, Prob15, Prob2 (probabilities for thresholds 0, -1, -1.5, -2)
  - File naming follows a project-specific convention (HistoricDroughtsBGSAquiMod_Output_Feb2018_SGI_Rockleyver1, etc.).
  - An additional metadata file, Metadata_forGWLandSGI_reconstructions.csv, lists sites and basic metadata (Site_name, coordinates, aquifer, MORECS_ID, etc.).

- Outputs and usage
  - Enables consistent, historical comparison of groundwater drought status across multiple sites.
  - Facilitates integration with meteorological and surface-water drought indicators (e.g., SPI, SSI) for cross-system drought understanding.
  - Useful for drought planning and utilities' reference events, providing a standardized basis for assessing past drought severity and drivers.

- Acknowledgements and references
  - Funded by the Natural Environment Research Council (NERC) under the Historic Droughts project (NE/L010151/1).
  - Key references include works by McKee et al. (1993), WMO (2012), Bloomfield & Marchant (2013, 2018), Barker et al. (2016), and Beven & Freer (2001).