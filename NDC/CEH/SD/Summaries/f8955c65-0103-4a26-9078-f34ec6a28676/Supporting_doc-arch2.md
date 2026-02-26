# Supporting documentation

## Overview
- Isolates the effect of hydrology on soil carbon turnover by comparing two versions of the same pool-based model: ECOSSE with its original hydrology and a HYDRUS-based hydrology version.
- 15-month simulation period starting October 2012 in the Sunjia catchment; results evaluated against soil water measurements.

## Study site and crops
- Sunjia CZO, Jiangxi Province, southeast China (50 ha; elevation 41–55 m).
- Cropping: peanuts (50%) and citrus (17%); peanuts ploughed annually affecting soil structure.
- Soil parent material: kaolinitic quaternary red clay.
- Climate: subtropical with distinct rainy/dry seasons; average rainfall 1884 mm (1584 mm during measurement period).

## Data inputs and measurements
- Soil data: 5 points per crop type, 4 depths (0.05, 0.2, 0.4, 0.8 m); inputs include bulk density, C, and N.
- Weather data: hourly measurements (temperature, precipitation, humidity, wind) from a single Sunjia station; potential evapotranspiration via Penman-Monteith.
- Soil moisture: measured at 3 locations and depths of 5, 20, 40, 80 cm using a moisture probe.
- All inputs used consistently for both ECOSSE and HYDRUS simulations.

## Hydrology and model structure
- ECOSSE: uses a moisture rate modifier and other drivers (air temperature, soil pH, crop cover) to adjust decomposition.
- HYDRUS: provides a more detailed hydrological representation.
- The moisture dynamics drive soil organic carbon turnover; outputs compared as soil organic carbon (SOC) in kg ha⁻¹.

## Climate data and downscaling for future scenarios
- CMIP5 HadGEM2 simulations used to test sensitivity to hydrological changes.
- Monthly CMIP5 outputs downscaled to daily data to fill gaps; daily RH derived from ET and temperature through fitted relationships.
- Daily ET_corr split into evaporation and transpiration components under assumed proportionality.

## Simulation scope and outputs
- 94-year horizon for soil moisture and SOC simulations using both hydrology approaches.
- Primary output: SOC (kg ha⁻¹) for ECOSSE with original hydrology and HYDRUS hydrology.

## Quality control and data products
- Input files checked for errors.
- Data product: ECOSSE_SOC_2wat.csv containing long-term SOC simulations for both hydrology versions (original ECOSSE hydrology and HYDRUS).

## References
- He, Z., Zhang, M., & Wilson, M. J. (2004). Distribution and classification of red soils in China.
- Smith, J. et al. (2010). Model to Estimate Carbon in Organic Soils—Sequestration and Emissions (ECOSSE).