# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

## Overview of the provided basin-level data
- The appendix presents basin-level time-series statistics for PET rc (reference evapotranspiration via Penman–Monteith) and PET PT (Priestley–Taylor), across multiple continental basins and time windows: 1901–1957, 1958–2001, and 1979–2001, with summary metrics:
  - Average values (mm/yr or W/m^2 for net radiation components)
  - Slope through the period (units/yr) and its range (slope-min to slope-max)
  - Neff (effective sample size) and Adjusted Slope P (p-value) flag
- Additional variables include Net Radiation (W/m^2), VPD (kPa), Wind (m/s), Rainfall (mm/yr), Snowfall (mm/yr), and Precipitation (mm/yr).
- Several basins show both PET rc and PET PT trends, with complex patterns across periods, reflecting regional drivers such as radiation, humidity, wind, and aerosols.
- Some entries for certain basins/periods are incomplete or marked with placeholders in the provided excerpt; overall, the dataset aims to enable cross-basin comparison of long-term evaporation drivers under diurnal-resolving forcing.

## Key basin highlights and notable patterns
- Orange River Basin
  - PET rc: 1901–1957 average 1586.19 mm/yr with a significant positive slope (1.2338); 1958–2001 average 1604.15 mm/yr with a smaller positive slope (0.6463); 1979–2001 average 1623.47 mm/yr with a strong negative slope (-2.3898).
  - PET PT: 1901–1957 average 1114.63 mm/yr with a small positive slope (0.2471); 1958–2001 average 1123.40 mm/yr with a positive slope (1.1023); 1979–2001 average 1131.46 mm/yr with a positive slope (0.7341).
  - Net Radiation and VPD show modest to small trends; rainfall shows an increase in 1958–2001 (slope ~0.85 mm/yr per year) and a steeper rise in 1979–2001 (slope ~3.88).
  - Overall, PET rc trends are not uniform across periods, with early period showing a strong positive trend and later periods showing variable or negative trends in some sub-windows, highlighting regional sensitivity to changing drivers and data corrections.
- Lena River Basin
  - PET rc: 1901–1957 average 363.47 mm/yr; 1958–2001 average 366.70 mm/yr (slight negative slope -0.0454); 1979–2001 average 366.11 mm/yr (positive slope 0.5366).
  - PET PT: 1901–1957 average 331.55 mm/yr; 1958–2001 average 340.08 mm/yr (positive slope 0.6888); 1979–2001 average 345.62 mm/yr (positive slope 0.3891).
  - Net Radiation, VPD, Wind, and Rainfall show generally small-to-moderate trends; rainfall exhibits a notable 1958–2001 increase (slope 0.2336) with continued growth into 1979–2001 (slope 0.1876).
  - Snowfall remains low; PET PT and PET rc trends are modest but indicate regional sensitivity to humidity and radiation changes.
- Murray–Darling River Basin
  - PET rc: 1901–1957 average 1429.10 mm/yr with a negative slope (-1.5615); 1958–2001 average 1449.35 mm/yr with a strong negative slope (-3.6782) and high significance (Adjusted Slope P < 0.001).
  - PET PT: 1901–1957 average 959.10 mm/yr with a negative slope (-1.0514); 1958–2001 average 997.21 mm/yr with a positive slope (2.5360); 1979–2001 average 1028.81 mm/yr with a positive slope (0.6654).
  - Rainfall shows notable variability; 1958–2001 rainfall average ~501.49 mm/yr with a positive slope, while 1979–2001 rainfall ~309.42 mm/yr with a positive slope (though less robust in some windows).
  - PET metrics indicate a shift from a decreasing trend in early-to-mid 20th century to a rising trend in later periods, suggesting substantial regional hydrological change drivers.
- Ganges–Brahmaputra River Basin
  - PET rc: 1901–1957 average 889.32 mm/yr with a small positive slope (0.0368); 1958–2001 average 869.68 mm/yr with a strong negative slope (-2.2561); 1979–2001 average 843.63 mm/yr with a strong negative slope (-1.8416).
  - PET PT: 1901–1957 average 798.70 mm/yr with a small positive slope (0.0968); 1958–2001 average 767.99 mm/yr with a negative slope (-1.2596); 1979–2001 average 752.00 mm/yr with a negative slope (-0.8951).
  - Net Radiation shows a downward trend in 1958–2001 (-0.1230) and continued negative tendency into 1979–2001 (-0.1041); VPD and Wind show modest shifts; Rainfall remains high and variable, with 1958–2001 average around 1426–1400 mm/yr and slopes indicating regional changes.
  - Snowfall remains comparatively small; overall, PET rc and PET PT trends suggest a shift toward drier radiative-humidity regimes in the latter half of the 20th century in this basin.
- Other basins in the excerpt (e.g., additional entries for pre-1957, 1958–2001, and 1979–2001 windows) illustrate a mix of increases and decreases in PET components, net radiation, and moisture-related variables, with many basins showing significant asymmetries between periods and several showing statistically significant slopes (Adjusted Slope P < 0.05 or < 0.001 in several windows).

## Data quality, interpretation, and caveats for Data Leaders
- Period-specific uncertainty:
  - Early period (1901–1957) often shows larger uncertainties and sometimes artificially damped decadal signals due to data sparsity, as reflected in several Adjusted Slope P values and Neff counts.
  - 1958–2001 and 1979–2001 periods generally exhibit stronger signals but can still vary by basin due to local data coverage and bias corrections.
- Methodological context:
  - PET rc and PET PT capture different evaporation-driving physics; PET rc relies on Penman–Monteith with fixed surface resistance assumptions, while PET PT emphasizes radiation and humidity. Differences between them can be large in humid vs arid regions, influencing interpretation and model intercomparison.
  - For multiple basins, the same data reconstruction framework (ERA-40 base, CRU/GPCC corrections, aerosol adjustments, etc.) is applied, but regional data density and gauge coverage affect reliability, especially for precipitation and rainfall components.
- Data provenance and reproducibility:
  - Appendix Table 1 documents the ERA-40 basis-year ordering used to assemble the WATCH Forcing Data for 1901–1957, emphasizing the importance of documented, reproducible basis-year sequencing for historical reconstructions.
  - Slopes, p-values, and Neff values provide transparency about statistical significance and sample robustness, aiding cross-basin comparability and uncertainty assessment.
- Implications for policy and planning:
  - Regional trends (where statistically significant) should be interpreted in the context of data quality, period-specific biases, and methodological choices. Early-period findings are most useful when complemented by sensitivity analyses and alternative data streams.

## Implications for data strategy and leadership
- Value of diurnal-resolving, bias-corrected forcing data:
  - The dataset demonstrates how harmonized, high-resolution forcing enables robust exploration of evaporation drivers and regional hydrological responses across the 20th century.
- Provenance, versioning, and documentation:
  - Maintain clear data lineage, including bias-correction steps, data sources (ERA-40, CRU, GPCC, HadGEM2-A aerosols), and the rationale for periodization; ensure traceability of basis-year orders (as in Appendix Table 1).
- Handling early-period uncertainties:
  - Communicate limitations of 1901–1957 data to stakeholders; use sensitivity analyses or complementary data streams to corroborate findings for policy guidance.
- Cross-basin collaboration and governance:
  - The comparable structure across basins supports multi-institution collaboration; reinforce governance around metadata, metadata completeness, and discoverability to support reproducibility and trust in model outputs.
- Actionable takeaways:
  - High-quality, diurnal, bias-corrected forcing data are essential for credible long-term hydrological and evaporation analyses; ensure ongoing data provenance, version control, and community engagement to strengthen decision-making in water resource management.