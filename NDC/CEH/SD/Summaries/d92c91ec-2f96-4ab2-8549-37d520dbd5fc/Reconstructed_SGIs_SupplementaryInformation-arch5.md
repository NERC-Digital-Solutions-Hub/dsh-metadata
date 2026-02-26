# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015)

- Project context
  - Part of the Historic Droughts project (2014–2018; £1.5m) funded by UK Research Councils to understand past UK droughts across hydrometeorological, environmental, regulatory, and social perspectives.
  - Aims to improve tools for managing droughts in the future by linking hydrometeorological and social systems during droughts.

- Inventory and collaborators
  - eight UK institutions: British Geological Survey (BGS), Centre for Ecology & Hydrology (CEH), Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, University of Oxford.
  - Historic Droughts Inventory includes: (i) hydro-meteorological timelines and drought indicators; (ii) references to past droughts (newspapers, legislation, agricultural media, oral histories).

- Dataset description
  - Standardized Groundwater level Index (SGI) time series for 54 UK observation boreholes, 1891–2015.
  - SGI values are monthly and derived from reconstructed groundwater levels using a non-parametric normal scores transform (per calendar month).
  - Probability estimates of SGI being below thresholds: 0, -1, -1.5, and -2 are provided.

- Data structure and formats
  - Datasets are provided as CSV files (one per site) with headers:
    - Date (YYYY-MM-DD, first day of month)
    - SGI (standardized groundwater level)
    - Prob0 (probability SGI < 0)
    - Prob1 (probability SGI < -1)
    - Prob15 (probability SGI < -1.5)
    - Prob2 (probability SGI < -2)
  - File naming follows: [HistoricDroughts Project] [Model Identifier] [Run] [Input/Output] [Time] [Variable] [Catchment/Borehole ID] [Version], e.g.
    HistoricDroughts_BGSAquiMod_Output_Feb2018_SGI_Rockleyver1
  - Metadata file: Metadata_forGWLandSGI_reconstructions.csv with site-level metadata:
    - Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS_site_name, Aquifer, MORECS_ID, etc.

- Methodology and governance
  - Data sources: reconstructed groundwater level data (Bloomfield et al., 2018) used as the basis for standardization.
  - Standardization method: monthly non-parametric normal scores transform; inverse normal CDF applied to ranks within each month.
  - Uncertainty quantification: Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets are “behavioural” if Nash-Sutcliffe Efficiency > 0.5; behavioural reconstructions are converted to SGI series; probability intervals are the fraction of behavioural SGI series within the date interval.
  - Interpretation of SGI:
    - SGI ≤ 0 indicates groundwater drought status.
    - Severe groundwater drought: SGI between -1.5 and -1.99.
    - Extreme groundwater drought: SGI ≤ -2.
  - Most boreholes are on the Chalk aquifer within Principal Aquifers, with sites mainly in southern/eastern England.

- Data sources and references
  - Primary data: reconstructed groundwater levels (Bloomfield et al., 2018).
  - Standardization methodology: Bloomfield & Marchant (2013); threshold definitions align with meteorological drought indices (e.g., SPI) for cross-comparison (McKee et al., 1993; WMO, 2012).
  - Project acknowledgments: NERC Historic Droughts (NE/L010151/1).

- Practical considerations for data stewards
  - Ensure metadata completeness and consistency across site files.
  - Maintain linkage between site CSVs and the central metadata file for provenance.
  - Support interoperability with drought indices (e.g., SPI) by maintaining standardized monthly SGI time series.
  - Track versioning and updates as part of the Historic Droughts Inventory governance.