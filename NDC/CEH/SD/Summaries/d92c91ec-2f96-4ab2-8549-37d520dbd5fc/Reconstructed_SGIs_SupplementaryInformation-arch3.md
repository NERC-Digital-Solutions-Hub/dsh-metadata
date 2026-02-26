# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015)

- Project context and aims
  - Part of the Historic Droughts project (2014–2018; £1.5m) funded by the UK Research Councils to develop cross-disciplinary understanding of past UK droughts and improve tools for drought management.
  - Addresses links between hydrometeorological and social systems during droughts to inform policy and decision-making on groundwater management.

- Inventory and dataset scope
  - Historic Droughts Inventory collects hydro-meteorological timelines and historical references to past droughts (19th century to present) from multiple sectors.
  - SGI dataset is a reconstructed groundwater-level dataset for 54 boreholes across Principal Aquifers in the UK, with time series from 1891 to 2015.
  - Most sites are in southern and eastern England, predominantly on Chalk aquifer.

- SGI concept and motivation
  - SGI provides standardised groundwater levels enabling direct comparison with meteorological drought indices (e.g., SPI) and hydrological drought indices (e.g., SSI).
  - Drought definitions: SGI ≤ 0 indicates drought; SGI ≤ -1 is groundwater drought; -1.5 to -1.99 is severe drought; ≤ -2 is extreme drought.
  - Tool supports retrospective drought assessment and reference events for planning (e.g., Drought Management Plans).

- Data sources and reconstruction
  - Base data: reconstructed groundwater level time series prepared for the Historic Droughts Inventory (Bloomfield et al., 2018).
  - Reconstruction enables extension of records back into the 19th century through data rescue and modelling.
  - Metadata: includes site coordinates, aquifer, MORECS code, and WellMaster identifiers.

- Standardization method (how SGI is produced)
  - Standardisation via a non-parametric normal scores transform applied to monthly data for each calendar month.
  - Process assigns ranks within each month across a borehole’s time series, then converts ranks to SGI values using the inverse normal CDF.
  - SGI values are subsequently ordered to match the rank ordering of months.

- Uncertainty and exceedance probabilities
  - Uncertainty quantified using Generalised Likelihood Uncertainty Estimation (GLUE) with behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5).
  - For each site, behavioural reconstructions generate SGI series; probabilities for SGI thresholds are given:
    - Prob0: probability SGI < 0
    - Prob1: probability SGI < -1
    - Prob15: probability SGI < -1.5
    - Prob2: probability SGI < -2

- Data formats and accessibility
  - Data delivered as CSV files (one per site) with headers: Date (YYYY-MM-DD, first of month), SGI, Prob0, Prob1, Prob15, Prob2.
  - File naming convention includes project, model, run, time, variable, site, and version.
  - An additional Metadata_forGWLandSGI_reconstructions.csv lists site metadata (Site_name, Easting/Northing, WellMaster_ID, Aquifer, MORECS_ID, etc.).
  - Data are housed as part of the Historic Droughts project outputs; acknowledges NERC funding and related data-centre hosting.

- Practical applications for monitoring and policy
  - Enables monitoring of groundwater drought status and trends over long historical periods.
  - Facilitates cross-comparison with meteorological drought indices (SPI) and hydrological drought indicators.
  - Provides a consistent framework for evaluating past drought impacts and drivers, informing future drought planning and groundwater management strategies.

- Key references and project acknowledgements
  - Project references: Historic Droughts (NERC NE/L010151/1); related datasets and methodological papers (Bloomfield et al., 2018; Bloomfield & Marchant, 2013; McKee et al., 1993; WMO, 2012; Barker et al., 2016).
  - Acknowledgement: funded by the Natural Environment Research Council; data description and methods described in the dataset documentation.