# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

- Purpose and scope
  - Global meteorological forcing data at 0.5° resolution for land surface and hydrological models, supporting diurnal-to sub-daily simulations across the 20th century.
  - Primary variables used to drive models include wind, temperature, humidity, pressure, radiation (shortwave and longwave), and precipitation (rainfall and snowfall).

- Spatial and temporal structure
  - Spatial: fixed 0.5° land grid (67,420 points, excluding Antarctica) using a land-sea mask; NetCDF format with ALMA convention.
  - Temporal: main series 1958–2001 with sub-daily (diurnal-cycle-resolving) capability; 6-hourly data for core forcing fields, with 3-hourly interpolation to a common time step.
  - Data packaging: suitable for GIS workflows and integration with other datasets, with explicit time-step and mask alignment requirements.

- Data construction and corrections
  - Basis and bias corrections: ERA-40 reanalysis as the starting point; bias corrections anchored to CRU observations and GPCC precipitation totals; elevation adjustments applied to interpolated variables; temperature and diurnal range bias corrections using CRU-based climatologies.
  - Radiation and aerosols: downward longwave and shortwave radiation corrected for cloud cover and aerosols; direct/indirect aerosol effects included, with volcanic aerosols incorporated in radiative transfer calculations.
  - Precipitation processing: six-step merging of ERA-40 rainfall and snowfall into physically consistent fields; adjustments to wet-day frequency using CRU counts and GPCC totals; rain/snow partitioning based on ERA-40-derived ratios; preservation of spatial coherence for significant events.
  - Aerosols and clouds: HadGEM2-A-derived AOD data used for shortwave corrections; ongoing uncertainties in indirect aerosol effects and pre-industrial conditions.
  - Temporal extension 1901–1957: re-ordered ERA-40 years to preserve diurnal-to-seasonal statistics similar to 1958–2001; sparse observations in early years managed with CRU climatology and GPCC constraints where possible.

- PET estimations and methods
  - PET_rc: Penman–Monteith-based reference evapotranspiration for a reference crop.
  - PET_PT: Priestley–Taylor PET as an alternative in some GHMs.
  - Differences between PET_rc and PET_PT are substantial in some regions, underscoring method choice sensitivity for hydrological applications.

- Validation and reliability
  - Validation against FLUXNET suggests strong agreement for temperature and radiation; precipitation validation remains challenging due to footprint and synoptic variability.
  - Data quality is robust for most variables at diurnal-to-synoptic scales; pre-1958 periods carry higher uncertainties due to randomized ERA-40 years and limited bias-correction for several drivers.

- Global and regional findings (highlights relevant to GIS use)
  - PET_rc trends: global PET_rc shows notable interannual variability with regional declines or increases linked to changes in vapor pressure deficit, radiation, wind, and temperature.
  - PET_PT vs PET_rc: local differences can exceed 1000 mm/yr in some basins, highlighting the need for consistent PET method selection in GIS analyses.
  - Regional patterns: patterns vary by basin (examples include Murray-Darling, Niger, Congo, Amazon, Lena, Ganges-Brahmaputra, Orange), with differences in PET trends, precipitation, net radiation, wind, and VPD across 1901–1957, 1958–2001, and 1979–2001 intervals.
  - Precipitation trends: no universal global precipitation trend; regional divergences exist with uncertainties higher in data-sparse regions and pre-1950 periods.

- Appendix and basin-level details
  - Appendix tables provide basin-by-basin statistics for key variables (PET_rc, PET_PT, Net Radiation, VPD, Wind, Rainfall, Snowfall, Precipitation) across multiple intervals (1901–1957, 1958–2001, 1979–2001) and for both PET methods.
  - Example basins included: Orange River, Lena, Murray-Darling, Ganges-Brahmaputra, and Lena, among others; includes average values, slope (trend) estimates, number of effective degrees of freedom (Neff), and significance levels (Adjusted Slope P).

- Practical implications for GIS workflows
  - Data format and accessibility: NetCDF at 0.5° is compatible with common GIS and remote sensing tools; includes explicit time stepping and land mask alignment.
  - Map-based analyses: enables spatial visualization of PET_rc, PET_PT, radiation, temperature, wind, VPD, and precipitation; differences between PET methods can be mapped to inform model choices.
  - Temporal considerations: when analyzing long-term trends (1901–2001), account for pre-1958 limitations and regional data density; ensure consistent PET method usage across analyses.
  - Data quality and limitations: exercise caution with precipitation-derived metrics in data-sparse regions and for event-based/extreme analyses; document baseline data sources and correction steps in GIS workflows.
  - Integration guidance: align with regional basemap masks, convert units/temporal steps as needed, and clearly document PET method (PET_rc vs PET_PT) used in downstream modeling and visualization.

- Key caveats for GIS users
  - Pre-1958 variability is limited by randomized ERA-40 years and partial bias corrections for several variables.
  - Gauge coverage and footprints introduce regional uncertainties, especially for precipitation.
  - Aerosol and cloud corrections carry residual uncertainties, particularly in historical periods with evolving atmospheric composition.

- Bottom-line takeaway for GIS-focused users
  - The WATCH Forcing Data 1958-2001 provides a bias-corrected, diurnally resolved meteorological forcing dataset at 0.5° suitable for driving land surface and hydrological models, with detailed basin-level context available in Appendix tables. Users should be mindful of pre-1958 limitations, regional data density, and the PET method chosen (PET_rc vs PET_PT) when conducting long-term, map-based analyses.