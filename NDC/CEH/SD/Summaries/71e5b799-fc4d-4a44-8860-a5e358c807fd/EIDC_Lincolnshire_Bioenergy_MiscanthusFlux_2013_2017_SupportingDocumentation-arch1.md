# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ).
- Turbulent fluxes measured with eddy covariance (EC) between 2013-07-05 00:30 and 2017-11-07 00:00.
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Data are provided as gap-filled, partitioned fluxes and complete time series ending 2017-11-07, with -9999 denoting missing records.

## Study site
- Location: Miscanthus x. giganteus plantation, 11.5 ha, about 10 km north of Lincoln, UK (53°19'10.07"N, 0°35'18.65"W).
- Climate: temperate maritime; mean annual temp ~9.8°C and precipitation ~614 mm (1981–2010).
- Soils: Beccles 1 association; seasonally waterlogged fine loams on Charnmouth Mudstone; bulk density ~1.46–1.53 g cm-3; 0–0.30 m soil layer SOC ~68 t C ha-1 and N ~11 t N ha-1; pH 6.8–7.3.
- History and management: established 2006 on former arable land; harvests annually since 2008; remedial cultivation in 2013; additions of wood waste compost (2013) and other soil amendments in 2014–2016.

## Sampling regime
- Automated flux, meteorological, and soil measurements conducted with EC above the Miscanthus canopy.
- Instrumentation: open-path EC system on a tall mast; LI-7500 CO2 analyzer; R3 sonic anemometer; 20 Hz data logged with CR3000.
- Measurement height set to roughly twice the canopy height; Ta and RH measured at 2 m height.
- Data are averaged to 30-minute intervals for fluxes and many ancillary variables; 20 Hz data used for QC and processing.

## Ancillary data acquisition
- Net radiation and components (SWin, SWout, LWin, LWout); Net radiation sensors and a BF3 sunshine sensor.
- Below-canopy PPFD (PPFDbc) at multiple below-canopy locations.
- Soil heat flux (G) at two locations; soil moisture (VWC) and soil temperature (Tsoil) at two locations.
- Precipitation measured with a tipping-bucket gauge.
- All ancillary data logged as 30-minute means (or sums for precipitation).

## Data processing
- Flux calculations via EddyPRO v6.1; corrections include QC of 20 Hz data, tilt corrections, coordinate rotation, spectral corrections, density corrections.
- Derived turbulence metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).
- Random uncertainties calculated for fluxes; data are quality-controlled for stationarity and representativeness.

## Quality control
- Outliers removed using median absolute deviation; non-stationary conditions cause exclusion.
- Flux ranges: H -200 to 400 W m-2; LE -100 to 500 W m-2; NEE -70 to 35 μmol CO2 m-2 s-1.
- NEE excluded at night and when u* < 0.14 m s-1 (per Reichstein et al. 2016 method).
- Footprint analysis (ART Footprint Tool) ensures flux representativeness (>75% from target ecosystem).
- Weekly visual checks and manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling of EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al. 2005).
- Gaps in key meteorological variables filled via linear relationships from nearby weather stations.
- NEE partitioned into gross ecosystem production (GEP) and total ecosystem respiration (TER) using partitioning methods driven by Ta (Reichstein et al. 2005).
- Gap-filling and partitioning performed with REddyProc (R).

## Details of data structure
- Time series stored in a single CSV: Lincolnshire_Bioenergy_Miscanthus_2013_2017.csv.
- Gap-filled and partitioned data included; missing data indicated by -9999.
- Columns include NEE, NEE_unc, LE, LE_unc, H, H_unc, τ, τ_unc, and partitioned terms (GEP, TER), plus gap-filled equivalents (NEE_filled, NEE_filled_sd, LE_filled, etc.) and multiple ancillary variables ( Ta, RH, SWin, etc.).

## Nature and units of recorded values
- DateTime: UTC in format yyyy-mm-dd HH:MM.
- Fluxes (pre-gap-filling): NEE (μmol CO2 m-2 s-1), LE (W m-2), H (W m-2), τ (kg m-1 s-2).
- Uncertainties provided for NEE, LE, H, and τ.
- Post-processing outputs: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER (μmol CO2 m-2 s-1), GEP (μmol CO2 m-2 s-1).
- Ancillary variables with units described in Table 1 (e.g., Ta, RH, SWin, G, VWC, PPFDbc, etc.).

## Acknowledgments
- Funded by the National Environment Research Council (NERC).
- Acknowledgment of landowners, field support, and technical staff from the Centre for Ecology & Hydrology.

## References
- Key methodological and site references for EC processing, QC, gap-filling, footprint analysis, and prior related studies on Miscanthus and carbon budgets.