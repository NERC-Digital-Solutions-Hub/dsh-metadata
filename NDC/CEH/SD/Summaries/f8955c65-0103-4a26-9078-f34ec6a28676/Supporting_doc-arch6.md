# Supporting documentation

## Objective
- Isolate the effect of hydrology within a typical pool-based soil carbon model by comparing two versions of the same model.
- Use ECOSSE with its original piston flow hydrology and HYDRUS (more detailed hydrology) to simulate soil carbon turnover in the Sunjia catchment for 15 months (Oct 2012–Dec 2013) and evaluate accuracy against soil water measurements.

## Site and data context
- Sunjia catchment (Sunjia CZO), Jiangxi Province, southeast China; 50 ha, elevation 41–55 m.
- Crops: peanuts (50% of area, shallow roots) and citrus trees (17%, deeper roots, perennial).
- Soil: kaolinitic quaternary red clay.
- Climate: subtropical with distinct rainy/dry seasons; average annual rainfall ~1884 mm (1584 mm during measurement period).
- Measurements: soil moisture at 3 locations, 4 depths (0.05, 0.2, 0.4, 0.8 m); soils sampled for bulk density, C, N; weather data from a single station; ET via Penman-Monteith; moisture probes at 5, 20, 40, 80 cm.

## Data inputs and preparation
- Inputs for both model versions include soil moisture, soil properties (bulk density, C, N), and weather conditions.
- Crop cover treated as having no influence in the baseline setup.
- CMIP5 climate projections (HadGEM2) used to test sensitivity to hydrological changes; outputs downscaled to daily data for compatibility with daily model requirements.
- Relative humidity for HYDRUS derived through a regression-based approach due to missing RH data in CMIP5 outputs.

## Hydrology modeling and data synthesis
- Two hydrology approaches evaluated:
  - ECOSSE original hydrology (piston flow)
  - HYDRUS (more detailed, moisture-driven hydrology)
- Daily time series created by downscaling CMIP5 monthly data to daily; daily ET estimates linked to temperature with linear relationships; monthly ET differences used to correct daily ET to preserve CMIP5 monthly water balance.
- Daily RH derived from corrected ET to drive HYDRUS simulations.
- simulations extended to a 94-year period to assess long-term soil moisture dynamics using both hydrology versions.

## Outputs and quality control
- Primary output: soil organic carbon (SOC) in kg ha^-1 for both hydrology versions.
- File: ECOSSE_SOC_2wat.csv containing long-term SOC simulations under both hydrology configurations.
- Quality control: input files checked for errors; references to data sources and model descriptions included.

## Challenges and data-use considerations
- Patchy or limited in-site data necessitated data reconstruction (e.g., RH and daily ET) for HYDRUS runs.
- Downscaling from CMIP5 introduced assumptions; daily data required interpolation and fitting procedures.
- Need to be mindful of how hydrology choice influences SOC predictions and model behavior.

## Implications for data support and reuse
- Demonstrates how data integration (field measurements, climate projections, and model inputs) enables comparative model evaluation.
- Provides a replicable data pipeline for assessing hydrological impact on soil carbon turnover.
- Outputs (SOC time series) can be used for further analyses, comparisons, or policy-relevant insights, and support sharing and reuse of model-derived data products.

## References
- He, Z., Zhang, M., & Wilson, M. J. (2004). Distribution and classification of red soils in China. In The Red Soils of China (pp. 29–33). Springer.
- Smith, J., Gottschalk, P., Bellarby, J., Richards, M., Nayak, D., Coleman, K., ... & Yeluripurti, J. (2010). Model to Estimate Carbon in Organic Soils—Sequestration and Emissions (ECOSSE). Carbon, 44, 1–73.