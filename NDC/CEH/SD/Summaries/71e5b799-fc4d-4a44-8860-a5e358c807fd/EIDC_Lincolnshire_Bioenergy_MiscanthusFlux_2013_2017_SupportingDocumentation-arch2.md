# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017 Ross Morrison, Hollie M. Cooper, Rebecca L. Rowe & Niall P. McNamara

## Overview
- Time-series dataset: Lincolnshire_Bioenergy_Miscanthus_2013_2017.csv
- Measurements: surface-atmosphere exchanges of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ)
- Method: eddy covariance (EC) technique from 2013-07-05 00:30 to 2017-11-07 00:00
- Ancillary data: weather and soil physics observations, plus atmospheric turbulence variables
- Output: gap-filled and partitioned fluxes (NEE_filled; NEE_filled_sd; LE_filled; LE_filled_sd; H_filled; H_filled_sd; TER; GEP) and related metadata

## Study site
- Location: Miscanthus x. giganteus plantation, 53°19'10.07"N, 0°35'18.65"W; 11.5 ha commercially cultivated bioenergy site ~10 km north of Lincoln, UK
- Climate: temperate maritime; long-term means ~9.8°C air temperature, ~614 mm annual precipitation
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; bulk densities ~1.46–1.53 g cm-3; 0–0.15 m and 0.15–0.3 m layers; textures ~49% sand, 36% silt, 15% clay; SOC ~68 t C ha-1; N ~11 t N ha-1; pH 6.8–7.3
- Land use history and management: established on former arable land in 2006; rhizome planting density 10,000 ha-1; annual harvest since 2008; soil and biomass amendments in 2013–2016 (wood waste compost 15 Mg ha-1; Fibrophos ~0.5 Mg ha-1; bio-mulch fungi mix and nutrients)

## Sampling regime and data collection
- Flux measurements: open-path EC system on a tall mast at plantation center; height adjusted to roughly twice canopy height
- Instrumentation: LI-7500 CO2 sensor, R3 sonic anemometer-thermometer
- Sampling: 20 Hz raw data; 30-minute aggregation for fluxes; Ta and RH at 2 m height
- Ancillary meteorology and soil observations: distributed on scaffold tower; net radiation (Rnet) and components; shortwave radiation sensors; below-canopy PPFD; soil heat flux; soil water content (VWC); soil temperature; precipitation
- Data recording: 30-minute averages for most variables; high-frequency data stored via Campbell Scientific dataloggers

## Data processing
- Flux calculation: EddyPRO v6.1; 30-minute block-averaged fluxes
- Processing steps: QC of 20 Hz data; angle-of-attack correction; 2D rotation to align with terrain; corrections for low/high-frequency co-spectral attenuation; humidity-related corrections for H; density corrections for LE and CO2; uncertainty estimates
- Derived metrics: wind speed and direction; friction velocity (u*); Turbulent Kinetic Energy (TKE); Obukhov length (L); stability parameter (z/L)

## Quality control
- Outlier handling: median absolute deviation method; removal of non-stationary periods
- Flux range checks: exclude H (-200 to 400 W m-2), LE (-100 to 500 W m-2), NEE (-70 to 35 μmol CO2 m-2 s-1)
- NEE screening: exclude at night and when u* < 0.14 m s-1
- Representativeness: footprints assessed with Kormann & Meixner model; fluxes considered representative if >75% originated from target ecosystem
- Manual checks: weekly data review; manual removal of clearly erroneous values

## Gap-filling and flux partitioning
- Gap-filling method for EC data: Marginal Distribution Sampling (Reichstein et al. 2005)
- Gap-filling for key meteorology: linear relationships using adjacent-field weather stations
- Flux partitioning: NEE partitioned into GEP and TER using Reichstein et al. (2005) approach driven by Ta
- Tools: REddyProc package in R (Reichstein et al. 2016)

## Data structure and contents
- Format: a single CSV file with tabular data; gap-filled and partitioned fluxes included as a complete time series (2013-07-05 00:30 to 2017-11-07 00:00)
- Missing data: denoted by -9999
- Variables: NEE, NEE_sd, LE, LE_sd, H, H_sd, TER, GEP, plus gap-filled and storage terms (CO2_strg, LE_strg, H_strg); ancillary variables include Ta, RH, SWin, SWout, LWin, LWout, Rnet, PPFD below canopy, soil moisture and temperature, soil heat flux, precipitation, wind metrics, footprint fraction, Ustar, TKE, L, zL, and related parameters

## Nature and units of recorded values
- Primary fluxes: NEE, LE, H (units: μmol CO2 m-2 s-1; LE and H in W m-2)
- Derived outputs: TER and GEP (μmol CO2 m-2 s-1)
- Ancillaries: temperatures (°C), radiation (W m-2), wind (m s-1), VWC (%), soil temp (°C), precipitation (mm), etc.
- Uncertainties: provided for NEE, LE, H (NEE_sd, LE_sd, H_sd)

## Acknowledgments and references
- Funding: National Environment Research Council
- Acknowledgments: landowners and technical/support teams; project collaborators and institutions
- Key references: foundational eddy covariance methods and data processing standards (e.g., Reichstein et al., Mauder et al., Moncrieff et al., Papale et al., Reichstein et al. REddyProc) and related site studies for context and methodology