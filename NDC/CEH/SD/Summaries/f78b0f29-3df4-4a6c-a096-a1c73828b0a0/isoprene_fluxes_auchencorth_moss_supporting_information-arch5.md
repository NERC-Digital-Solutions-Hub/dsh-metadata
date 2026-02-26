# Measurements of isoprene mixing ratios and fluxes

## Site Description
- Timeframe: 8 June – 21 July 2015
- Location: Auchencorth Moss, 55°47'32.4" N, 3°14'35.3" W, 270 m a.s.l.
- Environment: Ombrotrophic peatbog near Penicuik, Scotland; site composition ~85% peatland with grassland, area 5,612 km²

## Measurements and Methods
- Instrumentation: Eddy-covariance flux measurements using a quadrupole PTR-MS (IONICON) for isoprene
- Sampling: Air drawn through ~15 m of 1/4" PFA tubing at ~10 L min⁻¹; inlet 5 cm below an ultrasonic anemometer at 3.1 m
- PTR-MS conditions: Constant E/N = 110 Td; drift tube pressure 196 Pa, 450 V, 331 K
- Background monitoring: VOC-free air via zero-air generator with catalytic purifier; hourly background checks
- Calibration: Two calibrations (start 09/06/2015 and end 15/07/2015) with ~1 ppmv isoprene standard diluted to 0–20 ppbv; average sensitivity 2.6 ncps/ppbv
- Data processed with a LabVIEW analysis package; concentration data background-subtracted

## Flux Calculation and Time Lag
- Flux calculation: 25-minute averaging periods using a two-dimensional rotation to set average vertical wind velocity to zero
- Time lag: Initial Δt determined from cross-covariance peak; after filtering (>200 μg m⁻² h⁻¹), a fixed Δt of 2.6 s was applied per Langford et al. to avoid bias
- Random error and detection: Random flux error (RE) estimated per Langford et al. and converted to a 95% detection limit (1.96 × RE)
- Quality filter: Periods with flux < 200 μg m⁻² h⁻¹ removed from analysis

## Quality Assurance and Corrections
- Background subtraction: Instrument background subtracted hourly
- High-frequency attenuation: Flux attenuation corrected for eddies with frequency > PTR-MS 5 Hz response; correction uses a specified attenuation function with τc and α
- Stationarity checks: 
  - 25-minute fluxes compared to five 5-minute fluxes; large percentage differences (>60%) flagged as non-stationary
  - Integral turbulence statistics: σw/u* compared to predictions from Monin-Obukhov similarity; poor quality data flagged if divergences > 250%
- Data quality notes: Results of stationarity and turbulence tests provided as percentage differences; all data retained for user-defined QA thresholds
- Gaps: Missing flux periods due to instrument downtime or insufficient data points within averaging periods

## Data Structure and Units
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
- Columns: 0–12 (13 total)

## Data Use and Governance Considerations
- Data are documented with clear metadata (units, column indices, processing steps) to facilitate discoverability and reuse
- QA/QC procedures are described to inform data quality assessments and potential reprocessing
- Results are suitable for incorporation into broader datasets with standardised metadata and interoperability considerations
- When integrating with other datasets, users should apply their own QA thresholds consistent with project requirements

## References
- Langford, Acton, Ammann, Valach, & Nemitz (2015) on eddy-covariance data and time-lag determination
- Horst (1997) on attenuation of eddy fluxes for first-order sensors
- Davison et al. (2009); Foken & Wichura (1996); Foken et al. (2004) for quality assessment and turbulence statistics