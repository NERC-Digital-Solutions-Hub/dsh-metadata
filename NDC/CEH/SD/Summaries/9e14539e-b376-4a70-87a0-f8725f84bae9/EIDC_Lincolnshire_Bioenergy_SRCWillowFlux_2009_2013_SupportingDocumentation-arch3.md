# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance (EC) between 2009-10-14 and 2013-10-01.
- Includes ancillary weather and soil physics observations, plus variables describing atmospheric turbulence and QC metrics for turbulent flux observations.
- Data processing uses EddyPRO for EC flux calculations; gap-filling and partitioning of NEE performed with established methods; uncertainties quantified.
- Data are provided as a complete time series with 30-minute averaging periods; missing records denoted by -9999.
- The dataset supports carbon and energy balance analysis for a commercial short rotation coppice willow plantation, with emphasis on data quality, provenance, and openness.

## Study site
- Location: SRC willow flux site near Lincoln, UK (9.4 ha mature commercial plantation).
- Coordinates: 53°19'10.37"N, 0°35'3.06"W.
- Climate: temperate maritime; mean 1981-2010 temperatures ~9.8°C and annual precipitation ~614 mm.
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; soil bulk density ~1.4 g cm-3; pH ~5.8; upper 0.3 m soil C ~68.3 t ha-1 and N ~11.0 t ha-1.
- Land-use history: established on former arable land in 2000; coppiced in 2001; biomass harvests in March 2011 and October 2013.
- Management: minimal inputs apart from micronutrients and lime after 2011 harvest; plantation is rainfed with no irrigation.

## Sampling regime
- EC system installed on an extendible mast at plantation centre; measurement height adjusted to ~2× canopy height.
- Fluxes recorded: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2); data at 20 Hz.
- Ancillary measurements: net radiation (Rnet), incoming/outgoing shortwave and longwave radiation, below-canopy photosynthetically active radiation, soil heat flux, volumetric water content (0.0–0.3 m), soil temperature, precipitation, air temperature, and relative humidity.
- Observation period: 2009-10-14 00:30 to 2013-10-01 00:00; data logged with a CR10x datalogger.

## Data processing
- Fluxes computed with EddyPRO v6.1, including QC, angle-of-attack correction, 2D coordinate rotation, high/low-frequency co-spectral corrections, density corrections, and humidity/CO2 density effects.
- Outputs include turbulent metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).
- Data are averaged to 30-minute blocks; random uncertainties calculated for fluxes.
- Footprint analysis performed to ensure representativeness of fluxes for the target ecosystem.

## Quality control
- Outliers removed via median absolute deviation; flux QC flags used (flag >1 excluded).
- Flux value ranges applied: H [-200, 600] W m^-2, LE [-100, 600] W m^-2, NEE [-55, 25] μmol CO2 m^-2 s^-1.
- Flux representativeness assessed with the footprint model; fluxes retained if >75% originated within the target ecosystem.
- Additional manual checks performed on a weekly basis to remove clearly erroneous values.

## Data gap-filling and flux partitioning
- Data gaps in EC fluxes filled using Marginal Distribution Sampling (MDS) approach.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Reichstein et al. (2005) methodology driven by air temperature.
- Gap-filling and partitioning performed with REddyProc (R package) following established protocols.
- Outputs include gap-filled NEE (NEE_filled) and its uncertainty (NEE_filled_sd), plus gap-filled LE/H and partitioned TER and GEP values.

## Details of data structure
- Time series stored in a single CSV file with columns described in the dataset’s Table 1; timestamp is end of each 30-minute period (UTC).
- Gap-filled and partitioned data provided as a complete time series from 2009-10-14 to 2013-10-01.
- Missing records indicated by -9999; variables include:
  - NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc
  - CO2 storage term, pressures (Pa), air temperature (Ta), RH, VPD
  - Radiation terms (SW_in, SW_out, LW_in, LW_out, R_net)
  - Below-canopy PPFD (PPFDbc1-3), soil heat flux (G1-2), soil temperature (Tsoil1-2), volumetric water content (VWC1-2)
  - Precipitation (two records), windspeed (two), winddir (two)
  - FootprintFraction (two), Ustar, TKE, T*, L, zL
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP
- Units and descriptions follow LI-COR conventions and Reichstein et al. (2016) REddyProc outputs.

## Nature and Units of recorded values
- DateTime: dd/mm/yyyy HH:MM (UTC)
- NEE: μmol CO2 m^-2 s^-1 (pre-gap-filled)
- NEE_unc: μmol CO2 m^-2 s^-1
- LE: W m^-2 (pre-gap-filled)
- LE_unc: W m^-2
- H: W m^-2
- H_unc: W m^-2
- Tau: kg m^-1 s^-2
- Tau_unc: kg m^-1 s^-2
- CO2_strg: μmol CO2 m^-2 s^-1
- Ta: °C
- RH: %
- VPD: hPa
- SW_in/ SW_out/ LW_in/ LW_out: W m^-2
- R_net: W m^-2
- PPFDbc: μmol photons m^-2 s^-1
- G: W m^-2
- Tsoil: °C
- VWC: %
- Precipitation: mm
- windspeed: m s^-1
- winddir: degrees
- FootprintFraction: %
- Ustar: m s^-1
- TKE: m^2 s^-2
- L: m
- zL: dimensionless
- NEE_filled / NEE_filled_sd, LE_filled / LE_filled_sd, H_filled / H_filled_sd, TER, GEP: corresponding units as described above for filled/partitioned products

## Acknowledgments
- Data collection funded by the National Environment Research Council (CarboBiocrop) and CEH Integrating Fund.
- Gratitude extended to landowners for access and permission to install the flux tower.

## References
- Source materials and methodological references spanning EC processing, QC, footprint analysis, gap-filling, and partitioning algorithms (e.g., Reichstein et al., 2005; Reichstein et al., 2016; EddyPRO literature; footprint models; and site-specific studies on bioenergy crops).