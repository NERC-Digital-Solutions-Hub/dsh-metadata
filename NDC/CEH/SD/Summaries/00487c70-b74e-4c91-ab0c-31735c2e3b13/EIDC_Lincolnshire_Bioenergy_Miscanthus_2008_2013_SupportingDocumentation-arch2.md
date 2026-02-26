# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

## Summary at a glance
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured with eddy covariance (EC) from 2008-05-01 00:30 to 2013-02-18 00:00.
- Ancillary meteorological and soil physics observations and turbulence variables included.
- Data processed with EddyPRO, 30-minute flux averages, quality control, and footprint assessment.
- Gap-filled NEE and partitioned into gross ecosystem production (GEP) and total ecosystem respiration (TER); gap-filled outputs provided.
- Data stored as a single CSV with -9999 as missing values; includes both raw (pre-gap-fill) and processed (gap-filled) variables.

## Study site
- Location: Miscanthus x. giganteus plantation, 11.5 ha, near Lincoln, UK (53°19'10.07"N, 0°35'18.65"W).
- Climate: temperate maritime; mean annual temperature ~9.8 °C, precipitation ~614 mm year-1 (1981-2010 baseline).
- Soils: Beccles 1 association, seasonally waterlogged fine loams; bulk densities ~1.46–1.53 g cm-3; C ~68 t C ha-1, N ~11 t N ha-1 in upper 0–0.3 m; pH ~6.8–7.3.
- Land-use history: former arable land; Miscanthus planted spring 2006; harvested annually starting 2008; no fertiliser until 2010 (Fibrefoss 660 kg ha-1).

## Sampling regime
- Automated, long-term flux, meteorological, and soil observations from 2008-05-01 00:30 to 2013-02-18 00:00.
- EC system on an extendible mast, height adjusted to ~2× canopy height.
- Fluxes measured with open-path EC: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2); 20 Hz sampling.
- Ancillary data from scaffold tower: Ta, RH, net radiation (Rnet), shortwave/longwave components, below-canopy PPFD, soil heat flux (G), soil moisture (VWC), soil temperature (Tsoil), etc.

## Data processing and quality control
- EddyPRO v6.1 used for processing; fluxes computed as 30-minute block averages.
- QC includes: 20 Hz data quality checks, angle-of-attack correction, two-dimensional rotation, corrections for cospectral attenuation, humidity effects on H, density corrections for LE and NEE; uncertainty estimates.
- Footprint assessment (ART Footprint Tool) to ensure >75% of flux originates from target ecosystem.
- Outliers removed using median absolute deviation; fluxes with EddyPRO flags >1 removed; manual checks performed weekly.

## Gap filling and flux partitioning
- Gap-filling of EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al. 2005) via REddyProc.
- NEE partitioned into GEP and TER using flux partitioning driven by Ta; gap-filled outputs include NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.

## Data structure and variables
- Time series stored in a single CSV with timestamps ending each 30-minute period; -9999 marks missing records.
- Variables include: DateTime, NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse, PPFDbc1/2/3, G1/G2, Tsoil1/2, VWC1/2, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.

## Data provenance and usage notes
- Funding: Natural Environment Research Council (CarboBiocrop) and CEH Integrating Fund.
- Site and methodological references provided for deeper context (e.g., Drewer et al. 2012; Reichstein et al. 2005, 2016; Morrison et al. 2019).
- Dataset offers a comprehensive, standardized multi-year EC flux record suitable for environmental health and carbon/wate-energy budgets, aligning with standardised monitoring practices and enabling data reuse and cross-study comparisons.