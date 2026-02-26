# Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017

## Overview
- A merged soil moisture dataset for Great Britain combining satellite observations and model output to improve reliability and temporal variability.
- Time period: 1 April 2015 to 31 December 2017; daily timestep.
- Spatial resolutions: 12.5 km and 1 km.
- Data formats: NetCDF4 following CEH gridded dataset conventions.

## Data sources and inputs
- SMAP L3 radiometer soil moisture (9 km, daily) used as the reference in the merging.
- ASCAT active microwave soil moisture (12.5 km), converted from degree of saturation to volumetric water content using porosity estimates from HWSD and a pedotransfer function.
- JULES-CHESS soil moisture from the CHESS-met driven UK meteorology dataset (1 km resolution).
- COSMOS-UK soil moisture network for validation.

## Merging methodology
- Approach: least-squares merging with Triple Collocation (TC) to minimise random errors across three products (SMAP, ASCAT, JULES-CHESS).
- Process:
  - TC provides error variances and covariances to compute weights for each product.
  - SMAP L3 is treated as the reference (weight set to 1).
  - Non-collocated data merged using a scheme from Gruber et al. (2017), with TC-based weighted merging applied when TC p-values < 0.05.
  - If TC is not applicable, alternative schemes include selecting a single product or arithmetic means between two products.
- Outputs:
  - 12.5 km TC-based merged product (merge_12.5km_tc_ref_smap.nc).
  - 1 km TC-based merged product (merge_1km_tc_ref_smap.nc).
  - 12.5 km mean of SMAP, CHESS, ASCAT as a simple average (merge_12.5km_chess_smap_ascat_mean.nc).
  - Weights and method summary (weights_and_method_summary_12.5km.nc) including the method used per pixel (TC or other scheme).

## Data products and access
- Merged datasets are stored as NetCDF4 files:
  - merge_12.5km_tc_ref_smap.nc (12.5 km, TC merged, daily, volumetric water content in m3/m3)
  - merge_1km_tc_ref_smap.nc (1 km, TC merged, daily, volumetric water content)
  - merge_12.5km_chess_smap_ascat_mean.nc (12.5 km simple average, daily, volumetric water content)
  - weights_and_method_summary_12.5km.nc (per-pixel merging method map)
- Data is available from the Environmental Information Data Centre (EIDC) with DOI provided in the data access section.
- Citations:
  - Primary dataset citation (Tanguy et al., 2022) and methodology paper (Peng et al., 2021).
- GitHub repository (hydro-jules/soil_moisture) contains preprocessing, merging, and formatting code; currently private; request access via enquiries@ceh.ac.uk.

## Validation and performance
- Validation against COSMOS-UK in-situ observations used Pearson correlation (R) and unbiased RMSE (ubRMSD).
- Results:
  - The TC-based merged product generally outperforms individual satellite products and is comparable to JULES-CHESS, with improved temporal variability.
  - The merged product offers better representation of soil moisture dynamics than any single input dataset.

## Use and limitations
- Appropriate use:
  - Useful for drought monitoring, runoff modelling, and environmental monitoring at national scale.
- Limitations and cautions:
  - Less reliable over peatlands and other organic-rich soils; caution when interpreting values in organic soils.
  - Urban areas also tend to be less reliable; TC may be rejected in major cities (reliability map available per pixel).
  - Users should consult the merging method summary grid to understand which merging approach was used for their area of interest.

## Format and conventions
- NetCDF4 files following CEH gridded dataset conventions.
- Units: volumetric water content (m3/m3).

## Acknowledgements and further information
- Supported by NERC (NE/S017380/1).
- Acknowledges SMAP and ASCAT data producers and COSMOS-UK collaboration.
- Detailed methodology and evaluation are described in Peng et al. (2021); primary dataset description in Tanguy et al. (2022).
- For access to code or data copies, contact the provided enquiries email.