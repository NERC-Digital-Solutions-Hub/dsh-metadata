# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at a Miscanthus x. giganteus plantation in Lincolnshire, UK.
- Measurements used eddy covariance (EC) micrometeorology between 2013-07-05 00:30 and 2017-11-07 00:00.
- Ancillary weather and soil physics observations, plus variables describing atmospheric turbulence.
- Data processing includes quality control, gap-filling, and partitioning NEE into gross ecosystem production (GEP) and total ecosystem respiration (TER); outputs provided as a continuous time series with 30-minute resolution.

## Study site
- Location: Miscanthus flux site at 53°19'10.07"N, 0°35'18.65"W; 11.5 ha commercial bioenergy plantation, ~10 km north of Lincoln, UK.
- Climate: temperate maritime; mean 1981–2010 air temperature 9.8 ± 0.7 °C; precipitation 614 ± 93.5 mm yr⁻¹.
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; bulk density ~1.46–1.53 g cm⁻³; texture ~49% sand, 36% silt, 15% clay; soil organic carbon ~68 t C ha⁻¹ and nitrogen ~11 t N ha⁻¹ in top 0–0.3 m; pH 6.8–7.3.
- Management: established on former arable land in 2006; Miscanthus rhizomes planted at 10,000 ha⁻¹; annual spring harvests from 2008; remedial cultivation in 2013; soil amendments including wood waste compost (15 Mg ha⁻¹) in 2013, ~0.5 Mg ha⁻¹ Fibrophos in 2014, and biostimulants in 2016.

## Sampling regime
- Automated flux, meteorological and soil physics measurements conducted from 2013-07-05 to 2017-11-07.
- Flux tower equipped with EC system; canopy-height-adjusted mast to maintain measurement height ~2× canopy height.
- Measurements cover spring harvest, drying, and baling periods; data logged as 30-minute means.

## Flux data acquisition
- Fluxes: NEE (μmol CO₂ m⁻² s⁻¹), H (W m⁻²), LE (W m⁻²), and τ (kg m⁻¹ s⁻²) obtained with an open-path EC system (R3 sonic anemometer, LI-7500).
- Raw EC data at 20 Hz, logged by a CR3000 micrologger.
- Additional instantaneous air temperature and relative humidity at 2 m; logged as 30-minute means.

## Ancillary data acquisition
- Net radiation (Rnet) and components (SWin, SWout, LWin, LWout); BF3 sunshine sensor for total and diffuse shortwave radiation.
- Below-canopy photosynthetic photon flux density (PPFDbc) at three below-canopy locations.
- Soil heat flux (G) at two locations; soil volumetric water content (VWC) at two locations; soil temperature (Ts) at two locations.
- Precipitation measured with tipping-bucket gauge.
- All ancillary observations logged as 30-minute means (and sums for precipitation) to a CR1000 datalogger.

## Data processing
- Turbulent flux densities calculated with EddyPRO v6.1; 30-minute block-averaged fluxes.
- Processing includes: QC of 20 Hz data, angle-of-attack correction, 2D coordinate rotation, corrections for high/low-frequency co-spectral attenuation, humidity effects on H, density corrections for LE and CO2, and uncertainty estimates.
- Derived variables computed: wind speed, wind direction, friction velocity (u*), turbulent kinetic energy (TKE), Obukhov length (L), and stability parameter (z/L).

## Quality control
- Outliers removed via median absolute deviation; non-stationary conditions excluded fluxes.
- Flux ranges: H: -200 to 400 W m⁻²; LE: -100 to 500 W m⁻²; NEE: -70 to 35 μmol CO₂ m⁻² s⁻¹.
- NEE excluded at night and below u* threshold of 0.14 m s⁻¹ (per Reichstein et al., 2016).
- Representativeness assessed with footprint model; fluxes considered representative if >75% originated from the target ecosystem.
- Weekly visual checks of all fluxes and ancillary data, with manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled using Marginal Distribution Sampling (MDS).
- Gaps in key meteorological variables filled via linear relationships from nearby weather stations.
- NEE partitioned into GEP and TER using Reichstein et al. (2005) methodology driven by Ta; gap-filled and partitioned data produced with REddyProc (R package, Reichstein et al., 2016).

## Details of data structure
- Data provided as a single CSV with 30-minute time series; gap-filled and partitioned variables included.
- Missing records denoted by -9999.

## Nature and units of recorded values
- Variables documented (DateTime, NEE, NEE_sd, LE, LE_sd, H, H_sd, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.) with units such as μmol CO₂ m⁻² s⁻¹ for fluxes, W m⁻² for heat fluxes, and standard metadata (Ta, RH, SWin, etc.).
- Includes storage terms (CO2_strg, LE_strg, H_strg), atmospheric densities, vapor pressures, and stability metrics.

## Acknowledgments
- Funded by the National Environment Research Council; thanks to landowners and technical/field support teams for EC and instrumentation maintenance.

## References
- Includes foundational methods and related studies on eddy covariance processing, QC, footprint evaluations, gap-filling, and prior work on Miscanthus carbon budgets.