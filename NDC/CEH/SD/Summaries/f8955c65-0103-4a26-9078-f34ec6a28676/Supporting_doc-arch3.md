# Supporting documentation

- Purpose and approach
  - Isolate the effect of hydrology on soil carbon turnover by comparing two versions of the same pool-based model: ECOSSE with its original hydrology versus a more detailed HYDRUS hydrology.
  - Simulate soil carbon turnover in the Sunjia catchment (15 months starting Oct 2012) and evaluate model accuracy against soil water measurements.
  - Use measured data from Sunjia CZO to drive the simulations and assess sensitivity to hydrological representation.

- Study site and crops
  - Sunjia catchment, Jiangxi Province, southeast China (50 ha; elevation 41–55 m).
  - Cropping: peanuts (50% of area) and citrus trees (17%); crops influence rooting depth and soil structure (peanuts annual; citrus perennial).

- Data inputs and measurement
  - Soil data: measured at five points per crop type across four depths (0.05, 0.2, 0.4, 0.8 m); analyses for bulk density, C content, N content.
  - Climate data: hourly measurements from a single monitoring station; includes temperature, precipitation, humidity, wind speed; potential evapotranspiration computed with Penman–Monteith.
  - Soil moisture: measured at three locations across depths 5, 20, 40, 80 cm using moisture probes.
  - Soil and crop inputs used for model runs; Table 2 summarizes soils data.
  - Model inputs processed to align with both ECOSSE and HYDRUS requirements.

- Climate scenarios and data handling
  - CMIP5 HadGEM2 simulations used to illustrate model sensitivity to hydrological changes under future climates.
  - Climate outputs are monthly; daily values produced via downscaling and simple interpolation to meet HYDRUS daily data needs.
  - Relative humidity derived from a fitted model using daily ET_corr and ET data; daily ET_corr split into evaporation and transpiration components with proportional assumptions.
  - Daily meteorological variables (e.g., ET_d_corr, RH_d) produced to drive hydrological simulations over a 94-year period.

- Model specifics and workflow
  - ECOSSE inputs: soil moisture, air temperature, soil pH, crop cover (crop cover typically not influencing the base turnover rate).
  - Hydrology variants: internal ECOSSE hydrology vs HYDRUS hydrology; all other routines kept constant.
  - Soil moisture modifiers and temperature-dependent decomposition rate modifiers govern C turnover in the model pools.
  - Quality control: input files checked for errors; consistent use of long-term SOC outputs.

- Outputs and data management
  - Primary output: soil organic carbon (SOC) in kg per hectare for both hydrological representations.
  - File example: ECOSSE_SOC_2wat.csv (long-term SOC simulations for ECOSSE with original hydrology and with HYDROLOGY).
  - Emphasis on transparent data provenance and the ability to compare hydrological approaches side-by-side.

- Relevance for monitoring frameworks
  - Demonstrates a structured approach to evaluate how a key driver (hydrology) influences environmental health indicators (soil carbon turnover).
  - Combines field measurements, model intercomparison, and climate scenario analysis to inform decision-making about model selection and monitoring design.
  - Highlights data quality and provenance considerations, including handling missing data, downscaling requirements, and the necessity for consistent documentation to enable reproducibility.
  - Notes potential data-related barriers such as the need for detailed metadata and transparent data processing steps, which align with typical monitoring framework challenges.