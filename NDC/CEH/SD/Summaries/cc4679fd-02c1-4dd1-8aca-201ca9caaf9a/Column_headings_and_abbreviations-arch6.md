# Column heading explanations and abbreviations in full for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data

## Overview
- Describes column headings and abbreviations for a dataset examining the bioavailability and toxicity of nanomaterials in sewage sludge to earthworms.
- Study design includes different sludge treatments (engineered nanomaterials, ionic metals, or control), varying percentages of sewage sludge in soil, and replicated experiments.
- Measures include soil, earthworm, and porewater concentrations of metals, earthworm survival and reproduction, body burdens, and soil porewater chemistry.

## Data Structure and Treatments
- Sewage_sludge_treatment: Treatment type with categories — ENM (engineered nanomaterials), Ionic (ionic metals), or control.
- Percentage_sewage_sludge_in_soil-sludge_mixture: Proportion of sewage sludge in the soil-sludge mixture (in different proportions).
- Replicate_number: Replicate identifier for each treatment.
- A fully replicated soil control is included (Woburn sandy loam soil without sludge amendment).

## Earthworm and Biological Endpoints
- Earthworm_Survival_no_of_worms: Number of living earthworms after 28 days in each replicate.
- Earthworm_reproduction_Juveniles_per_worm_per_week: Juveniles produced per earthworm per week.
- Percentage_Earthworm_weight_change: Percent change in earthworm biomass after 28 days.
- Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3, Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3, Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3, Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3: Measured metal concentrations in each of three earthworms per replicate (in respective units), uncorrected for gut soil contamination.
- Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3, Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3: Metal concentrations in earthworms corrected for soil residue in the gut (units: µg/g).

## Measurements in Soil and Pore Water
- Measured_Ag_soil_conc_mgkg, Measured_Zn_soil_conc_mgkg: Silver and zinc concentrations in soil (mg/kg) measured by ICP-MS.
- Total_Ag_in_soil_pore_water_µgl_, Ultrafiltered_Ag_in_soil_pore_water_µgl_: Total and ultrafiltered silver in soil pore water (µg/L or specified unit).
- Total_Zn_in_soil_pore_water_µgl_, Ultrafiltered_Zn_in_soil_pore_water_µgl_: Total and ultrafiltered zinc in soil pore water (µg/L or specified unit).
- Total_dissolved_organic_carbon_in_soil_pore_water_ppm: Dissolved organic carbon in soil pore water (ppm).
- Porewater_pH: pH of the soil pore water.

## Abbreviations and Notation
- n/a: not measured
- Ag: Silver
- Zn: Zinc
- Al: Aluminium
- Ti: Titanium
- ENM: Engineered nanomaterials
- ICP-MS: Inductively coupled plasma mass spectrometry
- mg/kg: milligrams per kilogram
- µg/l: micrograms per liter
- µg/g: micrograms per gram
- ppm: parts per million
- Corrected: concentration after adjusting for gut soil residue using a correction formula; M_worm,corr = M_worm - m × Al_worm, where m is the slope from the linear regression of measured M_worm against Al_worm for each soil-sludge mixture.
- Uncorrected: the measured concentration in the earthworms before correction.

## Key Data Interpretations and Notes
- The dataset distinguishes uncorrected and corrected body concentrations to account for potential soil contamination in the gut.
- The correction uses Al as a proxy to estimate soil-derived contamination within the gut, with separate regressions per soil-sludge mixture.
- Values reported as "<" indicate measurements below a reporting threshold but above detection capabilities.

## Practical Considerations for Data Support
- Structure supports creating self-serve dashboards or reports that enable exploration of treatment effects, exposure concentrations, and earthworm outcomes.
- Requires joining treatment, replicate, and measurement data, with careful handling of corrected vs uncorrected body burdens.
- Attention to units and correction methodology is essential when comparing metal burdens across treatments.