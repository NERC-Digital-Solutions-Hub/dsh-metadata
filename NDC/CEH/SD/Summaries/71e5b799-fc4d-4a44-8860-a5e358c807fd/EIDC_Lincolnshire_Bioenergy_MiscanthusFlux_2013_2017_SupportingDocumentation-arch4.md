# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017

- Purpose: Provides long-term, high-quality eddy covariance data of surface-atmosphere exchanges (NEE, sensible heat H, latent heat LE, and momentum τ) over a mature Miscanthus plantation, with extensive ancillary meteorological and soil data to support carbon and energy balance analyses.
- Time frame: 2013-07-05 00:30 to 2017-11-07 00:00; data are processed to gap-filled NEE, LE, H and partitioned into GEP and TER, plus storage terms and other diagnostic variables.

## Study site
- Location: Miscanthus x. giganteus plantation, 11.5 ha, Lincolnshire, UK (coordinates provided in the document).
- Climate and soils: Temperate maritime climate; soils are seasonally waterlogged fine loams (Beccles 1 association).
- Management history: Established 2006 on former arable land; harvested annually since 2008; remedial cultivation in 2013; soil amendments in 2013–2016.
- Relevance: Site characteristics and management information support interpretation of carbon, energy, and water fluxes in a commercial bioenergy context.

## Data collection regime
- Automated measurements: Eddy covariance and micrometeorological observations from a mast above the Miscanthus canopy; height maintained at ~2x canopy height.
- Flux variables: Net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Instrumentation: Open-path EC system with R3 sonic anemometer and LI-7500 CO2/H2O sensor; data logged at 20 Hz and aggregated to 30-minute means.
- Ancillary meteorological data: Air temperature (Ta), relative humidity (RH) at 2 m; net radiation and its components; total incoming shortwave radiation; below-canopy PPFD; soil heat flux; soil moisture and temperature; precipitation.
- Data organization: Time series stored as 30-minute records; missing data flagged (-9999) after QC.

## Data processing and quality control (QC)
- Processing: Flux calculations using EddyPRO software (v6.1); includes quality control, tilt correction, coordinate rotation, attenuation corrections, density corrections, and uncertainty estimates.
- QC steps:
  - Outlier removal via median absolute deviation.
  - Non-stationarity checks; data excluded if non-stationary.
  - Plausible flux ranges: H (-200 to 400 W/m²), LE (-100 to 500 W/m²), NEE (-70 to 35 μmol CO2 m⁻² s⁻¹).
  - Nighttime NEE filtering (exclude when negative) and a friction velocity threshold (u* > 0.14 m s⁻¹).
  - Footprint analysis to ensure fluxes originate from the target ecosystem (≥75% within site).
  - Weekly visual checks to remove clearly erroneous values.
- Outputs: Derived metrics such as friction velocity (u*), turbulence metrics (TKE, L, z/L), and quality-flagged fluxes.

## Data gap-filling and flux partitioning
- Gap filling: Marginal Distribution Sampling approach for EC fluxes (NEE, LE, H); meteorological gaps filled via linear relationships from adjacent weather stations.
- Flux partitioning: NEE partitioned into gross primary production (GEP) and total ecosystem respiration (TER) using established Reichstein-based methods; Ta-driven partitioning with REddyProc (R).
- Data availability: Gap-filled and partitioned fluxes provided alongside original measurements.

## Details of data structure and units
- File format: A single CSV file containing the complete 30-minute time series from 2013-07-05 00:30 to 2017-11-07 00:00; missing records marked as -9999.
- Core variables (examples):
  - NEE, NEE_filled, NEE_filled_sd
  - LE, LE_filled, LE_filled_sd
  - H, H_filled, H_filled_sd
  - TER, GEP
  - Additional columns: CO2 storage terms, moisture and energy terms, Ta, RH, SWin, SWout, LWin, LWout, Rnet, PPFD, G, Tsoil, VWC, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, etc.
- Units: As described in the variable descriptions (e.g., NEE in μmol CO2 m⁻² s⁻¹, LE and H in W m⁻², etc.).
- Metadata: Variable names and units adapted from LI-COR and Reichstein et al. references; comprehensive documentation of variables and their meanings is included with the dataset.

## Data quality and provenance notes
- Data collection funded by the National Environment Research Council; authors acknowledge field support and landowners.
- Extensive references accompany the dataset describing processing choices, QC, and methodological standards (e.g., EddyPRO, Reichstein 2005/2016; footprint modeling; standard EC processing guidelines).

- Relevance for Data Leaders:
  - Demonstrates end-to-end data lifecycle: collection, processing, QC, gap-filling, and product generation.
  - Emphasizes robust metadata, standardized processing, uncertainty quantification, and footprint validation.
  - Illustrates handling of complex, multi-variable terrestrial data at a commercial scale with clear documentation for reuse and interoperability.