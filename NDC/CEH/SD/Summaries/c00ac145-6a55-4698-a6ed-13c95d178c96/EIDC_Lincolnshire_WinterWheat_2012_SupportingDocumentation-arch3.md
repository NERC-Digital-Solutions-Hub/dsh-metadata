# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

- A time-series dataset of surface-atmosphere fluxes and ancillary observations collected during the 2012 growing season at a winter wheat field in Lincolnshire, UK.
- Primary fluxes: net ecosystem exchange of CO2 (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Fluxes were measured with open-path eddy covariance at 3.0 m above the canopy, complemented by meteorological and soil physics data.
- Data processing and gap-filling applied to produce a complete, analyzed time series (30-minute intervals) including partitioning of NEE into gross ecosystem production (GEP) and total ecosystem respiration (TER).

## Study site
- Location: arable cropland about 10 km north of Lincoln, UK; coordinates 53°19'17.89"N, 0°35'7.83"W.
- Climate: temperate maritime (mean annual temperature ~9.8°C, mean annual precipitation ~614 mm).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk densities ~1.46–1.53 g cm^-3; soil texture ~49% sand, 36% silt, 15% clay; soil pH ~6.32.
- Site details referenced from Drewer et al. (2012) and Robertson et al. (2017).

## Sampling regime
- Period: 2012-04-05 00:30 to 2012-08-08 00:00 GMT (UTC).
- Automated, co-located flux, meteorological, and soil observations conducted throughout the growing season.

## Flux data acquisition
- Eddy covariance (EC) system mounted at 3.0 m above canopy center of the field.
- Instruments:
  - Open-path EC system with R3 sonic anemometer (Gill) and LI-7500 CO2/H2O infrared gas analyser (LI-COR).
  - Raw data: 20 Hz sampling of 3 velocity components, sonic temperature, and densities of water vapour and CO2.
  - Data logger: CR3000.
- Primary fluxes reported as 30-minute means: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2).

## Ancillary data acquisition
- Net radiation (Rnet) and components (SWin, SWout, LWin, LWout) at 1.5 m above canopy.
- Soil heat flux (G) at two locations (0.05 m depth).
- Air temperature (Ta) and relative humidity (RH) at 2.0 m height.
- Soil temperature (Tsoil) at 0.05 and 0.1 m; soil volumetric water content (VWC) at 0.05 and 0.1 m.
- Rainfall measured with a tipping-bucket gauge in an adjacent field.
- Data logged as 30-minute means to the CR3000.

## Data processing
- Fluxes calculated with EddyPRO software (Version 6.1) using block averaging (30 min).
- Processing steps include:
  - QC of raw 20 Hz data.
  - Angle-of-attack correction for Gill anemometer.
  - 2D coordinate rotation to align with local terrain.
  - Corrections for high/low-frequency co-spectral attenuation.
  - Humidity-related correction for H; density correction for LE and CO2.
  - Random uncertainties estimated per Finkelstein & Sims.
  - Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).
- Data quality and provenance emphasized through standardized processing.

## Quality control
- Outliers removed using median absolute deviation; non-stationary conditions excluded.
- Flux ranges applied: H (-200 to 400 W m^-2), LE (-100 to 500 W m^-2), NEE (-70 to 35 μmol CO2 m^-2 s^-1).
- NEE rejection criteria: negative CO2 flux at night (SWin < 20 W m^-2) and/or low friction velocity (u* < 0.07 m s^-1) as per Reichstein et al. 2016.
- Footprint analysis (ART Footprint Tool) used to ensure >75% flux originates from target ecosystem.
- Weekly visual QC to identify clearly erroneous values; some values manually removed.

## Data gap-filling and flux partitioning
- Gaps in EC fluxes (NEE, LE, H) filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- Gaps in key meteorological variables filled using linear relationships from adjacent weather stations.
- NEE partitioned into GEP and TER using Reichstein et al. (2005) approach, driven by Ta observations.
- Gap-filling and partitioning performed with REddyProc (R) version compatible with Reichstein et al. 2016.

## Details of data structure
- Output provided as a single CSV with tabular columns as described in Table 1.
- Gap-filled and partitioned data included; missing records denoted by -9999.
- Time axis: DateTime in GMT (UTC) with 30-minute resolution.
- Variables include:
  - NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc
  - CO2_strg, CO2_strg_unc, LE_strg, LE_strg_unc, H_strg, H_strg_unc
  - Pa (two columns), Ta (two columns), RH (two columns), VPD (two columns)
  - SWin, SWout, LWin, LWout, Rnet, G1/G2, Tsoil1–4, VWC1–4
  - Precipitation (two columns), Windspeed (two columns), Winddir (two columns)
  - Ustar, TKE, L, zL
  - FootprintFraction (two columns), x_peak/x_70/x_90 (two columns)
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd
  - TER, GEP
- Two-column pairings indicate raw versus processed (e.g., NEE_filled vs NEE_filled_sd).

## Acknowledgments and references
- Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE and relevant Carbo-Biocrop support.
- Dataset authors acknowledge landowners and collaborators; references provided for methods and supporting studies.

## Relevance for monitoring framework development
- Demonstrates end-to-end data lifecycle: instrument setup, data collection, processing, QC, gap-filling, and partitioning to derive ecosystem-level fluxes.
- Provides rich metadata on site conditions, instrumentation, processing corrections, and quality criteria, highlighting data governance needs.
- Illustrates practical barriers and decisions in environmental monitoring data, such as handling missing data, ensuring data provenance, and maintaining data quality standards.