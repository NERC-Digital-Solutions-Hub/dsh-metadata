# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

- Provides 0.5° global land-only meteorological forcing suitable for driving land surface and hydrological models across the 20th century, including diurnal/diurnal- to monthly-scale adjustments and bias corrections.
- Key variables included: PET (via PET_rc and PET_PT), Net Radiation, VPD, Wind, Rainfall, Snowfall, Precipitation, etc.
- Basin-focused results (for GIS use) cover PET_rc, PET_PT, Net Radiative fluxes, VPD, Wind, Rainfall, Snowfall, and Precipitation across 1901–1957, 1958–2001, and 1979–2001 intervals, highlighting regional trends and variability.
- Data construction relies on ERA-40 (1958–2001) with bias corrections and a reordered ERA-40 basis for 1901–1957. Appendix includes the ERA-40 basis-year ordering used for 1901–1957.

## Basin-focused findings relevant for map-based GIS analyses

- Orange River Basin
  - PET RC (mm/yr): 1901–1957 average ~1429; 1958–2001 average ~1449 with a negative long-term slope (-3.68 mm/yr per year) indicating a decline in PET_rc across that period; 1979–2001 also shows a negative trend.
  - PET PT (mm/yr): 1901–1957 average ~959; 1958–2001 average ~1123 with a positive slope (≈ +1.10 mm/yr per year), stronger increase than PET_rc.
  - Net Radiation (W/m^2): relatively stable around ~85–97, with a modest upward slope in 1958–2001.
  - VPD (kPa): ~1.27–1.53 across periods, small positive trends.
  - Wind (m/s): ~2.2 with small positive to neutral trends.
  - Rainfall (mm/yr): 1958–2001 ~346–337 mm/yr, showing an upward slope (1958–2001 ≈ +0.85 mm/yr per year) and larger increases in 1979–2001.
  - Snowfall (mm/yr): generally very small; ~0.1–0.12 in mid-periods.
  - Precipitation (mm/yr): aligned with Rainfall trends.
  - Implication for GIS: PET_pt-influenced evapotranspiration potential rising while PET_rc shows mixed or slight declines; precipitation shows notable increases in later period, useful for regional water-balance mapping.

- Lena River Basin
  - PET RC: 1901–1957 ~363; 1958–2001 ~367 with a small negative to near-zero trend in 1958–2001.
  - PET PT: 1901–1957 ~313; 1958–2001 ~313 with modest increases (1958–2001 slope ~+0.24–0.42 mm/yr^2 in some sub-periods).
  - Net Radiation: ~29 (1901–1957) to ~29–33 (1958–2001) with small positive trends.
  - Rainfall: 1958–2001 ~260–310 mm/yr; uptick in later period (1979–2001 ~309 mm/yr) indicating modest mid-century to late-century increases.
  - Snowfall: notable in some sub-periods (e.g., 132–135 mm/yr in 1958–2001) but lower than other basins.
  - VPD: around 0.24–0.27 kPa with slight increases in some periods.
  - Wind: ~1.7–1.9 m/s with small trends.
  - Precipitation: 1958–2001 around 1426–1427 mm/yr in some entries; mixed but generally high variability.
  - Implication for GIS: relatively modest PET changes with some late-period radiative and precipitation shifts; good for long-term evapotranspiration and hydrological visualization in boreal/temperate settings.

- Ganges-Brahmaputra River Basin
  - PET RC: 1901–1957 average ~889 mm/yr; 1958–2001 average ~870 mm/yr with a pronounced negative trend (1958–2001 slope ≈ -2.26 mm/yr^2) and stronger negative trend into 1979–2001.
  - PET PT: 1901–1957 average ~799; 1958–2001 average ~798 with a substantial negative trend in 1958–2001 (≈ -1.26 mm/yr^2) and continued decline into 1979–2001.
  - Net Radiation: 1901–1957 ~69.8 W/m^2; 1958–2001 ~67.0 W/m^2, steady decline.
  - Rainfall: 1958–2001 average ~1427 mm/yr with a positive trend in 1958–2001 (~+0.23 mm/yr^2) but a strong negative trend in 1979–2001 for rainfall (~ -1.33 mm/yr^2).
  - Snowfall: small but present (1958–2001 ~25.4 mm/yr; 1979–2001 ~26.3).
  - Precipitation: 1958–2001 average ~1426 mm/yr with a positive trend; 1979–2001 shows a sharp decrease in rainfall in some sub-periods.
  - VPD: around 0.95–0.97 kPa with generally small negative to near-zero trends.
  - Wind: around 1.7–1.9 m/s with a notable decrease in the 1979–2001 period in some entries.
  - Implication for GIS: strong sensitivity to monsoonal rainfall variability and a noted shift in PET relationships; useful for large-scale flood/hydrology mapping but with notable multi-decadal variability and period-dependent trends.

## Data characteristics for GIS practitioners

- Temporal coverage: 1901–1957 (ERA-40 basis years), 1958–2001 (WFD era with bias corrections), and 1979–2001 (subset for select basins). PET, Net Radiation, VPD, Wind, Rainfall, Snowfall, and Precipitation are provided as time-series with multi-period trends.
- Spatial resolution: 0.5° grid; suitable for regional to continental-scale GIS analyses and basin-wide map products; may require downscaling for very fine-scale local studies.
- Data quality and uncertainties: pre-1958 data have higher uncertainties due to sparse station coverage and reliance on ERA-40 substitutions; later periods incorporate bias corrections and calibration against CRU/GPCC-like references.
- Practical considerations: PET_rc and PET_PT enable cross-checks of evapotranspiration potential; ensure temporal alignment with your model or visualization (3-hourly vs 6-hourly steps mentioned in broader document); integrate Net Radiation, VPD, and Wind fields to assess energy-balance and atmospheric demand alongside precipitation/patterns.

## Appendices and methodological notes

- ERA-40 basis years: Appendix provides the exact ordering of ERA-40 basis years used to construct 1901–1957 WFD, illustrating how basis years map to continuous calendar years in the forced dataset.

- General GIS takeaway: The document supports map-based hydrological and land-surface analyses by offering multi-variable, multi-period forcing fields at a consistent grid. Basin-specific trends help inform regional map products showing changes in evapotranspiration potential, energy fluxes, and moisture availability over the 20th century, while caveats about pre-1958 data quality guide uncertainty-aware mapping.