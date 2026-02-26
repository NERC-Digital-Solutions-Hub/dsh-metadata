# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

## Overview
- Time series observations of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Two sites in the East Anglian Fens, England: a cropland site (EF-SA) and a grassland site (EF-GF).
- Fluxes measured with eddy covariance (EC) at 2.6 m height using open-path systems; data collected 2016-11-17 to 2018-09-24 (EF-SA) and 2017-04-27 to 2019-03-31 (EF-GF).
- Ancillary meteorological and soil physics observations and turbulence characteristics accompany EC data.
- Data processed with established QC, corrections, gap-filling, and flux-partitioning workflows.

## Study sites
- Location: East Anglian Fens (Fenland), UK; region with extensive lowland peat soils, historic drainage, and agriculture.
- Climate: temperate maritime; mean 1981–2010 air temperature ~10.4°C and mean precipitation ~564 mm yr−1.
- Cropland (EF-SA): lettuce, celery, cereals; peat degraded peat over clay; drainage via sub-surface pipes and ditches; peat depth 0.75–1.0 m; soil properties described (bulk density, pH, organic C, C/N).
  - Coordinates: 52.44° N, 0.41° E, ~−2 m amsl.
- Grassland (EF-GF): former arable peatland being rewetted/restored; low-intensity grazing; drainage network present but not connected to regional system; peat depth ~2.0 m; soil pH 5.2–6.0; organic C ~30%, total N ~1.4%.
  - Coordinates: 52.47° N, −0.19° E, ~−1 m amsl.

## Data collection and instrumentation
- Flux observations (NEE, H, LE, τ) above canopy using eddy covariance systems at 2.6 m height.
- Instruments:
  - Ultrasonic anemometer thermometer and LI-7500 IR gas analyser (open-path EC).
  - WindMaster ultrasonic (EF-SA) and Solent R3 (EF-GF) for wind measurements.
  - Raw 3-component wind and sonic temperature; H2O and CO2 densities recorded at 20 Hz.
  - Data loggers: CR3000 Microloggers.
- Ancillary sensors co-located with EC stations:
  - Air temperature (Ta) and relative humidity (RH) at 2 m.
  - Net radiation (Rnet) and its components (SWin, SWout, LWin, LWout).
  - Soil heat flux (G) at 0.03 m depth at two locations.
  - Water level relative to surface via vented transducers.
  - Soil moisture (VWC) and soil temperature (Tsoil) at multiple depths (EF-SA and EF-GF have differing depth schemes).
  - Precipitation from dedicated rain gauges (COSMOS-UK at EF-SA; SBS500 at EF-GF).
- Data granularity: 30-minute means for most variables; 20 Hz raw data for QC and processing.

## Data processing and quality control
- Processing software: EddyPRO Version 6.1.
- Flux calculation: 30-minute block averages; QC of 20 Hz data; corrections for:
  - Tilt/angle-of-attack (sonic anemometers).
  - 2D coordinate rotation to align with local terrain.
  - High- and low-frequency co-spectral attenuation.
  - Humidity effects on H; density corrections on LE and CO2 fluxes.
- Derived metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and flux footprint estimates (Kormann & Meixner model).
- Quality control criteria:
  - Outliers removed via median absolute deviation.
  - Periods of non-stationary turbulence removed.
  - Flux ranges filtered (H, LE, NEE) to physically plausible bounds.
  - NEE filtered to nighttime values and u* thresholds (0.22 m s−1 for EF-SA; 0.16 m s−1 for EF-GF).
  - Fluxes retained if footprint >75% from target ecosystem.
  - Weekly visual inspection to remove clearly erroneous values.
  
## Gap filling and flux partitioning
- Data gaps in EC fluxes (NEE, LE, H) filled with Marginal Distribution Sampling approach.
- NEE partitioned into:
  - Gross Ecosystem Production (GEP)
  - Total Ecosystem Respiration (TER)
- Partitioning driven by air temperature (Ta) using Reichstein et al. (2005) methods.
- Gap-filling and partitioning performed with REddyProc (R package).

## Data structure and format
- Time series provided as two separate CSV files containing tabular data (ascii).
- Gap-filled and partitioned data provided as a complete time series for each site.
- Missing records denoted by -9999.

## Variables and units
- Variables include: DateTime (UTC), NEE (μmol CO2 m−2 s−1), NEE_filled (μmol CO2 m−2 s−1), NEE_filled_sd, LE (W m−2), LE_filled (W m−2), H (W m−2), H_filled (W m−2), Tau (kg m−1 s−2), Tau_filled, Pa (kPa/bar), Ta (°C), RH (%), VPD (hPa), SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil1, Tsoil2, Tsoil3, VWC1-4, Precipitation, WaterLevel, Windspeed, Winddir, plus footprint metrics (x_peak, x_70, x_90) and ustar, TKE, L, zL, NEE_filled_sd, LE_filled_sd, H_filled_sd, TER, GEP.
- Site-specific notes:
  - EF-SA and EF-GF share a core set of flux and meteorological variables but have site-specific ancillary measurements (e.g., VWC and soil depths differ).

## Accessibility and credits
- Funding and support:
  - Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE programme).
  - SEFLOS project under NERC Soil Security Programme (NE/P014097/1).
  - EF-SA established under Defra SP1210 project; COSMOS-UK data contribution.
- References and methodological sources cited for processing, QC, gap-filling, and partitioning methods.