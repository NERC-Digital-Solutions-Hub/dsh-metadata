# Creation of the WATCHForcing Data and its use to assess global and regional = reference crop evaporation over land during the twentieth century.

- Purpose and scope
  - Provides the WATCH Forcing Data (WFD), a long-term (1901–2001) global meteorological forcing dataset to drive land surface and hydrological models.
  - Includes two key periods: 1958–2001 (ERA-40-based forcing with bias corrections) and 1901–1957 (data reordered to preserve statistical characteristics; biases and variability less robust).
  - Aims to enable analysis of evaporation drivers from diurnal to interannual scales.

- Data content, time coverage, and formats
  - Variables featured in the basin-focused tables include PET_rc (reference evapotranspiration from a well-watered reference crop) and PET_PT, Net Radiation, Vapor Pressure Deficit (VPD), Wind, Rainfall, Snowfall, and Precipitation (units vary by variable).
  - Basin-level entries are provided for multiple periods: 1901–1957, 1958–2001, and 1979–2001, with reported averages, slope (trend) estimates, minimum/maximum slope, Neff (effective sample size), and adjusted p-values for slope significance.
  - Some basins show significant long-term trends (positive or negative) in PET_rc, PET_PT, Net Rad, VPD, Rainfall, and Snowfall; others show weak or non-significant trends, reflecting regional variability.

- Regional basin highlights (examples from the appendix)
  - Orange River Basin
    - PET_rc and PET_PT generally increase from 1901–1957 to 1979–2001 (positive slopes), indicating rising reference evapotranspiration in later years.
    - Net Radiation tends to decrease modestly across later periods.
    - Rainfall and Snowfall show upward tendencies in later periods; VPD and Wind remain relatively stable.
  - Lena River Basin
    - PET_rc shows a small increase in 1901–1957, then a slight decrease in 1958–2001, with mixed signals in 1979–2001.
    - Net Radiation declines modestly after 1958–2001.
    - Rainfall and VPD exhibit basin-specific changes, with some periods showing increases.
  - Ganges–Brahmaputra River Basin
    - PET_rc and PET_PT trends are generally negative from 1958–2001 onward, indicating reductions in reference evapotranspiration in later periods.
    - Net Radiation declines across 1958–2001 and 1979–2001.
    - Precipitation shows increases in some periods, with Snowfall and VPD displaying variable patterns by sub-period.
  - (Note: The table includes other basins such as Murray–Darling, and additional detailed entries for PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation across periods; some fields in the excerpt are incomplete or placeholder.)

- Data quality, uncertainties, and caveats
  - ERA-40 biases affect early-period fields (notably surface pressure) and interannual variability, particularly before 1950.
  - The 1901–1957 period relies on randomized ERA-40 years to preserve statistical properties, which reduces the ability to infer exact historical events.
  - Bias correction is not global for all variables in the 1901–1957 period; some basins show adjusted Slope P-values indicating weaker confidence in long-term trends.
  - Sparse pre-1950 gauge coverage and regional data density contribute to uncertainties in trend estimates and regional comparisons.
  - Validation indicates good agreement for temperature, wind, and radiative fluxes at monthly to seasonal scales; precipitation validation is more challenging, especially in tropical and convective regimes.

- Governance, metadata, and re-use considerations
  - The dataset includes extensive metadata on bias corrections, aerosol adjustments, rainfall/snow partitioning, and validation outcomes to support transparent data governance.
  - Appendix Table 1 documents the order of ERA-40 basis years used for 1901–1957, clarifying the construction methodology.
  - Users should reference variable definitions, units, time-slice definitions, and the specific period (1901–1957, 1958–2001, 1979–2001) when interpreting basins and trends.
  - Data leaders should treat 1901–1957 results with appropriate caution due to early-era data sparsity and partial bias corrections, prioritizing 1958–2001 results for robust analyses.

- Implications for data strategy and usage
  - WFD enables long-term, diurnal-to-interannual analyses of evaporation drivers across global basins, supporting cross-basin comparisons and system-level data governance.
  - For decision-making and planning, rely on 1958–2001 (and, where appropriate, 1979–2001) results with documented uncertainties; use 1901–1957 findings with caveats tied to data limitations.
  - Ensure incorporation of baseline metadata (bias corrections, aerosol adjustments, rainfall-snow partitioning) and acknowledge region-specific data quality when communicating results.
  - Facilitate cross-network collaboration by referencing the documented data provenance and validation outcomes to strengthen data stewardship and reuse.