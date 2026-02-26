# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Turbulent flux densities were measured with an open-path eddy covariance system from 2015-01-01 00:30 to 2018-10-11 00:00.
- Includes ancillary weather and soil physics observations and variables characterising atmospheric turbulence.
- Data are provided as a complete time series, including gap-filled and partitioned fluxes where available.

## Study site
- AF-LN flux observation site (coordinates: 53° 18' 37.18" N, 4° 17' 28.06" W; 63 m amsl) at Cors Erddreiniog National Nature Reserve, Anglesey, North Wales.
- Habitat: high-quality valley-head fen, grazed by ponies; climate: temperate maritime.
- Substrate: deep fen peat with bands of marl; peat depth and properties described; water levels near peatland surface year-round.
- Site categorized as high quality by Natural Resources Wales; supporting context from Evans et al. (2017) and related peatland research.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements conducted continuously from 2015-01-01 to 2018-10-11.
- Measurements encompass 30-minute averages and sums for various ancillary parameters.

## Flux data acquisition
- Fluxes of NEE, H, LE, and τ measured above a grassland canopy at 2.0 m height.
- Instruments: CSAT3 ultrasonic anemometer with LI-7500 CO2/H2O infrared analyser; data logged with a CR3000 Micrologger.
- Raw data: 20 Hz samples of wind components, sonic temperature, and gas concentrations.

## Ancillary data acquisition
- Co-located meteorological and soil observations: air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (Rnet); shortwave radiation (SWin); two soil heat flux plates (G1, G2); soil temperature (Tsoil1); precipitation (two metrics: 0.5 h increments and total precipitation); wind speed and direction; friction velocity (u*); turbulence metrics (TKE, L, z/L).
- Data logged as 30-minute means or sums where appropriate.

## Data processing
- EddyPRO processing (Version 6.1) used for flux calculations and corrections.
- Processing steps include: QC of 20 Hz data, angle-of-attack correction, 2D coordinate rotation, spectral corrections, density corrections for H and LE, and CO2 storage terms.
- Derived metrics computed: wind speed, wind direction, friction velocity, Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L); preliminary flux footprint estimates.
- Random uncertainties for flux observations estimated; gap-filling and partitioning prepared via standard algorithms.

## Quality control
- Outliers removed using median absolute deviation approach.
- Exclusion of non-stationary turbulence periods and fluxes outside specified ranges (H, LE, NEE) to ensure data validity.
- NEE: nighttime fluxes removed when negative and below a friction velocity threshold (u* < 0.18 m/s).
- Weekly checks of all flux and ancillary data; clearly erroneous values removed manually when needed.

## Data gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled with Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using partitioning methods tied to Ta data; implementations via REddyProc (Reichstein et al., 2016).
- Where possible, missing meteorological data filled using observations from a nearby station within 1 km.

## Details of data structure
- Data provided as a single CSV file with columns described (Table 1 reference in the dataset documentation).
- Time series spans 2015-01-01 00:30 to 2018-10-11 00:00.
- Missing records denoted by -9999; gap-filled and partitioned products included where available (NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP).

## Nature and units of recorded values
- DateTime: dd-mm-yyyy HH:MM (GMT/UTC).
- NEE: μmol CO2 m^-2 s^-1 (net ecosystem CO2 exchange before gap-filling); NEE_sd: μmol CO2 m^-2 s^-1 (random error).
- LE: W m^-2; LE_sd: W m^-2 (random error).
- H: W m^-2; H_sd: W m^-2 (random error).
- Tau: kg m^-1 s^-2; Tau_sd: kg m^-1 s^-2 (random error).
- CO2_strg, LE_strg, H_strg: storage terms for CO2, LE, H.
- Ta: °C; Pa: kPa; RH: %; VPD: hPa; SWin, Rnet: W m^-2; G1, G2: W m^-2; Tsoil1: °C.
- Precipitation: mm per 0.5 h (P1) and total precipitation (P2).
- WS, WD: wind speed (m s^-1) and wind direction (degrees).
- Ustar: m s^-1 (friction velocity); TKE: m^2 s^-2; L: Obukhov length (m); zL: dimensionless stability parameter.
- x_peak, x_70, x_90: upwind distance metrics for flux source characterization.
- NEE_filled, LE_filled, H_filled, TER, GEP: gap-filled or partitioned flux values with corresponding SDs where provided.

## Acknowledgments and references
- Funding and support from Natural Environment Research Council (NE/R016429/1) and Defra SP1210; permissions from Natural Resources Wales for site access.
- Key references detailing methods and processing used in data generation and gap-filling (e.g., Reichstein et al., Reichstein et al. 2016; EddyPRO, Moncrieff et al.; and related micrometeorology literature).