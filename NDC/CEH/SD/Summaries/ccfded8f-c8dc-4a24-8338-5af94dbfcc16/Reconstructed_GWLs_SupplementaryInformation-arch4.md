# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

- Project context and aim
  - Historic Droughts was a four-year, £1.5m project (2014–2018) funded by UK Research Councils to develop a cross-disciplinary understanding of past UK droughts and to create improved tools for drought management.
  - Aims to integrate hydrometeorological, environmental, agricultural, regulatory, social, and cultural perspectives to understand drought drivers, impacts, and responses since the late 19th century.

- Inventory and outputs
  - Eight UK institutions contributed: British Geological Survey (BGS), Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, and University of Oxford.
  - Key output: Historic Droughts Inventory, a knowledge base consisting of:
    - Hydro-meteorological timelines (rainfall, river flows, groundwater) with consistent drought indicators.
    - References to past droughts from newspapers, legislation, agricultural media, and oral histories.
  - The groundwater-related dataset described here is part of the Inventory and includes:
    - Reconstructed groundwater level (GWL) dataset for 54 boreholes and the Standardised Groundwater Level Index (SGI).

- Dataset description
  - Contents: Reconstructed groundwater levels relative to Ordnance Datum (maOD) for 54 UK boreholes.
  - Time period: 1891–2015.
  - Uncertainty: For each site, 90th and 10th percentile confidence bounds (Cl90_GWL and Cl10_GWL) accompany the reconstructed time series.
  - Geographic and geological context: Sites located on Principal Aquifers across the UK, with a concentration on Chalk aquifers in southern/eastern England.

- Data sources and methodology
  - Data sources:
    - Groundwater level (GWL) data from the National Groundwater Level Archive (NGLA).
    - Precipitation data from an updated UKCP09 dataset (5x5 km grid cell for each borehole).
    - Temperature data used to estimate potential evapotranspiration (PET) via a temperature-based equation (McGuinness-Bordne approach).
  - Modelling and reconstruction:
    - Groundwater levels reconstructed using BGS AquiMod modelling (following Jackson et al., 2016).
    - Data preprocessing included linear interpolation of irregular raw GWL data to monthly timesteps prior to modelling.
    - Monte Carlo calibration: one million parameter sets sampled within published aquifer property ranges; parameter bounds based on literature and expert judgement.
    - Uncertainty quantification via Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets deemed behavioral if Nash-Sutcliffe Efficiency > 0.5.
    - Confidence bounds derived as the 10th and 90th percentiles across the behavioural ensemble for each date.

- Data format and access
  - Datasets are provided as CSV files (one file per site) with headers:
    - Date (YYYY-MM-DD, using first day of month)
    - GWL (groundwater level in metres above Ordnance Datum, maOD)
    - Cl90_GWL (90th percentile GWL)
    - Cl10_GWL (10th percentile GWL)
  - File naming convention example: HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1
  - Metadata: Additional CSV file named Metadata_forGWLandSGI_reconstructions.csv lists sites and basic metadata (Site_name, Easting, Northing, WellMaster_ID, Full_BGS-site_name, Aquifer, MORECS_ID, etc.).
  - Annex consulted: List of site names and coordinates/identifiers (e.g., BGS WellMaster IDs, aquifer types).

- Data provenance, collaboration, and acknowledgements
  - Funded by the Natural Environment Research Council (NERC) under grant NE/L010151/1.
  - Acknowledges the contribution of eight UK institutions and the Historic Droughts project team.
  - References include foundational works on aquifer properties, drought indicators, and the UKCP09 dataset.

- Relevance for data leadership and data strategy
  - Demonstrates a clear data provenance pathway from heterogeneous, irregular sources to a harmonised, monthly time series with explicit uncertainty bounds.
  - Provides a reproducible method combining physical groundwater modelling (AquiMod), climate inputs (PPT, PET), and robust uncertainty analysis (Monte Carlo, GLUE).
  - Highlights data governance aspects relevant to data leaders:
    - Documentation of data sources, model assumptions, parameter ranges, and metadata.
    - Versioning and naming conventions to support discoverability and reuse.
    - Interdisciplinary collaboration to build a cross-domain knowledge base (Historic Droughts Inventory) for broader applicability.
  - Useful for policy and planning contexts (e.g., drought planning, water resource management) where historical baselines and uncertainty quantification are critical.