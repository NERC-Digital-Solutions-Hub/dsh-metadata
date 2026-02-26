# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- The WATCH Forcing Data (WFD) is a comprehensive meteorological forcing dataset designed to drive land-surface and hydrological models across the 20th century, with half-degree global coverage and sub-daily resolution.
- Periods covered:
  - Main forcing: 1958–2001 (with full diurnal cycles)
  - Extension: 1901–1957 (constructed to match later period statistics)
- Variables included: wind speed at 10 m, 2 m temperature, surface pressure, 2 m specific humidity, downward longwave and shortwave radiation, rainfall, and snowfall; data stored on a global land grid excluding Antarctica with a consistent land-sea mask and NetCDF format.
- Core data sources and corrections:
  - 1958–2001 basis from ERA-40 reanalysis, bias-corrected and adjusted.
  - Temperature and diurnal range bias corrections using CRU observations; atmosphere forcing adjusted to align with CRU TS2.1.
  - Downward longwave radiation bias-corrected via comparison with NASA SRB and FEM; no global LW bias after ERA-40 corrections.
  - Downward shortwave radiation corrected for cloud, aerosols, and volcanic effects using HadGEM2-A-derived AOD data.
  - Precipitation revised through a six-step process to preserve monthly totals, wet-day frequency, and spatial coherence, with gauge adjustments.
  - 1901–1957 extension re-ordered ERA-40 years and corrected with the same framework, noting data sparsity and potential biases.
- Data processing and governance:
  - Elevation corrections applied post-interpolation; variables mapped to hourly, 3-hourly, or 6-hourly grids with consistent timing.
  - Validation against FluxNet sites shows good alignment for many variables on monthly-to-daily scales; some limitations remain for sub-daily precipitation in convective regimes and data-sparse regions.
  - Transparent documentation, metadata, and governance to support reproducibility and comparability.
- POTENTIAL and methods for evaluation:
  - PET estimates are provided to compare forcing fields against hydrological models, not to drive a single model.
  - PET_rc (reference crop) uses Penman–Monteith with fixed surface and wind resistances; PET_PT (Priestley–Taylor) uses available energy balance terms and can be more reliable in humid regions.
  - Both PET metrics are converted to depth (mm) for model-forcing comparability.
- Global and regional findings (highlights):
  - Global PET_rc shows substantial interannual variability with no uniform global trend; regional patterns dominate model scatter in multi-model analyses.
  - PET_rc vs PET_PT differences can be large locally (up to ~1000 mm/yr in some areas), affecting interpretation of model output and intercomparisons.
  - Basin-scale context (examples across eight major basins) shows contrasting behavior between PET_rc, PET_PT, precipitation, and radiation variables, underscoring regional dependencies in hydrological responses.
- Data accessibility and governance:
  - WFD methodology and data are documented in WATCH Technical Report 22 and publicly accessible.
  - Emphasizes provenance, metadata, data sharing, and reproducibility across modeling efforts.
- Implications for monitoring frameworks:
  - Provides a standardized, well-documented meteorological forcing dataset enabling monitoring authors to:
    - Assess external drivers of hydrological and environmental health processes across the 20th century.
    - Ensure data provenance, quality control, and reproducibility.
    - Compare model outputs (LSMs and GHMs) on a consistent forcing basis, improving comparability and reducing data-wrangling duplication.
  - Highlights the need to address data gaps, access barriers, and metadata adequacy when building long-term monitoring datasets.

## Appendix: Basin-level statistics (selected basins)

- c) Orange River Basin
  - PET_rc (mm/yr): 1901–1957 avg 1429.10; slope -1.56 (p<0.05); 1958–2001 avg 1449.35; slope -3.68 (p<0.001); 1979–2001 avg 1415.69; slope -5.46 (p>0.200).
  - PET_PT (mm/yr): 1901–1957 avg 959.10; slope -1.05 (p<0.050); 1958–2001 avg 997.21; slope +2.54 (p<0.001); 1979–2001 avg 1028.81; slope +0.67 (p>0.200).
  - Net Rad (W/m2): 1901–1957 avg 85.33; slope -0.07 (p>0.100); 1958–2001 avg 88.69; slope +0.22 (p<0.001); 1979–2001 avg 76.45; slope +0.11 (p>0.200).
  - VPD (kPa): 1901–1957 avg 0.2643; slope +0.0002; 1958–2001 avg 0.2724; slope -0.0032; 1979–2001 avg 0.2717; slope -0.0035 (various p-values, some <0.020).
  - Wind (m/s): generally small changes; all periods show slopes near zero; significance mostly >0.200.
  - Rainfall (mm/yr): values indicate substantial inter-period variability; 1958–2001 avg around 501–502 with limited slope significance; 1979–2001 avg around 309–337 with variable trends.
  - Snowfall (mm/yr): typically very small; minor changes across periods.
  - Neff (sample size) varies by period (e.g., 57, 28, 15); some periods show limited statistical significance (Adjusted Slope P often >0.100).

