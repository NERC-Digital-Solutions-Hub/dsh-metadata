# Climate Change and Future Drought Projections

- Overview: Provides near-future climate projections (2021-2050) for the Mun River basin in Northeast Thailand, covering maximum/minimum temperature and rainfall, plus projections of meteorological, hydrological, and agricultural droughts and climate extremes. Uses CMIP5 (RCP4.5 and RCP8.5) and CMIP6 (SSP5-8.5) ensembles at 0.25-degree resolution. Raw data were sourced from ESGF (Dec 2020), re-gridded to 0.25°, and bias-corrected using quantile mapping (rainfall via empirical distribution; temperature with normal distribution). Key references provided for methods.

- Datasets and structure:
  - 1_MeteorologicalDroughts
    - 1-, 3-, 6-, 12-month timescales
    - For each timescale: files documenting duration, intensity, and severity
    - Files organized as CSVs with 13 columns: grid_ID, lat, lon, Observed, projections from 8 CMIP6 models, and ensemble mean
  - 2_HydrologicalDroughts
    - Scenarios: CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only
    - Timescales: 1-, 3-, 6-, 12-month
    - Each contains three CSVs per timescale: duration, intensity, severity
    - Structure mirrors MeteorologicalDroughts (grid_ID, lat, lon, Observed, model projections, ensemble)
  - 3_AgriculturalDroughts
    - Same scenario and timescale structure as Hydrological Droughts
    - Three CSVs per timescale: duration, intensity, severity
  - 4_ETCCDI_ClimateExtremes
    - Indices: CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI
    - For each index: CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85
    - CSVs include lat, lon, grid_ID, Observed (1981-2010 baseline), model projections, and ensemble mean
  - All drought-related CSVs contain 13 columns; consistent format across datasets

- Data processing and bias correction details:
  - Re-gridding: raw data to 0.25-degree grids
  - Bias correction: Quantile mapping using 1981-2010 reference period
  - Temperature: normal distribution fitting
  - Rainfall: empirical distribution-based correction; higher quantiles adjusted for future periods
  - Near-future rainfall/temperature data available for 91 grids in the Mun River basin
  - Units: Rainfall in mm; Temperature in degrees Celsius

- Temporal and spatial coverage:
  - Near-future projection period: 2021-2050
  - Spatial resolution: 0.25-degree grids
  - Drought indices and meteorological/hydrological/agricultural drought projections cover multiple timescales (1, 3, 6, 12 months) and land-use scenarios

- Scenarios and case definitions:
  - Drought assessments under five future cases:
    - CC only (climate change only)
    - LUC_BAU (land-use change with business-as-usual)
    - LUC_CCU (land-use change with conservation and urban growth)
    - CC + LUC_BAU
    - CC + LUC_CCU
  - Agricultural and Hydrological drought projections are provided under these scenarios to explore combined climate and land-use effects

- Access, provenance, and governance:
  - Datasets are organized for straightforward access and reuse, with clear folder structures by drought type, scenario, and timescale
  - Data uploaded to relevant portals; explicit file naming and folder conventions support discoverability and provenance tracking
  - Documentation references model sources and methodological choices (bias correction, indices, and scenario definitions)

- Data quality, usability, and stewardship considerations:
  - QA: Data have undergone re-gridding and bias correction; metadata describes baseline and projection components
  - Usability: Uniform 13-column CSV format across drought and climate-extremes datasets facilitates cross-dataset analyses and integration
  - Governance: Clear delineation of scenarios (CC, LUC) and model ensembles supports reproducibility and auditing
  - Documentation references for methods and indices (Khadka et al. 2022; Penny et al. 2021; Karl et al. 1999) to support interpretation and methodological transparency

- Key references:
  - Khadka, D. et al. (2022) for near-future climate and extremes in Northeast Thailand
  - Penny, J. et al. (2021) for land-use change scenarios and public participation context
  - Karl, T.R. et al. (1999) for ETCCDI climate-extremes indices definitions

- Practical implications for data stewards:
  - Maintain alignment with established drought indices and multi-model ensembles
  - Ensure ongoing updates and versioning as newer climate simulations become available
  - Preserve consistent metadata, model provenance, and scenario descriptions to support governance and user needs
  - Facilitate usability by preserving standardized file structures and units across all datasets