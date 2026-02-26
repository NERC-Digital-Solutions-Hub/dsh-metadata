# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview of dataset
- Time series observations of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured over winter wheat in Lincolnshire, UK during 2012.
- Measurements obtained with eddy covariance (EC) technique from 2012-04-05 00:30 to 2012-08-08 00:00 (UTC); ancillary weather and soil observations and turbulence variables included.
- Data provided as a single CSV with gap-filled and partitioned fluxes (GEP and TER) and associated variables; missing records are indicated by -9999.

## Study site
- Flux observation site: arable cropland, ~10 km north of Lincoln, UK (53°19'17.89"N, 0°35'7.83"W).
- Climate: temperate maritime; mean 1981-2010 temperature 9.8 ± 0.7 °C; precipitation 614 ± 93.5 mm year-1.
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk densities ~1.46–1.53 g cm-3; sand 49%, silt 36%, clay 15%; pH ~6.32.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements from 2012-04-05 00:30 to 2012-08-08 00:00 (GMT, UTC).
- EC flux tower at 3.0 m height at field center; measurements logged as 30-minute means.

## Flux data acquisition
- EC system: open-path, with R3 sonic anemometer (Gill) and LI-7500 CO2/H2O infrared gas analyzer (LI-COR).
- Raw 20 Hz data collected for wind components, sonic temperature, water vapor density, and CO2 density; logged with CR3000 data logger.

## Ancillary data acquisition
- Net radiation components (SWin, SWout, LWin, LWout) at 1.5 m above canopy; soil heat flux (G) at 0.05 m depth at two locations.
- Air temperature (Ta) and relative humidity (RH) at 2 m; soil temperature (Tsoil) and soil volumetric water content (VWC) at 0.05 m and 0.1 m depths (two replicates).
- Rainfall recorded with a tipping-bucket gauge in an adjacent field.
- Data logged as 30-minute means.

## Data processing
- Turbulent flux densities computed from raw EC data using EddyPRO® Flux Calculation Software v6.1; 30-minute block averaging.
- Processing steps include quality control of 20 Hz data, tilt/rotation corrections, co-spectral attenuation corrections, density corrections for LE and CO2, and random uncertainty estimates.
- Derived metrics: wind speed and direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).

## Quality control
- Statistical outliers removed via median absolute deviation; non-stationarity tests applied.
- Fluxes excluded if outside plausible ranges: H (-200 to 400 W m-2), LE (-100 to 500 W m-2), NEE (-70 to 35 μmol CO2 m-2 s-1).
- NEE rejected when nighttime CO2 fluxes (SWin < 20 W m-2) were negative and when u* < 0.07 m s-1.
- Flux representativeness checked with footprint model; Fluxes considered representative if >75% originated from target ecosystem.
- Weekly visual checks to remove clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filled NEE, LE, H using Marginal Distribution Sampling (MDS) approach.
- Gaps in key meteorological variables filled via linear relationships with adjacent-field weather station data.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using partitioning approach driven by Ta; implemented with REddyProc (R) package.

## Details of data structure
- Time series provided in a single CSV file; columns described in accompanying Table 1.
- Gap-filled and partitioned data included for the full period; missing records due to QC or system issues marked as -9999.

## Nature and units of recorded values
- DateTime: yyyy-mm-dd HH:MM (GMT/UTC).
- NEE: μmol CO2 m-2 s-1; NEE_unc: μmol CO2 m-2 s-1 (random error for NEE).
- LE: W m-2; LE_unc: W m-2 (random error for LE).
- H: W m-2; H_unc: W m-2 (random error for H).
- Tau: kg m-1 s-2; Tau_unc: kg m-1 s-2 (random error).
- CO2_strg: μmol CO2 m-2 s-1; CO2_strg is the CO2 storage term.
- LE_strg, H_strg: W m-2 (storage terms).
- Pa: kPa; Pa_2: barometric pressure at 2 m.
- Ta: °C; RH: %; VPD: hPa.
- SWin, SWout, LWin, LWout, Rnet: W m-2.
- G1, G2: W m-2 (soil heat flux at location 1 and 2).
- Tsoil1–4: °C (soil temperatures at various depths/locations).
- VWC1–4: % (soil volumetric water content at depths).
- Precipitation: mm[0.5] h-1; Precipitation_2: total precipitation over 30 minutes.
- Windspeed1–2: m s-1; Winddir1–2: degrees; Ustar1–2: m s-1.
- TKE1–2: m-2 s-1; L1–2: Obukhov length; zL1–2: dimensionless stability parameter.
- FootprintFraction1–2: %; x_peak1–2, x_70_1–2, x_90_1–2: distances related to footprint contributions.
- NEE_filled, NEE_filled_sd; LE_filled, LE_filled_sd; H_filled, H_filled_sd; TER, TER_unc; GEP, GEP_unc: gap-filled/partitioned values and uncertainties.

## Acknowledgments and references
- Data processing and methodology align with established micrometeorological guidance and numerous referenced sources (e.g., Reichstein et al., Mauder et al., Moncrieff et al., EddyPRO documentation, REddyProc).
- Project and data support acknowledged, including NERC funding and site permissions.