# Site Description

- Measurements of isoprene mixing ratios and fluxes were conducted from 8 June to 21 July 2015 at Auchencorth Moss, Scotland (55°47'32.4" N, 3°14'35.3" W; 270 m above sea level), a peatbog site located 4.4 km southwest of Penicuik. The area is described as 5,612 km² with peatland making up 85% of the landscape.

- In situ setup:
  - Eddy covariance flux measurements using a quadrupole PTR-MS (IONICON) operated with a sampling path of 15 m along 1/4" O.D. (I.D. 4 mm) PFA tubing at ~10 L min⁻¹.
  - Inlet positioned 5 cm below an ultrasonic anemometer at 3.1 m above ground.
  - PTR-MS operating conditions: E/N = 110 Td; drift tube pressure 196 Pa; voltage 450 V; temperature 331 K.
  - VOC-free air supplied via a zero-air generator (GC-1500) with a catalyst heated to 250°C to monitor and subtract instrument background.

- Calibration and sensitivity:
  - Isoprene calibrations at the start (09/06/2015) and end (15/07/2015) using a ~1 ppmv standard diluted to a 0–20 ppb range (three-point calibration).
  - Average instrument sensitivity: 2.6 ncps/ppb, applied across the measurement period.

- Flux computation:
  - Fluxes calculated with eddy-covariance after a two-dimensional rotation to set average vertical wind velocity to zero.
  - Initial approach used an absolute maximum in the cross-covariance for each 25-minute period; later reprocessed with a fixed 2.6 s time lag (∆t) to reduce bias, following Langford et al. (2015).
  - Periods with fluxes below 200 μg m⁻² h⁻¹ were removed to improve signal-to-noise and a time lag of 2.6 s was retained for final processing.
  - Random flux error (RE) estimated via Langford et al. (2015) method and converted to a 95% confidence limit using a factor of 1.96.

- Quality assessment and data correction:
  - Processing performed in a LabVIEW-based package; instrument background subtracted hourly using measurements from the zero-air generator.
  - Flux corrections applied for attenuation due to eddy fluxes with frequencies above the 5 Hz PTR-MS response time, using a frequency-domain attenuation correction dependent on the characteristic time τc and a frequency term fm.
  - Displacement height used: d = 0.27 m (derived from canopy height h = 0.4 m, via d = 2h/3).
  - Stationarity checks (Foken & Wichura): compare 25-minute flux with the five 5-minute fluxes within the same period; non-stationary if differences exceed ~60%.
  - Turbulence statistics quality check (σw/u*): compare measured σw/u* to predictions from Monin-Obukhov similarity; poor quality when deviations exceed ~250%.
  - Stability-dependent parameters (C1, C2) for σw/u* are provided in Table 1 (values depend on z/L; e.g., z/L in 0 to -0.032 range: C1 ≈ 1.3, C2 ≈ 0; z/L < -0.032: C1 ≈ 2.0, C2 ≈ 1/8).
  - All data retained; missing flux periods attributed to instrument downtime or insufficient data points. Users can apply their own quality thresholds if desired.

- Data structure and units:
  - Date & Time: UTC (dd/mm/yyyy hh:mm:ss)
  - Isoprene mixing ratio: ppbv
  - Isoprene flux: μg m⁻² h⁻¹
  - Random error: μg m⁻² h⁻¹
  - Flux limit of detection: μg m⁻² h⁻¹ (1.96 × random error)
  - Temperature: °C
  - Photosynthetically active radiation (PAR): μmol m⁻² s⁻¹
  - Sensible heat flux: W m⁻²
  - Friction velocity: m s⁻¹
  - Wind speed: m s⁻¹
  - Wind direction: degrees from North
  - Stationarity test: % difference
  - Turbulence statistics test: % difference

- References:
  - Langford B, Acton W, Ammann C, Valach A, & Nemitz E (2015). Eddy-covariance data with low signal-to-noise ratio: time-lag determination, uncertainties and limit of detection. Atmospheric Measurement Techniques.
  - Horst TW (1997). A simple formula for attenuation of eddy fluxes measured with first-order-response scalar sensors. Boundary-Layer Meteorology.
  - Davison B, et al. (2009). Concentrations and fluxes of biogenic VOCs above a Mediterranean macchia ecosystem. Biogeosciences.
  - Foken T & Wichura B (1996). Tools for quality assessment of surface-based flux measurements. Agricultural and Forest Meteorology.
  - Foken et al. (2004). Post-field data quality control. Handbook of Micrometeorology.