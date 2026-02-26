# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Executive summary for analysts

- The document presents basin- and period-specific trends in PET as estimated by the WATCH Forcing Data (WFD), focusing on PET_rc (Penman–Monteith reference crop) and PET_PT (Priestley–Taylor) across major basins and time slices.
- Time slices covered in the provided data include 1901–1957, 1958–2001, and 1979–2001, with additional note of the 1901–1957 ERA-40 basis-year ordering and bias corrections used for pre-1958 data.
- Key patterns observed in the included basins:
  - Orange River Basin
    - PET_rc: high, ~1400–1600 mm/yr; 1901–1957 average ~1429 mm/yr with a negative slope (~-1.56 mm/yr); 1958–2001 average ~1450 mm/yr with a steeper negative trend (~-3.68 mm/yr); 1979–2001 further negative (~-5.46 mm/yr).
    - PET_PT: generally lower but rising across periods (1901–1957 ~959 mm/yr with negative slope; 1958–2001 ~997 mm/yr with positive slope; 1979–2001 ~1131 mm/yr with positive slope).
    - Net radiation, VPD, wind show modest changes; rainfall trends shift from decline in mid-century to notable increases by 1979–2001.
  - Lena River Basin
    - PET_rc: ~363–367 mm/yr; small negative trend 1958–2001 (~-0.05 mm/yr); 1979–2001 modest uptick (~0.54 mm/yr).
    - PET_PT: ~313–315 mm/yr; mild positive trends across periods (~0.15–0.42 mm/yr).
    - Net radiation: ~29–33 W/m2 with small declines; VPD gradually rising (~0.24–0.27 kPa); rainfall around ~310–315 mm/yr with modest increases in 1958–2001 and 1979–2001.
  - Ganges–Brahmaputra River Basin
    - PET_rc: 1901–1957 ~889 mm/yr; 1958–2001 ~870 mm/yr; 1979–2001 ~844 mm/yr (overall decreasing trend with time).
    - PET_PT: 1901–1957 ~799 mm/yr; 1958–2001 ~768 mm/yr; 1979–2001 ~752 mm/yr (decreasing).
    - Net radiation: ~70–69 W/m2 with slight declines; VPD relatively stable around 0.95 kPa; rainfall broadly around 1400–1427 mm/yr with modest changes; snowfall minimal.
  - Murray–Darling River Basin
    - The provided excerpt contains incomplete or missing data for PET and related variables, indicating data gaps in this particular slice of the table.
- Across basins, PET_rc frequently declines from 1958–2001 relative to earlier periods, while PET_PT shows more mixed or rising trends in some basins, illustrating how PET formulation influences hydrological interpretation.
- Precipitation signals in the excerpt are basin-dependent: some regions show no global land-wide trend but notable sub-basin changes; rainfall tends to show substantial interannual variability and basin-specific trends rather than a uniform global pattern.
- Snowfall remains small in high-latitude basins and exhibits some basin- and period-specific changes, but generally does not dominate PET dynamics in these basins.

## Basin-specific highlights (selected basins)

- Orange River Basin
  - PET_rc: 1901–1957 average ~1429 mm/yr; slope ~-1.56 mm/yr; 1958–2001 average ~1449 mm/yr; slope ~-3.68 mm/yr; 1979–2001 slope ~-5.46 mm/yr.
  - PET_PT: 1901–1957 average ~959 mm/yr; slope ~-1.05 mm/yr; 1958–2001 average ~997 mm/yr; slope ~+2.54 mm/yr; 1979–2001 average ~1131 mm/yr; slope ~+0.73 mm/yr.
  - Net Radiation: gradual increase from ~85 W/m2 (1901–1957) to ~89 W/m2 (1958–2001); slopes small but positive in later period.
  - VPD: modest rise from ~0.26 kPa (1901–1957) to ~0.27 kPa (1958–2001); small changes in wind (~2.2 m/s) with near-flat trends.
  - Rainfall: 1958–2001 ~259.7 mm/yr (slight decline trend; slope ~-0.15 mm/yr); 1979–2001 ~309.4 mm/yr (strong rise; slope ~+3.9 mm/yr).
- Lena River Basin
  - PET_rc: ~363–367 mm/yr; 1958–2001 slight decrease (~-0.05 mm/yr); 1979–2001 small increase (~+0.54 mm/yr).
  - PET_PT: ~313–315 mm/yr; gradual increases across periods (~+0.15 to +0.42 mm/yr).
  - Net Radiation: ~29–33 W/m2; slight decline into 1958–2001; rainfall around ~310–315 mm/yr with modest upward trend in 1958–2001 and 1979–2001.
  - VPD: around 0.24–0.25 kPa with small increases by 1979–2001.
- Ganges–Brahmaputra Basin
  - PET_rc: 1901–1957 ~889 mm/yr; 1958–2001 ~870 mm/yr; 1979–2001 ~844 mm/yr (overall downward trend).
  - PET_PT: 1901–1957 ~799 mm/yr; 1958–2001 ~768 mm/yr; 1979–2001 ~752 mm/yr (downward).
  - Net Radiation: ~69–70 W/m2 with modest declines; rainfall ~1400–1427 mm/yr with minor changes; snowfall small.
  - VPD: ~0.95 kPa across periods with minor variability.
- Murray-Darling River Basin
  - Data in this excerpt are not populated for PET and many driving variables, indicating gaps in this basin within the provided table slice.

## Methodological notes and data interpretation

- Baseline and periods
  - 1901–1957 data are tied to ERA-40 basis years and include area-weighted averaging with adjustments; 1958–2001 data use bias-corrected ERA-40 inputs with corrections for aerosols, cloudiness, and wet-day adjustments.
  - Pre-1958 data rely on re-ordering ERA-40 years to preserve diurnal-to-monthly variability and interannual characteristics, with some variables only partially bias-corrected.
- PET definitions
  - PET_rc follows FAO Penman–Monteith with a grass reference canopy, while PET_PT uses Priestley–Taylor formulation; differences between PET_rc and PET_PT are a focal point for interpreting evaporation potential across basins and periods.
- Uncertainty and interpretation
  - Basin-level trends in PET_rc and PET_PT can diverge due to formulation differences, changes in wind, radiation, VPD, and precipitation; caution is advised when comparing results across basins or basing decisions on a single PET formulation.
  - For the Murray–Darling Basin, data gaps in this excerpt limit interpretability; other parts of the full dataset would be required for a complete assessment.

## Practical implications for analysts

- When using WATCH Forcing Data-derived PET estimates, consider the PET formulation (PET_rc vs PET_PT) as a primary driver of inter-basin differences and trend interpretation.
- Use period-specific trends (1901–1957, 1958–2001, 1979–2001) to distinguish structural climate changes from pre-bias-correction uncertainties, especially for pre-1958 signals.
- For high-latitude basins, snowfall and diurnal/seasonal shifts may modulate PET and precipitation interactions; account for snow-to-rain transitions in regional water-balance assessments.
- Be mindful of data gaps in certain basins within this excerpt (e.g., Murray-Darling) and consult full tables or supplementary materials for complete basin coverages and uncertainties.