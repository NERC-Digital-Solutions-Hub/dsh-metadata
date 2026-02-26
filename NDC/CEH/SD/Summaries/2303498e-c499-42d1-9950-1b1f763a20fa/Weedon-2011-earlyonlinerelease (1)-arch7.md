# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

- The dataset provides bias-corrected meteorological forcing for land-surface and hydrological models on a half-degree global land grid.
- Key variables include: PET_rc, PET_PT, Net Radiation, VPD, Wind, Rainfall, Snowfall, Precipitation, and related diurnal/seasonal patterns.
- Two main temporal covers are used:
  - 1958-2001 as the primary, bias-corrected period for GIS analyses.
  - 1901-1957 produced by re-ordering ERA-40 years to preserve statistical characteristics for early-20th-century analyses (with limitations on interannual variability and trends).

- Baseline data processing and corrections (GIS relevance)
  - Elevation-corrected interpolation to a CRU land-sea mask; subsequent bias and consistency corrections applied in a defined sequence.
  - Temperature, pressure, and humidity bias-corrected against CRU observations; diurnal ranges anchored to CRU for ERA-40.
  - Shortwave radiation adjusted for tropospheric aerosols and cloud correlations; longwave not bias-corrected globally.
  - Precipitation processed through six steps to preserve ERA-40 rainfall/snow ratio, align with GPCC, adjust wet-day counts, and cap outliers; emphasis on maintaining coherence of large frontal-scale events across grid cells.
  - Validation highlights: good agreement for many variables at monthly scales; sub-daily precipitation validation is variable by site.
  - Early era (pre-1958) data are statistically constrained and not intended to reproduce exact historical events.

- Practical GIS guidance
  - Use WATCH Forcing Data 1958-2001 for map-based hydrological and ecohydrological analyses with diurnal cycles and regionally relevant trends.
  - Treat pre-1958 (1901-1957) data as statistics-focused rather than precise historical events; PET_rc vs PET_PT differences are relevant for model comparisons.
  - Be mindful of precipitation and wind uncertainties when mapping trends or planning resource management.
  - Data are designed for integration into GIS workflows to map forcing fields, PET estimates, and related hydrological indicators at basin scales.

- Basin-level statistics snapshot (examples from the provided data excerpt)
  - Orange River Basin
    - PET_rc (1901-1957): average ~1586 mm/yr; slope ~1.23 mm/yr per year.
    - PET_rc (1958-2001): average ~1604 mm/yr; slope ~0.65 mm/yr per year.
    - PET_PT (1901-1957): average ~1115 mm/yr; slope ~0.25 mm/yr per year.
    - Net Rad: ~96–97 W/m2 across periods.
    - VPD: ~1.45–1.53 kPa.
    - Wind: ~2.20–2.38 m/s.
    - Rainfall: ~305–346 mm/yr.
    - Snowfall: minimal (around 0–0.12 mm/yr range in later periods).
  - Lena River Basin
    - PET_rc: 363–409 mm/yr (1901-1957); ~366–408 mm/yr (1958-2001); PET_rc shows small positive to modest negative trends depending on period.
    - PET_PT: ~312–344 mm/yr across periods.
    - Net Rad: ~29–78 W/m2.
    - VPD: ~0.95–2.27 kPa.
    - Wind: ~1.12–2.00 m/s.
    - Rainfall: ~259–393 mm/yr.
    - Snowfall: ~0–142 mm/yr (1958-2001 and 1979-2001 ranges).
    - Precipitation: ~1426–1427 mm/yr (1958-2001 typical), with higher values in later sub-periods.
  - Murray-Darling River Basin
    - Data present but the excerpt contains incomplete entries for several metrics; overall pattern indicates basin-specific PET_rc and PET_PT behavior with variations in Net Rad, VPD, Wind, Rainfall, Snowfall and Precipitation across eras (1901-1957, 1958-2001, 1979-2001).
  - Ganges-Brahmaputra River Basin
    - PET_rc: ~889 mm/yr (1901-1957) decreasing to ~869 mm/yr (1958-2001) and ~844 mm/yr (1979-2001) with significant negative slopes in later periods.
    - PET_PT: ~799–798 mm/yr (1901-1957 to 1958-2001) with strong negative trends in the 1958-2001 and 1979-2001 windows.
    - Net Rad: ~69–79 W/m2; notable declines in some periods.
    - VPD: rising values in certain intervals (e.g., 1958-2001 around 0.95–2.27 kPa).
    - Rainfall: ~1400–1430 mm/yr across periods, with basin-wide variability and intervals showing increases or decreases.
    - Snowfall: modest to notable in some periods (up to ~142 mm/yr in 1958-2001).
  - Other basins (e.g., Lena, Orange, etc.) show consistent reporting of PET_rc and PET_PT with corresponding Net Rad, VPD, Wind, Rainfall, and Snowfall values; intervals commonly include 1901-1957, 1958-2001, and 1979-2001 with slopes indicating regional trends.

- Appendix notes
  - Appendix Table 1 documents the order of ERA-40 basis years used to construct the WATCH Forcing Data for 1901-1957.

- Access and usage
  - WATCH data are published as WATCH Technical Report 22 and are accessible via the EU-WATCH project (www.eu-watch.org).
  - The data are intended for integration into GIS workflows to produce maps of forcing variables, PET estimates, and other hydrological indicators alongside basin-scale analyses.