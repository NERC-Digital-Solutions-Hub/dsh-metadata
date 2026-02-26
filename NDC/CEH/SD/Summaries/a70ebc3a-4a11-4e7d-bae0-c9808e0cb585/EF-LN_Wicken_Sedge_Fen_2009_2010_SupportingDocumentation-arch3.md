# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010 Jon Kelvin, Mike Acreman, Richard J. Harding & Ross Morrison

- Overview
  - Time-series dataset of land-surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ) measured at Wicken Sedge Fen (EF-LN) using eddy covariance (EC) between 2009-03-20 and 2011-01-16/17, with ancillary weather and soil observations and atmospheric turbulence variables.
  - Data processed to provide gap-filled fluxes and partitioned components, plus quality-controlled ancillary data and turbulence metrics.
  - Utilizes standardized processing and uncertainty assessment to support analyses of carbon, energy and water fluxes in a lowland fen ecosystem.

- Study site
  - Wicken Sedge Fen National Nature Reserve, Cambridgeshire, UK (site code EF-LN), conservation-managed rich fen on undrained deep peat.
  - Climate: temperate maritime; mean annual temperature ~10.7°C, ~563 mm year-1 precipitation (1981–2010).
  - Peat depth ~2–4 m; hydrologically isolated from surrounding arable land; calcareous water from Monks Lode; soil properties provided (peat bulk density, pH, C content, C:N).

- Sampling regime
  - Automated flux, meteorological and soil data collected during two periods: 2009-03-20 14:30 to 2009-12-31 08:30 and 2010-04-09 12:30 to 2011-01-17 00:00.

- Flux data acquisition
  - EC measurements above grass canopy at 3.95 m height.
  - Instruments: Solent R3 ultrasonic anemometer with LI-7500 infrared gas analyser; raw data at 20 Hz; data logged by a CR3000 micrologger.
  - Fluxes recorded: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2).

- Ancillary data acquisition
  - Co-located meteorology and soil observations: air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (Rnet); incoming/outgoing shortwave (SWin/SWout) and longwave (LWin/LWout) radiation; soil heat fluxes (G) at two locations; soil temperature at upper 0.1 m.
  - Instruments: HMP45, CNR1 net radiometer, HFP01 flux plates, TCAV thermocouples.

- Data processing
  - Flux calculations using EddyPRO software (v7.0.6); 30-minute averaging periods.
  - QC and corrections: quality control of 20 Hz data; angle-of-attack correction for Gill sensors; 2D coordinate rotation; corrections for high/low-frequency co-spectral attenuation; H flux correction for humidity; LE and NEE corrections for density fluctuations; random uncertainty per 30-minute flux per Finkelstein & Sims.
  - Derived turbulence metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).

- Quality control
  - Removal of statistical outliers (median absolute deviation method).
  - Flux ranges applied: H (-200 to 550 W m^-2), LE (-60 to 600 W m^-2), NEE (-50 to 30 μmol CO2 m^-2 s^-1).
  - NEE checks: nighttime negative fluxes, friction velocity threshold (u* > 0.18 m s^-1), and ≥80% flux footprint from target ecosystem.
  - Weekly visual checks and manual removal of clearly erroneous values.

- Data gap-filling and flux partitioning
  - Gap-filling for EC data (NEE, LE, H) via Marginal Distribution Sampling (Reichstein et al., 2005).
  - Partitioning NEE into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven approach (no soil temperature data available at site); implemented with REddyProc (R) version (Reichstein et al., 2016).
  - Gap-filling of meteorological data where possible using on-site automated weather station data.

- Details of data structure
  - Output: a single CSV with tabular data; gap-filled and partitioned data provided over 2009-01-01 to 2011-01-17, with actual flux measurements present during 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-17.
  - Missing records denoted by -9999.
  - Table 1 describes variable names and units (e.g., NEE, LE, H, Tau, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G, WS, WD, Ustar, TKE, L, zL, Xpeak, x70, x90, fp2D, NEE_filled, and corresponding uncertainties).

- Nature and units of recorded values
  - Fluxes: NEE (μmol CO2 m^-2 s^-1), LE and H (W m^-2), τ (kg m^-1 s^-2).
  - Ancillary meteorology/soil: Ta (°C), RH (%), VPD (hPa), SWin/SWout/LWin/LWout/Rnet (W m^-2), G (W m^-2), Ta/RH at 2 m, wind speed/direction (ms^-1, degrees), u* (ms^-1), L (m), zL (dimensionless), TKE (m^2 s^-2), etc.
  - Derived variables: NEE_filled, LE_filled, H_filled with associated uncertainties; GEP and TER values.

- Acknowledgments and references
  - Supported by Natural Environment Research Council award NE/R016429/1 (UK-SCAPE National Capability).
  - Acknowledges National Trust and Wicken Fen staff; additional author support noted.
  - Core methodological references for EC processing, QC, gap-filling, and partitioning cited (e.g., Reichstein et al. 2005; Reichstein et al. 2016; Mauder et al. 2013; Moncrieff et al. 1997, 2004; Webb et al. 1980; Wilson et al. 2001).