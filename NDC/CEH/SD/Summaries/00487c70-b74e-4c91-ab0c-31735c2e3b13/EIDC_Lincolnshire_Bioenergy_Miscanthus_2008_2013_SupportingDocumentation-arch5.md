# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

- Purpose and scope
  - Time-series dataset of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance (EC) at a Miscanthus plantation in Lincolnshire, UK.
  - Ancillary meteorological and soil observations included to support interpretation and quality assessment.
  - Data processed to provide gap-filled and partitioned fluxes, with associated uncertainties.

- Study site context
  - Location: Miscanthus x. giganteus plantation (11.5 ha) about 10 km north of Lincoln, UK.
  - Climate and soils described: temperate maritime, loamy soils with specific bulk density, texture, organic carbon, nitrogen content, and pH ranges.
  - Plantation history: established 2006 on former arable land; annual harvests from 2008; limited fertiliser use (2010 onward).

- Sampling regime and data collection
  - Automated flux, meteorological, and soil observations from 2008-05-01 to 2013-02-18.
  - Flux measurements: open-path EC system on a mast; fluxes sampled at 20 Hz and aggregated to 30-minute means.
  - Ancillary data: meteorological (air temperature, humidity, net/radiation, radiation components, photosynthetically active radiation below canopy), soil measures (volumetric water content, soil temperature, soil heat flux), and wind metrics.
  - Data processing performed with EddyPRO software, including QC, coordinate rotations, and corrections for density and spectral effects.

- Quality control and data integrity
  - QC includes outlier removal (median absolute deviation), EddyPRO quality flags, and physical range checks for H, LE, and NEE.
  - Footprint analysis to ensure observations predominantly reflect the target ecosystem (>75% within site).
  - Visual inspection of data (weekly) to identify and remove clearly erroneous values.

- Gap-filling and flux partitioning
  - Gaps in NEE, LE, and H filled using Marginal Distribution Sampling (Reichstein et al. 2005) with Ta-driven partitioning of NEE into GEP and TER.
  - Gap-filling and partitioning performed with REddyProc (R) package.

- Data structure and contents
  - Time series provided as a single CSV file with columns defined in Table 1 (DateTime in GMT, NEE, LE, H, τ, CO2_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse, PPFDbc, G, Tsoil, VWC, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.).
  - Units and meanings mirror LI-COR conventions and Reichstein et al. (2016) conventions.
  - Timestamp granularity: end of each 30-minute averaging period.
  - Missing data indicated by -9999.
  - Gap-filled and partitioned flux values provided alongside original observations (e.g., NEE_filled, NEE_filled_sd, LE_filled, etc.).

- Nature and units of recorded values (highlights)
  - NEE: μmol CO2 m^-2 s^-1; NEE_filled and NEE_filled_sd accompany observed values.
  - LE: W m^-2; LE_filled and LE_filled_sd accompany observed values.
  - H: W m^-2; H_filled and H_filled_sd accompany observed values.
  - Tau: kg m^-1 s^-2; Tau_filled or related measures included with uncertainties.
  - Ancillaries: Ta (°C), RH (%), VPD (hPa), gas and radiation components, soil metrics (G, Tsoil, VWC), wind metrics, footprint fraction, Ustar, TKE, L (Obukhov length), z/L.
  - Data gaps and uncertainties are explicitly recorded to enable propagation of errors in downstream analyses.

- Provenance, processing, and references
  - Raw data processing and QC follow established micrometeorological protocols and cited literature (e.g., Mauder et al., Reichstein et al., Papale et al., Moncrieff et al.).
  - Gap-filling and partitioning rely on Reichstein et al. (2005) and the REddyProc package (Reichstein et al. 2016).
  - Flux footprint and quality checks implemented to ensure data representativeness of the target ecosystem.

- Data governance, reuse, and acknowledgments
  - Data collection funded by the Natural Environment Research Council (CarboBiocrop; CEH Integrating Fund).
  - Clear attribution to contributing authors and site landowners; dataset designed to be reusable, with thorough metadata and processing references for reproducibility.

- Practical relevance for data stewardship
  - Clear, standardized structure: a single time-series CSV with gap-filled and partitioned outputs and comprehensive ancillary data.
  - Explicit QC criteria, processing steps, and references enable auditability and governance.
  - Use of established tools (EddyPRO, REddyProc) and documented methodologies supports interoperability and future data integration.
  - -9999 as a sentinel value for missing data supports robust data handling in downstream systems.