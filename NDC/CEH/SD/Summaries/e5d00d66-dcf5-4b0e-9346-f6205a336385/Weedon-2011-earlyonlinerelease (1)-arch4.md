# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- Overview and scope
  - Presents the WATCH Forcing Data (WFD), a global climate forcing dataset used for land surface and hydrological modeling, spanning 1901–2001 with higher-resolution sub-daily inputs (e.g., 3-hourly radiation; 6-hourly other variables).
  - Pre-1958 data are constructed by reorganizing ERA-40 data to preserve statistical characteristics; the dataset supports evaluation of external drivers of evaporation and regional to global modeling.
  - Includes multiple climate variables (PET rc, PET PT, Net Rad, VPD, Wind, Rainfall, Snowfall, Precipitation) and their time-series statistics by basin.

- Data architecture, sources, and processing (key governance highlights)
  - Global coverage with a half-degree grid; variables stored in netCDF with standardized conventions.
  - Bias corrections and adjustments applied to temperature, pressure, humidity, radiation, and precipitation fields; efforts to maintain diurnal cycles and spatial coherence.
  - Validation and uncertainty context provided (FluxNET comparisons; regional limitations pre-1958 due to ERA-40 biases and sparse gauges).
  - Clear documentation of data lineage, bias-correction steps, and uncertainties to support governance, reproducibility, and reuse.

- Basin-level findings (illustrative examples from the provided chunks)
  - Orange River Basin
    - PET rc (mm/yr): 1901–1957 avg 1586.19; 1958–2001 avg 1604.15; 1979–2001 avg 1623.47; slope trends show change across intervals (e.g., modest positive slope 1958–2001, with notable variation in 1979–2001).
    - PET PT (mm/yr): 1901–1957 avg 1114.63; 1958–2001 avg 1123.40; 1979–2001 avg 1131.46.
    - Net Radiance: around 96–97 W/m^2 across intervals; VPD around 1.45–1.53 kPa; Wind near 2.20 m/s.
    - Rainfall: 1958–2001 avg ~346–347 mm/yr; 1979–2001 ~338 mm/yr; Snowfall small (0.12–0.00 mm/yr); Precipitation ~447–445 mm/yr.
  - Lena River Basin
    - PET rc: 1901–1957 avg ~363.5; 1958–2001 avg ~366.7; 1979–2001 avg ~366.1.
    - PET PT: 1901–1957 avg ~312.8; 1958–2001 avg ~313.5; 1979–2001 avg ~314.7.
    - Net Rad: ~29.1–28.7 W/m^2 across periods; VPD ~0.24–0.25 kPa; Wind ~1.69–1.68 m/s.
    - Rainfall: ~1400–1427 mm/yr (1958–2001 and 1979–2001); Snowfall ~132.3–26.3 mm/yr; Precipitation ~1426.3–1426.7 mm/yr.
  - Ganges–Brahmaputra Basin
    - PET rc: 1901–1957 avg ~889.3; 1958–2001 avg ~869.7; 1979–2001 avg ~843.6.
    - PET PT: 1901–1957 avg ~798.7; 1958–2001 avg ~767.9; 1979–2001 avg ~752.0.
    - Net Rad: ~69.8–65.5 W/m^2 over periods; VPD ~0.95–0.93 kPa; Wind ~1.97–1.99 m/s.
    - Rainfall: 1958–2001 avg ~1401–1427 mm/yr; Snowfall ~25–26 mm/yr (1901–1957 vs 1958–2001); Precipitation ~1426–1427 mm/yr.
  - Murray-Darling Basin (data partially presented; some entries incomplete in the excerpt)
    - PET rc, PET PT, Net Rad, VPD, Wind, Rainfall, Snowfall, Precipitation records begin to show interval-based trends, but several entries are placeholders or incomplete in the provided text.
- Temporal and trend context
  - PET rc and PET PT display basin- and interval-specific trends, with some intervals showing significant changes (as indicated by adjusted slope probabilities).
  - Net radiation, VPD, wind, rainfall, and snowfall exhibit regionally varying trends, underscoring the importance of basins as distinct data products for model validation and impact assessment.
- Data quality, validation, and limitations
  - Validation against FluxNET and observational products shows reasonable skill for near-surface temperature and radiation terms; precipitation capture is more challenging at sub-daily scales but coherent at daily/monthly scales.
  - Pre-1958 data are subject to ERA-40 biases and sparser gauge coverage; uncertainties are documented and incorporated into interpretation.
  - Footprints, spatial resolution, and cross-variable consistency are addressed through bias corrections and careful data processing, but basins differ in data density and temporal coverage.
- Access, governance, and use in data leadership
  - WFD is provided as a technical data resource for land-surface and hydrological modeling within WATCH projects and related studies.
  - Emphasizes traceability, reproducibility, and detailed documentation of data sources, bias corrections, and uncertainties to support governance, collaboration, and cross-network data sharing.
  - Appendix Table 1 outlines the ERA-40 basis-year sequencing used for 1901–1957, illustrating the methodological approach to reconstructing earlier periods and maintaining temporal coherence across basins.

- Implications for Data Leaders
  - Demonstrates robust multi-source data integration (ERA-40, CRU, GPCC, aerosols) with explicit bias corrections and end-to-end data lineage.
  - Highlights the need to preserve spatial coherence and diurnal-cycle fidelity when aggregating climate forcing for hydrological modeling.
  - Shows how to balance global coverage with regional accuracy, and how to document limitations and uncertainties to support governance and decision-making.
  - Underlines the importance of cross-community collaboration to refine metadata, improve data standards, and enhance discoverability and reuse across networks, enabling co-ownership of data assets.