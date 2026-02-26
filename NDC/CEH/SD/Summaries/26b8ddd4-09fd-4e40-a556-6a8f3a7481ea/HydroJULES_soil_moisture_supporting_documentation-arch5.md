# Data access and citation

- Data availability
  - Environmental Information Data Centre (EIDC) hosting: https://doi.org/10.5285/26b8ddd409fd-4e40-a556-6a8f3a7481ea
  - Time period and resolution: 1 April 2015 – 31 December 2017; daily timestep; two spatial resolutions (12.5 km and 1 km)
  - Data products included:
    - Merged soil moisture dataset (TC-based): merge_12.5km_tc_ref_smap.nc and merge_1km_tc_ref_smap.nc
    - Alternative merged dataset (arithmetic mean of three products): merge_12.5km_chess_smap_ascat_mean.nc
    - Weights and method summary: weights_and_method_summary_12.5km.nc
  - Data sources used to derive the merged product:
    - NASA SMAP radiometer L3 soil moisture (9 km, daily)
    - EUMETSAT ASCAT backscatter-derived soil moisture (12.5 km)
    - JULES-CHESS soil moisture (UK CHESS-met driven, 1 km)
    - COSMOS-UK in-situ soil moisture for evaluation (ground truth)
  - Data format: NetCDF4 following CEH gridded dataset conventions
  - Access to code: GitHub repository https://github.com/hydro-jules/soil_moisture (currently private; request access via enquiries@ceh.ac.uk)

- Citations and acknowledgment
  - Primary dataset citation: Tanguy, M.; Peng, J.; Robinson, E.; Pinnington, E.; Evans, J.; Ellis, R.; Cooper, E.; Hannaford, J.; Blyth, E.; Dadson, S. (2022). Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/26b8ddd4-09fd-4e40-a556-6a8f3a7481ea
  - Equal contribution note for authors
  - Methodology and evaluation papers to cite:
    - Peng, J.; Tanguy, M.; Robinson, E.; Pinnington, E.; Evans, J.; Ellis, R.; Cooper, E.; Hannaford, J.; Blyth, E.; Dadson, S. (2021). Estimation and evaluation of high-resolution soil moisture from merged model and Earth observation data in the Great Britain. Remote Sensing of the Environment, 264, 112610. https://doi.org/10.1016/j.rse.2021.112610
    - Related triple collocation and merging methodology papers (Gruber et al., 2016–2019)
  - Acknowledgments: UK NE/NERC support; NASA SMAP; H SAF ASCAT; UKCEH COSMOS-UK dataset and CHESS soil moisture

- Data governance and stewardship notes
  - The merged dataset provides transparency on provenance and methodology (TC-based merging, rescaling, and weighting) and includes a method summary grid per pixel
  - A dedicated GitHub repository contains pre-processing and merging workflow, with full documentation; access is restricted to HydroJULES program members
  - Data users should consult the merging method map and notes to assess which merging approach was applied in their area of interest

- Use, quality, and caveats
  - Validation and performance
    - Evaluation against COSMOS-UK in-situ observations shows the merged product generally outperforms individual satellite products and matches JULES-CHESS in overall performance, with improved temporal variability
    - Metrics used: Pearson correlation (R) and unbiased RMS difference (ubRMSD)
  - Appropriate use considerations
    - Soil moisture over peatlands and other high organic content areas is more uncertain; caution advised
    - Urban areas can be less reliable; TC-based merging may be rejected in some cities (check the method summary grid)
  - Data reliability indicators
    - The dataset includes a per-pixel map (Figure 3-like) showing which merging scheme was used (TC weighted, SMAP-only, CHESS-only, ASCAT-only, or various arithmetic means)
    - If TC merging is rejected and only two datasets are available, a least-squares weighted average is used; when three datasets are available, TC-based merging is preferred
  - Format and access considerations
    - Primary dataset files are single NetCDF files covering the whole period for each resolution
    - An alternative simple mean product is available only at 12.5 km
    - The full processing code is currently private; request access for reproducibility and governance auditing

- How to cite and reference
  - Use the dataset citation above for data usage
  - Also cite Peng et al. (2021) for the methodology underpinning the merging approach
  - Include data source acknowledgments (SMAP, ASCAT, COSMOS-UK) as appropriate in dissemination material

- File structure at a glance
  - merge_12.5km_tc_ref_smap.nc: 12.5 km, TC-merged product (April 2015–Dec 2017)
  - merge_1km_tc_ref_smap.nc: 1 km, TC-merged product (April 2015–Dec 2017)
  - merge_12.5km_chess_smap_ascat_mean.nc: 12.5 km arithmetic mean merged product
  - weights_and_method_summary_12.5km.nc: per-pixel merging method map
  - Figure 3: map illustrating merging method per pixel (TC vs. single-source vs. averages)

- End-user guidance
  - Review per-pixel merging method summary before applying data to ensure expectations about temporal coverage and method robustness
  - Consider regional caveats (peatlands, urban areas) in analysis and interpretation
  - When reproducibility is required, request access to the GitHub code and accompanying documentation

- References (for governance and provenance)
  - Cooper et al. (2021) COSMOS-UK: national soil moisture and hydrometeorology data for environmental science research
  - Gruber et al. (2016, 2017, 2019) on triple collocation and merging approaches
  - O’Neill et al. (2019) SMAP L3 Radiometer dataset
  - H SAF (2020) ASCAT soil moisture data
  - Wieder et al. (2014) Harmonized World Soil Database and pedotransfer functions
  - Toth et al. (2015) European soil hydraulic parameters
  - Robinson et al. (2017) CHESS-met meteorology for UK