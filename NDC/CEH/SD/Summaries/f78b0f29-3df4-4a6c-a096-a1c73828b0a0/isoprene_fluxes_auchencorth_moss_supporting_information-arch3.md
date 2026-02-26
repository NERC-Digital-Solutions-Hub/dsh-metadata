Measurements of isoprene mixing ratios and fluxes at Auchencorth Moss (8 June – 21 July 2015)

## Overview and site description
- Auchencorth Moss is an ombrotrophic peat bog near Penicuik, Scotland (55°47'32.4" N, 3°14'35.3" W; 270 m a.s.l.).
- Site composition: ~85% peatland with some grassland; area documented as 5,612 km2.
- Objective: measurements of isoprene mixing ratios and fluxes to understand environmental health and atmospheric exchange processes.

## Instrumentation and sampling setup
- Eddy covariance flux measurements using a quadrupole PTR-MS (IONICON) to quantify isoprene.
- Air sampled through 15 m of 4 mm ID PFA tubing at ~10 L/min; inlet located 5 cm below a 3.1 m high ultrasonic anemometer.
- PTR-MS operated to maintain a fixed E/N ratio of 110 Td; VOC-free air supplied via a zero-air generator to monitor instrument background.
- Calibration against a gas standard at the start and end of the period; calibration range 0–20 ppb isoprene with ~1 ppmv standard.

## Calibration and data processing
- Instrument sensitivity averaged from start and end calibrations: 2.6 ncps/ppb.
- Flux calculation: 25-minute averaging periods with a two-dimensional rotation to set average vertical wind to zero; time lag between sampling and analysis determined as 2.6 seconds.
- Flux estimates derived from cross-covariance, with post-processing to remove low signal-to-noise periods (fluxes below 200 μg m−2 h−1 discarded).
- Data reprocessed with a fixed time lag to minimize bias from drift in the covariance search.

## Quality assessment and corrections
- Data processed with a LabVIEW-based analysis package; hourly instrument background subtraction using zero-air samples.
- Flux attenuation corrected for eddies with frequencies above PTR-MS 5 Hz response, based on a specified correction equation.
- Stationarity checks (per Foken & Wichura) compare 25-minute fluxes with the mean of five 5-minute fluxes; large deviations indicate non-stationarity.
- Integral turbulence statistics checks (e.g., normalized vertical wind speed variance, σw/u*) compared to predictions from stability-adjusted models using Monin-Obukhov length L and height z.
- Table 1 (C1, C2 coefficients) provides stability-dependent parameters; data retained across tests, with missing periods attributed to instrument downtime or insufficient data points.
- Note: Users can apply their own quality thresholds when interpreting the dataset.

## Data structure and units
- Date and time: UTC; columns indexed for each variable.
- Isoprene mixing ratio: ppbv.
- Isoprene flux: μg m−2 h−1.
- Random error and flux limit of detection: μg m−2 h−1.
- Meteorological and QA metrics: temperature (°C), photosynthetically active radiation (μmol m−2 s−1), sensible heat flux (W m−2), friction velocity (m s−1), wind speed (m s−1), wind direction (degrees from North).
- QA metrics: stationarity test (% difference) and turbulence statistics test (% difference).

## Outputs and relevance for monitoring frameworks
- Provides quantified isoprene mixing ratios and surface fluxes with associated random errors and LODs, enabling evaluation of biological/atmospheric interactions.
- Demonstrates a structured QA/QC workflow: background subtraction, attenuation correction, stationarity checks, and turbulence statistics consistency – aligning with standard governance and data quality expectations.
- Includes metadata on measurement height, sensor configuration, calibration procedure, and data processing steps, supporting transparency and reproducibility.
- Data format and detailed documentation (units, column indices) facilitate integration into monitoring dashboards, reports, and policy-relevant summaries.

## References
- Langford B, Acton W, Ammann C, Valach A, & Nemitz E (2015). Eddy-covariance data with low signal-to-noise ratio: time-lag determination, uncertainties and limit of detection. Atmospheric Measurement Techniques.
- Horst TW (1997). A simple formula for attenuation of eddy fluxes measured with first-order-response scalar sensors. Boundary-Layer Meteorology.
- Davison B, et al. (2009). Concentrations and fluxes of biogenic VOCs above a Mediterranean macchia ecosystem. Biogeosciences.
- Foken T & Wichura B (1996). Tools for quality assessment of surface-based flux measurements. Agricultural and Forest Meteorology.
- Foken T, et al. (2004). Post-field data quality control. In Handbook of Micrometeorology.