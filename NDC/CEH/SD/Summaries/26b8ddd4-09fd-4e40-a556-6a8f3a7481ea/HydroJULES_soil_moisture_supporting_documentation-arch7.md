# Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017

## Data access and citation
- Data available from Environmental Information Data Centre (EIDC): https://doi.org/10.5285/26b8ddd409fd-4e40-a556-6a8f3a7481ea
- Must cite: Tanguy et al. (2022) Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/26b8ddd4-09fd-4e40-a556-6a8f3a7481ea
- Equal contribution note for authors.
- A detailed methodology description is available in Peng et al. (2021): Estimation and evaluation of high-resolution soil moisture from merged model and Earth observation data in the Great Britain. Remote Sensing of the Environment. https://doi.org/10.1016/j.rse.2021.112610

## Brief description
- Three input soil moisture products merged into a single, more reliable product:
  - SMAP radiometer (9 km)
  - ASCAT active microwave (12.5 km; converted to volumetric water content)
  - JULES-CHESS land surface model
- Merging uses triple collocation error estimation and a least-squares scheme to minimize random errors.
- Coverage: 1 April 2015 to 31 December 2017, daily timestep.
- Resolutions: 12.5 km and 1 km (1 km achieved by resampling inputs).
- Validation with COSMOS-UK in-situ data shows the merged product improves temporal variability and performs comparably to JULES-CHESS while leveraging satellite observations.

## Data sources
- SMAP L3 soil moisture (9 km, daily)
- ASCAT soil moisture (12.5 km; units converted from degree of saturation to volumetric water content using HWSD porosity estimates)
- JULES-CHESS soil moisture (driven by CHESS-met, 1 km)
- COSMOS-UK network observations for validation

## Merging methodology
- Core approach: weighted least-squares merging of SMAP (X), ASCAT (Y), and JULES-CHESS (Z)
- Reference dataset: SMAP L3 (X)
- Relative rescaling factors (β) derived via Triple Collocation to align variability across products
- Collocated samples: compute weights using error variances/covariances; TC-based merging applied when p-value < 0.05
- Non-collocated samples: use Gruber et al. (2017) approach with one-tailed Pearson significance; fall back to alternative schemes (X, Y, Z combinations) per Table 1
- For two datasets: derive least-squares weights and apply a weighted average
- Spatial treatment:
  - 12.5 km: resample X and Z to 12.5 km; merge with ASCAT
  - 1 km: resample SMAP L3 and ASCAT to 1 km
- Output options include a TC-weighted merge and a simple mean merge for comparison

## Validation
- Evaluation against COSMOS-UK in-situ soil moisture (Pearson correlation R and unbiased RMSD ubRMSD)
- Findings: merged product outperforms individual satellite products; comparable to JULES-CHESS with improved temporal variability

## Dataset formats and files
- NetCDF4 format following CEH gridded dataset conventions
- Files (whole-period single files):
  - merge_12.5km_tc_ref_smap.nc (12.5 km, TC merged; volumetric water content in m3/m3)
  - merge_1km_tc_ref_smap.nc (1 km, TC merged; volumetric water content in m3/m3)
  - merge_12.5km_chess_smap_ascat_mean.nc (12.5 km, simple arithmetic mean of inputs; for comparison only)
  - weights_and_method_summary_12.5km.nc (map of merging method used per pixel; 12.5 km only)
- Figure 3 (merging method map) details methods used per pixel (0 = TC, 1 = SMAP only, 2 = CHESS only, 3 = ASCAT only, 4–6 = various arithmetic means)
- Notes: TC was not applied in several urban areas due to low cross-product agreement

## Appropriate use and caveats
- Peatlands and other areas with high organic matter: higher uncertainty; use with caution
- Urban areas: lower reliability; TC applicability may vary by location
- Check the merging method summary grid for local merging approach (TC vs. alternatives)
- The TC-based product provides higher sample density; in some areas, a simple mean may be used where TC is rejected

## Access to code and reproducibility
- Full preprocessing and merging pipeline available in a GitHub repository: https://github.com/hydro-jules/soil_moisture
- Repository currently private; contact enquiries@ceh.ac.uk for access

## Additional acknowledgements and references
- Funded by UK Natural Environment Research Council (NE/S017380/1)
- Acknowledges NASA SMAP, EUMETSAT H SAF ASCAT, and COSMOS-UK datasets
- Key references: Peng et al. (2021); Gruber et al. (2016, 2017, 2019); Gruber et al. (2017) on triple collocation merging; Cooper et al. (2021) COSMOS-UK; CHESS-met data (Robinson et al., 2017)