Supporting information for: Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) using eddy covariance (EC) at EF-DA site, 2012-06-22 00:30 to 2020-01-01 00:00.
- Includes ancillary weather and soil physics observations and turbulence-related variables.
- Data processed to produce gap-filled and partitioned fluxes, with associated uncertainties.

## Study site (including site activity, crop details)
- Location: East Anglian Fens, UK (The Fenland). Coordinates: 52°31'N, 0°29'E; elevation ~0 m amsl.
- Climate: temperate maritime; mean annual temperature ~10.4°C and ~564 mm rainfall (1981–2010).
- Site characteristics: drained deep peat, agriculture-dominated landscape with trapezoidal arable fields, hedgerows, ditch systems.
- Farm: Rosedene farm, >100 fields (~1,400 ha).
- Crops over study period: lettuce (2012, 2014, 2016, 2018), leek (2013), celery (2015), sugar beet (2017), potatoes (2019).

## Sampling regime
- Automated measurements (flux, meteorology, soil physics) from 2012-06-22 00:30 to 2020-01-01 00:00.

## Flux data acquisition
- Measurement height: 1.5 m above canopy.
- Instruments: LI-7500 IRGA for CO2/H2O; CSAT3 sonic anemometer; wind orientation ~225° SW.
- Data: raw 20 Hz; 30-minute flux averages for NEE (μmol CO2 m−2 s−1), LE (W m−2), H (W m−2), τ (kg m−1 s−2); turbulence variables and gas densities recorded.

## Ancillary data acquisition
- Radiometry: NRLite2 and CNR4 radiometers for net radiation and components.
- PAR: SKP01 sensor.
- Air conditions: Ta (°C), RH (%), measured at 2 m.
- Precipitation: ARG100 tipping-bucket gauge (4 m away).
- Soil: two arrays with soil heat flux (G), soil temperature (Tsoil), volumetric water content (VWC) sensors, spaced beneath EC instrumentation.

## Data processing
- Flux calculation: EddyPRO v6.1; QC, 2D rotation, spectral corrections, density corrections for LE and CO2, random uncertainties per Finkelstein & Sims (2001).
- Outputs: wind speed, wind direction, u*, TKE, Obukhov length (L), z/L; flux footprints estimated (Neftel et al., 2008).
- Time series: 30-minute block-averaged fluxes and turbulence metrics.

## Quality control
- Outliers removed via median absolute deviation; non-stationary turbulence periods removed.
- Flux ranges: H −200 to 400 W m−2; LE −200 to 600 W m−2; NEE −40 to 40 μmol CO2 m−2 s−1.
- Nighttime NEE excluded; footprint criterion: >70% contribution from target ecosystem.
- Weekly visual checks; clearly erroneous values removed manually.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005).
- Partitioning NEE into GEP and TER using Ta-driven partitioning (Reichstein et al., 2005).
- Tools: REddyProc (R) for gap-filling and partitioning (Reichstein et al., 2016).

## Details of data structure
- Time series provided as CSV with ASCII format; missing records denoted as -9999.
- Includes both raw (NEE_f, LE, H, τ, etc.) and gap-filled/partitioned products (NEE_filled, LE_filled, H_filled, TER, GEP).

## Nature and units of recorded values
- DateTime: yyyy-mm-dd HH:MM:SS (UTC).
- NEE: μmol CO2 m−2 s−1; NEE_unc: μmol CO2 m−2 s−1.
- LE: W m−2; LE_unc: W m−2.
- H: W m−2; H_unc: W m−2.
- τ: kg m−1 s−2; τ_unc: kg m−1 s−2.
- Additional fields include storage terms, pressure (Pa/Bar), Ta, RH, VPD, Rnet, Rg, G, Tsoil, VWC, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.

## Acknowledgements
- Site established and supported through NERC and Defra-funded projects; long-term site support from University of Leicester; farm owners and managers acknowledged.

## References
- Key methodological and processing references for eddy covariance, QC, gap-filling, and partitioning methods and tools (e.g., Reichstein et al., 2005; Reichstein et al., 2016; EddyPRO; Neftel et al., 2008; Moncrieff et al.; Vickers & Mahrt; Webb et al.; etc.).