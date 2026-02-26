# Measurements of isoprene mixing ratios and fluxes

## Overview
- Measurements of isoprene mixing ratios and fluxes were conducted from June 8 to July 21, 2015 at Auchencorth Moss, Scotland (peatbog site, ~270 m above sea level; coordinates 55°47'32.4" N, 3°14'35.3" W).
- Instrumentation focused on eddy covariance flux measurements using a quadrupole PTR-MS, paired with an ultrasonic anemometer for wind measurements.
- Data aim to enable calculation of isoprene fluxes and support analysis of biogenic VOC exchange over a peatland ecosystem.

## Site description
- Location: Auchencorth Moss, ~4.4 km southwest of Penicuik, Scotland.
- Environment: Ombrotrophic peatbog with a mixture of peatland and grassland.
- Site area: described as approximately 5.6 km^2 in the document.
- Inlet setup: PTR-MS sampling along a 15 m 1/4" O.D. (I.D. 4 mm) PFA tubing; inlet positioned 5 cm below the ultrasonic anemometer at 3.1 m above ground.

## Measurements and instrumentation
- PTR-MS: operating under stable drift-tube conditions (E/N ≈ 110 Td) with calibrated VOC-free air supplying instrument background checks.
- Calibration: isoprene calibrated against a gas standard (~1 ppmv) at start and end of measurement period; three-point calibration in 0–20 ppb range; average instrument sensitivity ≈ 2.6 ncps/ppb.
- Other measurements: ambient temperature, photosynthetically active radiation (PAR), sensible heat flux, wind speed/direction, friction velocity.
- Data processing: concentration data background-subtracted hourly using zero-air checks.

## Flux calculation and time alignment
- Fluxes computed using eddy-covariance methods with a two-dimensional rotation to ensure mean vertical wind velocity is zero.
- Time lag: initial Δt determined (2.6 seconds found to be appropriate) and later fixed to 2.6 seconds to avoid bias from scanned maxima in covariance calculations.
- Averaging: fluxes calculated over 25-minute periods; periods with flux < 200 μg m^-2 h^-1 removed to improve signal-to-noise.
- Post-processing: whole dataset reprocessed with prescribed 2.6 s lag.

## Quality assessment and corrections
- Background correction: instrument background subtracted using hourly zero-air checks.
- High-frequency attenuation: corrected fluxes for loss of flux due to eddies above the PTR-MS 5 Hz response using a frequency-domain attenuation factor involving Fm, τc, and α.
- Stationarity checks: 25-minute fluxes compared with the mean of the five preceding five-minute fluxes; percentage difference used to flag non-stationary periods.
- Integral turbulence statistics: assessed using σw/u* against predicted values based on z/L; poor quality flagged when deviations exceeded ~250%.
- Data retention: all data retained with users free to apply their own quality thresholds; missing flux periods indicated by instrument downtime or insufficient data points.

## Data structure and units
- Date & Time: UTC (dd/mm/yyyy hh:mm:ss)
- Isoprene mixing ratio: ppbv
- Isoprene flux: μg m^-2 h^-1
- Random error: μg m^-2 h^-1
- Flux limit of detection: μg m^-2 h^-1
- Temperature: °C
- PAR: μmol m^-2 s^-1
- Sensible heat flux: W m^-2
- Friction velocity: m s^-1
- Wind speed: m s^-1
- Wind direction: degrees from North
- Stationarity test: % difference
- Turbulence statistics test: % difference

## Notes on data quality and usability
- The dataset includes detailed QA/QC metadata (stationarity results and turbulence statistics) to help end users assess data suitability for their analyses.
- It provides uncertainties (random errors) and detection limits for each flux measurement, enabling proper interpretation and downstream analysis.
- The data are suitable for self-service analysis of isoprene fluxes in peatland environments and can be integrated with ancillary meteorological measurements for flux interpretation.

## References informing QA and methods
- Langford et al. 2015 (eddy-covariance data with low S/N: time-lag determination, uncertainties, LOD)
- Horst 1997; Davison et al. 2009; Foken & Wichura 1996; Foken et al. 2004
- Methodological sources underpining stationarity and turbulence statistics quality assessments