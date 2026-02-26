# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview
- Time series of surface-atmosphere fluxes: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ), plus ancillary weather and soil observations.
- Study area: winter wheat field in Lincolnshire, UK; data from the 2012 growing season.
- Measurements: eddy covariance (EC) observations from 2012-04-05 00:30 to 2012-08-08 00:00 UTC, logged at 20 Hz and averaged to 30-minute intervals.
- Data products include both raw/quality-controlled fluxes and gap-filled/partitioned fluxes (GEP and TER) and related variables.

## Study site
- Location: flux tower at arable cropland, approximately 10 km north of Lincoln, UK (53°19'17.89"N, 0°35'7.83"W).
- Climate: temperate maritime; mean 1981–2010 air temperature ~9.8°C and precipitation ~614 mm year-1.
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; soil bulk densities ~1.46–1.53 g cm^-3; texture ~49% sand, 36% silt, 15% clay; soil pH ~6.32.
- Flux tower setup: EC system at 3.0 m height, centered in the field.

## Sampling regime and flux data acquisition
- Instruments: open-path EC system with R3 sonic anemometer and LI-7500 CO2/H2O infrared gas analyser.
- Data collection: raw 20 Hz measurements of turbulent variables and gas concentrations; logged with CR3000 Micrologger.
- Ancillary measurements co-located with flux tower: net radiation, soil heat flux, air temperature, relative humidity, soil temperature, soil moisture, rainfall.
- Data are provided as a continuous 30-minute time series, with missing records encoded as -9999.

## Ancillary data
- Radiation: SWin, SWout, LWin, LWout; Rnet.
- Soil heat flux: G at two locations.
- Weather/meteorology: Ta, RH, VPD, wind speed (Windspeed), wind direction (Winddir), friction velocity (Ustar), turbulence metrics (TKE), Obukhov length (L) and z/L.
- Soil: soil temperature (Tsoil) at 0.05 m and 0.1 m; soil volumetric water content (VWC) at 0.05 m and 0.1 m.
- Precipitation: rain gauge data; 0.5 mm sensitivity.
- Data are logged as 30-minute means.

## Data processing
- Flux calculation: EddyPRO software (Version 6.1) used to compute NEE, H, LE, and τ with standard micrometeorological corrections.
- Quality control: QC of 20 Hz data, angle-of-attack correction, 2D rotation, corrections for spectral attenuation and density effects, and uncertainty estimation.
- Data screening: outlier removal via median absolute deviation; non-stationary conditions removal; flux value bounds applied:
  - H: -200 to 400 W m^-2
  - LE: -100 to 500 W m^-2
  - NEE: -70 to 35 μmol CO2 m^-2 s^-1
- Representativeness: footprint analysis via a simple analytical footprint model; fluxes considered representative if >75% originated from the target ecosystem.
- Post-processing checks: weekly visual review of flux and ancillary data for clearly erroneous values.

## Gap filling and flux partitioning
- Gap filling: Marginal Distribution Sampling (MDS) approach ( Reichstein et al., 2005).
- Meteorological gaps: filled using linear relationships derived from adjacent fields’ weather stations.
- NEE partitioning: separated into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Reichstein et al. 2005 method, with Ta驱iven partitioning.
- Tools: REddyProc package in R (Reichstein et al., 2016) used for gap-filling and partitioning.

## Data structure and variables
- Primary data file: Lincolnshire_Winter_Wheat_2012.csv containing 30-minute time series from 2012-04-05 00:30 to 2012-08-08 00:00 UTC.
- Gap-filled and partitioned products included:
  - NEE_filled, NEE_filled_sd
  - LE_filled, LE_filled_sd
  - H_filled, H_filled_sd
  - TER, GEP
- Storage terms included (CO2_strg, LE_strg, H_strg) and sunrise/sunset related variables as described in Table 1.
- Additional metadata fields cover standard units and descriptions for each variable (e.g., DateTime in UTC, NEE in μmol CO2 m^-2 s^-1, etc.).
- -9999 used to denote missing values.

## Data quality, provenance, and limitations
- Provenance: measurements and processing follow established EC practices with documented QC and correction steps; metadata describe instruments, processing software, and references for methods.
- Limitations and considerations for use:
  - Data represent a single site and season; applicability to other ecosystems requires caution.
  - Gap-filled data rely on modeled relationships and partitioning algorithms; uncertainty is reported (sd) for filled variables.
  - Footprint representativeness requires that a majority of flux originates from the target ecosystem; value >75% is indicated.
  - QC criteria and thresholds may exclude some valid data under atypical conditions.
  - Data are provided with comprehensive methodological references (e.g., Reichstein et al., Papale et al., Moncrieff et al., Mauder et al.) to support reproducibility.

## Accessibility, licensing, and acknowledgments
- Funded by Natural Environment Research Council (NERC) awards NE/R016429/1 and NE/H010726/1 as part of the UK-SCAPE and Carbo-Biocrop projects.
- Acknowledgments to landowners and individuals contributing to site operations.
- Data processing relies on open/standard tools (EddyPRO, REddyProc) and widely cited methodologies in the micrometeorology community.