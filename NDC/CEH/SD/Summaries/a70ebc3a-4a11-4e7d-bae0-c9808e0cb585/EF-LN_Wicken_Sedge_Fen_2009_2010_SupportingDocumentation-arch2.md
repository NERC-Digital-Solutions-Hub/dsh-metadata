# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010 Jon Kelvin, Mike Acreman, Richard J. Harding & Ross Morrison

## Overview
- Time series of land–surface atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at Wicken Sedge Fen (EF-LN) in Cambridgeshire, UK.
- Data collected via open-path eddy covariance (EC) between 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16.
- Includes ancillary meteorological and soil physics observations and variables describing atmospheric turbulence.

## Study site
- Wicken Sedge Fen (EF-LN) flux site: 52° 18' 34.86" N, 0° 16' 47.01" E, 2 m above mean sea level.
- Climate: temperate maritime; mean annual air temperature ~10.7°C and precipitation ~563 mm year−1 (1981–2010).
- Environment: largest remaining semi-natural fenland on undrained deep peat in East Anglia; peat depth ~2–4 m; hydrologically isolated from surrounding cropland.
- Primary water source: Monks Lode (eastern boundary). Peat properties: bulk density ~0.37 g cm−3, pH ~7.5, C content ~32%, C:N ~15.
- Site code: EF-LN; references to detailed flux site descriptions.

## Sampling regime
- Automated flux, meteorological, and soil measurements conducted during two periods within 2009–2011 (specific dates above).
- Flux measurements at 3.95 m height above a grass canopy using an open-path EC system.
- Sensor setup included an ultrasonic anemometer/thermometer and a CO2 gas analyzer; data loggers operated at 20 Hz.

## Flux data acquisition
- Fluxes measured: NEE (μmol CO2 m−2 s−1), H (W m−2), LE (W m−2), and τ (kg m−1 s−2).
- Instruments: Solent R3 ultrasonic anemometer + LI-7500 CO2 sensor; data logged by a CR3000 Micrologger.
- Raw data include three turbulent velocity components, sonic temperature, humidity, and CO2 density.

## Ancillary data acquisition
- Meteorological: air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (Rnet) and its shortwave/longwave components.
- Soil physics: soil heat fluxes (G) at two locations (0.03 m depth); soil temperature near the surface (0.1 m depth).

## Data processing
- Flux calculations with EddyPRO software (v7.0.6); 30-minute averaging windows.
- Processing steps include quality control of 20 Hz data, tilt/coordinate rotation, spectral corrections, density corrections, and calculation of derived variables (u*, TKE, L, z/L, etc.).
- Random uncertainty estimated for each 30-minute flux.
- Additional outputs include wind speed/direction, friction velocity, and footprint characteristics.

## Quality control
- Outlier removal and testing based on EC theory; thresholds applied to fluxes:
  - H: −200 to 550 W m−2
  - LE: −60 to 600 W m−2
  - NEE: −50 to 30 μmol CO2 m−2 s−1
- Nighttime NEE excluded when negative flux or low friction velocity (u* < 0.18 m s−1) or insufficient footprint from target ecosystem (<80%).
- Weekly visual checks to remove any remaining clearly erroneous values.

## Data gap-filling and flux partitioning
- Gaps in EC data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into GEP and TER using Ta as driver (no soil temperature data at site) following Reichstein et al. (2005).
- Gap-filling and partitioning performed with REddyProc (R package; Reichstein et al., 2016); where possible, meteorological gaps filled using local automated weather station data.

## Details of data structure
- Data provided as a single CSV with tabular format; gap-filled and partitioned flux and ancillary data cover 2009-01-01 to 2011-01-17.
- Original flux data were collected during defined periods within 2009 and 2010; missing records due to system issues are marked as -9999.
- Table 1 (described in the document) lists variable names, descriptions, and units for the 30-minute time series (variables include NEE, LE, H, Tau, Ta, RH, VPD, radiation components, soil variables, wind metrics, U*, TKE, L, zL, footprint metrics, and gap-filled fluxes).

## Nature and units of recorded values
- Variables and units are standardized for micrometeorological flux measurements (e.g., NEE in μmol CO2 m−2 s−1; LE, H in W m−2; Ta in °C; RH in %; VPD in hPa; flux-related QA/flags and derived components included).

## Acknowledgments and references
- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE; site access granted by National Trust and Wicken Fen staff.
- References provided for methodological background and processing tools (e.g., EddyPro, Reichstein et al. methods, REddyProc, and quality control standards).