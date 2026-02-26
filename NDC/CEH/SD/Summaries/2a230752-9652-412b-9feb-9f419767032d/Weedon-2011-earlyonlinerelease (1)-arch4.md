# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

- Purpose and scope
  - Provides consistent, long-span meteorological forcing data for land surface models (LSMs) and general hydrological models (GHMs), enabling century-scale analysis of external drivers on evaporation and hydrologically important variables.
  - Global dataset at half-degree resolution with diurnal-to-sub-daily fidelity, designed to support cross-model comparability and multi-institution collaboration.
  - 1901–1957 data generated to bridge ERA-40 availability before 1958; 1958–2001 data derived from ERA-40 reanalysis with targeted bias corrections; includes aerosol and cloud corrections and careful precipitations adjustments.

- Data structure and coverage
  - Global half-degree (0.5°) grid; 3-hourly time steps (and some variables 6-hourly) with netCDF ALMA convention; 67,420 land grid points (Antarctica excluded).
  - Variables include: wind speed at 10 m, air temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall and snowfall rates; additional variables used for corrections and diagnostics.
  - Time spans:
    - 1901–1957: generated to complement ERA-40 gaps, preserving diurnal/seasonal statistics and interannual statistics via randomized ERA-40 year assignment.
    - 1958–2001: bias-corrected ERA-40-based forcing with aerosol and cloud corrections; precipitation adjustments to align with GPCC/CRU diagnostics.
  - Data products are documented with explicit metadata, lineage, and caveats to support reproducibility.

- Data creation, corrections, and governance
  - Temperature, pressure, and humidity corrected for elevation to maintain internal consistency and avoid supersaturation; downward longwave radiation bias-corrected to ERA-40 baseline; shortwave radiation adjusted monthly using CRU cloud cover and aerosol data from HadGEM2-A.
  - Aerosol and cloud corrections implemented for clear- and cloudy-sky components; volcanic aerosols treated separately; cloud data modulates shortwave fluxes.
  - Precipitation processing:
    - Wet-day correction to align rainfall counts with CRU; totals adjusted to GPCCv4; rain/snow partitioning retained from ERA-40.
    - Ensures spatial coherence of precipitation events across neighboring grid boxes to preserve hydrological relevance; outliers capped where months are unrealistically dry.
  - Validation and limitations:
    - Validation against FluxNET sites shows strong agreement for temperature and radiation; precipitation correlations are weaker due to convective rainfall representation and station coverage differences.
    - Spatial coherence for large-scale precipitation events is maintained, supporting large-scale hydrological modeling; sub-daily precipitation and convective rainfall representations can diverge from observations in some basins.
  - Data lineage and governance:
    - Clear lineage from ERA-40 to corrected forcing (with multiple bias-correction steps); metadata, format (NetCDF ALMA), and discovery metadata emphasized.
    - Documentation highlights limitations (pre-1958 variability, sparse early observations, precipitation representation) to guide uncertainty budgeting.

- Regional basins: key patterns (PET rc, PET PT, Net Rad, VPD, Wind, Rainfall, Snowfall, Precipitation)
  - Orange River Basin
    - PET metrics: PET rc and PET PT computed; trends vary by interval (1901–1957, 1958–2001, 1979–2001) with some periods showing increases and others declines.
    - Other drivers: Net radiation and wind are relatively stable; VPD shows slight fluctuations; precipitation and rainfall exhibit basin-scale variability across intervals.
    - Snowfall generally very small; precipitation totals show intermittent increases/decreases by period.
  - Murray-Darling River Basin
    - PET rc and PET PT exhibit interval-dependent trends; overall patterns indicate sensitivity to regional radiation and wind changes.
    - Precipitation and rainfall show notable variability across periods; Net Rad and VPD show evolving patterns consistent with arid-to-semiarid conditions.
  - Lena River Basin
    - PET rc and PET PT show modest changes across intervals, with some periods exhibiting notable shifts in PET PT.
    - Net Rad and VPD display pre- and post-1958 variability; Wind remains relatively stable; Rainfall shows pronounced interannual-to-decadal variability.
  - Ganges-Brahmaputra River Basin
    - PET rc and PET PT indicate regionally varying trends across intervals; precipitation and rainfall demonstrate substantial fluctuations across periods.
    - Net Rad and VPD trends show regional differences; wind remains near historical averages with small shifts; snowfall is minimal in most subregions.
  - Across basins, PET rc vs PET PT comparisons reveal that forcing assumptions can drive local divergences in evapotranspiration estimates, underscoring the impact of data choices on hydrological interpretations.

- PET rc vs PET PT: implications for modeling
  - PET rc (Penman-based reference evapotranspiration for a grass reference surface) and PET PT (Priestley–Taylor PET) can diverge locally due to forcing assumptions and available drivers.
  - The comparison highlights the sensitivity of evaporation metrics to the selected PET formulation when using long-span forcing data, reinforcing the need to align PET choices with modeling objectives and data provenance.

- Validation, reliability, and usage considerations for Data Leaders
  - Strengths:
    - Robust, well-documented data lineage from ERA-40 with comprehensive bias corrections and aerosol/cloud treatments.
    - High diurnal fidelity and cross-variable coherence intended to support interoperable hydrological modeling across institutions.
  - Caveats:
    - Pre-1958 variability and exact event timing should not be interpreted as precise historical sequences; randomization preserves statistics but not exact chronology.
    - Precipitation representation remains challenging in high latitudes and some tropical regions; sub-daily convective events may be misrepresented.
  - Practical considerations for adoption:
    - Emphasize data lineage, uncertainty attribution (especially for precipitation and sub-daily variability), and the impact of forcing choices on downstream model outputs.
    - Leverage the documented PET rc vs PET PT comparison to frame scenario analyses and sensitivity studies.
    - Use the Appendix documenting ERA-40 basis-year ordering to reproduce the generation workflow and maintain reproducibility across partners.

- Appendix and data governance notes
  - Appendix Table: order of ERA-40 basis years used in the WATCH Forcing Data 1901-1957, detailing how ERA-40 and WFD cycles alternate across years to construct the forcing time series.
  - Emphasis on reproducibility, transparency of methodology, and the ability to integrate with partner data ecosystems through clear metadata and data provenance.

- Takeaways for Data Leaders
  - The WATCH Forcing Data provides a comprehensive, reusable century-scale meteorological forcing framework with a rigorous data governance approach, enabling cross-institution modeling and analysis of external hydrological drivers.
  - Its multi-tier bias-correction, aerosol/cloud corrections, and careful precipitation handling illustrate mature data stewardship; however, users must account for pre-1958 limitations and precipitation uncertainties when budgeting risk or interpreting regional trends.
  - PET rc vs PET PT differences underscore how forcing assumptions shape derived hydrological metrics, a critical consideration for data strategy involving model outputs and scenario analyses.