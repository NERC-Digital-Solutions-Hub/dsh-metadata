# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

## Overview
- The WATCH Forcing Data (WFD) comprises corrected meteorological forcing for the twentieth century to drive land surface models and hydrological models.
- The dataset spans 1901-1957 (1901-1957 series created by re-ordering ERA-40 data to preserve statistics) and 1958-2001 (ERA-40 based, bias-corrected and adjusted via auxiliary datasets).
- Key variables include wind, temperature, humidity, pressure, downward longwave and shortwave radiation, rainfall, snowfall, and precipitation.
- For governance and usability, WFD v1958-2001 is bias-corrected and validated; 1901-1957 is a constructed continuation with acknowledged limitations.

## What the dataset contains (data structure and corrections)
- Forcing data relied on:
  - ERA-40 reanalysis (1958-2001) with bias corrections via CRU climatologies and GPCC precipitation adjustments.
  - Aerosol and cloud corrections applied to shortwave radiation (HadGEM2-A based) to account for 20th-century aerosol loading.
  - Temperature and humidity corrected to maintain internal consistency; precipitation corrected through a multi-step process linked to GPCC and CRU data.
- Data formats and grid:
  - NetCDF format, ALMA convention, half-degree grid (~67,420 land points), sub-daily forcing for LSMs and daily for GHMs.
- Documentation and provenance:
  - Detailed processing steps, interpolation/elevation corrections, and validation against FluxNET observations.
  - Pre-1958 data have limitations in bias corrections for wind, pressure, humidity, and longwave radiation; post-1958 data are more robust.
- Appendix and basin-level detail:
  - Appendix-like entries provide basin-specific time-series statistics for several basins (e.g., Orange River, Lena, Ganges-Brahmaputra, Murray-Darling, etc.) across multiple periods.
  - For each basin and period, metrics include:
    - PET rc (Penman-Monteith reference crop) and PET PT (Priestley-Taylor) in mm/yr
    - Net radiation, VPD, Wind, Rainfall, Snowfall, Precipitation
    - Averages, slopes (with units/yr), slope min/max, Neff (effective sample size), and adjusted P-values for slope significance
    - Periods covered: 1901-1957, 1958-2001, and 1979-2001 (where provided)

## Regional basins: illustrative highlights from the appended data (examples)
- Orange River Basin
  - PET rc (mm/yr): 1901-1957 average ~1586; 1958-2001 average ~1604; 1979-2001 average ~1623
  - PET PT: 1901-1957 average ~1115; 1958-2001 ~1123
  - Net Rad: ~96 W/m2 across periods
  - Rainfall: ~346-337 mm/yr with generally positive but often non-significant slopes
- Lena River Basin
  - PET rc averages around 363-366 mm/yr (1901-1957 to 1958-2001)
  - PET PT: 1901-1957 ~959; 1958-2001 ~997
  - Precipitation: ~313-392 mm/yr across periods with notable positive slope in 1958-2001
  - Net Rad: ~29-68 W/m2 with strong 1958-2001 trend signals
- Ganges-Brahmaputra Basin
  - PET rc high (approx. 850-900 mm/yr range across periods)
  - PET PT around 798-867 mm/yr (1901-1957 to 1958-2001)
  - Precipitation and Snowfall show substantial regional variability and regime shifts across periods
- Murray-Darling Basin
  - Data present but detailed basin-specific slope and significance indicators vary; general patterns indicate regionally diverse trends in PET and precipitation
- General note across basins
  - PET rc and PET PT often show different trend signals, illustrating sensitivity to the PET formulation
  - Pre-1958 data carry larger uncertainties; post-1958 periods are more reliable for trend interpretation
  - Snowfall contributions are typically small relative to PET and precipitation in these basins

## Validation, uncertainties, and caveats
- Validation
  - FluxNET comparisons show good alignment for temperature and radiation; precipitation and wind alignment is weaker at sub-daily scales due to footprint differences.
- Uncertainties and limitations
  - Pre-1958 wind, pressure, humidity, and downward longwave biases are less well constrained; may affect decadal trend interpretation.
  - Sparse gauge coverage pre-1950 introduces regional biases in precipitation corrections.
  - Global and regional trends before 1958 may be less reliable; interannual variability may be underrepresented in 1901-1957 reconstructions due to randomized basis-year assignment.
  - Some basin-level signals (e.g., for the Amazon, Congo) are influenced by data limitations and ERA-40 issues rather than pure climate signals.
- Implications for use
  - Be cautious when interpreting long-term trends across the entire 20th century; emphasize periods with stronger data support (1958-2001) and acknowledge pre-1958 uncertainties.
  - Use PET rc and PET PT comparatively to understand methodological sensitivity in model intercomparisons.

## Data governance, accessibility, and documentation considerations for Data Stewards
- Provenance and versions
  - WFD v1958-2001 is bias-corrected and validated against observations; 1901-1957 is a constructed ERA-40-based extension with acknowledged limitations.
- Metadata and documentation
  - Ensure metadata capture of: interpolation/elevation correction methods, bias corrections (CRU, GPCC), aerosol/cloud corrections (HadGEM2-A), and precipitation adjustments; document known ERA-40 issues and pre-1958 uncertainties.
- Data formats and standards
  - NetCDF with ALMA convention; 0.5° grid; sub-daily forcing data suitable for LSMs and GHMs; include clear references to applicable model compatibilities.
- Data quality, lineage, and access
  - Catalog data with validation results (FluxNET comparisons) and caveats about pre-1958 data; record the exact processing chain and versions used for reproducibility.
  - Provide access points and licensing (e.g., WATCH project materials, with references to technical reports and the EU-WATCH resources).
- Reproducibility and updates
  - Maintain a versioned processing log; document any future updates to reanalysis inputs, bias corrections, or additional baselines; preserve the Appendix Table 1 relation to ERA-40 basis years for 1901-1957.
- Practical guidance for users
  - Distinguish clearly between PET rc and PET PT results when communicating model implications.
  - Flag basins with strong data limitations or significant pre-1958 uncertainty to avoid overinterpretation of trends.
  - Encourage basin-specific metadata enrichment to support correct interpretation of (and replication for) hydrological modeling.

## Practical takeaways for Data Stewards
- The WATCH Forcing Data provide a comprehensive, corrected meteorological forcing set for the twentieth century, suitable for basin-scale and regional hydrological modeling, with explicit documentation of corrections and validation.
- Governance should emphasize robust provenance, rich metadata, version control, and explicit communication of known limitations, especially for pre-1958 data and precipitation corrections.
- Be attentive to regional variability and methodological differences (PET rc vs PET PT) when guiding users on basins and hydrological interpretations.
- Ensure data catalogs clearly distinguish PET rc and PET PT results and provide guidance on how to compare them in model experiments and climate-change interpretations.