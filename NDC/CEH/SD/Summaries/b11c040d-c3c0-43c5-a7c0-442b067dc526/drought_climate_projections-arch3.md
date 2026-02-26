# Climate Change and Future Drought Projections

- Provides near-future (2021-2050) climate and drought projections for the Mun River basin, Northeast Thailand, focusing on maximum/minimum temperature and rainfall, plus meteorological, hydrological, and agricultural drought indicators.
- Uses multi-model ensembles from CMIP5 (RCP4.5 and RCP8.5) and CMIP6 (SSP5-8.5) with spatial resolution of 0.25 degrees; raw data were bias-corrected and bias-corrected rainfall uses empirical distribution while temperature is corrected by fitting a normal distribution.
- Baseline reference period for bias correction is 1981-2010; rainfall units are mm, temperatures in °C.
- Drought projections are produced under five future scenarios combining climate change and land-use change (LUC): CC; LUC_BAU; LUC_CCU; CC+LUC_BAU; CC+LUC_CCU.

- Drought types and indices
  - Meteorological drought: Standardized Precipitation Evapotranspiration Index (SPEI).
  - Hydrological drought: Standardized Runoff Index (SRI).
  - Agricultural drought: Standardized Soil Moisture Index (SSMI).
  - Agricultural and Hydrological droughts are also evaluated under land-use change scenarios (BAU, CCU) and combinations thereof.
  - ETCCDI climate extremes (e.g., TX90p, TN90p, TXx, TNx, RX1day, RX5day, CDD, CWD, R20, R40, R95p, R99p, SDII, WSDI).

- Data organization and outputs
  - Drought and climate-extremes data are organized into folders:
    - 1_MeteorologicalDroughts: subfolders by timescale (1-, 3-, 6-, 12-month) with duration, intensity, severity CSVs.
    - 2_HydrologicalDroughts: subfolders by combination of climate-land-use scenarios (CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only) and timescales (1-, 3-, 6-, 12-month) with duration, intensity, severity CSVs.
    - 3_AgriculturalDroughts: same scenario-timescale structure as Hydrological droughts with duration, intensity, severity CSVs.
    - 4_ETCCDI_ClimateExtremes: indices folders (CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI) each containing CMIP5-RCP45, CMIP5-RCP85, and CMIP6-SSP5-85 CSVs.
  - All drought CSV files include 13 columns: grid_ID, lat, lon, Observed (baseline), eight CMIP6 model projections, and ensemble average.
  - ETCCDI CSVs include lat, lon, grid_ID, Observed (baseline), projections from climate models, and ensemble average.

- Spatial and temporal coverage
  - Meteorological, hydrological, and agricultural drought projections cover grids across the Mun River basin (91 grids for bias-corrected near-future data; units: rainfall in mm, temperatures in °C).
  - Timescales: 1, 3, 6, and 12 months for drought characteristics (duration, intensity, severity).
  - ETCCDI climate extremes provide multi-model projections at the same spatial resolution and baseline.

- Processing details and references
  - Raw data accessed from Earth System Grid Federation (ESGF) in December 2020; data re-gridded to 0.25 degrees via bilinear interpolation.
  - Rainfall bias correction uses empirical distribution; rainfall-high quantiles adjusted; temperature bias-corrected by normal distribution fitting.
  - References for methodology include Khadka et al. (2022) on near-future climate and extreme events in northeast Thailand, and related works on drought indices (Khadka et al., 2021) and land-use change scenario development (Penny et al., 2021).

- Practical considerations for monitoring frameworks
  - The multi-model ensemble approach supports uncertainty assessment and scenario planning for decision-making.
  - Data are structured to facilitate ingestion into dashboards and reports, with clear separation by drought type, timescale, and scenario.
  - The combination of climate and land-use scenarios enables assessment of policy options (e.g., forest conservation, urban growth management) on drought risk.
  - Disclosure and governance considerations (metadata quality, data sharing, and up-to-date updates) are relevant when integrating these datasets into ongoing monitoring programs.