# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

- Project context
  - Historic Droughts project (2014–2018) funded by UK Research Councils (£1.5m) to develop a cross-disciplinary understanding of past UK droughts and improve tools for future drought management.
  - Aims to connect hydrometeorological data with social/regulatory factors to understand drivers, impacts, and responses of droughts since the late 19th century.

- Inventory and outputs
  - Eight institutions contributed: British Geological Survey (BGS), Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, University of Oxford.
  - Historic Droughts Inventory comprises:
    - Hydro-m meteorological timelines (rainfall, river flows, groundwater) with consistent drought indicators extending back to the 19th century.
    - References to droughts from newspapers, legislation, agricultural media, and oral histories.
  - Datasets include groundwater-related data, notably reconstructed groundwater levels and the Standardised Groundwater level Index (SGI).

- Dataset focus
  - Reconstructed groundwater level (GWL) time series for 54 observation boreholes across Principal Aquifers in the UK, primarily Chalk aquifer locations.
  - Time span for reconstructed GWL: 1891–2015.

- Dataset details
  - Output values: GWL in metres above Ordnance Datum (maOD) with 90th and 10th percentile confidence bounds for each date.
  - Format: CSV files (one per site) with headers Date, GWL, Cl90_GWL, Cl10_GWL.
  - Metadata: Additional CSV (Metadata_forGWLandSGI_reconstructions.csv) listing site-specific metadata (Site_name, coordinates, WellMaster ID, Aquifer, MORECS_ID, etc.).
  - Site listing: Includes location and aquifer information for all reconstructed boreholes (e.g., BaydonHoleOBH, Rockley, WestDean, etc.).

- Data sources and reconstruction methodology
  - Groundwater level data from the National Groundwater Level Archive (NGLA, BGS, 2017).
  - Precipitation data from UKCP09-based gridded products; potential evapotranspiration (PET) estimated using a temperature-based method (McGuinness-Bordne).
  - Lagoons: Monthly GWLs reconstructed using BGS AquiMod, a lumped conceptual model.
  - Temporal interpolation: Raw GWLs (often irregular) interpolated to monthly time steps prior to modelling.
  - Model calibration: Monte Carlo (MC) simulations generating ~1,000,000 parameter sets; bounds anchored on aquifer properties from literature/expert judgment.
  - Uncertainty quantification: Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets deemed behavioural if Nash-Sutcliffe Efficiency (NSE) > 0.5.
  - Output: Reconstructed monthly GWL time series with associated 10th and 90th percentile confidence bounds.

- Data formatting and accessibility
  - Files named to reflect project, model, run, and variable (e.g., HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1).
  - Metadata file provides site-specific coordinates (Easting/Northing), site names, aquifer, and identifiers for integration with other datasets.

- Motivations and applications for analysts
  - Enables long-run drought analysis and cross-site comparisons to identify patterns in groundwater responses.
  - Supports calibration/validation of hydrological models and exploration of relationships between groundwater levels, precipitation, and evapotranspiration.
  - Provides a historical reference baseline for drought planning and utility resilience (e.g., informing drought management plans).

- Acknowledgments and references
  - Funded by the Natural Environment Research Council (NERC) through the Historic Droughts project (NE/L010151/1).
  - References to foundational works on aquifer properties, drought indicators, and PET estimation underpinning the reconstruction methodology.