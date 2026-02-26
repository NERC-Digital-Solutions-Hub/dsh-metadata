# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010

- Purpose and contents
  - Time series observations of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) at the EF-LN Wicken Sedge Fen site.
  - Data collected using eddy covariance (EC) between 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16.
  - Includes ancillary meteorological and soil physics observations and variables characterising atmospheric turbulence.

- Study site context
  - Wicken Sedge Fen (EF-LN) flux site coordinates: 52° 18' 34.86" N, 0° 16' 47.01" E, 2 m amsl.
  - Conservation-managed rich fen within the Cambridgeshire Fens, UK; temperate maritime climate; peat depth 2–4 m.
  - Hydrologically isolated from surrounding arable land; primary water source Monks Lode.
  - Site properties: peat bulk density 0.37 g m-3, pH 7.5, C content 32%, C:N ~15.

- Sampling regime and data acquisition
  - Automated flux, meteorological, and soil measurements.
  - EC fluxes measured above grass canopy at 3.95 m using a Solent R3 ultrasonic anemometer and LI-7500 CO2 analyzer; raw data at 20 Hz.
  - Data logger: CR3000.
  - Ancillary meteorology and soil measurements colocated with EC station.

- Ancillary data collection
  - Air temperature (Ta) and relative humidity (RH) at 2 m.
  - Net radiation (Rnet) and components of short- and long-wave radiation.
  - Soil heat flux (G) at two locations (0.03 m depth).
  - Upper 0.1 m soil temperature.

- Data processing and variables
  - Flux densities computed with EddyPRO v7.0.6; 30-minute averaging.
  - Processing includes QC of 20 Hz data, angle-of-attack corrections, 2D rotation, spectral corrections, humidity and density corrections; random uncertainty via established methods.
  - Derived metrics: friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), footprint metrics, and flux partitioning outputs.

- Quality control (QC) and validation
  - Outlier removal using median absolute deviation; flux ranges enforced for H, LE, NEE.
  - NEE quality checks: night-time rejection, minimum friction velocity threshold, and >80% flux originating from the target ecosystem based on footprint.
  - Visual QC: weekly inspection and manual outlier removal as needed.

- Gap filling and flux partitioning
  - Gaps in EC data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
  - NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven algorithms; REddyProc (R) used for gap filling and partitioning (Reichstein et al., 2016).
  - Missing meteorological data filled where possible with site automation station observations.

- Data structure and documentation
  - Single CSV file containing the time series with columns detailed in Table 1.
  - Gap-filled and partitioned outputs provided for the full timespan; original flux data available for the measurement periods.
  - Time stamps in GMT; missing records denoted by -9999.
  - Table 1 documents variable names, units, and descriptions (including NEE, NEE_sd, LE, LE_sd, H, H_sd, Tau, Tau_sd, CO2_strg, Ta, RH, VPD, radiation terms, Rnet, G, WS, WD, Ustar, TKE, L, zL, Xpeak, x70, x90, fp2D, NEE_filled, and corresponding uncertainties).

- Data provenance and references
  - Data supported by NERC UK-SCAPE program; acknowledgments to Wicken Fen staff and related contributors.
  - Key references for data processing, QC, and methodology are provided (e.g., EddyPRO, Reichstein et al. gap-filling and partitioning methods, footprint concepts, and QC standards).

- Practical considerations for data leaders
  - Accessible as a documented, gap-filled, and partitioned time series suitable for carbon balance and energy flux analyses in peatland ecosystems.
  - Clear metadata on instruments, processing steps, QC criteria, and data limitations (periods measured, gaps, and uncertainty estimates).
  - Reproducible workflow: processing with EddyPRO v7.0.6 and REddyProc in R; explicit QC and gap-filling procedures outlined.