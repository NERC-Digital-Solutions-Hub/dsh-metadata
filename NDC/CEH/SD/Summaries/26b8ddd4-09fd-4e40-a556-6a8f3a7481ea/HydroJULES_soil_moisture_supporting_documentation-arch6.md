# Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017

## Overview
- A merged soil moisture product for Great Britain combining three datasets:
  - NASA SMAP radiometer (L3, ~9 km)
  - EUMETSAT ASCAT backscatter (12.5 km; converted to volumetric water content)
  - JULES-CHESS land surface model (driven by CHESS-met, 1 km)
- Temporal coverage: 1 April 2015 to 31 December 2017, with daily timestep.
- Spatial resolutions: 12.5 km (primary) and 1 km (resampled) product versions.
- Primary goal: improve temporal variability and reduce random errors by merging model and satellite data.

## Data sources and preparation
- SMAP L3 radiometer soil moisture (9 km, daily)
- ASCAT backscatter soil moisture (12.5 km; converted to volumetric water content using porosity estimates)
- JULES-CHESS model soil moisture (1 km CHESS-met meteorology)
- COSMOS-UK in-situ data used for validation
- Data prepared and merged to create a single, more reliable soil moisture product

## Merging method
- Least-squares merging using triple collocation TC to minimize random errors:
  - SMerged = wX SMX + wY SMY + wZ SMZ
  - SMAP L3 (X) used as the reference (βX = 1)
  - Scaling factors for Y and Z derived from error covariances; rescaled to match X
  - Weights wi computed from product variances to optimally combine the three inputs
- Non-collocated grid merging:
  - When TC significance (p-value) < 0.05 for X–Z and/or Y–Z, TC weighted merging is applied
  - Otherwise, alternative merging schemes (X alone, Y alone, Z alone, arithmetic means) or pixel exclusion are chosen per Table 1
  - A simple arithmetic mean is used in some cases to maximize data coverage, acknowledging potential quality trade-offs
- Outputs:
  - 12.5 km TC-based merged product (primary)
  - 1 km TC-based merged product (derived by resampling inputs to 1 km before merging)
  - 12.5 km CHESS+SMAP+ASCAT mean product (alternative simple average)
- Summary of merging method and per-pixel method decisions provided in weight/method summary file

## Validation and performance
- Evaluation against COSMOS-UK in-situ soil moisture
- Metrics: Pearson correlation coefficient (R) and unbiased RMSD (ubRMSD)
- Findings:
  - Merged product outperforms individual satellite products
  - Merged product has comparable performance to JULES-CHESS with improved temporal variability

## Appropriate use and caveats
- Higher uncertainty in organic soils (peatlands) and urban areas; reliability decreases in these regions
- TC merging may be rejected in certain areas; check the method summary map to know which merging approach was used
- When using the dataset, consider the recommended region-specific merging method (TC vs. alternatives)

## Data products and format
- File formats: NetCDF-4 (CEH gridded dataset conventions)
- Primary files:
  - merge_12.5km_tc_ref_smap.nc (12.5 km, TC-based, full period, volumetric water content)
  - merge_1km_tc_ref_smap.nc (1 km, TC-based, full period, volumetric water content)
  - merge_12.5km_chess_smap_ascat_mean.nc (12.5 km, simple mean of inputs)
  - weights_and_method_summary_12.5km.nc (per-pixel merging method map; 12.5 km)
- Units: m3/m3 (volumetric water content)

## Access, citation, and code
- Data access: Environmental Information Data Centre (EIDC)
  - DOI and dataset page provided in the documentation
  - When using the data, cite: Peng et al. (2021) and the COSMOS-UK validation framework; and the 2022 dataset description
- Code and processing:
  - Full preprocessing, merging, and formatting code available on GitHub: hydro-jules/soil_moisture (private; contact enquirie s@ceh.ac.uk for access)
- Acknowledgements:
  - Funded by UK Natural Environment Research Council (NE/S017380/1)
  - Thanks to NASA SMAP, H SAF ASCAT, and COSMOS-UK collaborators

## Practical use for data support
- Build dashboards and dashboards-like explorations of soil moisture anomalies over GB
- Integrate into drought monitoring, hydrological modelling, or runoff simulations
- Create self-serve data products by exposing the 1 km and 12.5 km merged datasets and method maps
- Compare merged products with COSMOS-UK measurements or CHESS-based simulations for quality checks
- Use the method summary map to tailor analyses to regions where TC merging was applied versus simple averaging or single-product reliance