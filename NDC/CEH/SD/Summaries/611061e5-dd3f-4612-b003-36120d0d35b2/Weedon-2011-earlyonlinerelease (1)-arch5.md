# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

- Overview
  - Presents the WATCHForcing Data (WFD) used to drive land surface models and hydrological models across the 20th century.
  - Provides sub-daily meteorological forcing data, bias-corrected and regionally coherent, to support evaporation and hydrological analyses and model intercomparisons.

- Data content and structure
  - Forcing variables include: wind at 10 m, 2 m air temperature, surface pressure, 2 m specific humidity, downward longwave and shortwave radiation, rainfall and snowfall rates.
  - Spatial resolution: half-degree grid; format: netCDF with ALMA conventions; CRU land-sea mask; Antarctic excluded.
  - Temporal structure: 3-hourly values for most variables; 6-hourly values for temperature, pressure, humidity, and longwave radiation, interpolated to 3-hourly as needed.
  - Time periods:
    - Primary forcing: 1958–2001.
    - Pre-1958 extension: 1901–1957, constructed to match 1958–2001 statistics rather than exact historical timings.
  - PET estimates provided for model comparisons:
    - PET_rc: Penman-Monteith for a reference crop (uses ERA-40-based forcing, fixed surface resistance, VPD, and net radiation).
    - PET_PT: Priestley-Taylor method (radiation- and energy-based, suitable in humid regions).
  - Additional variables used in analyses: Net Radiation, VPD, Wind, Rainfall, Snowfall.

- Data sources, bias corrections, and processing
  - Basis data: ERA-40 reanalysis (1958–2001); reordered ERA-40 data for pre-1958 period (1901–1957).
  - Bias and ancillary corrections:
    - Temperature, pressure, humidity, and longwave radiation corrected for elevation and biases; CRU data used as anchors where appropriate.
    - Shortwave radiation corrected for aerosols via HadGEM2-A AOD, with cloud corrections anchored to CRU observations.
    - Longwave radiation adjusted for aerosol effects; no global bias correction required after adjustments.
    - Precipitation adjusted via a multi-step approach to preserve wet-day frequency and large-scale coherence, combining ERA-40 with GPCCv4 totals and CRU counts; rain/snow partitioning preserved from ERA-40.
  - Pre-1958 data governance:
    - ERA-40 years are randomly assigned to 1901–1957 years to preserve overall statistics (extremes, diurnal/seasonal variability) while not preserving exact event timing.
    - Similar processing steps (elevation, diurnal range, aerosols, cloud corrections) applied to reordered data; limitations acknowledged due to sparser early observations.

- Validation, limitations, and uncertainties
  - Validation shows good agreement for daily-to-monthly surface temperature and radiation fluxes; precipitation correlations are weaker due to scale and convection representation.
  - Sub-daily precipitation is less reliable; monthly means and interannual trends align better with observations in many regions.
  - Differences exist between grid-scale (WFD) and site-scale observations due to footprint and orography, impacting local accuracy.
  - Pre-1958 data carry uncertainties related to historical data sparsity and the randomization approach.

- Global and regional findings (context for data stewardship)
  - PET_rc exhibits significant global relationships with varying regional trends; PET_pt shows complementary patterns in humid regions.
  - Global and regional analyses emphasize that PET and precipitation/PET balance can vary substantially by basin, with notable regional heterogeneity in trends and interannual variability.
  - Precipitation changes over 1958–2001 are generally not globally uniform; regional shifts and variability influence hydrological interpretation.

- Documentation, provenance, and governance
  - Extensive provenance is documented, including:
    - ERA-40 as the basis, CRU for bias anchors, GPCC for gauge-based adjustments, CRU cloud data, HadGEM2-A aerosols for radiative forcing.
  - Clear data quality notes, uncertainties, and caveats to aid proper interpretation and reproducibility.
  - Provenance and processing details are provided to support audit trails and reproducibility of analyses.

- Usage guidelines and caveats for data stewards
  - Use PET_rc for energy- and humidity-driven evaporation analyses in humid to semi-arid contexts; use PET_PT for radiative forcing and energy-balance perspectives in humid regions.
  - Treat 1901–1957 as surrogate forcing with preserved statistics, not exact historical event timing; exercise caution when interpreting interannual/decadal trends for this period.
  - Be mindful of uncertainties in precipitation, especially in tropical and high-latitude regions; interpret precipitation-driven outputs in light of validation limitations.
  - Maintain linkage to original data sources and corrections (ERA-40 basis, bias corrections, aerosol adjustments, cloud-based corrections) in metadata for reproducibility.
  - Leverage Appendix Table 1 and methodology sections to reproduce processing steps and assess suitability for basin- or regional-scale studies.

- Data sharing, accessibility, and lifecycle
  - WFD is presented as a documented forcing dataset to support land-surface and hydrological modeling and cross-model comparisons.
  - Documentation and online resources are provided to enable access, reproducibility, and audit trails.
  - Aims to support hydrological planning, climate impact assessments, and intercomparison projects (e.g., WATCH, WaterMIP).