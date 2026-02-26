# Supporting documentation

- Objective and study design
  - Compare the effect of hydrology on soil carbon turnover by running two versions of the same model: ECOSSE with its original piston flow hydrology vs an alternative HYDRUS hydrology.
  - Keep all other routines identical to isolate hydrological influence.
  - Simulate soil organic carbon turnover in the Sunjia catchment for 15 months starting October 2012 and evaluate model outputs against soil water measurements.

- Data sources and inputs
  - Sunjia Catchment Characteristics (CZO, Jiangxi Province, 50 ha)
    - Crops: peanuts (50%) and citrus trees (17%); differences in rooting depth and management (peanuts ploughed annually).
    - Parent material: kaolinitic quaternary red clay.
    - Climate: subtropical with distinct rainy/dry seasons; average rainfall ~1884 mm (1584 mm during the study period Oct 2012–Dec 2013).
  - Field measurements for model inputs
    - Soil data: measured at 5 points per crop type, at depths 0.05, 0.2, 0.4, 0.8 m; samples analyzed for bulk density, carbon, and nitrogen contents.
    - Weather data: hourly measurements of temperature, precipitation, humidity, wind speed from a single Sunjia station; potential evapotranspiration calculated via Penman-Monteith.
    - Soil moisture: measured at three locations, at depths 5, 20, 40, and 80 cm.
  - Model inputs
    - ECOSSE and HYDRUS require the same soil data inputs (moisture, temperature, pH, crop cover, etc.), with crop cover typically not driving turnover in ECOSSE.
  - Climate scenarios for sensitivity analysis
    - CMIP5 HadGEM2 projections used to illustrate sensitivity to hydrological changes.
    - Outputs downscaled from monthly to daily data to provide inputs for daily HYDRUS simulations.
    - Daily ET and RH derived from fitted relationships using CMIP5 temperature data and site-derived parameters; ET and RH values adjusted to preserve monthly water balance.

- Data processing and downscaling
  - Daily data derivation
    - ET and RH were estimated from fit-to-site relationships using daily CMIP5 temperatures and monthly ET outputs, then reconciled to maintain monthly water balance.
    - Daily evaporation and transpiration components split from corrected ET assuming proportional contributions.
  - Handling data gaps
    - Downscaling introduced a need for interpolation and fitted parameters due to missing RH in the CMIP5 outputs.

- Simulation design and outputs
  - Long-term simulations
    - Soil moisture and SOC simulated over a 94-year period using both ECOSSE’s internal hydrology and HYDRUS.
  - Outputs
    - Primary output: soil organic carbon (kg ha^-1) for both hydrology versions.
    - Data file: ECOSSE_SOC_2wat.csv contains long-term SOC results for ECOSSE with original hydrology and with HYDRYOLGY-enabled simulations.

- Quality control and reproducibility
  - Input files subjected to error checks to ensure data integrity.

- Implications for data governance and leadership
  - Data provenance and versioning
    - Clear separation of model versions (original ECOSSE hydrology vs HYDRUS) with identical inputs aside from hydrology to ensure traceability.
  - Data quality and metadata
    - Comprehensive input measurements (soil properties, bulk density, C/N, moisture at multiple depths and points) and documented processing steps; explicit handling of downscaling and daily data construction.
  - Data interoperability and discoverability
    - Standardized formats and a central file (ECOSSE_SOC_2wat.csv) for long-term SOC outputs to facilitate reuse and comparison across hydrology configurations.
  - Reproducibility challenges
    - Downscaling assumptions (monthly-to-daily interpolation) and RH estimation introduce uncertainties; transparency in methods is essential for reproducibility.
  - Collaboration considerations
    - Integration of field measurements, climate projections, and model outputs highlights the importance of well-documented data pipelines and metadata to enable cross-team use and validation.