# Supporting documentation

- Objective
  - Isolate the effect of hydrology within a pool-based soil carbon turnover model by comparing two versions of the same model: the original piston-flow ECOSSE hydrology and a more detailed HYDRUS hydrology.
  - Simulate soil carbon turnover in the Sunjia catchment for 15 months (Oct 2012–Dec 2013) and evaluate accuracy against soil water measurements.

- Study area and data inputs
  - Sunjia CZO, Jiangxi Province, southeast China (50 ha; elevation 41–55 m; crops: peanuts 50%, citrus 17%).
  - Soil: kaolinitic quaternary red clay; subsite soils extended beyond CZO (101.9 ha).
  - Climate: subtropical with distinct rainy/dry seasons; average annual rainfall ~1884 mm (1584 mm during study period).
  - Soil data: measured at 5 points per crop type across depths 0.05, 0.2, 0.4, 0.8 m; inputs include bulk density, C, N for both depths and crops.
  - Weather data: hourly measurements (temperature, precipitation, humidity, wind); Penman–Monteith for potential evapotranspiration.
  - Vegetation/crop data: crop cover treated as non-influential in base model.

- Model structure and drivers
  - ECOSSE with original hydrology vs ECOSSE with HYDRUS hydrology (other routines identical).
  - Key drivers: soil moisture, air temperature, soil pH, crop cover (base model); soil moisture acts as a primary control on C turnover via decomposition rate modifiers.
  - Moisture rate modifier applied to base turnover; explicit treatment of soil moisture dynamics.

- Climate inputs and data processing
  - CMIP5 HadGEM2 climate scenarios used to test sensitivity to hydrological conditions; monthly data downscaled to daily values due to missing inputs.
  - Daily data reconstruction:
    - Derived daily ET_corr from monthly ET with linear fits to daily temperature.
    - Adjusted daily ET_corr to preserve CMIP5 monthly water balance.
    - Split ET_corr into evaporation and transpiration assuming proportional contributions from monthly data.
    - Calculated daily relative humidity RH_d from ET_corr using a linear fit.
  - Daily inputs used to drive HYDRUS and ECOSSE HYDROLOGY over a 94-year period to assess long-term soil moisture changes.

- Simulation details and outputs
  - Timeframes:
    - 15-month period for direct comparison of hydrology effects on soil carbon turnover (Oct 2012–Dec 2013).
    - 94-year period for long-term soil moisture dynamics.
  - Outputs:
    - Soil organic carbon (SOC) values in kg ha^-1 for both hydrology versions.
    - Quality-controlled input data files.
  - Validation: SOC model outputs were compared with soil water measurements to evaluate hydrological approaches.

- Data products and files
  - Output file: ECOSSE_SOC_2wat.csv (long-term SOC simulations for ECOSSE with original hydrology and with HYDROLOGY).

- References
  - He, Z., Zhang, M., & Wilson, M. J. (2004). Distribution and classification of red soils in China.
  - Smith, J. et al. (2010). Model to Estimate Carbon in Organic Soils—Sequestration and Emissions (ECOSSE).