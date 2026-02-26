# Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017

## Overview
- A merged soil moisture dataset for the Great Britain mainland, spanning 1 April 2015 to 31 December 2017, at daily resolution.
- Uses a triple-collocation-based merging approach to combine three data sources and produce a single, more reliable soil moisture product.
- Available at two spatial resolutions: 12.5 km (original) and 1 km (resampled) with NetCDF4 format following CEH conventions.
- Intended as a tool for environmental monitoring, drought assessment, and hydrological applications, with emphasis on data quality, transparency, and governance.

## Data access and citation
- Data hosted by Environmental Information Data Centre (EIDC). DOI and access details provided in the dataset record.
- Please cite:
  - Tanguy, M., Peng, J., Robinson, E., et al. (2022). Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/26b8ddd4-09fd-4e40-a556-6a8f3a7481ea
- Methodology reference:
  - Peng, J., Tanguy, M., Robinson, E., et al. (2021). Estimation and evaluation of high-resolution soil moisture from merged model and Earth observation data in the Great Britain. Remote Sensing of the Environment, 264, 112610. https://doi.org/10.1016/j.rse.2021.112610
- Code and workflow:
  - Full pre-processing and merging code available in the Hydro-JULES GitHub repository (private; contact enquiries@ceh.ac.uk for access).

## Data sources and inputs
- SMAP L3 soil moisture (9 km, passive microwave) from NASA.
- ASCAT backscatter-derived soil moisture (12.5 km) from EUMETSAT H SAF; converted to volumetric water content using porosity estimates from HWSD and pedotransfer functions.
- JULES-CHESS soil moisture from a land-surface model driven by CHESS-met meteorology (1 km).
- Validation data from COSMOS-UK network for independent ground-truth comparison.

## Merging methodology
- Core approach: least-squares merging of three products (SMAP, ASCAT, JULES-CHESS) with triple-collocation (TC) to estimate and align random errors.
- Reference product: SMAP used as the primary reference in rescaling and weighting.
- Weight calculation: weights for X, Y, Z derived from error variances and covariances; TC yields scaling factors for cross-product alignment.
- For collocated data: standard TC-based weighted merge.
- For non-collocated data: merging uses a scheme based on one-tailed Pearson significance; if p<0.05, TC-based weighted merging is applied; otherwise alternative schemes (e.g., arithmetic mean of available products) are used to maximize data coverage.
- When only two datasets are available, a weighted average based on uncertainties is used.
- Outputs include a 12.5 km TC-merged product, a 1 km TC-merged product, and a 12.5 km simple average product (SMAP, CHESS, ASCAT) for comparison.

## Data products and formats
- merge_12.5km_tc_ref_smap.nc: 12.5 km TC-merged soil moisture (m3/m3), 2015-04-01 to 2017-12-31.
- merge_1km_tc_ref_smap.nc: 1 km TC-merged soil moisture (m3/m3), same period.
- merge_12.5km_chess_smap_ascat_mean.nc: 12.5 km simple mean of the three datasets (not TC-weighted).
- weights_and_method_summary_12.5km.nc: Map of the merging method used per pixel (Figure 3), with categories indicating TC, single-product, or arithmetic-mean merges.
- Notes: All datasets stored in NetCDF4 format following CEH conventions; units are volumetric water content (m3/m3).

## Validation and performance
- Validation against COSMOS-UK in-situ measurements using Pearson correlation (R) and unbiased RMSE (ubRMSD).
- Overall findings: the TC-merged product outperforms individual satellite products, performs comparably to JULES-CHESS, and shows improved temporal variability compared with model-only outputs.
- Caveats from validation:
  - Soil moisture over organic-rich soils (e.g., peatlands) and urban areas tends to be less reliable; check the method summary grid to understand the merging approach in a given area.
  - TC merging was not always applied in some urban/heterogeneous regions, affecting reliability there.

## Use guidelines and caveats
- The dataset is designed for monitoring and modeling support, but users should be cautious in peatlands and urban areas where data quality and merging confidence are lower.
- Always consult the method summary grid (Figure 3) to determine the merging approach applied in the user’s region of interest.
- The dataset emphasizes data transparency, with underlying data sources, processing steps, and validation documented; however, data governance and access constraints apply (code repository is private).

## Acknowledgements
- Funded by the UK Natural Environment Research Council (NE/S017380/1).
- Acknowledges NASA for SMAP data, EUMETSAT H SAF for ASCAT, and UKCEH COSMOS-UK dataset and CHESS soil moisture data.

## Practical notes for monitoring framework authors
- This dataset demonstrates a governance-conscious workflow: multi-source data integration, error characterization via triple collocation, transparent weighting, and clear documentation of data provenance and limitations.
- Provides a model for data access, citation, and reproducibility, including a public-facing data record and a private codebase with controlled access.
- Useful as a case study of balancing data coverage and quality to deliver timely environmental indicators for policy evaluation and decision-making.