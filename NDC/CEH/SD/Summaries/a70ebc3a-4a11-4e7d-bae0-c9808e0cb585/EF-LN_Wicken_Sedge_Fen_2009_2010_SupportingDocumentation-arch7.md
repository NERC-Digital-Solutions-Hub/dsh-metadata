# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010 Jon Kelvin, Mike Acreman, Richard J. Harding & Ross Morrison

## Overview
- Time series of land–surface–atmosphere exchanges at Wicken Sedge Fen (EF-LN) in Cambridgeshire, UK.
- Variables include net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ), along with atmospheric turbulence diagnostics.
- Data collected in 30-minute flux averaging periods during 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16.
- Ancillary meteorological and soil physics observations accompany flux data.
- Processed with standardized eddy-covariance procedures; gap-filled and partitioned NEE into GEP and TER where possible.

## Study site
- Wicken Sedge Fen (EF-LN), 52° 18' 34.86" N, 0° 16' 47.01" E; 2 m above mean sea level.
- Conservation-managed rich fen within the Wicken Fen National Nature Reserve, Cambridgeshire, UK.
- Climate: temperate maritime; mean annual temperature ~10.7°C, mean annual precipitation ~563 mm (1981–2010).
- Peat depth ~2–4 m; hydrologically isolated from surrounding arable land; calcareous water from Monks Lode boundary.
- Site metadata includes peat bulk density, pH, C content, and C:N ratio.

## Sampling regime and data collection
- Automated measurements of flux, meteorology, and soil physics.
- Fluxes measured 3.95 m above grass canopy using an open-path eddy covariance system (Solent R3 ultrasonic anemometer + LI-7500).
- Raw 20 Hz data logged with a CR3000 Micrologger; auxiliary variables sampled at appropriate sensors (temperatures, radiation, soil heat flux, etc.).

## Data processing and quality control
- Flux calculations performed with EddyPRO software (v7.0.6) to produce 30-minute flux densities.
- Processing includes:
  - QC of raw data, angle-of-attack correction, 2D coordinate rotation, corrections for high/low-frequency co-spectral attenuation.
  - Density corrections for heat and water vapor, and adjustments to LE and CO2 for density fluctuations.
  - Calculation of ancillary metrics (wind speed/direction, u*, TKE, Obukhov length, stability).
- Quality control criteria include removal of statistical outliers and flux values outside established ranges; NEE QC includes night-time negative flux checks, friction velocity threshold, and flux-footprint checks.
- Random uncertainties computed for each 30-minute flux observation.

## Data gaps, gap-filling, and flux partitioning
- Gaps in EC data (NEE, LE, H) filled using Marginal Distribution Sampling.
- NEE partitioned into GEP and TER using Ta-driven algorithms (REddyProc in R).
- Where possible, missing meteorological data filled using readings from the on-site automated weather station.

## Data structure and units
- Data provided as a single CSV with columns described in Table 1.
- Time series spans 2009-01-01 to 2011-01-17 (gap-filled and partitioned data end-to-end); actual flux data collected during defined windows in 2009 and 2010–2011.
- Missing records denoted by -9999.
- Key variables and units include:
  - NEE (μmol CO2 m−2 s−1), LE (W m−2), H (W m−2), τ (kg m−1 s−2)
  - CO2 storage term, Ta (°C), RH (%), VPD (hPa)
  - Radiation components (SWin, SWout, LWin, LWout, Rnet)
  - Soil heat flux at two locations (G1, G2), wind speed/direction, u*, TKE, L, zL, Xpeak/x70/x90, fp2D (fractional footprint from target ecosystem)
  - NEE_filled, LE_filled, H_filled and their associated uncertainties
- Columns derived from LI-COR and Reichstein et al. processing standards.

## GIS-relevant notes
- Provides precise site coordinates and measurement height, enabling spatial integration with other GIS layers (e.g., land cover, hydrology).
- Offers time-resolved, gap-filled flux data and partitioned components (GEP, TER) suitable for landscape carbon balance mapping over time.
- Data quality and footprint metrics included, aiding confidence assessments when integrating with spatial analyses.

## Acknowledgments and references
- Supported by Natural Environment Research Council (UK-SCAPE) and local partnerships; site access and installation permissions acknowledged.
- References detail methodologies and processing standards used (EddyPRO, QC approaches, gap-filling and partitioning algorithms).