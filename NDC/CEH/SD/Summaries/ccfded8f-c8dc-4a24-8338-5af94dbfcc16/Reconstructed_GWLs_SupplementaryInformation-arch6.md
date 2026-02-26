# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

- Project context
  - Part of the Historic Droughts project (2014–2018), a £1.5m, cross-disciplinary effort to understand past UK droughts and develop better tools for drought management.
  - Aims to link hydrometeorological and social factors to drought history since the late 19th century.
  - Inventory output includes a knowledge base of past drought characteristics, impacts, and responses.

- Inventory and outputs
  - Historic Droughts Inventory, compiled by eight UK institutions.
  - Two main elements:
    - hydro-meteorological timelines (rainfall, river flows, groundwater) with consistent drought indicators extended back to the 19th century.
    - references to past droughts from newspapers, legislation, agricultural media, and oral histories.
  - Groundwater data are part of the groundwater-related datasets within the Inventory (including the Standardised Groundwater Level Index).

- Dataset description
  - Reconstructed groundwater levels (maOD) for 54 observation boreholes across the UK.
  - Provides 90th and 10th percentile confidence bounds for each time series.
  - Time period covered: 1891–2015.
  - Sites are located on Principal Aquifers, predominantly Chalk in southern/eastern England.

- Motivation and use
  - Created by the British Geological Survey to extend understanding of historic droughts before the modern record.
  - Supports drought management planning by providing reference events and long-term groundwater histories.

- Data sources and inputs
  - Groundwater level data from the National Groundwater Level Archive (NGLA, BGS).
  - Raw data are irregular (monthly or more frequent) and were linearly interpolated to a monthly time step for modelling.
  - Precipitation data from an updated/extended UKCP09 dataset, at 5x5 km grid cells around each borehole.
  - Temperature data used to estimate potential evapotranspiration (PET) via the McGuinness-Bordne method (temperature-based).

- Reconstruction methodology
  - Groundwater levels reconstructed with BGS’s AquiMod lumped conceptual model.
  - Model calibration via Monte Carlo simulations: 1,000,000 parameter sets sampled within plausible ranges.
  - Parameter bounds derived from published aquifer properties and expert judgement.
  - Uncertainty quantified using Generalised Likelihood Uncertainty Estimation (GLUE).
  - Behavioural parameter sets defined as Nash–Sutcliffe Efficiency > 0.5.
  - Uncertainty bounds: 10th and 90th percentiles calculated from the behavioural ensemble for each date.

- Dataset format and files
  - Datasets delivered as CSV files, one per site.
  - Each file contains:
    - Date: YYYY-MM-DD (first day of each month)
    - GWL: Groundwater level (maOD)
    - Cl90_GWL: 90th percentile GWL
    - Cl10_GWL: 10th percentile GWL
  - File naming exemplars indicate project, model, run, and variable (e.g., HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1).
  - Metadata file: Metadata_forGWLandSGI_reconstructions.csv with fields such as Site_name, Easting, Northing, WellMaster_ID, Full_BGS_site_name, Aquifer, MORECS_ID, and other site descriptors.
  - Annex lists the 54 sites with coordinates and aquifer information (e.g., Chalk, Carboniferous Limestone, Permo-Triassic sandstone, etc.).

- Data access and structure
  - CSV-based delivery suitable for integration into data analyses and dashboards.
  - Metadata supports geospatial association and aquifer context for each site.

- Acknowledgements
  - Funded by the Natural Environment Research Council (NERC) through the Historic Droughts project (NE/L010151/1).

- References and context
  - Key methodological and data references include shaping the GLUE framework, AquiMod model, and drought indicators; relevant works cited span groundwater modelling, drought reconstruction, and earth-system processes.

- Applications and considerations
  - Enables exploration of multidecadal groundwater behavior and drought history prior to 1960s records.
  - Useful for drought management planning and scenario development by utilities and policymakers.
  - Users should consider interpolation-derived monthly time steps and GLUE-based uncertainty when interpreting reconstructed series.