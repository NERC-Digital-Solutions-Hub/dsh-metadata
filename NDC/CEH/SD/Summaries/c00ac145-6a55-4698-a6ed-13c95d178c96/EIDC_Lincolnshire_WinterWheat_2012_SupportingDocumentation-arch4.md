# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview of dataset
- Time series observations of surface-atmosphere exchanges (fluxes) for NEE, sensible heat (H), latent heat (LE), and momentum (τ) above a winter wheat crop.
- Measurements span 2012-04-05 00:30 to 2012-08-08 00:00 UTC using the micrometeorological eddy covariance (EC) technique.
- Includes ancillary weather and soil physics data, plus variables describing atmospheric turbulence.

## Study site
- Flux observation site located on arable cropland near Lincoln, UK (53°19'17.89"N, 0°35'7.83"W).
- Temperate maritime climate; mean annual temperature ~9.8°C and precipitation ~614 mm (1981–2010).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk densities ~1.46–1.53 g/cm³; soil texture ~49% sand, 36% silt, 15% clay; pH ~6.32.

## Sampling regime and flux data acquisition
- Automated flux, meteorological, and soil measurements from 2012-04-05 00:30 to 2012-08-08 00:00 GMT.
- EC system installed at 3.0 m height at field center; open-path EC with R3 sonic anemometer and LI-7500 CO2 analyzer.
- Raw data at 20 Hz; logged with CR3000 Micrologger.
- Ancillary meteorological and soil observations co-located with the flux tower; includes net radiation components, soil heat flux, air and soil temperatures, relative humidity, soil moisture, and rainfall.

## Data processing and quality control
- Fluxes calculated with EddyPRO software (v6.1); 30-minute block-averaged.
- Processing steps include: QC of 20 Hz data, tilt/angle corrections, 2D rotation to local terrain, corrections for spectral attenuation, humidity effects on H, density corrections for LE and CO2, and random uncertainties.
- Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).
- QC procedures: outlier removal via median absolute deviation; non-stationary conditions removal; flux range checks; NEE checks with night-time conditions; footprint checks using ART Footprint Tool; weekly visual checks for obvious errors.

## Data gap-filling and flux partitioning
- Gap-filled EC data (NEE, LE, H) using Marginal Distribution Sampling.
- Gaps in key meteorological variables filled via linear relationships from adjacent-field weather stations.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using tensioned partitioning guided by air temperature.
- Gap-filling and partitioning performed with REddyProc (R).

## Details of data structure and recorded values
- Data are provided as a single CSV file with a table of variables described in Table 1.
- Time series start 2012-04-05 00:30 and end 2012-08-08 00:00 (UTC); missing records coded as -9999.
- Variables include:
  - NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc
  - CO2_strg, CO2_strg_unc, LE_strg, LE_strg_unc, H_strg, H_strg_unc
  - Pa (kPa and bar), Ta (°C), RH (%), VPD (hPa)
  - SWin, SWout, LWin, LWout, Rnet
  - G1/G2, Tsoil1–4, VWC1–4, Precipitation, Windspeed, Winddir
  - Ustar, TKE, L, zL
  - FootprintFraction, x_peak, x_70, x_90
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, TER_sd, GEP, GEP_sd
- Variables are standardized to 30-minute time steps; units and names aligned with LI-COR conventions and Reichstein et al. (2016).

## Accessing and using the dataset
- Contains both raw EC measurements and gap-filled/partitioned outputs for comprehensive analysis.
- Suitable for cross-site comparisons, data quality governance assessments, and methodological evaluations in data systems design and management.

## Acknowledgments and references
- Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE; additional support from Carbo-Biocrop project.
- Dataset authors acknowledge landowners and site contributors.
- References include foundational EC processing and QC guidelines and related methodological papers.