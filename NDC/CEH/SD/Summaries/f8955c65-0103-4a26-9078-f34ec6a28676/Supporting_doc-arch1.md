# Supporting documentation

- Objective: Isolate the effect of hydrology within a pool-based ECOSSE model by comparing the original piston flow hydrology with the HYDRUS model. Simulate soil organic carbon turnover in the Sunjia catchment for 15 months (Oct 2012–Dec 2013) and evaluate accuracy by comparing soil hydrology outputs to soil water measurements.

- Site and data
  - Sunjia catchment, Jiangxi Province, southeast China (50 ha; elevation 41–55 m).
  - Cropping: peanuts ~50% of area; citrus ~17%; typical regional crops; peanut is annual with shallow roots; citrus perennial with deeper roots; ploughed annually.
  - Soil: kaolinitic quaternary red clay; parent material extends beyond CZO boundaries.
  - Climate: subtropical with distinct wet/dry seasons; average annual rainfall ~1884 mm (study period ~1584 mm; rainfall slightly below average).
  - Measurements: soil moisture at 4 depths (0.05, 0.2, 0.4, 0.8 m) across 5 points per crop; soil bulk density, C, N contents measured at two depths; weather data from a single Sunjia station (hourly temperature, precipitation, humidity, wind; PET via Penman–Monteith). Soil moisture measured at three locations (5, 20, 40, 80 cm) using ML-2x devices.

- Models and inputs
  - ECOSSE: soil moisture acts as a key moisture driver for soil C turnover; other drivers include temperature, soil pH, and crop cover (crop cover generally has no influence in the setup). Turnover rates adjusted by moisture-based modifiers.
  - HYDRUS: a more detailed hydrology approach used for comparison with ECOSSE.
  - Inputs common to both: soil data (bulk density, C, N) and weather data; crop type information.
  - Future climate: CMIP5 HadGEM2 projections used to test hydrological sensitivity; monthly outputs downscaled to daily data for the simulations.

- Data processing and downscaling
  - Daily data generation: since HYDRUS requires daily inputs (including RH), monthly CMIP5 outputs were downscaled to daily values via interpolation and simple modelling.
  - PET and ET relationships: daily ET calculated from daily temperature using ET_d = a_ET * T_d + b_ET; daily RH derived from ET_d_corr via RH = a_RH * ET_d_corr + b_RH.
  - Monthly to daily balance: ET_d_corr = ET_d + (ET_m_CMIP5 − ET_m)/N to preserve monthly water balance; ET_d_corr split into evaporation Ed_corr and transpiration Td_corr assuming the same proportional contribution as in the CMIP5-derived monthly data.
  - Relative humidity for CMIP5 period: RH_d = a_RH * ET_d_corr + b_RH.
  - Simulation horizon for hydrology: long-term 94-year period using both ECOSSE and HYDRUS hydrology.

- Outputs and data handling
  - Primary output: soil organic carbon (SOC) in kg ha−1 for both hydrology versions.
  - File produced: ECOSSE_SOC_2wat.csv (long-term SOC simulations using ECOSSE with original hydrology and with HYDROLOGY).
  - Quality control: input files checked for errors; data and modeling steps documented to ensure reproducibility.

- Validation and interpretation
  - The two hydrological approaches were evaluated by comparing simulated soil moisture outputs to Sunjia soil water measurements from the CZO.
  - The study focuses on assessing how hydrological representation affects soil carbon turnover predictions under sub-tropical cropland conditions with mixed crops and depth-varying soil properties.

- References
  - He, Z., Zhang, M., & Wilson, M. J. (2004). Distribution and classification of red soils in China.
  - Smith, J., Gottschalk, P., Bellarby, J., et al. (2010). Model to Estimate Carbon in Organic Soils—Sequestration and Emissions (ECOSSE).