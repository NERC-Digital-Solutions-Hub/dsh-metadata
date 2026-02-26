# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

- Purpose and scope
  - Provides half-degree, sub-daily meteorological forcing to drive land surface and hydrological models for the twentieth century.
  - Enables robust assessment of evaporation, soil moisture, and runoff by supplying consistent diurnal and sub-daily forcing data.
  - Delivers two main periods: 1901-1957 historical forcing (based on re-ordered ERA-40) and 1958-2001 modern forcing (ERA-40 based with bias correction and harmonization).

- Data provenance and governance
  - Data lineage paths: ERA-40 surface variables augmented with observational datasets (CRU, GPCC) and aerosol corrections (HadGEM2-A) to support realism and traceability.
  - Clear separation of periods: 1901-1957 (historical, with re-ordered ERA-40 years) and 1958-2001 (primary modern forcing).
  - Extensive documentation and governance artifacts to support reproducibility, auditability, and versioning.

- Data content and formats
  - Variables included: wind speed (10 m), temperature (2 m), surface pressure, specific humidity (2 m), downward longwave and shortwave radiation, rainfall rate, snowfall rate; additional Net Rad and VPD metrics used in analyses.
  - Spatial and temporal structure: global half-degree grid with CRU land-sea mask; data published in netCDF (ALMA convention).
  - Temporal resolution: rainfall/snowfall at 3-hourly; other variables interpolated to 3-hourly or 6-hourly as appropriate.
  - Accessibility: data are accompanied by technical reports and publications to support traceability and reuse.

- Processing steps and data corrections
  - Temperature, pressure, humidity, and longwave radiation: ERA-40 biases corrected against CRU; elevation adjustments applied; diurnal ranges anchored to CRU observations.
  - Downward shortwave radiation: corrected for aerosols using HadGEM2-A aerosol depths; corrections account for both clear-sky and cloudy-sky components.
  - Precipitation (rainfall and snowfall): six-step procedure emphasizing spatial coherence and frontal-event continuity; includes bilinear interpolation, ratio preservation, wet-day adjustments, gauge-catch corrections, and GPCC cross-checks.
  - Preservation of diurnal and inter-variable covariances: methodological emphasis on maintaining realistic diurnal cycles and inter-variable relationships.
  - Special handling for 1901-1957: ERA-40 years extracted in random order and assigned to historical years to preserve global statistics, while maintaining similar variability and covariances.
  - Documentation and provenance: corrections, sources, and validation are thoroughly documented (WATCH Technical Report 22 and related publications).

- Validation and limitations
  - Validation against Fluxnet sites shows good agreement for temperature and radiation; precipitation validation is weaker due to scale and model limitations.
  - Overall, 1958-2001 forcing exhibits strong fidelity at monthly to interannual scales; sub-daily precipitation fidelity is more variable, particularly in tropical regions.
  - Important caveats: pre-1958 data may have biases from limited station coverage and the randomization approach; exact historical event timing for 1901-1957 is not site-accurate; sub-daily tropical precipitation fidelity remains a challenge.

- Basin-level insights (illustrative content)
  - Appendix tables provide basin-level statistics for PET estimates (PET rc and PET PT), net radiation, vapor-pressure deficit (VPD), wind, rainfall, snowfall, and precipitation across multiple basins (e.g., Orange, Murray-Darling, Lena, Ganges-Brahmaputra, etc.).
  - For each basin and period (1901-1957, 1958-2001, 1979-2001), the data include average values, slopes (trend), minimum/maximum slopes, effective sample size (Neff), and significance indicators.
  - The results show regional variability in PET estimates and their trends, with PET_rc and PET_PT diverging in some basins under different moisture regimes, underscoring the sensitivity of hydrological assessments to forcing and method.

- Data governance and usage notes for Data Stewards
  - Maintain and publish comprehensive metadata detailing data sources, corrections, and validation results to support traceability and accountability.
  - Document methodological rationales (e.g., wet-day corrections, aerosol adjustments) to aid auditability and future re-use.
  - Clearly communicate period-specific caveats and uncertainties, enabling informed data use and decision-making.
  - Provide access to associated technical reports and methodological papers to facilitate reproducibility and secondary analyses.
  - Encourage proper citation of WATCH data and underlying sources to preserve data lineage.

- Practical takeaways for data stewardship
  - The WATCH Forcing Data deliver a provenance-backed, multi-period instrument for long-term hydrological analysis and inter-model comparisons.
  - The 1958-2001 dataset offers robust forcing for real-world meteorological events and climate trends; the 1901-1957 dataset preserves statistical continuity with caveats on event timing and data sparsity.
  - Users should account for known limitations (especially sub-daily tropical precipitation and early-century data) and leverage the documented processing and validation when interpreting results.

- Conclusion
  - The WATCH Forcing Data provide a robust, governance-friendly foundation for driving land surface and hydrological models across the twentieth century, with careful documentation, period-specific caveats, and basin-level context to support transparent data use and reproducibility.