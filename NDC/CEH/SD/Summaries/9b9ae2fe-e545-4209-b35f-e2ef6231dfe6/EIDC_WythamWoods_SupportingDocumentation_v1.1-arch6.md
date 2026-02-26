# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

## Overview
- Time-series dataset of turbulent surface-atmosphere exchanges: sensible heat (H) and momentum (τ) measured above an ancient broadleaved deciduous forest in Oxfordshire, UK.
- Collected using eddy covariance (EC) at 27 m height, from 2014-06-13 13:00 to 2016-01-04 22:00.
- Includes ancillary weather and soil observations, plus variables describing turbulence and QC for the flux observations.
- Data are processed to thirty-minute flux averages with quality control and uncertainty estimates; outputs suitable for self-service analysis and visualization.

## Study site
- Location: Wytham Woods flux observation site (51.77°N, -1.33°W), within ~400 ha of ancient deciduous forest, ~5 km NW of Oxford.
- Climate: temperate maritime; mean annual ~10.1°C and ~730 mm precipitation.
- Forest canopy and flux tower: canopy ~20 m tall; flux tower on the north-facing slope; 27 m measurement height.
- Surroundings: area dominated by Pedunculate Oak, Ash, and Sycamore; soil types range from poorly to well-drained clays over sandstone.

## Sampling regime and data acquisition
- Fluxes and micrometeorological observations collected above the canopy at 27 m.
- Instruments: Windmaster sonic anemometer thermometer; raw 20 Hz EC data; 30-minute means for Ta (air temperature) and RH.
- Ancillary data from COSMOS-UK station merged with site data; includes net radiation and soil/precipitation measurements.
- Continuous data collection with 30-minute averaging periods for fluxes and ancillary variables.

## Data processing
- Flux calculation: EddyPRO v6.1; 30-minute block averages; includes:
  - Corrections for boost-bug in vertical wind, angle of attack, tilt/coordinate rotation, high/low-frequency attenuation, and humidity effects on H.
  - Uncertainty estimates for H and τ (per Finkelstein & Sims).
  - Derived metrics: friction velocity (u*), Turbulent Kinetic Energy (TKE), temperature scaling (T*), Obukhov length (L), stability parameter (z/L), and flux footprint.
- Quality control: QC flags per flux (0 = high quality, 1 = acceptable, 2 = poor). Outliers removed using median absolute deviation and range checks (-200 < H < 600 W m^-2 for H; QC > 1 fluxes excluded).
- Users can choose to filter by QC and other quality metrics (e.g., footprint, u*).

## Data structure and content
- Single CSV file with a complete 30-minute time-series from 2014-06-13 13:00 to 2016-01-04 22:00.
- Missing records indicated by -9999.
- Variables described in the accompanying table (names/units adapted from Li-COR). Key fields include:
  - DateTime
  - H, rand_err_H, qc_H
  - Tau, rand_err_Tau, qc_Tau
  - Wind speed and direction (wind_speed, max_wind_speed, wind_dir)
  - Ustar, TKE, Tstar, L, zL, X_peak, X_10, X_30, X_50, X_70, X_90 (footprint-related metrics)
  - Radiation: SW in, SW out, LW in, LW out, R net
  - Soil heat flux (SHF_1, SHF_2)
  - Air/soil conditions: Ta, RH, Pa, Ts_1, Ts_2, VWC_1, VWC_2
  - Precip
- Data are self-contained with ancillary data merged from COSMOS-UK.

## Data quality and notes
- QC-driven cleansing employed; final use may depend on user needs and QC thresholds.
- Data quality relies on proper processing steps and corrections for EC methodology; “patchy” data and instrument-specific issues acknowledged.
- Final data users should consider footprint estimates and u* filters when interpreting flux results.

## Access and acknowledgments
- Data collection funded by the Natural Environment Research Council (NERC); ancillary COSMOS-UK data provided.
- Acknowledgments extend to site access permissions, technical support, and maintenance of instrumentation.

## References
- Cited methodological and site-context references for EDdyPRO processing, QC methods, instrumentation, and site description (listed in the document).