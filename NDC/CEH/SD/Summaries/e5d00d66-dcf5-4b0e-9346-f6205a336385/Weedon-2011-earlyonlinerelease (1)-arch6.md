# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview of the data in this chunk
- Presents basin-scale time series (1901–1957, 1958–2001, and 1979–2001) for:
  - PET_rc (mm/yr) and PET_PT (mm/yr)
  - Net radiation (W/m2)
  - Vapor pressure deficit (VPD, kPa)
  - Wind (m/s)
  - Rainfall (mm/yr) and Snowfall (mm/yr)
  - Precipitation (mm/yr)
- Basins included (examples with representative trends):
  - Orange River Basin
    - PET_rc: ~1586.19 (1901–1957) increasing to ~1604.15 (1958–2001); notable positive slope 1901–1957 (1.23) and later decline 1979–2001 (-2.39)
    - PET_PT: ~1114.63 (1901–1957) rising to ~1123.40 (1958–2001); similar incremental growth
    - Net Rad: ~96–97 W/m2 with small changes
    - Rainfall: ~346.5 (1958–2001) increasing; ~337.8 (1979–2001) with higher short-term slope
    - Snowfall: generally negligible in later periods
  - Lena River Basin
    - PET_rc: ~363–367 mm/yr across periods; slight rise 1979–2001 (0.54) after a small dip 1958–2001
    - PET_PT: ~312–315 mm/yr; modest increases in later periods
    - Net Rad, VPD, Wind: moderate, with small changes; snowfall present but small
    - Rainfall: substantial totals (~1400–1427 mm/yr) with variable slopes
  - Ganges-Brahmaputra River Basin
    - PET_rc: ~889 mm/yr (1901–1957) to ~869 mm/yr (1958–2001) and ~843 mm/yr (1979–2001) showing declines over time
    - PET_PT: ~799 mm/yr (1901–1957) to ~752 mm/yr (1979–2001) also declining
    - Net Rad: declines from ~69.75 (1901–1957) to ~65.45 (1979–2001)
    - VPD: generally around 0.95–1.0 kPa with small late-time declines
    - Rainfall: totals around ~1400–1427 mm/yr with late-time variations
    - Snowfall: notable declines in later periods
- Appendix notes:
  - Order of ERA-40 basis years used for 1901–1957 (randomized assignment with ramp adjustments to maintain statistics)

## Cross-basin patterns and key insights
- PET_rc vs PET_PT
  - In several basins, PET_rc trends differ from PET_PT trends, highlighting regional differences between radiation- and energy-driven evapotranspiration estimates.
  - Example: Orange and Lena basins show persistent PET_rc values with varying slopes; PET_PT trends can diverge in magnitude or direction, contributing to inter-method variability.
- Temporal changes by period
  - 1901–1957: PET_rc often high (baseline conditions) with mixed slopes; PET_PT generally similar but not identical.
  - 1958–2001: PET_rc and PET_PT frequently show reduced radiative/energy constraints in some basins, but trends vary regionally (e.g., Ganges-Brahmaputra shows notable declines in PET_rc and PET_PT).
  - 1979–2001: PET_rc and PET_PT slopes remain basin-dependent, with some basins showing continuing declines, others showing modest increases or stable behavior.
- Other driving variables
  - Net radiation: modest global declines in some basins (e.g., Ganges-Brahmaputra); variations exist across basins and periods.
  - VPD and Wind: generally stable to modestly increasing VPD in early periods, with some late-period declines; wind shows small, basin-specific trends.
  - Rainfall and Snowfall: rainfall totals show substantial regional variability; some basins experience increases, others declines; snowfall generally declines in many basins as periods advance.
- Data use implications
  - The dataset provides multi-decadal, diurnally resolved forcing fields and evapotranspiration benchmarks across major basins, enabling inter-basin comparisons and model intercomparisons.
  - Differences between PET_rc and PET_PT underscore the importance of selecting appropriate reference evapotranspiration formulations for regional hydrological modeling.

## Data quality, caveats, and interpretation
- Basis and bias corrections
  - Data rely on ERA-40 for core periods with bias corrections; early periods (1901–1957) involve randomized basis years and ramp adjustments, which may dampen interannual–decadal variability in PET_rc and drivers.
- Significance and interpretation
  - Many slope results have varying significance (Adjusted Slope P values shown); some long-running trends are statistically robust in certain periods but not in others.
- Representation limits
  - Sub-daily precipitation representation remains a challenge; coarse grid (half-degree) and aggregation limits precise event timing but preserves broader synoptic and seasonal patterns.
- Applicability
  - Designed for forcing land surface and hydrological models across the twentieth century; outputs are most reliable for long-term tendencies and basin-scale analyses rather than point-scale interpretations.

## Practical takeaways for data use
- Use PET_rc and PET_PT in tandem to explore how radiation versus energy balance drives evapotranspiration across basins and periods.
- Examine trends in Net Rad, VPD, Wind, Rainfall, and Snowfall collectively to understand drivers behind PET changes rather than relying on a single variable.
- Be mindful of period-specific significance and the caveats around pre-1958 data when interpreting long-term variability.
- Leverage the ERA-40 basis-year sequencing note and the Appendix for methodological context and reproducibility of basin-level analyses.