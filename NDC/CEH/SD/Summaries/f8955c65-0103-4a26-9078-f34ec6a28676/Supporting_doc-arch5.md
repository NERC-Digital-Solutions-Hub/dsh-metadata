# Supporting documentation

## Overview
- Compares two hydrology approaches within a single soil carbon turnover model to isolate the effect of hydrology: the original piston-flow ECOSSE hydrology and a more detailed HYDRUS hydrology.
- 15-month simulation (October 2012 to end of December 2013) for the Sunjia catchment in southeast China to evaluate accuracy of the two approaches against soil water measurements.
- Uses Sunjia CZO data to drive simulations; Sunjia CZO characteristics: 50 ha area, crops include peanuts (annual, shallow roots) and citrus (perennial, deeper roots), kaolinitic red clay, subtropical climate with distinct rainy/dry seasons.

## Data inputs and sources
- Site and crop data: crop types, rooting characteristics, soil parent material, and land cover (peanuts 50%, citrus 17%).
- Soil data: collected at 5 points per crop type across four depths (0.05, 0.2, 0.4, 0.8 m); measurements include bulk density, carbon content, and nitrogen content.
- Weather/meteorological data: hourly measurements from a single Sunjia weather station (temperature, precipitation, humidity, wind speed); potential evapotranspiration computed via Penman-Monteith.
- Soil moisture: measured at three locations and four depths (5, 20, 40, 80 cm) with moisture probes.
- Model inputs common to both hydrology methods include soil moisture, air temperature, soil pH, and crop cover (crop cover generally not influential in the base ECOSSE setup).

## Climate and downscaling
- CMIP5 climate scenarios (HadGEM2) used to assess sensitivity to hydrological changes; outputs provided monthly and downscaled to daily data for simulations.
- Relative humidity values required by HYDRUS were not available from CMIP5; daily RH was derived using simple relationships with daily evapotranspiration and fitted coefficients.
- Daily potential evapotranspiration ETd_corr is derived by combining daily ET with CMIP5 monthly water balance adjustments and splitting ETd_corr into evaporation and transpiration components according to monthly contributions.
- Daily RH is then calculated from ETd_corr using a fitted RH model.

## Processing and modeling
- Two parallel model setups:
  - ECOSSE with its original hydrology.
  - ECOSSE with HYDRUS-based hydrology.
- Long-term simulations cover a 94-year period using daily climate inputs derived from downscaled CMIP5 data; short-term validation against observed soil moisture and water data from 2012–2013.
- Key calculation steps include:
  - Moisture-driven adjustments to base decomposition rates (moisture rate modifiers).
  - Inputs from measured soil properties, weather, crop data, and soil moisture to drive carbon turnover in soil pools.
  - Daily partitioning of ET into evaporation and transpiration using the derived ETd_corr.
- Outputs include soil organic carbon (SOC) in kg ha^-1 for both hydrology implementations.

## Quality control and file assets
- Input files checked for errors prior to simulations.
- Primary output: ECOSSE_SOC_2wat.csv, consisting of long-term SOC simulations under the two hydrology configurations.
- Documentation references provided for model components (ECOSSE, related soil carbon modeling, and the 2010 Smith et al. moisture modifier methodology).

## Data provenance, assumptions, and limitations
- Provenance: measurements and inputs drawn from Sunjia CZO site data (soil properties, moisture, weather) and CMIP5 HadGEM2 climate projections.
- Assumptions:
  - Daily RH and ET can be reliably reconstructed from monthly CMIP5 outputs via simple interpolation and fitted relationships.
  - The two hydrology models (ECOSSE original vs HYDRUS) are appropriate contrast points for assessing hydrological impact on soil carbon.
- Limitations:
  - Downscaling and interpolation introduce uncertainties (daily values derived from monthly inputs).
  - RH estimation relies on fitted coefficients; potential propagation of errors into moisture and SOC estimates.
  - Cropping system specifics (peanuts vs citrus) and seasonal ploughing are embedded inputs and may influence generalizability.

## Reproducibility and governance considerations for data stewards
- Metadata and provenance should capture:
  - Site details (location, area, soil type, crops, management practices).
  - Depths and locations for soil moisture and soil property measurements.
  - Data sources (in-situ measurements, CMIP5 HadGEM2, downscaling method).
  - Processing steps (MOISTURE modifiers, ET and RH derivations, daily aggregation, and SOC computation).
  - Model versions (ECOSSE original vs HYDRUS) and any parameter settings or calibration notes.
- Data formats and access:
  - Primary dataset file name: ECOSSE_SOC_2wat.csv.
  - Clear versioning and lineage are important for reproducibility (specify model version, input data versions, and processing scripts if available).
- Data quality and stewardship actions:
  - Maintain thorough metadata for inputs (soil depths, crop types, measurement stations, weather station specifics).
  - Document data transformations (downscaling equations, ETd_corr split, RH estimation) and any assumptions.
  - Ensure traceability from observed measurements through modeled outputs to support data discovery and reuse.