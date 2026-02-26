# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a winter wheat field, Lincolnshire, UK, 2012

## Overview of dataset
- Time series of surface-atmosphere fluxes: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured above a winter wheat canopy.
- Turbulent flux densities obtained via micrometeorological eddy covariance (EC) technique from 2012-04-05 00:30 to 2012-08-08 00:00 (UTC).
- Ancillary meteorological and soil physics observations and variables describing atmospheric turbulence are included.
- Data provided as a single CSV with gap-filled and partitioned fluxes and associated metadata.

## Study site
- Flux observation site located on arable cropland near Lincoln, UK (53°19'17.89"N, 0°35'7.83"W), ~10 km north of Lincoln.
- Climate: temperate maritime (mean annual temp ~9.8°C, precipitation ~614 mm/yr, 1981–2010 baseline).
- Soils: Beccles 1 association, seasonally waterlogged fine loams over Charnmouth Mudstone; bulk density ~1.46–1.53 g/cm³; texture ~49% sand, 36% silt, 15% clay; pH ~6.32.

## Sampling regime
- Automated flux, meteorological, and soil measurements from 2012-04-05 00:30 to 2012-08-08 00:00 (GMT).
- EC system mounted at 3.0 m height at field center; 20 Hz sampling; open-path CO2/H2O analyzer and sonic anemometer for wind and temperature.

## Flux data acquisition
- Fluxes: NEE (μmol CO2 m⁻² s⁻¹), H (W m⁻²), LE (W m⁻²), and τ (kg m⁻¹ s⁻²).
- Raw data logged with 20 Hz resolution and processed to 30-minute intervals.
- Instrumentation: LI-COR LI-7500 CO2/H2O analyzer, R3 sonic anemometer, CR3000 data logger.

## Ancillary data acquisition
- Net radiation (Rnet) and components (SWin, SWout, LWin, LWout) at 1.5 m above canopy.
- Soil heat flux (G) at 0.05 m depth at two locations.
- Air temperature (Ta) and relative humidity (RH) at 2 m; soil temperature (Tsoil) and soil moisture (VWC) at 0.05 m and 0.1 m depths (two replicates).
- Precipitation via tipping-bucket rain gauge in adjacent field.
- Data logged as 30-minute means.

## Data processing
- Flux calculation with EddyPRO v6.1, using 30-minute block averaging.
- Processing includes: QC of 20 Hz data; tilt correction and coordinate rotation; correction for spectral attenuation; humidity-related H corrections; density corrections for LE and CO2 fluxes.
- Random uncertainties for fluxes computed; derived meteorological variables (u*, TKE, Obukhov length L, z/L) calculated.
- EddyPRO also produced wind speed/direction, footprint metrics, and stability parameters.

## Quality control
- Outlier removal using median absolute deviation; non-stationary conditions flagged and removed.
- Fluxes rejected if outside plausible ranges (-200 to 400 for H, -100 to 500 for LE, -70 to 35 for NEE).
- NEE rejected at night when CO2 fluxes negative with low net radiation, and below a friction velocity threshold (u* < 0.07 m s⁻¹) per Reichstein et al. (2016).
- Footprint analysis (ART Footprint Tool) to ensure >75% flux originates from target ecosystem.
- Weekly visual QA to remove clearly erroneous values.

## Data gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled with Marginal Distribution Sampling (Reichstein et al. 2005).
- Gaps in meteorological variables filled using linear relationships from adjacent-field stations.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) driven by Ta using Reichstein et al. (2005) approach.
- Gap-filling and partitioning performed with REddyProc (R package).

## Details of data structure
- Time series data stored in a single CSV file with columns described in Table 1.
- Gap-filled and partitioned data included; missing records denoted by -9999.
- Time stamps in GMT (UTC).

## Nature and units of recorded values
- Core variables and their derived counterparts are provided, including:
  - NEE (μmol CO2 m⁻² s⁻¹) and NEE_filled with associated uncertainties
  - LE (W m⁻²) and LE_filled
  - H (W m⁻²) and H_filled
  - τ (kg m⁻¹ s⁻²) and its uncertainty
  - CO2 storage term, LE/H storage terms
  - Atmospheric pressure (Pa), air temperature (Ta, °C), RH, VPD
  - Shortwave and longwave radiation components (SWin, SWout, LWin, LWout), net radiation (Rnet)
  - Soil heat flux (G1, G2) and corresponding soil temperatures (Tsoil1–Tsoil4)
  - Soil volumetric water content (VWC1–VWC4)
  - Precipitation, Windspeed, Winddir, Ustar (friction velocity), TKE, L (Obukhov length), z/L
  - Footprint fraction and x_peak/x_70/x_90 (upwind distances contributing to flux)
  - NEE_filled_sd, LE_filled_sd, H_filled_sd
  - GEP and TER (μmol CO2 m⁻² s⁻¹)
- Units and variable descriptions are provided in adapted table form (Table 1).

## Acknowledgments and references
- Funding and support from Natural Environment Research Council (NERC) awards NE/R016429/1 and NE/H010726/1; UK-SCAPE and Carbo-Biocrop projects.
- Site access permission granted by landowners; acknowledgments to individuals contributing to site work.
- References listed for methodological context (eddy covariance processing, QC, footprint analysis, gap-filling, and related soil/biogeochemistry literature).