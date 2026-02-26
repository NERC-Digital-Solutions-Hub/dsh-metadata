# WATCH Forcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- Scope of the data
  - Provides basin-scale, long-term meteorological forcings and derived hydrological indicators to support evaluation of external drivers of evaporation (PET_rc and PET_PT) and related variables.
  - Includes multiple basins (e.g., Orange River, Murray–Darling, Lena, Ganges–Brahmaputra) with detailed statistics across three historical windows: 1901–1957, 1958–2001, and, where available, 1979–2001.
  - Variables covered per basin include PET_rc, PET_PT, Net Radiation, VPD, Wind, Rainfall, Snowfall, and Precipitation (all in appropriate units).

- Basins: key patterns and implications for monitoring

  - Orange River Basin
    - PET_rc: generally high (around 1400–1500 mm/yr) with a long-term slight to moderate decline across periods.
    - PET_PT: consistently lower than PET_rc, with modest increases over later periods.
    - Net Radiation: ~96–97 W/m2, relatively stable with small changes.
    - VPD: around 1.2–1.5 kPa, with small positive trends in some windows.
    - Wind: mid-range (~2.2 m/s), relatively stable over time.
    - Rainfall: variable but showing increases in some periods; Snowfall minimal.
    - Precipitation: moderate totals with basin-to-basin variability; overall data indicate regional shifts in moisture availability affecting PET calculations.
    - Monitoring note: PET contrasts (PET_rc vs PET_PT) and small but detectable trends in moisture and radiation drivers are important for policy-oriented hydrological risk assessments.

  - Murray–Darling River Basin
    - PET_rc: substantial values with generally positive but modest trends in some windows; overall variability across 1901–2001.
    - PET_PT: higher than PET_rc, reflecting radiation-dominated estimates; trend directions vary by period.
    - Net Radiation: around low to mid-80s–90s W/m2, with regional differences across windows.
    - VPD: typically around 0.9–1.0 kPa, with fluctuations over time.
    - Wind: ~1.7–2.0 m/s on average, showing some temporal changes.
    - Rainfall/Precipitation: notable interannual variability with periods of both increase and decrease; Snowfall generally small but detectable in some subregions.
    - Monitoring note: the region exhibits pronounced sensitivity of PET metrics to moisture supply and radiation balance; long-term trends require careful attribution to data period validity and measurement density.

  - Lena River Basin
    - PET_rc: around mid-300s mm/yr, with modest upward or mixed slopes in various windows.
    - PET_PT: generally lower than PET_rc, with substantive increases in some periods.
    - Net Radiation: low to moderate (≈ 29–32 W/m2), with small positive trends in some windows.
    - VPD: around 0.25–0.27 kPa, typically small changes over time.
    - Wind: around 1.6–2.0 m/s, with slight temporal variation.
    - Rainfall/Precipitation: large annual totals (hundreds to over a thousand mm/yr) with regional variability; Snowfall more notable than in some other basins, yet still modest overall.
    - Monitoring note: PET_PT vs PET_rc differences are meaningful in cold, melt-driven regimes; data show consistent but regionally varying moisture and radiation signals.

  - Ganges–Brahmaputra River Basin
    - PET_rc: high (roughly 700–900+ mm/yr for different windows), with strong interannual variability and period-specific trends.
    - PET_PT: typically lower than PET_rc but increases in some windows, reflecting radiation-dominated dynamics.
    - Net Radiation: around 60–100 W/m2 depending on window, with modest trend fluctuations.
    - VPD: near 0.9–1.3 kPa across periods, with periods of increase.
    - Wind: ~1.7–2.0 m/s, showing temporal fluctuations.
    - Rainfall/Precipitation: substantial totals with notable increases in some windows and declines in others; Snowfall variable by subregion.
    - Monitoring note: strong regional drivers (moisture variability and radiation) influence PET and hydroclimate assessments; significant interannual variability requires robust uncertainty handling in monitoring frameworks.

- Common themes for monitoring frameworks
  - Long-term consistency: PET_rc and PET_PT trends vary by basin and period; radiation and moisture balance are key interpreters of PET changes.
  - Data requirements: robust, well-documented metadata for each variable (and period) is essential; differences between PET_rc and PET_PT provide a useful sensitivity check for policy-relevant water resource metrics.
  - Uncertainty and governance: use multiple forcing products and keep provenance transparent; document limitations for pre-1958 windows where ERA-40-based basis years were reallocated, and where gauge data density affects reliability.
  - Regional heterogeneity: basins show divergent trajectories in moisture supply, radiation, wind, and VPD; monitoring frameworks should avoid overgeneralizing global trends and instead tailor assessments to regional drivers.
  - Open data and reproducibility: data are designed for transparency and reproducibility, with explicit methodology notes on bias corrections and interpolation; ensure outputs link to open sources and metadata for governance.

- Appendix and data governance notes
  - Appendix Table 1 lists the order of ERA-40 basis years used for 1901–1957, illustrating how ERA-40 years are mapped to WATCH Forcing Data components and basis years.
  - Overall implication for monitoring: the WATCH forcing data provide a structured, long-term, multi-variable foundation to scrutinize external drivers of evaporation and related hydrological variables, while highlighting where caution is needed due to data period limitations and regional data sparsity.

- Key takeaways for authors of monitoring frameworks
  - Build monitoring outputs on forcing data with explicit data sources, correction steps, and validation details to minimize hidden biases.
  - Use multi-dataset bias correction and clearly communicate uncertainties; maintain traceable data lineage.
  - Account for regional heterogeneity in drivers (radiation, wind, humidity) when deriving policy-relevant metrics like PET and water-resource indicators.
  - Clearly indicate period robustness (e.g., 1958–2001 confidence) versus periods with higher uncertainty (1901–1957) and link outputs accordingly to decision-making timelines.