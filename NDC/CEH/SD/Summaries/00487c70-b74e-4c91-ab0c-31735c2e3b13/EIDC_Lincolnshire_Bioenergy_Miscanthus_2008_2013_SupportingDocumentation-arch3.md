# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via micrometeorological eddy covariance (EC).
- Data collection period: 2008-05-01 00:30 to 2013-02-18 00:00.
- Includes ancillary weather and soil physics observations and variables describing atmospheric turbulence.
- Dataset file: Lincolnshire_Bioenergy_Miscanthus_2008_2013.csv with gap-filled and partitioned flux data as a complete time series.

## Study site
- Location: Miscanthus x. giganteus plantation, 11.5 ha, near Lincoln, UK.
- Climate: temperate maritime (mean annual temperature ~9.8°C; ~614 mm rainfall).
- Soils: Beccles 1 association, seasonally waterlogged fine loams; specific soil properties provided (bulk density, texture, soil organic carbon, nitrogen, pH).
- Management: established 2006 on former arable land; rhizome planting density ~10,000 ha−1; partial replanting in 2007; no fertilizer until 2010 (Fibrefoss at 660 kg ha−1); annual spring harvests from 2008 onwards.

## Sampling regime
- EC and micrometeorological measurements conducted on a mast near plantation center; measurement height periodically adjusted to ~2× canopy height.
- Fluxes measured: NEE (μmol CO2 m−2 s−1), H (W m−2), LE (W m−2), τ (kg m−1 s−2) using open-path EC system with sonic anemometer and IR gas analyser.
- Raw data: 20 Hz sampling; logged with Hydra dataloggers.
- Ancillary measurements: air temperature, relative humidity, net radiation components, incoming/outgoing shortwave and longwave radiation, ground-based photosynthetic photon flux density, soil heat flux, soil moisture, soil temperature; data logged as 30-minute means.

## Data processing
- Flux calculations: using EddyPRO v6.1; 30-minute flux averages.
- Processing steps: QC of 20 Hz data, angle-of-attack corrections, 2D rotation to traffic terrain, corrections for high/low-frequency attenuation, humidity effects on H, density corrections on LE and NEE, uncertainty estimates.
- Additional outputs: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).
- Quality control: removal of outliers (median absolute deviation; Papale et al. 2006), EddyPRO quality flag, flux ranges checks, footprint assessment (≥75% flux originating within target ecosystem), visual inspection of weekly plots.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (MDS) approach (Reichstein et al. 2005).
- Flux partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using flux partitioning methods (Reichstein et al. 2005).
- Tools: REddyProc package in R (Reichstein et al. 2016) for gap-filling and partitioning.

## Details of data structure
- Data stored as a single CSV with columns described in Table 1; gap-filled and partitioned data provided as a complete time series from 2008-05-01 00:30 to 2013-02-18 00:00.
- Timestamps: end of each 30-minute flux averaging period (UTC).
- Missing values indicated by -9999.

## Nature and units of recorded values
- Key variables and units include:
  - NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc
  - CO2_strg (CO2 storage term), Pa (barometric pressure), Ta (air temperature), RH, VPD
  - SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse
  - PPFDbc1/2/3 (below canopy PAR) and corresponding locations
  - G1/G2 (soil heat flux), Tsoil1/Tsoil2 (soil temperature), VWC1/VWC2 (volumetric water content)
  - Windspeed, Winddir, FootprintFraction
  - Ustar (friction velocity), TKE, L (Obukhov length), zL (stability parameter)
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP
- Variable names and units follow adaptations from LI-COR and Reichstein et al. (2016).

## Data quality and governance
- Rigorous QC and processing standards applied; data provenance maintained via references to established methodologies (Ed dyPRO, Reichstein et al., Moncrieff et al., etc.).
- Footprint analysis ensures representativeness of the target ecosystem.
- Data use involves public sharing of datasets and underlying data, subject to data governance considerations and metadata completeness.

## Acknowledgments and references
- Data collection funded by the Natural Environment Research Council and related CEH funds.
- Authors acknowledge landowner permission and reference foundational methodological sources for EC measurements, QC, gap-filling, and partitioning.

## Relevance to Monitoring Frameworks
- Demonstrates end-to-end monitoring workflow: site description, sensor suite, data acquisition, processing, QC, gap-filling, and flux partitioning.
- Highlights importance of metadata completeness, data provenance, and transparent processing steps for monitoring frameworks.
- Illustrates challenges and governance considerations around data sharing, standardization, and up-to-date data maintenance.
- Provides a rich, multi-variable dataset suitable for evaluating environmental carbon and energy flux monitoring approaches and informing future monitoring design decisions.