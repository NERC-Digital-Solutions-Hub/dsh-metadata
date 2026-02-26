# Measurements of isoprene mixing ratios and fluxes at Auchencorth Moss

## Site description
- Location: Auchencorth Moss (55°47'32.4" N, 3°14'35.3" W), 270 m above sea level, Scotland.
- Environment: Ombrotrophic peatbog with a mix of peatland (85%) and grassland.
- Size: Site area reported as 5,612 km².
- Measurement period: 8 June to 21 July 2015.

## Measurements and instrumentation
- Instrumentation: Eddy covariance flux measurements using a quadropole PTR-MS (IONICON) for isoprene.
- Air sampling: Along 15 m of 1/4" O.D. PFA tubing (~10 L/min); inlet 5 cm below an ultrasonic anemometer at 3.1 m height.
- PTR-MS operating conditions: E/N ratio of 110 Td; drift tube pressure 196 Pa; voltage 450 V; temperature 331 K.
- Clean air: VOC-free air produced by a zero-air generator (heated catalyst) to monitor and subtract instrument background.
- Calibration: Isoprene calibrations at start (09/06/2015) and end (15/07/2015) using a ~1 ppmv standard diluted to 0–20 ppbv; average sensitivity 2.6 ncps/ppbv applied across the period.

## Flux calculation approach
- Flux calculation: Based on a two-dimensional rotation to set average vertical wind velocity to zero; flux F_x(Δt) computed from fluctuations in vertical wind and isoprene concentration.
- Time lag: Determined from cross-covariance; initial Δt of 2.6 s (later used for reprocessing).
- Data filtering: Excluded periods with flux < 200 μg m^-2 h^-1 to improve signal-to-noise.
- Reprocessing: All data reprocessed with a prescribed time-lag of 2.6 s to reduce bias.
- Random error and detection: Random flux error estimated per Langford et al. (2015) and scaled by 1.96 to yield a 95% confidence limit for each flux measurement.

## Data processing and QA
- Processing environment: Custom LabVIEW analysis package.
- Background subtraction: All concentrations corrected by hourly instrument background measurements from the zero-air generator.
- Attenuation correction: Fluxes corrected for eddies with frequencies above the PTR-MS 5 Hz response; attenuation factor derived from a defined integral equation.
- Stationarity checks: Per 25-minute averaging period, flux compared to the mean of five 5-minute fluxes; large differences indicate non-stationarity.
- Turbulence statistics checks: Integrated turbulence statistics (e.g., σ_w/u*) used to gauge data quality; compare measured σ_w/u* with predictions from Monin–Obukhov similarity; poor-quality data typically rejected if deviations exceed ~250%.
- Stability-related parameters: Coefficients C1 and C2 in relation to stability z/L; table provided with values for different stability regimes.

## Data structure and units
- Time: Date & Time in UTC (dd/mm/yyyy hh:mm:ss).
- Isoprene mixing ratio: ppbv (column index 1).
- Isoprene flux: μg m^-2 h^-1 (column index 2).
- Random error: μg m^-2 h^-1 (column index 3).
- Flux limit of detection: μg m^-2 h^-1 (column index 4).
- Temperature: °C (column index 5).
- PAR (photosynthetically active radiation): μmol m^-2 s^-1 (column index 6).
- Sensible heat flux: W m^-2 (column index 7).
- Friction velocity: m s^-1 (column index 8).
- Wind speed: m s^-1 (column index 9).
- Wind direction: Degrees from North (column index 10).
- Stationarity test: % difference (column index 11).
- Turbulence statistics test: % difference (column index 12).

## Data quality notes
- Missing flux periods due to instrument downtime or insufficient data points within averaging periods.
- Data retained with QA resources enabling end-users to apply their own quality thresholds.

## GIS-relevant metadata and usage
- Spatial context: Precise site coordinates and altitude enable mapping within GIS workflows.
- Temporal resolution: 25-minute averaging periods with 2.6 s time lag corrections; suitable for time-series visualization and integration with meteorological layers.
- Variables for mapping: Isoprene mixing ratio, isoprene flux, random error, LOD, temperature, PAR, sensible heat flux, wind speed/direction, and quality flags (stationarity and turbulence statistics).
- Data quality indicators: Stationarity and turbulence statistics differences provide essential QA flags for map-based analyses.
- Potential applications: Visualizing spatial-temporal patterns of isoprene fluxes alongside wind fields, stability maps, and background correction layers; integrating with other GIS-ready datasets for ecosystem-atmosphere interaction studies.

## References
- Langford B, Acton W, Ammann C, Valach A, & Nemitz E (2015). Eddy-covariance data with low signal-to-noise ratio: time-lag determination, uncertainties and limit of detection. Atmospheric Measurement Techniques.
- Horst TW (1997). A simple formula for attenuation of eddy fluxes measured with first-order-response scalar sensors. Boundary-Layer Meteorology.
- Davison B, et al. (2009). Concentrations and fluxes of biogenic VOCs above a Mediterranean macchia ecosystem. Biogeosciences.
- Foken T & Wichura B (1996). Tools for quality assessment of surface-based flux measurements. Agricultural and Forest Meteorology.
- Foken et al. (2004). Post-field data quality control. Handbook of Micrometeorology.