# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Dataset of soil and vegetation radionuclide activity concentrations and calculated dose rates at the Red Forest site, Chernobyl (2016–2017).
- Plot- and coordinate-level data enabling map-based visualization of radiological contamination and dose rates.
- Includes ambient dose rates, sampling dates, vegetation and soil mass measurements, and derived dose-rate calculations for multiple isotopes and media.

## Spatial and Temporal Coverage
- Spatial: Plot-level data with plot coordinates (Northing, Easting) and location descriptors.
- Temporal: Ambient dose rates measured in September 2016 and March 2017; vegetation/soil sampling date; notes on historical pine forest cover (past and present).

## Key Variables and Data Categories
- Plot and location data
  - Plot_number, Plot_location, Northing, Easting
  - Plot_pine_forest_past_history (current vs past pine forest status)
  - Plot_burn_score_2016 (0–3 scale for burn extent)

- Ambient dose rates
  - Ambient_dose_rate_September_2016_µSv_per_h
  - Ambient_dose_rate_March_2017_µSv_per_h

- Sampling and physical measurements
  - Date_of_vegetation_and_soil_sampling (DD:MM:YY)
  - Grassy_vegetation_sample_FM_g, Grassy_vegetation_sample_DM_g, Grassy_vegetation_sample_DM_fraction
  - Other_vegetation_sample_FM_g, Other_vegetation_sample_DM_g
  - Soil_%_DM_in_March_2017, Soil_%_DM_in_September_2017
  - Soil_pH_September_2017
  - Soil_%_LOI_September_2017

- Isotope activity concentrations (grassy vegetation, tree wood, soil)
  - Grassy vegetation: Sr-90, Cs-137 (DM and FM where available), with associated uncertainties
  - Deciduous tree wood: Sr-90, Cs-137, Am-241, Pu-238/239/240 (FM)
  - Soil: Sr-90, Cs-137, Am-241, Pu-238/239/240 (DM)
  - Includes both measured concentrations (DM, FM) and where applicable, predicted concentrations (noted as such)

- Derived dose and transfer metrics
  - Weighted_absorbed_internal_dose_rate_[isotope]_[media] (µGy/h)
  - Weighted_absorbed_external_dose_rate_[isotope]_[media] (µGy/h)
  - Total_weighted_absorbed_dose_rate_[isotope]_[media] (µGy/h)
  - Totals and cross-media sums (e.g., grass, tree, soil, bacteria) for Sr-90, Cs-137, Am-241, Pu isotopes
  - Media categories include grassy vegetation, tree wood, soil, bacteria

- Transfer parameter notes and data provenance
  - Use of CR_wo-soil transfer parameters for Agrostis gigantea (grass) and Pinus sylvestris (wood) from Beresford et al. 2020 (with DOI provided)
  - Sr-90 and Cs-137 tree transfer parameters for deciduous trees based on CEZ site data (Ukrainian source)
  - Some activity concentrations for Am-241 and Pu isotopes in grassy vegetation and trees are predicted values derived from site transfer parameters
  - Explicit notes reference the datasets used for transfer parameters and measured soil concentrations

## Data Quality, Gaps, and Processing Notes
- Several fields marked as not available (n/a); some DM fractions were estimated from averages when missing.
- Some predicted activity concentrations rely on transfer-parameter assumptions rather than direct measurement.
- The dataset includes references for transfer parameters and sites, indicating careful but model-based estimation in parts of the data.

## GIS and Visualization Considerations
- Plot coordinates enable spatial mapping of radionuclide concentrations and dose rates across the Red Forest plots.
- Multiple media and isotopes allow thematic GIS layers (e.g., grass vs tree vs soil, Sr-90 vs Cs-137 vs Pu isotopes).
- Dose-rate layers (internal/external, per isotope and per media) support ecological and human-exposure visualizations.
- When mapping, pay attention to DM vs FM and March vs September sampling, as these affect unit consistency and comparability.

## Notable References and Data Sources
- Transfer parameter framework and site-specific data references:
  - Beresford et al. 2020 (transfer parameters for Am-241 and Pu isotopes in grassy vegetation and pine wood)
  - Ukrainian CEZ site data (Sr-90 and Cs-137 transfer to deciduous trees)
- Data provenance notes and DOI links provided within the dataset for traceability.

## Caveats for Users
- Data completeness varies; some fields are not available or are estimated.
- Units vary (µSv/h, µGy/h; Bq/kg_DM, Bq/kg_FM/DM) and must be consistently handled in GIS workflows.
- Some concentrations are predicted rather than measured; interpret with the accompanying transfer parameter notes.