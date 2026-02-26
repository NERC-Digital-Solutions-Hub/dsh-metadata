# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

- Purpose and scope
  - Time series of turbulent surface–atmosphere exchanges: sensible heat flux (H) and momentum flux (τ) measured with eddy covariance (EC) at Wytham Woods, Oxfordshire, UK.
  - Covering 2014-06-13 13:00 to 2016-01-04 22:00.
  - Includes ancillary weather and soil physics observations, plus turbulence descriptors, footprints, and data quality information.

- Study site and conditions
  - Wytham Woods flux site within ~400 ha of ancient broadleaved deciduous forest, ~5 km NW of Oxford.
  - Temperate maritime climate; mean annual temp ~10.1°C, precip ~730 mm.
  - Soils range from poorly to well drained clays over sandstone; canopy ~20 m; flux tower on a north-facing slope.

- Sampling regime and data collection
  - EC measurements above the canopy at 27 m height.
  - Raw 20 Hz velocity components and sonic temperature with a Windmaster sonic anemometer; 0.1 Hz air temperature and relative humidity.
  - Fluxes computed as 30-minute block averages.

- Ancillary data
  - Co-located COSMOS-UK station data merged for comprehensive meteorology and soil observations.
  - Net radiation (Rnet) and components (SWin, SWout, LWin, LWout); soil heat flux (G); soil water content (VWC) and soil temperatures (Ts); precipitation (Pluvio 2).
  - All ancillary data provided as 30-minute means.

- Data processing and quality control
  - EddyPRO® Flux Calculation Software Version 6.1 used; includes conditioning, coordinate rotation, spectral corrections, humidity corrections, and boost-bug correction.
  - Quality control: flags per flux (0 = high quality, 1 = acceptable, 2 = poor); H and τ fluxes with QC > 1 are excluded.
  - Random uncertainties estimated for H and τ; weekly visual checks and manual cleaning.
  - H fluxes excluded if outside the range of -200 to 600 W m^-2 (as per dataset rules).

- Data structure and format
  - Single CSV file: WythamWoodsMicromet_v1.0.csv, time series from 201406-13 13:00 to 2016-01-04 22:00.
  - Missing data indicated by -9999.
  - Variables include: H, rand_err_H, qc_H, τ (Tau), rand_err_Tau, qc_Tau, wind_speed, max_wind_speed, wind_dir, Ustar, TKE, Tstar, L, zL, footprint metrics (X_peak, X_10, X_30, X_50, X_70, X_90 and related distances), radiation components (SW in/out, LW in/out, R net), SHF (soil heat flux), Ta, RH, Pa, Ts, VWC, Precip, and additional metadata.

- Nature of recorded values and units
  - Fluxes in W m^-2 (H), τ in kg m^-1 s^-2; wind speeds in m s^-1; stability metrics (L, z/L) in m and dimensionless form; temperatures in °C; soil moisture in %; precipitation in mm per 0.5 h.

- Usage and provenance
  - Data collected with support from NERC; ancillary data from COSMOS-UK; site access permissions via University of Oxford.
  - Acknowledgments and key references provided for processing steps, QC, footprint modeling, and site context.

- Key considerations for analysts
  - Only flux observations with QC flag 0 or 1 are generally suitable; QC flag 2 are excluded by default.
  - 30-minute resolution; consider footprint and stability (L, z/L) when interpreting fluxes.
  - Use ancillary variables (Rnet, SWin/LWin/LWout, G, Ts, VWC, Precip) to investigate energy balance and soil–atmosphere coupling.
  - Data gaps exist due to QC and instrument downtime; missing values marked as -9999.