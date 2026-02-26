# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview of the provided data in this excerpt
- Presents basin-scale trend statistics for multiple hydroclimate variables across several basins (Orange River Basin; Lena River Basin; Murray-Darling River Basin; Ganges-Brahmaputra River Basin) using WATCH Forcing Data (WFD) constructs.
- Variables covered for each basin and period include:
  - PET_rc (Penman-Monteith reference crop evaporation for a well-watered grass surface)
  - PET_PT (Priestley-Taylor PET)
  - Net Radiation (Net Rad)
  - VPD (vapour pressure deficit)
  - Wind
  - Rainfall
  - Precipitation
  - Snowfall
- Time periods analyzed: 1901-1957, 1958-2001, and 1979-2001 (with corresponding basin-specific averages, slopes, and uncertainty indicators).
- For each variable and period, the data provide:
  - Average value
  - Slope (units/yr) and its range (slope-min, slope-max)
  - Neff (effective sample size)
  - Adjusted Slope P (significance level)
- Appendix Table 1 documents the order of ERA-40 basis years used in WFD for 1901-1957, illustrating the data provenance and methodological context.

## Key patterns by variable (basin-level and period highlights)
- PET_rc (mm/yr)
  - Orange: 1901-1957 shows a positive slope (0.2074); 1958-2001 remains positive but smaller (0.0561); 1979-2001 shows a strong positive average but with a negative slope estimate (-2.3898) and limited significance.
  - Lena: 1901-1957 modest positive slope (0.1315); 1958-2001 near flat to slight negative (-0.0454); 1979-2001 positive (0.5366).
  - Murray-Darling: available values indicate substantial PET_rc levels with generally positive slopes in early period and strongly negative slope in 1979-2001 for PET_rc.
  - Ganges-Brahmaputra: 1958-2001 and 1979-2001 show notable negative slopes, indicating reductions in PET_rc in later periods.
- PET_PT (mm/yr)
  - Across basins, PET_PT trends are generally positive over the long runs (1901-1957, 1958-2001, 1979-2001), with varying magnitudes and significance. Some basins show stronger increases in PET_PT than in PET_rc, reflecting radiation-based PET sensitivity.
- Net Radiation (W/m2)
  - Generally small changes over time; several basins show relatively steady Net Rad with modest trends (e.g., Lena, Ganges-Brahmaputra) suggesting modest shifts in radiative balance.
- VPD (kPa)
  - Values typically around 0.25–0.95 kPa depending on basin and period, with modest positive trends in some intervals and notable significance in others (e.g., pre-1958 vs. post-1958 periods in several basins).
- Wind (m/s)
  - Relatively stable across basins with small year-to-year fluctuations; slopes are mostly near zero, indicating weak long-term trends in this forcing.
- Rainfall and Precipitation (mm/yr)
  - Basin-dependent signals:
    - Some basins exhibit increases in Rainfall or Precipitation in later periods (e.g., certain periods for Ganges-Brahmaputra and Lena), while others show declines or mixed signals.
    - Precipitation trends often show broader regional heterogeneity, with some periods showing pronounced changes (positive or negative) and others remaining relatively flat.
- Snowfall (mm/yr)
  - Generally small magnitudes with mostly negative or near-zero trends in several basins; regional signals vary.
- Neff and significance
  - Neff values indicate varying effective sample sizes per basin/period, influencing the confidence in slope estimates.
  - Adjusted Slope P-values highlight which basin-period trends are statistically noteworthy; many slopes are not strongly significant across all basins and variables, underscoring regional specificity and data limitations.

## Implications for data strategy and governance (Data Leaders perspective)
- Baseline and regionalization
  - The dataset provides basin-specific baselines and trend contexts essential for regionally tailored hydrological and climate-impact analyses.
  - Emphasizes the need for region- and period-specific interpretation rather than assuming global coherence.
- Provenance, metadata, and uncertainty
  - Clear documentation of ERA-40 basis-years ordering (Appendix Table 1) is critical for traceability and reproducibility.
  - Inclusion of Neff and Adjusted Slope P-values supports transparent uncertainty quantification and risk assessment in model applications.
- Versioning and governance
  - The presence of multiple time slices and derived PET metrics (PET_rc vs PET_PT) reinforces the value of explicit versioning, metadata enrichment, and clear definitions of each variable.
  - Data leaders should ensure discoverability of basin-specific metadata, assumptions, and limitations to enable appropriate user interpretation.
- Cross-institution collaboration
  - Basin-specific trends across multiple variables illustrate the value of multi-team collaboration (e.g., hydrological models, climate scientists) to reconcile diverse signals and produce coherent forcing products.
- Practical use considerations
  - Users should account for scale and footprint differences when applying grid-scale forcing data to local or sub-grid processes.
  - Practitioners should weigh the relative importance of PET_rc vs PET_PT depending on model structure and regional conditions, as differences can be substantial in some basins.

## Takeaways for practitioners and decision-makers
- The WATCH Forcing Data provides detailed, basin-level, time-resolved forcing information with explicit trend analyses for key hydroclimate variables, enabling basin-specific hydrological and climate-impact studies.
- Trends are highly basin- and period-dependent; seasonality, spatial heterogeneity, and data limitations (as reflected in Neff and significance values) should guide interpretation and application.
- Effective data governance ( provenance, metadata, uncertainty quantification, and versioning) is essential to leverage these data for policy, water-resource planning, and risk assessment across networks of partners.