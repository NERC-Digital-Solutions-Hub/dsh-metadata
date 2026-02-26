# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

## Overview of Basin-Level Trend Tables (1901–1957, 1958–2001, 1979–2001)

- The document includes basin-scale trend statistics for multiple variables (PET rc, PET PT, Net Radiative flux, VPD, Wind, Rainfall, Snowfall, Precipitation) across several basins, with three overlapping periods: 1901–1957, 1958–2001, and 1979–2001.
- For each basin and period, the tables report:
  - Average values (units provided per variable)
  - Slopes (units/yr) indicating trend direction and magnitude
  - Minimum and maximum slope values
  - Neff (effective sample size)
  - Adjusted Slope P. (significance indicators; e.g., <0.050, <0.001, or >0.200)
- Significance and direction of trends vary by basin and period, reflecting regional differences in climate signals and potential data-field biases.
- The data illustrate how some basins show statistically significant trends in PET components and radiative measures in certain periods, while others show weak or non-significant trends in other periods.

## Basin Highlights

- Orange River Basin
  - PET rc (mm/yr): 1901–1957 avg 1586.19; slope 1.2338/yr; adjusted P < 0.010 (significant). 1958–2001 avg 1604.15; slope 0.6463/yr; adjusted P > 0.200 (not significant). 1979–2001 avg 1623.47; slope −2.3898/yr; adjusted P < 0.200 (not clearly significant).
  - PET PT (mm/yr): 1901–1957 avg 1114.63; slope 0.2471/yr (not significant). 1958–2001 avg 1123.40; slope 1.1023/yr (significant at P < 0.020). 1979–2001 avg 1131.46; slope 0.7341/yr (not significant).
  - Net Rad (W/m^2): near-constant with small slopes; 1958–2001 shows slight positive slope; 1979–2001 positive slope.
  - VPD (kPa): small positive slopes in 1901–1957 (significant at P < 0.050); minimal/slightly positive or non-significant in 1958–2001 and 1979–2001.
  - Wind (m/s): generally small slopes; largely non-significant across periods.
  - Rainfall and Snowfall: rainfall shows positive trends in some periods; snowfalls remain small with non-consistent significance.
- Murray-Darling River Basin
  - Data in this excerpt are largely garbled/incomplete; basin-wide trends cannot be reliably interpreted from the provided values.
- Lena River Basin
  - PET rc (mm/yr): 1901–1957 avg 363.47; slope 0.1315/yr (not significant). 1958–2001 avg 366.70; slope −0.0454/yr (not significant). 1979–2001 avg 366.11; slope 0.5366/yr (not significant).
  - PET PT (mm/yr): 1901–1957 avg 331.55; slope 0.1970/yr (not significant). 1958–2001 avg 340.08; slope 0.6888/yr (not significant). 1979–2001 avg 345.62; slope 0.3891/yr (not significant).
  - Net Rad (W/m^2): modest changes; 1958–2001 slope is ~0.0608/yr (significance not consistently indicated). 1979–2001 slope ~0.0052/yr (not significant).
  - VPD (kPa): generally small changes; 1958–2001 slope −0.0032/yr (not significant); 1979–2001 slope 0.0046/yr (not significant.
  - Wind (m/s), Rainfall, Snowfall: trends are modest with varying significance; rainfall shows positive slope in 1958–2001 and 1979–2001 but with limited significance notes.
- Ganges-Brahmaputra River Basin
  - PET rc (mm/yr): 1901–1957 avg 889.32; slope 0.0368/yr (not significant). 1958–2001 avg 869.68; slope −2.2561/yr (significant; P < 0.001). 1979–2001 avg 843.63; slope −1.8416/yr (significant; P < 0.010).
  - PET PT (mm/yr): 1901–1957 avg 798.70; slope 0.0968/yr (not significant). 1958–2001 avg 767.99; slope −1.2596/yr (significant; P < 0.001). 1979–2001 avg 752.00; slope −0.8951/yr (not significant).
  - Net Rad (W/m^2): 1958–2001 avg 67.01; slope −0.1230/yr (significant; P < 0.001). 1979–2001 avg 65.45; slope −0.1041/yr (not significant).
  - VPD (kPa): 1958–2001 avg 0.9570; slope −0.0032/yr (significant; P < 0.001). 1979–2001 avg 0.9281; slope −0.0035/yr (not significant).
  - Wind (m/s): small, generally non-significant slopes across periods.
  - Rainfall and Snowfall: rainfall shows positive trends in 1958–2001 and 1979–2001 with varying significance; snowfall varies with period.
- Appendix Table 1
  - Describes the order of ERA-40 basis years used in WATCH Forcing Data 1901–1957, detailing which years serve as basis year vs. year, and the alternating pattern of ERA-40 and WFD basis years.

## Appendix Table 1: ERA-40 Basis Year Ordering

- Provides the sequence of ERA-40 and WATCH Forcing Data (WFD) basis years used to construct 1901–1957 forcing.
- Details which years act as basis years and which years are actual data years for each calendar year, illustrating the methodological framework behind the 1901–1957 construction.

## Data Provenance and Quality Notes

- The trend statistics are part of the appendix supporting the long-term interpretation of the WATCH Forcing Data 1958–2001, including 1901–1957 extensions.
- Significance indicators (Adjusted Slope P.) help users gauge which basin-period combinations show robust trends versus those that may reflect noise, sampling, or data generation artifacts.
- Neff provides the effective sample size for trend estimation, informing uncertainty in slope estimates.
- The period 1901–1957 involves basis-year randomization in some datasets, which can affect interannual variability and long-term trend interpretation.
- The data underscore regional differences in climate signals (e.g., PET components, net radiation, VPD) and caution against applying basin-wide trends uniformly in hydrological modeling without period-specific context.

## Implications for Data Stewards

- Provenance and transparency:
  - The appendix documents basin-level trends across multiple variables and periods, reinforcing the need to store per-basin metadata on temporal coverage, methods, and significance.
- Metadata completeness:
  - Include period-specific trend information (annual means, slopes, Neff, and significance) in data catalogs to support model calibration and uncertainty assessment for basin-scale studies.
- Data quality and interpretation:
  - Recognize that significance varies by basin and period; ensure users interpret long-term trends with awareness of methodological caveats (e.g., ERA-40 basis-year construction, 1901–1957 randomization).
- Reproducibility:
  - The ERA-40 basis-year ordering in Appendix Table 1 is essential for reproducing the 1901–1957 extension; ensure this ordering is captured in reproducibility workflows and metadata.
- Guidance for reuse:
  - When applying WATCH forcing data to basin-scale hydrological models, consider period-specific trend signals (where significant) and treat pre-1958 baselines with caution due to potential data quality and randomization effects.
- Governance recommendations:
  - Maintain explicit caveats and documentation about regional biases, data generation choices, and the varying significance of trends across basins to support downstream users in making informed, auditable analyses.