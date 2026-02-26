# Data access and citation

- This document describes a merged soil moisture dataset for Great Britain, combining satellite (SMAP, ASCAT) and model (JULES-CHESS) data with triple-collocation-based merging to improve reliability and temporal variability.
- Time period covered: 1 April 2015 to 31 December 2017.
- Spatial resolutions: 12.5 km (original) and 1 km (high-resolution, resampled from underlying datasets).
- Primary aim: provide a more reliable soil moisture product by leveraging multiple data sources and minimizing random errors.

## What the dataset contains

- Merged soil moisture products at two resolutions:
  - 12.5 km: merge_12.5km_tc_ref_smap.nc (NetCDF4, volumetric water content, single file for the whole period)
  - 1 km: merge_1km_tc_ref_smap.nc (NetCDF4, volumetric water content, single file for the whole period)
- Additional products:
  - merge_12.5km_chess_smap_ascat_mean.nc: alternative mean-merged product (12.5 km only)
  - weights_and_method_summary_12.5km.nc: map of merging methods used per pixel (12.5 km)
- Figures referenced in the method description (e.g., merging method map, TC applicability) are summarized in the provided tables and figures within the dataset documentation.

## Data sources

- SMAP L3 radiometer soil moisture dataset (NASA), 9 km daily resolution
- ASCAT soil moisture data (EUMETSAT H SAF), 12.5 km sampling version
- JULES-CHESS soil moisture output, driven by CHESS-met meteorology (1 km resolution over the UK)
- COSMOS-UK in-situ soil moisture network for validation
- Additional inputs for conversion and porosity estimation:
  - Harmonized World Soil Database (HWSD)
  - Pedotransfer relationships to estimate porosity
- The dataset evaluation references Peng et al. (2021) for methodology and validation details

## Method for deriving the merged dataset

- Merging approach: least-squares merging of SMAP, ASCAT, and JULES-CHESS to minimize random errors.
- Core concept: Triple Collocation (TC) used to estimate relative error variances and derive rescaling factors for compatibility across products.
- Process details:
  - Set SMAP L3 as the reference product (X); compute scaling factors for Y (ASCAT) and Z (JULES-CHESS) using TC-derived relations.
  - Apply rescaling: Y_r escaled = β_Y * (Y - mean(Y)) + mean(X); Z_r escaled = β_Z * (Z - mean(Z)) + mean(X).
  - Compute merging weights (w_X, w_Y, w_Z) based on error variances and covariances; weights favor lower-variance products.
  - For collocated triplets, use TC-based weights; for non-collocated samples, apply a Gruber et al. (2017) based approach using one-tailed Pearson significance to determine merging method.
  - When only two datasets are available, use least-squares-based weights and a weighted average.
- Handling of data gaps:
  - If TC merging is rejected in a region, alternative schemes (e.g., X, Y, Z means or arithmetic means) are used per Table 1 in the documentation to maximize data coverage.
- 12.5 km workflow: resample SMAP L3 and JULES-CHESS to 12.5 km, then merge with ASCAT.
- 1 km workflow: resample SMAP L3 and ASCAT to 1 km, then merge (with CHESS integrated as available).

## Validation and performance

- Validation against COSMOS-UK in-situ measurements using:
  - Pearson correlation coefficient (R)
  - Unbiased root-mean-square difference (ubRMSD)
- Key findings:
  - The merged product generally outperforms each individual satellite product.
  - The merged product achieves performance similar to JULES-CHESS but with improved temporal variability, reducing the limited temporal dynamics of the model alone.
  - The evaluation includes comparisons depicted in figures showing absolute soil moisture values and time series at COSMOS-UK stations.

## Appropriate use and caveats

- Reliability varies by land type:
  - Soils with high organic content (e.g., peatlands) and urban areas tend to be less reliable; consider these limitations when applying the dataset to such regions.
- Regions where triple collocation was not applicable (TC not applied) may have less reliable estimates; users should consult the merging method summary grid for their area of interest.
- Higher data coverage and temporal variability are beneficial for drought monitoring and runoff simulations, even when some regional data quality is lower.

## Access, use, and reproducibility

- Data access and citation:
  - Data available from the Environmental Information Data Centre (EIDC) with the DOI: https://doi.org/10.5285/26b8ddd409fd-4e40-a556-6a8f3a7481ea
  - Required citation: Tanguy et al. (2022) Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017. NERC EDS Environmental Information Data Centre.
  - Additional methodological reference: Peng et al. (2021) Estimation and evaluation of high-resolution soil moisture from merged model and Earth observation data in Great Britain, Remote Sensing of the Environment.
- GitHub repository:
  - Full preprocessing, merging, and formatting code with documentation is available at https://github.com/hydro-jules/soil_moisture (currently private; request access via enquiries@ceh.ac.uk)
- Data format:
  - NetCDF-4 format following CEH gridded dataset conventions
  - Files include 12.5 km and 1 km merged products, an alternative mean-merged product, and a method summary grid

## Acknowledgements and references

- Funded by the UK Natural Environment Research Council (NE/S017380/1)
- Acknowledges NASA SMAP, ESA H SAF ASCAT, COSMOS-UK, and UKCEH CHESS datasets
- References include key methodological and validation sources:
  - Gruber et al. on triple-collocation merging
  - Gruber et al. on merging methodology evolution
  - Ongoing foundational works on TC-based soil moisture merging and related datasets