# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Turbulent flux densities measured with open-path eddy covariance (EC) between 2013-07-05 00:30 and 2017-11-07 00:00.
- Ancillary weather and soil physics observations and atmospheric turbulence variables included.
- Main data file: Lincolnshire_Bioenergy_Miscanthus_2013_2017.csv; includes gap-filled and partitioned flux data.
- Data are provided as 30-minute averages, with -9999 used for missing records.
- Dataset supports assessments of carbon, energy, and water fluxes for a commercial Miscanthus plantation.

## Study site
- Location: Miscanthus x. giganteus plantation, 53°19'10.07"N, 0°35'18.65"W, ~10 km north of Lincoln, UK.
- Size: 11.5 ha mature plantation on former arable land.
- Climate: temperate maritime; mean 1981–2010 air temperature 9.8 ± 0.7 °C; precipitation 614 ± 93.5 mm year-1.
- Soils: Beccles 1 association; seasonally waterlogged fine loams; density ~1.46–1.53 g cm-3 in upper 0–0.3 m.
- Soil properties: 68 t C ha-1 and 11 t N ha-1 in upper 0.3 m; pH 6.8–7.3.
- Management history: established 2006, annual spring harvest since 2008; 2013 remedial cultivation and soil amendments (wood waste compost, Fibrophos, bio-mulch, fungi mix).

## Sampling regime
- Automated flux, meteorological, and soil physics measurements over 2013-07-05 to 2017-11-07.

## Flux data acquisition
- EC system mounted on a extendible mast, height ≈ twice Miscanthus canopy.
- Measurements: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2); 20 Hz sampling.
- Instruments: R3 sonic anemometer, LI-7500 IR gas analyser; data logged with CR3000.
- Ancillary EC variables: Ta and RH measured at 2 m; 0.1 Hz, logged as 30-minute means.

## Ancillary data acquisition
- Above-canopy net radiation components (Rnet, SWin, SWout, LWin, LWout) via CNR1 and BF3 sensors.
- Below-canopy PPFD (PPFDbc) at three below-canopy locations.
- Soil heat flux (G) at two locations; soil water content (VWC) at 0–0.3 m; soil temperature (Tsoil) at two locations.
- Precipitation measured with tipping-bucket gauge.
- All ancillary data stored as 30-minute means (or sums for precipitation).

## Data processing
- EddyPRO processing (Version 6.1) used to compute fluxes from raw EC data.
- Processing steps: QC of 20 Hz data, angle-of-attack corrections, 2D rotation, spectral corrections, humidity and density corrections; uncertainties calculated per standard methods.
- Derived metrics: wind speed, wind direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).

## Quality control
- Outlier removal via median absolute deviation; non-stationary conditions excluded.
- Flux filters: H (-200 to 400), LE (-100 to 500), NEE (-70 to 35 μmol CO2 m^-2 s^-1).
- NEE excluded at night and when u* below 0.14 m s^-1 (per Reichstein et al. 2016 method).
- Footprint analysis with ART Footprint Tool; fluxes considered representative if >75% originates from target ecosystem.
- Weekly visual QA and manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling of EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al. 2005).
- Meteorological gaps filled via linear relationships from adjacent weather stations.
- NEE partitioned into GEP and TER using flux partitioning driven by air temperature (per Reichstein et al. 2005).
- Gap-filling and partitioning performed with REddyProc (R package).

## Details of data structure
- Time series delivered as a single CSV with columns described in the dataset documentation.
- Gap-filled and partitioned variables included: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- Missing data represented by -9999.

## Nature and units of recorded values
- Variables and units detailed in the accompanying table, including:
  - DateTime; NEE and NEE_sd; LE and LE_sd; H and H_sd; τ and τ_sd; gap-filled terms (NEE_filled, LE_filled, H_filled) and their uncertainties; storage terms (CO2_strg, LE_strg, H_strg); meteorological and soil variables (Ta, RH, SWin, etc.); footprint fraction; Ustar; TKE; L; zL;  as appropriate for 30-minute records.

## Acknowledgments
- Data collection funded by the National Environment Research Council.
- Thanks to landowners, field support teams, and institutional collaborators for maintenance of EC and ancillary instrumentation.

## References
- Foundational methodological and site-specific references for EC processing, QC, gap-filling, flux partitioning, footprint analysis, and prior related studies on Miscanthus systems and site characteristics.