- f) Lena River Basin
  - PET_rc: 1901–1957 avg 363.47; slope +0.13 (p>0.200); 1958–2001 avg 366.70; slope -0.45 (p>0.200); 1979–2001 avg 366.11; slope +0.54 (p>0.200).
  - PET_PT: 1901–1957 avg 312.82; slope +0.15 (p>0.200); 1958–2001 avg 313.48; slope +0.24 (p<0.050); 1979–2001 avg 314.73; slope +0.42 (p>0.200).
  - Net Rad (W/m2): 1901–1957 avg 29.05; slope +0.01; 1958–2001 avg 28.65; slope +0.06; 1979–2001 avg 28.65; slope -0.07 (various p-values, many not highly significant).
  - VPD (kPa): generally low and modestly variable; 1958–2001 avg 0.2443; slope -0.0032; 1979–2001 avg 0.2453; slope +0.0046 (mixed significance).
  - Wind (m/s): around 1.6–2.0 with small slopes; significance typically >0.100.
  - Rainfall (mm/yr): variable across periods; 1958–2001 avg ~1400–1426; 1979–2001 avg ~1426; slopes indicate increases in some periods, declines in others.
  - Snowfall (mm/yr): small values with modest changes in late period.
  - Precipitation totals (mm/yr): large basins show sustained rainfall totals with substantial inter-annual and inter-decadal variability.
  - Neff: variable by period (generally high in earlier periods, decreasing in later periods for some variables).

- h) Ganges-Brahmaputra River Basin
  - PET_rc: 1901–1957 avg 889.32; slope +0.037 (p>0.200); 1958–2001 avg 869.68; slope -2.256 (p<0.001); 1979–2001 avg 843.63; slope -1.84 (p<0.010).
  - PET_PT: 1901–1957 avg 798.70; slope +0.097 (p>0.200); 1958–2001 avg 767.99; slope -1.26 (p<0.001); 1979–2001 avg 752.00; slope -0.89 (p>0.200).
  - Net Rad (W/m2): 1901–1957 avg 69.75; slope -0.0008 (p>0.200); 1958–2001 avg 67.01; slope -0.123 (p<0.001); 1979–2001 avg 65.45; slope -0.104 (p<0.100).
  - VPD (kPa): 1901–1957 avg 0.9467; slope +0.0003; 1958–2001 avg 0.9570; slope -0.0032; 1979–2001 avg 0.9281; slope -0.0035 (various p-values, many <0.001).
  - Wind (m/s): around 1.7–2.0 with small slopes; significance often >0.200.
  - Rainfall (mm/yr): substantial variability; 1958–2001 avg 1400.84; 1979–2001 avg 1426.74 with large slopes in some series; earlier periods show different magnitudes and direction.
  - Snowfall (mm/yr): generally small; some basins show low but non-zero values in certain periods.
  - Precipitation (mm/yr): overall variability with periods of increases and decreases depending on era; Neff varies by variable and period.
  - Neff: variable across datasets and periods; some series have relatively large sample sizes, others smaller.

- Appendix Table 1 (ERA-40 basis years order)
  - Describes the alternating sequence used to construct the 1901–1957 basis years for WFD (ERA-40 and WFD alternations) and provides a year-by-year mapping for basis-year usage across 1901–1957.

- Overall interpretation for monitoring frameworks:
  - The Appendix documents substantial regional differences in long-term trends across PET, radiation, humidity, wind, and precipitation variables, highlighting the need for basin- or region-specific monitoring and tailoring of interpretive frameworks.
  - The data provide a rich, bias-corrected historical forcing backbone, but users should account for era-dependent data quality, sample sizes (Neff), and varying statistical significance across basins and periods.
  - The structured presentation of averages, slopes, and significance across multiple basins and periods supports standardized evaluation of environmental health drivers and model intercomparison within long-term monitoring efforts.