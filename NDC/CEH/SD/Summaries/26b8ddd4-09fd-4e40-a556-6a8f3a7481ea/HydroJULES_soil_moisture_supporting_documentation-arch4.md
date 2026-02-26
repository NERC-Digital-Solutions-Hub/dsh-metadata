# Soil moisture product merged from satellite and modelled data for Great Britain, April 2015-December 2017

- Purpose: A merged soil moisture dataset for Great Britain covering 1 April 2015 to 31 December 2017, produced by combining satellite observations (SMAP and ASCAT) with a land-surface model (JULES-CHESS) to reduce random errors and improve temporal variability.

- Temporal and spatial coverage:
  - Daily soil moisture values.
  - Resolutions: 12.5 km (original grid) and 1 km (high-resolution, via resampling).

- Data products and files:
  - merge_12.5km_tc_ref_smap.nc: 12.5 km, triple-collocation weighted merge (SMAP as reference).
  - merge_1km_tc_ref_smap.nc: 1 km, triple-collocation weighted merge.
  - merge_12.5km_chess_smap_ascat_mean.nc: 12.5 km, simple mean of the three datasets (alternative).
  - weights_and_method_summary_12.5km.nc: per-pixel merging method summary (Figure 3).
- Units and format:
  - NetCDF4, CEH gridded dataset conventions.
  - Units: volumetric water content (m3/m3).

- Data sources and conversions:
  - SMAP L3 radiometer soil moisture (9 km, daily).
  - ASCAT backscatter soil moisture (12.5 km); converted to volumetric water content using porosity derived from HWSD and a pedotransfer function.
  - JULES-CHESS soil moisture (UK CHESS-met meteorology, 1 km).
  - COSMOS-UK in-situ soil moisture for validation.

- Merging methodology:
  - Triple Collocation (TC) to estimate random errors and derive rescaling factors.
  - Least-squares merging: SMmerged = wX SMX + wY SMY + wZ SMZ, with weights computed from error variances/covariances.
  - Reference product: SMAP L3 (X); Y and Z are rescaled before merging.
  - Non-collocated merging: procedure based on Gruber et al. (2017, 2019) with decision rules (Table 1) when TC is rejected; otherwise TC-based weighted mean.
  - For two datasets, weights derived from uncertainties and a weighted average is used.
  - 12.5 km workflow: resample SMAP L3 and JULES-CHESS to 12.5 km, merge with ASCAT; 1 km workflow: resample all to 1 km, merge.

- Validation and performance:
  - Validation against COSMOS-UK in-situ measurements using Pearson correlation (R) and unbiased RMSD (ubRMSD).
  - Overall finding: the merged product offers better performance than any single satellite product and is comparable to JULES-CHESS, with improved temporal variability.

- Appropriate use and caveats:
  - More uncertain over peatlands and other high organic matter areas; avoid over-interpreting in these zones.
  - Urban areas tend to be less reliable; check Fig. 3 merging method map to see which approach was used in a given area.
  - TC merging may be rejected in some locations; use the method summary grid to assess per-pixel merging approach.
  - The dataset is suitable for applications needing higher temporal coverage (e.g., drought monitoring, hydrological modeling).

- Access, citation, and governance:
  - Data access: Environmental Information Data Centre (EIDC) with DOIs provided in the data record.
  - Primary citation: Tanguy et al. (2022) for the soil moisture dataset; methodology described in Peng et al. (2021).
  - Usage note: Please cite the dataset and associated methodology articles when using the data.
  - Code and reproducibility: Full preprocessing and merging code available in a private GitHub repository (https://github.com/hydro-jules/soil_moisture); access upon request by emailing enquiries@ceh.ac.uk.
  - Acknowledgments: UK Natural Environment Research Council (NE/S017380/1); NASA SMAP; EUMETSAT H SAF ASCAT; COSMOS-UK; CHESS.

- Governance and contact:
  - Data produced under CEH/NERC auspices; data providers include NASA, EUMETSAT, and COSMOS-UK collaborators.
  - For access to the code, contact CEH; for data access, use the EIDC links and citation guidance provided.