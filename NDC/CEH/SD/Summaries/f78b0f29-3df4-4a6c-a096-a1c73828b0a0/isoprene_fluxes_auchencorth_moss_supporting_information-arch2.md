# Site Description

- Location and site characteristics
  - Auchencorth Moss, 55°47'32.4" N, 3°14'35.3" W, 270 m above sea level
  - Ombrotrophic peatbog with ~85% peatland and surrounding grassland; area around 5,612 km2
  - Measurement period: 8 June to 21 July 2015

- Measurements and instrumentation
  - Isoprene measurements by eddy covariance using a quadrupole PTR-MS (IONICON)
  - Air sampled through 15 m of 1/4" O.D. PFA tubing at ~10 L min-1
  - Inlet positioned 5 cm below an ultrasonic anemometer at 3.1 m above ground
  - PTR-MS operated with E/N ratio of 110 Td; drift tube 196 Pa, 450 V, 331 K
  - VOC-free air supplied via a zero-air generator to monitor instrument background
  - Calibration against a ~1 ppmv isoprene gas standard, diluted to 0–20 ppb, at start (09/06/2015) and end (15/07/2015)

- Data products and outputs
  - Isoprene mixing ratio (ppbv) and isoprene flux (μg m-2 h-1)
  - Random error (μg m-2 h-1) and flux limit of detection (1.96 × random error)
  - Auxiliary measurements: temperature (°C), photosynthetically active radiation (μmol m-2 s-1), sensible heat flux (W m-2), friction velocity (m s-1), wind speed (m s-1), wind direction (° from North)
  - Quality indicators: stationarity test (% difference) and turbulence statistics test (% difference)

- Flux calculation and data processing
  - Fluxes computed from cross-covariance with a two-dimensional rotation to set average vertical wind to zero
  - Initial fluxes per 25-minute averaging period; filtered to remove periods with flux < 200 μg m-2 h-1
  - Time lag Δt determined as 2.6 seconds (via cross-covariance peak analysis) and reprocessed with this fixed lag to avoid bias
  - Random flux error (RE) estimated as per Langford et al. (2015) and scaled to 95% confidence (LOD = 1.96 × RE)

- Quality assurance and corrections
  - Data processed with a custom LabVIEW analysis package; hourly instrument background subtraction
  - Attenuation correction for high-frequency flux parts exceeding PTR-MS 5 Hz response
  - Displacement height and canopy height used to derive correction parameters (e.g., d = 2h/3 with h = 0.4 m → d = 0.27 m)
  - Stationarity assessment following Foken and Wichura (1996): compare 25-min flux to the average of five 5-min fluxes; non-stationary flagged if >60% difference
  - Turbulence statistics quality check using σw/u* against Monin–Obukhov predictions; z/L stability parameter with coefficients C1 and C2 (Table 1 values)
  - Data retention: all data kept; users may apply their own quality thresholds; missing flux periods result from instrument downtime or insufficient data points

- Data structure and units
  - Date & Time: UTC (dd/mm/yyyy hh:mm:ss)
  - Isoprene mixing ratio: ppbv (column 0)
  - Isoprene flux: μg m-2 h-1 (column 2)
  - Random error: μg m-2 h-1 (column 3)
  - Flux LOD: μg m-2 h-1 (column 4)
  - Temperature: °C (column 5)
  - PAR: μmol m-2 s-1 (column 6)
  - Sensible heat flux: W m-2 (column 7)
  - Friction velocity: m s-1 (column 8)
  - Wind speed: m s-1 (column 9)
  - Wind direction: degrees from North (column 10)
  - Stationarity test: % difference (column 11)
  - Turbulence statistics test: % difference (column 12)

- References (method and QA context)
  - Langford et al. 2015: cross-covariance time-lag, uncertainties, and LOD for low S/N data
  - Horst 1997; Davison et al. 2009; Foken & Wichura 1996; Foken et al. 2004 (QA methodologies and flux corrections)