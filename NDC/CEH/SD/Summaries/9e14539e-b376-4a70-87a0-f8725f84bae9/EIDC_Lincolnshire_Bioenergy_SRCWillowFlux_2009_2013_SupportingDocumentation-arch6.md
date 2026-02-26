# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance (EC) between 2009-10-14 00:30 and 2013-10-01 00:00.
- Ancillary meteorological and soil physics observations, plus variables describing atmospheric turbulence and measurement quality.
- Data processed to 30-minute flux averages; includes gap-filled and partitioned products (GEP and TER) for NEE.

## Study site
- SRC willow flux site: 53°19'10.37"N, 0°35'3.06"W; 9.4 ha mature commercial bioenergy plantation, ~10 km north of Lincoln, UK.
- Climate: temperate maritime; mean annual air temperature ~9.8°C and precipitation ~614 mm/year (1981–2010 baseline).
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; pH ~5.8; upper 0.3 m soil organic C ~68.3 t ha−1 and N ~11.0 t ha−1.
- Land-use and management: established on former arable land in 2000; coppiced 2001; biomass harvests in March 2011 and October 2013; minimal inputs except micronutrients and compost post-2011 harvest; rainfed with no irrigation.

## Sampling regime and data acquisition
- EC and micrometeorological measurements taken above the canopy using an open-path EC system mounted on a mast, periodically raised to keep measurement height ~2× mean canopy height.
- Recorded fluxes: NEE (μmol CO2 m−2 s−1), H (W m−2), LE (W m−2), and τ (kg m−1 s−2); raw data at 20 Hz.
- Ancillary sensors: net radiation (Rnet), shortwave/longwave components, below-canopy PAR (PPFDBc), soil heat flux (G), soil water content (VWC), soil temperature (Tsoil), air temperature (Ta), and relative humidity (RH).
- Data logged with CR10x datalogger; timestamps are end of 30-minute averaging periods.

## Data processing and quality control
- Flux calculations via EddyPRO v6.1, including:
  - QC of 20 Hz data, angle-of-attack correction, 2D coordinate rotation, corrections for spectral attenuation, humidity effects on H, and density corrections for LE and CO2.
  - Uncertainty estimates for fluxes.
  - Computation of wind characteristics, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).
- Quality control procedures:
  - Outlier removal using median absolute deviation; EddyPRO quality flag ≤ 1; flux ranges: H −200 to 600 W m−2, LE −100 to 600 W m−2, NEE −55 to 25 μmol CO2 m−2 s−1.
  - Footprint analysis (Kormann & Meixner, 2001) to ensure >75% of flux originates within the target ecosystem.
  - Weekly visual checks and manual removal of clearly erroneous values.

## Gap-filling and flux partitioning
- Gap-filling for EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al., 2005).
- Partitioning NEE into GEP and TER using flux-partitioning approach driven by air temperature (Ta).
- Gap-filling and partitioning performed with REddyProc (R) package (Reichstein et al., 2016).

## Data structure and variables
- Single CSV: Lincolnshire_Bioenergy_SRCWillow_2009_2013.csv containing 30-minute time series; missing records denoted as -9999.
- Included variables and their units (examples):
  - DateTime (dd/mm/yyyy HH:MM, GMT)
  - NEE (μmol CO2 m−2 s−1) and NEE_filled
  - LE (W m−2) and LE_filled
  - H (W m−2) and H_filled
  - Tau (kg m−1 s−2) and TER, GEP
  - Ta (°C), RH (%), VPD (hPa)
  - Rnet, SWin, SWout, LWin, LWout
  - PPFDbc, G, Tsoil, VWC, Precipitation
  - FootprintFraction, Ustar (friction velocity), TKE, L, zL, NEE_filled_sd, LE_filled_sd, H_filled_sd
- Gap-filled and partitioned products included: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.

## Usage and applications
- Useful for constructing carbon budgets of perennial bioenergy crops and evaluating ecosystem energy and water exchanges.
- Enables validation of EC processing pipelines, QC thresholds, and gap-filling/partitioning approaches.
- Provides a multi-year dataset suitable for remote-sensing model validation and cross-site analyses of SRC willow ecosystems.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (CarboBiocrop) and CEH Integrating Fund; authors acknowledge landowners and collaborators.
- Key references include methods for QC, flux processing (Mauder et al., 2013; Foken et al., 2004), footprint modeling (Kormann & Meixner, 2001), gap-filling/partitioning (Reichstein et al., 2005), and REddyProc (REddyProc, Reichstein et al., 2016).