# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

- Overview of dataset
  - Time series of turbulent surface-atmosphere exchanges of sensible heat (H) and momentum (τ) measured above a 27 m forest canopy.
  - Location: ancient broadleaved deciduous forest in Wytham Woods, Oxfordshire, UK.
  - Period: 2014-06-13 13:00 to 2016-01-04 22:00.
  - Includes ancillary meteorological and soil observations, plus variables describing atmospheric turbulence and quality of flux observations.
  - Data file: WythamWoodsFluxMicromet_v1.0.csv (30-minute flux observations; plus ancillary data).

- Study site
  - Wytham Woods flux observation site (52.7667°N, -1.3333°W), ~400 ha of ancient woodland.
  - Climate: temperate maritime; mean annual temp ~10.1°C; mean annual precip ~730 mm.
  - Topography: hill location, ~160 m a.s.l.; canopy ~20 m tall.
  - Flux tower on the north-facing slope within disturbed ancient forest; dominants include Pedunculate Oak, Ash, and Sycamore.

- Sampling regime
  - Automated flux measurements from 2014-06-13 13:00 to 2016-01-04 22:00.
  - Fluxes measured above canopy at 27 m height using a Windmaster sonic anemometer and logged at 20 Hz; 30-minute means computed for fluxes.
  - Additional air temperature and relative humidity measured at 0.1 Hz; logged as 30-minute means.

- Data processing
  - Eddy covariance (EC) fluxes calculated with EddyPRO v6.1; 30-minute block averages.
  - Corrections applied: boost-bug wind correction; angle-of-attack corrections for Gill sonic anemometers; 2D coordinate rotation; corrections for high/low-frequency attenuation; humidity-related corrections for H.
  - Uncertainty estimation for H and τ provided.
  - Quality control (QC) flags generated for each 30-minute flux (0 = high quality, 1 = acceptable, 2 = poor); random uncertainties and other diagnostics computed (u*, TKE, T*, L, z/L, footprint).
  - Additional QC guidance and processing details documented for reproducibility.

- Quality control
  - Outliers removed using median absolute deviation for H; fluxes with QC flag >1 excluded.
  - Physical bounds applied to H (-200 to 600 W m^-2) as a data-quality check.
  - All flux and ancillary data visually reviewed weekly; clearly erroneous values removed.
  - Data user can choose to exclude flagged fluxes (>0) or apply other QC metrics (e.g., u*, footprint) as needed.

- Details of data structure
  - Single CSV file containing the complete time series from 201406-13 13:00 to 2016-01-04 22:00.
  - Missing records denoted by -9999.
  - Columns described in Table 1; variable names and units adapted from Li-COR Biosciences references.

- Nature and Units of recorded values
  - Variables include: DateTime, H (W m^-2), rand_err_H, qc_H, Tau (kg m^-1 s^-2), rand_err_Tau, qc_Tau, wind_speed, max_wind_speed, wind_dir, Ustar, TKE, Tstar, L, zL, X_peak, X_10, X_30, X_50, X_70, X_90, SW in/out, LW in/out, R net, SHF_1/SHF_2 (soil heat flux), Ta (°C), RH (%), Pa (kPa), Ts_1, Ts_2 (soil temps), VWC_1, VWC_2 (soil moisture), Precip.
  - Units and meanings follow standardized micrometeorological conventions; -9999 marks missing values.

- Acknowledgments
  - Funded by the Natural Environment Research Council (NERC).
  - Ancillary data provided by COSMOS-UK network.
  - Field access and support provided by the University of Oxford and Wytham Woods management.
  - Technical support acknowledged.

- References
  - Citations for COSMOS-UK data, site descriptions, processing methods (EddyPRO; footprint models; QC guidelines; sonic anemometer corrections; related methodological literature).