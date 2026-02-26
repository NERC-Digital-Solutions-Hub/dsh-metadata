# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

## Overview
- Time series of surface-atmosphere exchanges measured via eddy covariance (EC) at a Miscanthus plantation in Lincolnshire, UK.
- Variables include net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ), with supplementary weather, soil, and turbulence data.
- Coverage: 2008-05-01 00:30 to 2013-02-18 00:00; data provided as a complete time series with gap-filled and partitioned flux estimates.

## Study site
- Location: 11.5 ha commercial Miscanthus plantation, ~10 km north of Lincoln, UK (53°19'10.07"N, 0°35'18.65"W).
- Climate: temperate maritime; mean annual temperature ~9.8°C and precipitation ~614 mm (1981–2010).
- Soils: Beccles 1 association; mixture of fine loams with seasonal waterlogging; bulk densities ~1.46–1.53 g cm^-3; texture ~49% sand, 36% silt, 15% clay; SOC ~68 t C ha^-1; N ~11 t N ha^-1; pH 6.8–7.3.
- Land-use history: planted spring 2006 on former arable land; 10,000 rhizomes ha^-1; ~1/3 replanted in 2007; fertiliser applied first in 2010 (Fibrefoss 660 kg ha^-1).
- Management: annual spring harvests from 2008 onwards.

## Sampling regime
- Automated flux, meteorological, and soil observations collected between 2008-05-01 and 2013-02-18.

## Flux data acquisition
- EC system mounted on an extendible mast; height adjusted to ~2× canopy height.
- Fluxes measured: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2); raw data at 20 Hz.
- Instrumentation: LI-7500 IRGA, sonic anemometer-thermometer, with data logged on a 30 Hz system.

## Ancillary data acquisition
- Meteorological and soil observations from a scaffold tower:
  - Air temperature (Ta, °C) and relative humidity (RH) at 4 m.
  - Net radiation and components (SWin, SWout, LWin, LWout) and net radiation (Rnet).
  - Direct and diffuse incoming shortwave (SWin_total, SWin_diffuse).
  - Below-canopy photosynthetic photon flux density (PPFDbc) at three locations.
  - Soil heat flux (G) at two locations; volumetric water content (VWC) at upper 0.3 m; soil temperature (Tsoil) at two locations.
  - Data averaged to 30-minute means and logged with CR10 dataloggers.

## Data processing
- Fluxes computed with EddyPRO v6.1; 30-minute block averages.
- Processing steps include QC of 20 Hz data, angle-of-attack correction, 2-D coordinate rotation, corrections for co-spectral attenuation, humidity effects on H, density corrections on LE and NEE; uncertainty estimates per Mauder et al. and related references.
- Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).

## Quality control
- Outliers removed via median absolute deviation; EddyPRO quality flag thresholds (flag > 1) leads to exclusion.
- Flux ranges enforced: H [-200, 400] W m^-2, LE [-100, 500] W m^-2, NEE [-70, 35] μmol CO2 m^-2 s^-1.
- Footprint assessment using Kormann & Meixner model via ART Footprint Tool; retain fluxes with >75% within target ecosystem.
- Weekly visual checks; clearly erroneous values removed.

## Data gap-filling and flux partitioning
- Gaps in EC data filled with Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using flux-partitioning methods; Ta used to drive the algorithm.
- Gap-filling and partitioning performed with REddyProc (R) package (Reichstein et al., 2016).

## Details of data structure
- Data provided as a single CSV with columns described in Table 1; gap-filled and partitioned data included.
- Time range: 2008-05-01 00:30 to 2013-02-18 00:00; timestamps mark the end of each 30-minute averaging period.
- Missing data denoted by -9999.

## Nature and units of recorded values
- DateTime: yyyy-mm-dd HH:MM (UTC).
- NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, Ta, RH, VPD, SWin, SWin_total, SWin_diffuse, PPFDbc1/2/3, G1/G2, Tsoil1/2, VWC1/2, Windspeed1/2, Winddir1/2, FootprintFraction1/2, Ustar1/2, TKE1/2, L1/2, zL1/2.
- NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP (gap-filled and derived metrics) with corresponding uncertainties or estimates as described in the table.

## Acknowledgments and references
- Funded by the National Environment Research Council (CarboBiocrop project) and CEH Integrating Fund.
- Data contributors acknowledge landowners and cite related methodological and site-specific references for context and processing.