# Creation of the WATCHForcing Data and its use to assess global and regional = reference crop evaporation over land during the twentieth century..

- Purpose of the dataset
  - Long-term meteorological forcings from ERA-40 basis years used to drive land surface and hydrological models.
  - Provides basis for assessing external drivers of evaporation, water balance, and enabling basin-scale policy monitoring and model intercomparison.

- Basins and key PET metrics (selected from the provided excerpt)
  - Orange River Basin
    - PET_rc (mm/yr): 1901–1957 average roughly 1586; 1958–2001 average roughly 1604; 1979–2001 average about 1623.
    - PET_rc trend: positive slope in 1901–1957 and 1958–2001; negative trend in 1979–2001.
    - PET_PT (mm/yr): 1901–1957 average about 1115; 1958–2001 average about 1123; 1979–2001 average about 1131.
    - PET_PT trend: generally positive across periods, with notable increases in 1958–2001 and 1979–2001.
    - Supporting variables (selected): Net Radiation ≈ 96–97 W/m2; VPD ≈ 1.27–1.53 kPa; Rainfall ≈ 305–347 mm/yr (with period-specific changes); Snowfall generally small.
  - Lena River Basin
    - PET_rc: 1901–1957 average ≈ 363.5; 1958–2001 average ≈ 366.7; 1979–2001 average ≈ 366.1.
    - PET_rc trend: small positive 1901–1957, slight decline 1958–2001, modest rise 1979–2001.
    - PET_PT: 1901–1957 average ≈ 312.8; 1958–2001 average ≈ 313.5; 1979–2001 average ≈ 314.7.
    - PET_PT trend: generally positive across periods.
    - Supporting variables: Net Radiation ≈ 29–34 W/m2; VPD ≈ 0.24–0.28 kPa; Rainfall ≈ 260–320 mm/yr; Snowfall ≈ 132–135 mm/yr (1958–2001); Precipitation ≈ 1426 mm/yr (scale varies by metric).
  - Ganges–Brahmaputra River Basin
    - PET_rc: 1901–1957 average ≈ 889; 1958–2001 average ≈ 870; 1979–2001 average ≈ 844.
    - PET_rc trend: modest decline from 1901–1957 to later periods.
    - PET_PT: 1901–1957 average ≈ 799; 1958–2001 average ≈ 768; 1979–2001 average ≈ 752.
    - PET_PT trend: declines across later periods.
    - Supporting variables: Precipitation ≈ 392 mm/yr (1958–2001) decreasing to ~386–387 mm/yr (1979–2001); Rainfall varies (1958–2001 ≈ 1401–1427 mm/yr depending on metric); Net Radiation ≈ 65–69 W/m2 (late periods lower than early); VPD ≈ 0.95–1.0 kPa; Wind ≈ 1.0–2.0 m/s; Snowfall generally small.
  - Murray-Darling River Basin
    - The excerpt includes limited complete basin-wide values; many fields are not fully populated in this extract.
    - Overall indication: PET metrics and ancillary variables are provided in similar formats, but complete trend interpretation requires the full table.

- Time periods and data construction notes
  - Time spans covered: 1901–1957 (extension), 1958–2001 (core), with subset 1979–2001 visible for several basins.
  - 1901–1957 values often derived by rearranging ERA-40 years to preserve diurnal and monthly variability and coherence, with bias corrections where possible.
  - For subperiods, slopes indicate year-to-year change (units: mm/yr for PET metrics; other variables in their respective units).
  - Neff indicates effective sample size; Adjusted Slope P shows statistical significance of trends (smaller p-values indicate significant Trends).

- Data corrections and interpretation guidance
  - PET_rc vs PET_PT provide alternative perspectives on evapotranspiration demand; PET_rc (Penman–Monteith) uses fixed resistances for a reference crop, while PET_PT uses Priestley–Taylor with available energy emphasis.
  - In several basins, differences between PET_rc and PET_PT can be large locally, affecting policy-relevant conclusions; use both to bound uncertainty.
  - Pre-1958 data carry higher uncertainty due to limited observations and the randomization of ERA-40 basis years; interpret early-period trends with caution.
  - Metadata, provenance, and corrections (bias corrections, aerosol/radiation adjustments, and precipitation processing) are essential for monitoring outputs; ongoing data governance and versioning are recommended.

- Practical implications for monitoring frameworks
  - The WATCH Forcing Data enables cross-basin monitoring of PET drivers and basin-scale water balance through long-term forcings.
  - It supports baseline trend analyses and multi-model intercomparisons for policy and resource-management decisions.
  - Governance needs highlighted: transparent metadata, data provenance, openly shared underlying data, clear documentation of corrections, and versioned releases as data improve.

- Appendix context
  - Appendix Table 1 shows the order of ERA-40 basis years used to construct WATCH Forcing Data 1901–1957, illustrating the randomized approach to span construction and baseload year assignment.

- Overall takeaway for monitoring framework authors
  - WATCH Forcing Data provides a rigorous, well-documented long-term meteorological forcing framework with basin-scale PET evaluations (PET_rc and PET_PT) and supporting hydrometeorological variables.
  - Strengths include diurnal/sub-daily variability preservation, detailed bias-correction workflows, and independent validation references.
  - Limitations to consider in monitoring design include early-period data uncertainties, regional data density gaps, and sensitivity of outputs to the choice between PET_rc and PET_PT.
  - Recommendations: use dual PET metrics to bound projections, maintain robust metadata and governance, update analyses with reanalysis improvements, and validate against independent observations to inform policy-oriented environmental health measures.