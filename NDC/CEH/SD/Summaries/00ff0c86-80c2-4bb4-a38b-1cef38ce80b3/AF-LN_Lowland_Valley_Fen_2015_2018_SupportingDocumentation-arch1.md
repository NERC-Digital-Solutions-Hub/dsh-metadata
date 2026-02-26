# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

## Overview
- Time-series dataset of land surface–atmosphere exchanges, including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) fluxes.
- Measurements taken above a grassland canopy at AF-LN site from 2015-01-01 00:30 to 2018-10-11 00:00.
- Ancillary meteorological and soil-physics observations accompany flux data; turbulence characterisation variables are included.
- Fluxes computed via eddy covariance (EC) with quality control, gap-filling, and partitioning into GEP and TER.

## Study site
- Location: AF-LN flux site, Cors Erddreiniog National Nature Reserve, Anglesey, North Wales (53° 18' 37.18'' N, 4° 17' 28.06'' W; 63 m amsl).
- Habitat: Conservation-managed valley-head rich fen; low-intensity pony grazing.
- Climate: Temperate maritime; mean annual Ta ≈ 10.4°C and precipitation ≈ 841 mm (1981–2010).
- Substrate: Deep fen peat with bands of marl; peat depth up to ~2.5 m; peat bulk density ~0.17 g cm-3; carbon content ~45%.
- Hydrology: Water levels near the peatland surface year-round.

## Sampling regime
- Automated measurements of flux, meteorology, and soil physics at 30-minute intervals.
- EC setup: Fluxes measured above canopy at 2.0 m using CSAT3 ultrasonic anemometer and LI-7500 CO2 sensor; 20 Hz sampling; data logged with a CR3000.
- Ancillary data: Air temperature, relative humidity, net radiation, shortwave radiation, soil heat flux at two locations, soil temperature, and precipitation.

## Flux data acquisition
- Target fluxes: NEE (μmol CO2 m-2 s-1), H (W m-2), LE (W m-2), and τ (kg m-1 s-2).
- Turbulent observations: Raw turbulence components and gas densities recorded for processing.

## Ancillary data acquisition
- Meteorological: Ta (2 m), RH (2 m); radiation components (Rnet, SWin); precipitation (0.5 h bins).
- Soil physics: Two soil heat flux measurements (G1, G2), soil temperatures (Tsoil1), and related variables.
- Data are logged as 30-minute means and/or sums.

## Data processing
- Flux computation: EddyPRO software (Version 6.1) used to derive flux densities; provides QC and corrections.
- Corrections and transformations: Angle-of-attack correction, 2D coordinate rotation, high/low-frequency co-spectral attenuation corrections, humidity-related correction for H, density corrections for LE and CO2 fluxes; random uncertainties computed.
- Derived telemetry: Wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and 1-D footprint estimates (Kormann & Meixner model).

## Quality control
- Outlier detection: Median absolute deviation method; manual checks on weekly plots.
- Turbulence criteria: Exclude non-stationary turbulence periods.
- Flux range gates: H (-200 to 500), LE (-60 to 500), NEE (-50 to 30) W m-2 or μmol CO2 m-2 s-1 as applicable.
- NEE handling: Exclude night-time negative fluxes; apply friction velocity threshold (u*) of 0.18 m s-1.
- Data cleaning: Additional manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005).
- Flux partitioning: NEE partitioned into Gross Primary Production (GEP) and Total Ecosystem Respiration (TER) per Reichstein et al. (2005); Ta-driven partitioning.
- Tools: REddyProc package in R for gap-filling and partitioning; where possible, meteorological gaps filled using data from a nearby 2nd EC station (<1 km away).

## Details of data structure
- Data format: Single CSV file with tabular columns as described in Table 1.
- Coverage: Gap-filled and partitioned time series from 2015-01-01 00:30 to 2018-10-11 00:00.
- Missing data: Denoted by -9999.

## Nature and units of recorded values (selected variables)
- DateTime: dd-mm-yyyy HH:MM (GMT/UTC)
- NEE: μmol CO2 m-2 s-1
- NEE_sd: μmol CO2 m-2 s-1
- LE: W m-2
- LE_sd: W m-2
- H: W m-2
- H_sd: W m-2
- Tau: kg m-1 s-2
- Tau_sd: kg m-1 s-2
- CO2_strg: μmol CO2 m-2 s-1
- LE_strg, H_strg: W m-2
- Pa: kPa
- Ta: °C
- RH: %
- VPD: hPa
- SWin: W m-2
- Rnet: W m-2
- G1, G2: W m-2
- Tsoil1: °C
- Precipitation: mm (0.5 h)
- WS, WD: m s-1; wind direction degrees
- Ustar: m s-1
- TKE: m-2 s-2
- L: m
- zL: dimensionless
- x_peak, x_70, x_90: m (footprint metrics)
- NEE_filled, NEE_filled_sd: μmol CO2 m-2 s-1
- LE_filled, LE_filled_sd: W m-2
- H_filled, H_filled_sd: W m-2
- TER, GEP: μmol CO2 m-2 s-1

## Data availability and provenance
- Funded by Natural Environment Research Council (NE/R016429/1) and Defra SP1210; site permissions from Natural Resources Wales.
- Datasets and processing steps align with standard EC processing references and include metadata for discoverability and reusability.

## Acknowledgments and references
- Acknowledges support from NERC UK-SCAPE programme and Defra project; permission from Cors Erddreiniog Nature Reserve.
- Key methodological references encompass EddyPRO processing, gap-filling and partitioning algorithms, and footprint modelling.