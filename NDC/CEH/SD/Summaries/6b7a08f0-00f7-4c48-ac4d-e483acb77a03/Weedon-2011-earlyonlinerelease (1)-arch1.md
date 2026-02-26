# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview
- The WATCH Forcing Data (WFD) provides meteorological forcing to drive land surface and hydrological models for studying the 20th century water cycle.
- It derives global and regional reference crop evaporation (PET rc) and compares PET rc with Priestley–Taylor PET (PET PT).
- Data are at half-degree spatial resolution with sub-daily time steps for forcing variables and daily steps for some components, spanning 1901–1957 (pre-58 extension) and 1958–2001 (primary period), plus bias-corrected ERA-40-based extensions.

## WATCH Forcing Data (WFD) contents and time periods
- Variables included: wind speed at 10 m, temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall, snowfall.
- Coverage and format: global land grid (half-degree), 3-hourly radiation/precipitation components, 6-hourly other fields; netCDF, CRU-based land-sea mask.
- Periods and processing:
  - 1958–2001: ERA-40 reanalysis data bias-corrected/adjusted to CRU/GPCC observations where feasible.
  - 1901–1957: constructed by reordering ERA-40 years to preserve diurnal/seasonal characteristics and interannual covariances; limited bias correction where observations sparse.
  - Altitude/elevation corrections, aerosol/cloud adjustments, humidity/temperature corrections, and rainfall/snowfall reallocation using ERA-40-derived rain–snow ratios.
- Validation and limitations:
  - Validation against FLUXNET sites shows good agreement for temperature and radiation; precipitation correlations weaker, especially diurnal and tropical sites.
  - Pre-1958 data include artifacts from sparse observations; regional data gaps and potential decadal variability dampening in PET rc estimates in some areas.

## PET rc and PET PT estimation
- PET rc: Penman–Monteith formulation with fixed surface and aerodynamic resistances for a reference crop; units in mm/yr.
  - ra, rs constants used to compute PET rc from driving variables (temperature, humidity, wind, radiation).
- PET PT: Priestley–Taylor formulation, using available energy and albedo assumptions.
- Consistent conversion to mm/yr allows direct comparison of PET rc and PET PT and assessment of regional differences.

## Processing and validation
- Data corrections:
  - Elevation corrections, bias corrections against CRU/GPCC observations, aerosol/cloud adjustments for shortwave, humidity/temperature corrections for longwave.
  - Wet-day statistics adjusted to observed patterns; precipitation reallocated between rainfall and snowfall using ERA-40-derived ratios.
- Global/global-regional patterns and uncertainties:
  - Global PET rc trends (1958–2001) are not statistically significant overall, but strong regional variability exists.
  - VPD generally rises, net radiation declines, and wind speeds decline globally in this period.
  - Validation indicates reliable temperature and radiation fields for hydrological use; diurnal/convective precipitation remains challenging, especially in tropical regions.

## Global patterns and regional variability (1958–2001; and 1901–1957 context)
- PET rc and PET PT exhibit notable regional differences; several basins show divergent trends between PET rc and PET PT, explaining spread in hydrological model outputs.
- In many regions, PET rc trends do not mirror PET PT trends, reflecting differences in how the two formulations respond to drivers like VPD, radiation, and wind.
- Precipitation and snowfall trends show substantial regional variability; changes in PET are driven by evolving radiation, humidity, and wind fields rather than uniform global trends.

## Basin-level highlights (selected basins from the dataset)

- Orange River Basin
  - PET rc:
    - 1901–1957: Average 1586.19 mm/yr; Slope 1.2338 (significant with p<0.01).
    - 1958–2001: Average 1604.15 mm/yr; Slope 0.6463 (not consistently significant across sub-intervals).
    - 1979–2001: Average 1623.47 mm/yr; Slope −2.3898 (not significant at the 0.2 level).
  - PET PT:
    - 1901–1957: Average 1114.63 mm/yr; Slope 0.2471 (not highly significant).
    - 1958–2001: Average 1123.40 mm/yr; Slope 1.1023 (significant; p<0.02).
    - 1979–2001: Average 1131.46 mm/yr; Slope 0.7341 (not highly significant).
  - Other drivers (Net Rad, VPD, Wind, Rainfall, Snowfall) show basin-specific patterns with varying significance; rainfall increases (1958–2001) but with large variability.

- Lena River Basin
  - PET rc:
    - 1901–1957: Average 363.47 mm/yr; Slope 0.1315 (not highly significant).
    - 1958–2001: Average 366.70 mm/yr; Slope −0.0454 (negligible to weak).
    - 1979–2001: Average 366.11 mm/yr; Slope 0.5366 (moderate).
  - PET PT:
    - 1901–1957: Average 312.82 mm/yr; Slope 0.1505 (not strong).
    - 1958–2001: Average 313.48 mm/yr; Slope 0.2437 (moderate).
    - 1979–2001: Average 314.73 mm/yr; Slope 0.4203 (notable).
  - Net Rad, VPD, Wind, Rainfall, Snowfall show nuanced changes; some periods exhibit small to moderate trends while others are stable.

- Ganges–Brahmaputra River Basin
  - PET rc:
    - 1901–1957: Average 889.32 mm/yr; Slope 0.0368 (not strong).
    - 1958–2001: Average 869.68 mm/yr; Slope −2.2561 (significant decline; p<0.001).
    - 1979–2001: Average 843.63 mm/yr; Slope −1.8416 (significant decline; p<0.01).
  - PET PT:
    - 1901–1957: Average 798.70 mm/yr; Slope 0.0968 (not strong).
    - 1958–2001: Average 767.99 mm/yr; Slope −1.2596 (significant).
    - 1979–2001: Average 752.00 mm/yr; Slope −0.8951 (moderate).
  - Net Rad: declines in 1958–2001 and 1979–2001; Precipitation generally stable with some increases/decreases; Snowfall modest.
  - VPD, Wind, Rainfall vary by sub-period; rainfall shows modest positive to negative slopes depending on interval.

- Note on completeness
  - Some basins have incomplete entries in certain intervals, reflecting data availability; pre-1958 results are particularly sensitive to ERA-40-based construction and limited bias corrections.

## Implications for hydrological modeling
- Differences between PET rc (Penman–Monteith with fixed resistances) and PET PT (Priestley–Taylor) across basins help explain variability across multi-model outputs (e.g., WaterMIP) when using different PET formulations.
- The WFD provides a consistent, bias-corrected forcing dataset suitable for century-scale hydrological analyses, but users should account for regional data gaps and pre-1958 artifacts when interpreting trends, particularly at local scales.

## Caveats and validation
- Global PET rc trends 1958–2001 show no universal global trend; regional basins can exhibit significant changes.
- Validation supports reliability for temperature and radiation fields; precipitation diurnal/convective accuracy remains a limitation, especially in tropical basins.
- Pre-1958 data carry potential spurious trends due to limited observations and reconstruction choices.

## Availability and context
- The WATCH Forcing Data is a foundational component of the EU WATCH project and related hydrological/climate-change analyses.
- Methodologies, validations, and uncertainties are documented to guide modelers in applying WFD to long-term hydrological assessments.