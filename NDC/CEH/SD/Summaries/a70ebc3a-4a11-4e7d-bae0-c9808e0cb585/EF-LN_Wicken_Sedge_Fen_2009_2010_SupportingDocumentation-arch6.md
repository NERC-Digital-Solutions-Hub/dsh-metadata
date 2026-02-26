# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010 Jon Kelvin, Mike Acreman, Richard J. Harding & Ross Morrison

## Overview
- Time series of land–surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ) at Wicken Sedge Fen (EF-LN), Cambridgeshire, UK.
- Turbulent fluxes captured using open-path eddy covariance (EC) between 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16.
- Dataset includes ancillary meteorological and soil-physics observations and turbulence-characterising variables.
- Provided as a single CSV with gap-filled and partitioned flux data and associated uncertainties, enabling self-contained data exploration.

## Study site
- Wicken Sedge Fen (EF-LN) flux observation site, coordinates 52° 18' 34.86" N, 0° 16' 47.01" E, 2 m amsl.
- Temperate maritime climate; mean annual temperature ~10.7°C and precipitation ~563 mm yr-1 (1981–2010).
- Large remaining fragment of undrained deep peat fen; peat depth ~2–4 m; hydrologically isolated from surrounding cropland.
- Primary calcareous water source: Monks Lode. Peat bulk density ~0.37 g m-3, pH 7.5, C content 32%, C:N ~15.

## Sampling regime
- Automated flux, meteorological, and soil measurements conducted during specified periods in 2009 and 2010–2011.

## Flux data acquisition
- EC measurements above a 3.95 m grass canopy.
- Fluxes: NEE (μmol CO2 m-2 s-1), H (W m-2), LE (W m-2), τ (kg m-1 s-2).
- Instruments: Solent R3 ultrasonic anemometer and LI-7500; data logged at 20 Hz with a CR3000 Micrologger.

## Ancillary data acquisition
- Meteorological: air temperature (Ta, °C) and relative humidity (RH, %) at 2 m; net radiation (Rnet) and short/longwave components; soil heat flux (G) at two depths; soil temperature (0–0.1 m).
- Co-located sensors and standard meteorological equipment utilized for context and QC.

## Data processing
- EC data processed with EddyPRO v7.0.6; 30-minute flux averages.
- Corrections and QC include: quality control of 20 Hz data, angle-of-attack corrections, 2D coordinate rotation, spectral corrections, density correction for H and LE, and adjustments for CO2 and humidity effects.
- Derived variables: wind speed, wind direction, friction velocity (u*), turbulence metrics (TKE), Obukhov length (L), stability parameter (z/L).

## Quality control
- Outlier removal via median absolute deviation; flux ranges used to filter extreme values (e.g., H, LE, NEE).
- NEE vetted with night-time criteria (negative fluxes excluded), friction velocity threshold (u* > 0.18 m s-1), and 2D footprint criterion (≥80% from target ecosystem).
- Weekly visual checks to catch additional anomalies; manual removal of clearly erroneous data.

## Data gap-filling and flux partitioning
- Gaps in EC data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into GEP (gross ecosystem production) and TER (ecosystem respiration) using Ta-driven partitioning approaches (Reichstein et al., 2005).
- Gap-filling and partitioning performed with REddyProc (2016) in R; where possible, meteorological gaps filled using an automated weather station at the site.

## Details of data structure
- Time series provided in a single CSV file with the structure described in Table 1.
- Gap-filled and partitioned data cover 2009-01-01 00:30 to 2011-01-17 00:00.
- Flux data available for the measurement windows; missing records denoted by -9999.

## Nature and units of recorded values
- Core variables: NEE (μmol CO2 m-2 s-1) and NEE_filled; LE (W m-2) and LE_filled; H (W m-2) and H_filled; τ (kg m-1 s-2) and τ_filled; plus ecosystem storage term (CO2_strg).
- Ancillary variables: Ta (°C), RH (%), VPD (hPa); radiation components (SWin, SWout, LWin, LWout, Rnet); soil heat fluxes (G1, G2); soil and canopy temperature; wind metrics (WS, WD, Ustar); turbulence metrics (TKE, L, zL); footprint metrics (Xpeak, x70, x90, fp2D).
- Data columns include both pre-gap-filling and gap-filled values, with standard deviations where provided.

## Acknowledgments
- Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE; appreciation to Wicken Fen National Nature Reserve staff and collaborators.

## References
- Key methodological and processing references for EC, QC, gap-filling, and flux partitioning are provided (e.g., Reichstein et al., 2005; Reichstein et al., 2016; EddyPRO documentation; Moncrieff et al.; Webb et al.; Mauder et al.).