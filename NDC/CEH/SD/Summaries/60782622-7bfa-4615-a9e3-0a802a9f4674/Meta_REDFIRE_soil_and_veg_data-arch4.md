# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Documentation of soil and vegetation radionuclide activity concentrations and calculated dose rates measured at the Red Forest site in Chernobyl, Ukraine, during 2016–2017.
- Data encompass plot-level measurements across grassy vegetation, other vegetation, and soil, with ambient dose rates and both internal and external weighted dose rates calculated for multiple radionuclides.
- Key isotopes included: Sr-90, Cs-137, Am-241, and Pu isotopes (Pu-238, Pu-239, Pu-240); includes both measured concentrations (dry mass and fresh mass where available) and some predicted concentrations for transfer scenarios.
- Several data elements are provided or implied: sampling dates, biomass mass (FM/DM), DM fractions, soil properties (pH, LOI, %DM), burn history, pine forest history, and plot location.

## Scope and data structure
- Plot-level metadata:
  - Plot_number, Plot_location, Northing, Easting
  - Pine_forest_past_history (whether pine forest was present in the past, before 1986)
  - Plot_burn_score_2016 (0 = no burn, 1 = some burn, 2 = all plot burnt)
- Sampling and sample types:
  - Date_of_vegetation_and_soil_sampling
  - Grassy_vegetation_sample_FM_g, Grassy_vegetation_sample_DM_g, Grassy_vegetation_sample_DM_fraction
  - Other_vegetation_sample_FM_g, Other_vegetation_sample_DM_g
  - Soil measurements: Soil_%_DM_in_March_2017, Soil_%_DM_in_September_2017, Soil_pH_September_2017, Soil_%_LOI_September_2017, Soil_pH/LOI as noted
- Dose and activity data:
  - Ambient_dose_rate_September_2016_µSv_per_h, Ambient_dose_rate_March_2017_µSv_per_h
  - Activity_concentration_Sr90_grassy_vegetation_Bq_per_kg_DM, Activity_concentration_Cs137_grassy_vegetation_Bq_per_kg_DM, etc. for grassy vegetation; similar entries for other vegetation and soil (DM and FM where applicable)
  - Uncertainty fields for key activity concentrations (typically K=1.96)
  - Predicted activity concentrations for Am-241 and Pu isotopes in grassy vegetation and tree wood (using CR_wo-soil parameters)
  - Activity concentrations for Sr-90 and Cs-137 in tree wood and for other isotopes where predicted
- Dose calculations:
  - Weighted_absorbed_internal_dose_rate_…_µGy_per_h for grassy vegetation, tree, bacteria, and multiple isotopes
  - Weighted_absorbed_external_dose_rate_…_µGy_per_h for corresponding components
  - Total_weighted_absorbed_dose_rate_…_µGy_per_h (sums of internal and external components)
  - Total_weighted_absorbed_dose_rate_tree, total for grassy vegetation, Cs-137, Sr-90, Am-241, Pu isotopes, etc., including per-tissue aggregations (bacteria, wood, etc.)
- Data completeness:
  - Not every field has data; n/a indicates data not available
  - Some DM fractions and concentrations were estimated or inferred (e.g., plot 11.3 DM fraction)
  - Some transfer/concentration values for Am-241 and Pu isotopes in grasses and trees are predicted using site-specific transfer parameters from literature

## Data quality, gaps and notes
- Gaps and estimations:
  - Several fields marked n/a (data not available)
  - Some DM fractions and certain activity concentrations are estimated or predicted rather than measured
  Some transfer parameters are derived from external studies (CR_wo-soil) for Agrostis gigantea and Pinus sylvestris, and from CEZ deciduous trees for Sr-90 and Cs-137
- Uncertainty and reporting:
  - Uncertainties are provided for several activity concentrations (K=1.96)
  - Ambient dose rates and weighted dose rates are reported in standard units (µSv/h, µGy/h)
- Data provenance:
  - Ground transfer parameters and methodology referenced to Beresford et al. 2020 and Ukrainian site data (JNPAE 2020)
  - Some values derived using published transfer relationships and soil activity measurements

## Methodology and provenance
- Sampling timeframe:
  - Vegetation and soil sampling occurred in 2016–2017, with ambient dose rates measured in September 2016 and March 2017
- Data processing:
  - Fresh mass (FM) and dry mass (DM) were measured for vegetation samples; DM fraction used to convert concentrations between FM and DM
  - Soil properties (DM, LOI, pH) determined at specified time points
  - Activity concentrations computed for grassy vegetation, tree wood, soil (DM), and, where available, tree and bacterial compartments
  - Internal and external dose rates calculated per isotope and per component; totals computed per plot and per tissue group
- Transfer parameters:
  - Grass (Agrostis gigantea) and tree (Pinus sylvestris) transfer parameters used to estimate Am-241 and Pu isotopes in grassy vegetation and tree wood
  - Sr-90 and Cs-137 transfer parameters for deciduous trees derived from CEZ site data with soil concentrations as inputs

## Implications for Data Leaders
- System-wide perspective:
  - Demonstrates handling of multi-tissue, multi-isotope environmental radiological data with complex dose calculations
  - Highlights importance of metadata (plot history, sampling dates, biomass fractions, soil properties) for data usability
- Data discovery and quality:
  - Multiple data streams (ambient, internal/external dose rates; grassy/other vegetation; soil) require clear provenance and consistent units
  - Gaps and reliance on transfer parameters from literature underscore the need for transparent data quality assessments and documenting assumptions
- Reusability and collaboration:
  - Potential for cross-site comparisons within the CEZ or similar contexts
  - Encourages co-ownership of data products through standardized metadata, clear data gaps, and documentation of modeling assumptions
- Actionable considerations:
  - Priorities may include filling data gaps (e.g., complete concentration measurements for missing isotopes, reducing reliance on predicted values)
  - Use of this dataset to benchmark ecological and radiological transfer models, and to inform risk assessment for vegetation and soil systems in contaminated environments

## References and provenance
- Beresford et al. 2020 (transfer parameters for Agrostis gigantea and Pinus sylvestris)
- JNPAE 2020 (Ukrainian site data for deciduous trees)
- Notes on data interpretation and methodology embedded in the dataset metadata