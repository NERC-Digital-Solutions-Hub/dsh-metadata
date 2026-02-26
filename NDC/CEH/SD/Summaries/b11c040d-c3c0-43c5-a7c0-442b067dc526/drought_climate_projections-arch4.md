# Climate Change and Future Drought Projections

- Provides near-future climate projections (2021-2050) for the Mun River basin, Northeast Thailand, covering maximum/minimum temperature and rainfall.
- Spatial resolution: 0.25-degree grids; baseline period 1981-2010 for Observed values.
- Scenarios and models:
  - CMIP5: RCP4.5 and RCP8.5
  - CMIP6: SSP5-8.5
  - Projections derived from multiple models (14 CMIP5, 8 CMIP6) with ensemble averages.
- Data processing and bias correction:
  - Raw data accessed from the Earth System Grid Federation (ESGF) in December 2020.
  - Regridded to 0.25 degrees via bilinear interpolation.
  - Bias-corrected using Quantile Mapping for temperature and rainfall; rainfall bias correction uses empirical distribution; rainfall high quantiles corrected; temperature bias corrected assuming normal distribution.
  - Document references for methods: Khadka et al. (2022).
- Dataset scope: includes meteorological, hydrological, and agricultural drought projections, plus climate extremes.

## Drought Projections and Indices

- Meteorological drought: Standardized Precipitation Evapotranspiration Index (SPEI).
- Hydrological drought: Standardized Runoff Index (SRI).
- Agricultural drought: Standardized Soil Moisture Index (SSMI).
- Land-use change scenarios (LUC) and direct climate change scenarios:
  - Business As Usual (BAU)
  - Combination of Forest Conservation and Urban Growth (CCU)
  - Five future cases: CC only (CC), LUC_BAU, LUC_CCU, CC+LUC_BAU, CC+LUC_CCU

## Data Organization and File Structure

- Drought datasets are organized into four main folders:
  - 1_MeteorologicalDroughts
  - 2_HydrologicalDroughts
  - 3_AgriculturalDroughts
  - 4_ETCCDI_ClimateExtremes

- Meteorological droughts (1_MeteorologicalDroughts):
  - Subfolders by timescale: 1-month, 3-month, 6-month, 12-month.
  - Each timescale contains three CSV files: duration, intensity, severity.

- Hydrological droughts (2_HydrologicalDroughts):
  - Subfolders by scenario combinations: CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
  - Each scenario contains 1-, 3-, 6-, and 12-month timescale subfolders with three CSV files per timescale: duration, intensity, severity.

- Agricultural droughts (3_AgriculturalDroughts):
  - Structure mirrors Hydrological droughts with the same scenario folders: CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
  - Each timescale (1, 3, 6, 12 months) includes duration, intensity, severity CSVs.

- All drought CSV files:
  - Contain 13 columns: grid_ID, lat, lon, Observed (baseline), 8 CMIP6 model projections, and ensemble average (final column).

- Climate extremes (4_ETCCDI_ClimateExtremes):
  - Indices: CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI.
  - For each index, three CSV files: CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85.
  - Columns: lat, lon, grid_ID, Observed (1981-2010 baseline), projections from models, ensemble average.
  - Units and descriptions align with ETCCDI definitions (as detailed in the accompanying table).

## Model Details and Output

- Model references:
  - CMIP5 models include listed families (e.g., ACCESS1-0, BNU-ESM, CanESM2, etc.).
  - CMIP6 models include listed families (e.g., CNRM-CM6-1, EC-Earth3P, HadGEM3 variants, etc.).
- Outputs are presented as model projections and ensemble means for each grid cell within the Mun River basin (91 grids for near-future rainfall and temperature data).
- Units:
  - Rainfall: millimeters (mm)
  - Temperature: degrees Celsius (°C)
- Time frame and coverage:
  - Projections are for 2021-2050 (near-future) with a focus on drought characteristics and climate extremes.

## Practical Considerations for Data Leaders

- Data completeness and provenance:
  - Multi-model, multi-scenario dataset with clearly defined Observed baseline and ensemble means.
  - Bias correction and regridding introduce standardization, but users should account for method-specific uncertainties.
- Accessibility and compatibility:
  - Data organized in a consistent, hierarchical folder structure; CSV format with 13 columns facilitates integration with analysis pipelines.
- Relevance for policy and planning:
  - Enables assessment of changes in meteorological, hydrological, and agricultural drought characteristics under multiple climate and land-use futures.
  - ETCCDI climate extremes provide insights into extreme temperature and precipitation behaviors.
- Metadata and traceability:
  - Explicit model lists, scenarios, baseline period, and correction methods referenced; cross-check Khadka et al. (2022) for methodology details.
- Potential limitations:
  - Bias correction methods rely on historical distributions; regional applicability and assumption of stationarity may affect interpretation.
  - Spatial resolution limited to 0.25 degrees; finer-scale impacts may require downscaling or local calibration.
  - Data gaps may exist across different scenario combinations, though structure aims to be comprehensive.

## References and Supporting Details

- Methodology references:
  - Khadka et al. (2022) for near-future climate projections and bias correction approach.
  - Penny et al. (2021) and related sources for land-use change scenario descriptions.
  - CLIVAR/GCOS/WMO framework references for ETCCDI indices (Table 1 descriptions provided in the dataset).
- Data access:
  - Projections and raw climate data accessed via ESGF portal (December 2020).