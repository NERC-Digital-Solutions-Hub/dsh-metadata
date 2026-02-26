# Creation of the WATCHForcing Data and its use to assess global and regional = reference crop evaporation over land during the twentieth century.

## Overview
- Documents the WATCH Forcing Data (WFD), a half-degree gridded meteorological forcing dataset for land surface and hydrological models.
- Provides sub-daily forcing across the twentieth century to assess external drivers of evaporation (PET) and related variables.
- Covers global and regional analyses across major basins and includes tools for comparing PET estimates and climate drivers.

## Key data components and variables
- PET and related meteorology:
  - PET rc (Penman-Monteith) and PET PT (Priestley-Taylor) as reference-evaporation estimates.
  - Forcing variables: Net Radiation, VPD, Wind, Rainfall, Snowfall, Precipitation.
- Temporal coverage and basins:
  - 1901–1957: data generation based on ERA-40 with period-appropriate substitutions.
  - 1958–2001: bias-corrected ERA-40-based fields (with CRU/GPCC inputs for validation and corrections).
  - 1979–2001: extended interval for trend analysis where available.
- Spatial framework:
  - 0.5° grid with CRU land-sea mask; variables provided in mm/yr for PET and W m-2 or kPa for atmospheric variables.
- Example basin categories included in the appendix (e.g., Orange River, Lena, Murray-Darling, Ganges-Brahmaputra) with basin-specific statistics.

## Temporal coverage, data generation and bias correction
- 1958–2001:
  - ERA-40 basis data merged with observations; temperature, pressure, humidity, and radiation bias-corrected against CRU/Flux validation datasets; aerosol and cloud corrections applied to radiation fields.
- 1901–1957:
  - ERA-40 years randomly assigned to 1901–1957 years in a fixed order (to preserve diurnal/seasonal structure as far as possible); same preprocessing steps applied where data were available.
  - Caveats: pre-1958 variability is less reliable due to randomization, sparse station coverage, and reliance on climatology substitutions in data-poor regions.
- 1979–2001:
  - Used where available to strengthen trend analyses; per-basin statistics provided for this interval.
- Data provenance and reproducibility:
  - Explicit documentation of ERA-40 basis years, randomization scheme for pre-1958 years, and all bias/adjustment steps.
  - Appendix includes the ERA-40 basis year order used for 1901–1957.

## Basin-level trends and key findings (as presented in Appendix-style data)
- PET rc (mm/yr) and PET PT (mm/yr) across basins show varied trends by interval:
  - Some basins exhibit significant trends in PET rc and PET PT (as indicated by low Adjusted Slope P values in certain intervals).
  - Examples show substantial changes in PET estimates across 1901–1957, 1958–2001, and 1979–2001 intervals, with both increasing and decreasing patterns depending on basin and interval.
- Net Radiation, VPD, Wind, Rainfall, Snowfall, Precipitation:
  - Basin-by-basin statistics indicate diverse patterns across intervals, with some periods showing increasing net radiation or VPD, others showing declines.
  - Precipitation generally presents substantial regional variability; Snowfall remains relatively small in many basins but shows notable regional deviations in some cases.
- Interval-specific interpretation:
  - 1901–1957: often large interannual variability and distinct slope signs, reflecting data generation method and early-period uncertainties.
  - 1958–2001: more robust bias-corrected forcing; clearer signals of change in certain basins and variables.
  - 1979–2001: additional perspective on shorter-term trends; some basins show marked changes in PET/PT and radiation-related drivers.

## Practical data quality notes for data stewards
- Pre-1958 reliability:
  - Data prior to 1958 are less reliable in parts of the world due to limited station coverage and the ERA-40-based randomization approach.
- Sub-daily precipitation:
  - Sub-daily precipitation variability and convective rainfall remain challenging to reproduce consistently across all basins.
- Elevation and site biases:
  - Temperature, pressure, and humidity can be affected by elevation differences between stations and grid cells.
- Significance and interpretation:
  - Many basin-level slopes have varied significance across intervals; use Adjusted Slope P values to assess reliability of trends for each basin and variable.

## Data availability and governance considerations
- Publication and access:
  - WATCH Forcing Data is documented in the WATCH Technical Report and is intended to drive multiple LC/GLM model applications.
- Format and metadata:
  - NetCDF ALMA format; half-degree grid; comprehensive metadata on bias corrections (aerosols, clouds), precipitation corrections, and data provenance.
- Provenance and versioning:
  - Track ERA-40 basis years, re-ordering scheme for 1901–1957, and all bias/correction steps to enable reproducibility.
- Guidance for usage:
  - Clearly document differences between PET rc and PET PT usage, regional interpretation of trends, and caveats for pre-1958 data reliability.
  - Provide access to both the 1958–2001 dataset and the 1901–1957 re-ordered dataset, with regional caveats and recommended aggregation levels.

## Practical implications and guidance for Data Stewards
- Ensure robust provenance: document ERA-40 basis data, pre-1958 randomization scheme, and all corrections applied.
- Maintain rich metadata: specify grid resolution, variable definitions, time stepping, and interpolation/extrapolation rules; record aerosol, cloud, and gauge-bias corrections.
- Support discoverability and reuse: include usage notes, data limitations, and guidance on PET rc vs PET PT selection for different climate regimes.
- Manage versioning and updates: track changes in bias corrections, aerosol representations, and precipitation adjustments when updating to newer reanalyses or auxiliary datasets.
- Explicitly flag data quality constraints: identify regions/times with uncertain precipitation, wind, or surface-pressure fields; guide users toward appropriate aggregated timescales (monthly vs daily) for robust analyses.