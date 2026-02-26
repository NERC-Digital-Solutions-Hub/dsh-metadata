# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance (EC) between 2009-10-14 00:30 and 2013-10-01 00:00.
- Includes ancillary weather and soil physics observations, plus variables describing atmospheric turbulence and flux quality.
- Data provided as a single CSV with gap-filled and partitioned flux data (NEE_filled, TER, GEP, etc.) alongside original measurements, at 30-minute averaging intervals.

## Study site
- Site: 9.4 ha mature commercial short rotation coppice (SRC) willow plantation near Lincoln, UK (coordinates provided).
- Climate: temperate maritime; mean annual air temperature ~9.8 °C and ~614 mm annual precipitation (1981–2010 normals; Met Office data).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; pH ~5.8; bulk density ~1.4 g cm^-3.
- Land-use and management: established on former arable land in 2000; coppiced in 2001; biomass harvests in 2011 and 2013; minimal inputs aside from micronutrients, lime, and compost wood waste after 2011; rainfed with no irrigation.

## Sampling regime and flux data acquisition
- Flux measurements: open-path EC system on a movable mast at ~2× canopy height; center of plantation.
- Variables: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2).
- Instruments: Li-COR LI-7500 and modified Gill sonic anemometerthermometer; raw 20 Hz data logged by Hydra Mk4 datalogger.
- Ancillary meteorology and soil observations: net radiation (Rnet), shortwave/longwave components, below-canopy PPFD, soil heat flux (G), soil volumetric water content (VWC), soil temperature (Ts), air temperature (Ta), relative humidity (RH); data averaged to 30-minute periods.

## Data processing and quality control
- Processing: EddyPRO® Flux Calculation Software v6.1; 30-minute block averages; includes QC and necessary corrections (angle-of-attack, 2D rotation, spectral attenuation, humidity effects, density corrections).
- Random uncertainties calculated; fluxes screened using EddyPRO quality flags; bounds applied for H, LE, and NEE.
- Footprint assessment: evaluate representativeness with ART Footprint Tool; fluxes retained if >75% originate within target ecosystem.
- Additional QC: weekly visualization checks; manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005) for EC data gaps (NEE, LE, H).
- Flux partitioning: NEE decomposed into gross ecosystem production (GEP) and total ecosystem respiration (TER) using partitioning approaches driven by Ta; implemented with REddyProc (R package).
- Outputs: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, plus corresponding uncertainty metrics.

## Nature and units of recorded values / Data structure
- Time series provided as a CSV with columns described in Table 1; timestamps are end of 30-minute flux periods in GMT/UTC.
- Recorded and gap-filled variables include: NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, Pa, Ta, RH, VPD, SW_in, SW_out, LW_in, LW_out, R_net, PPFDbc1/2/3, G1/2, Tsoil1/2, VWC1/2, Precipitation1/2, windspeed1/2, winddir1/2, FootprintFraction1/2, Ustar1/2, TKE1/2, L1/2, zL1/2, NEE_filled1/2, NEE_filled_sd1/2, LE_filled1/2, LE_filled_sd1/2, H_filled1/2, H_filled_sd1/2, TER1/2, GEP1/2.
- Missing data denoted by -9999.

## Access, usage and documentation notes
- Time span: 2009-10-14 00:00 to 2013-10-01 00:00 (UTC) with 30-minute flux intervals.
- Dataset includes both raw (pre-gap-filling) and gap-filled, partitioned flux products for robust analyses of carbon and energy exchange.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (CarboBiocrop) and CEH Integrating Fund; appreciation expressed to landowners for site access.
- Key references cited for methods and context (eddy covariance processing, QC, footprint analysis, and related studies).