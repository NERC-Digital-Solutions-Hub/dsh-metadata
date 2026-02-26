# Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms

## Purpose and scope
- Documents the treatments and measured outcomes of earthworms exposed to soil-sludge mixtures containing engineered nanomaterials (ENM), ionic metals (Ionic), or no amendments (control).
- Includes a fully replicated soil control without sludge amendment for baseline comparison.

## Experimental design and treatments
- Sewage_sludge_treatment: ENM, Ionic, or control.
- Replicate_number: replicate identifier for each treatment.
- Percentage_sewage_sludge_in_soil-sludge_mixture: varying proportions of sewage sludge in the soil-sludge mixture.
- Additional soil control: a soil-only condition without sludge amendment.

## Measured outcomes (biological and chemical)
- Earthworm_survival_no_of_worms: number of live earthworms in each replicate after 28 days.
- Earthworm_reproduction_Juveniles_per_worm_per_week: juvenile offspring produced per worm per week.
- Percentage_Earthworm_weight_change: biomass change (%; (Initial weight - Final weight) / Initial weight × 100) after 28 days.
- Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3: silver concentration in each earthworm measured by ICP-MS (unadjusted).
- Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3: zinc concentration in each earthworm (unadjusted).
- Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3: titanium concentration in each earthworm (unadjusted).
- Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3: aluminium concentration in each earthworm (unadjusted).
- Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3: silver concentration corrected for gut soil residue (µg/g).
- Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3: zinc concentration corrected for gut soil residue (µg/g).
- Total_Ag_in_soil_pore_water_µgl: total silver concentration in soil pore water (ICP-MS; µg/L).
- Ultrafiltered_Ag_in_soil_pore_water_µgl: ultrafiltered silver concentration in soil pore water (ICP-MS; µg/L).
- Total_Zn_in_soil_pore_water_µgl: total zinc concentration in soil pore water (ICP-MS; µg/L).
- Ultrafiltered_Zn_in_soil_pore_water_µgl: ultrafiltered zinc concentration in soil pore water (ICP-MS; µg/L).
- Total_dissolved_organic_carbon_in_soil_pore_water_ppm: dissolved organic carbon concentration in soil pore water (ppm).
- Porewater_pH: pH of the soil pore water (unitless).
- Notes on data quality: Some values are reported as "<" values when below detection limits but not precisely quantified.

## Correction methodology and definitions
- Corrected_ values: earthworm tissue concentrations adjusted to account for soil residue remaining in the gut.
- Correction formula: M_worm,corr = M_worm - m × Al_worm, where:
  - M_worm is the measured metal concentration in the worm.
  - Al_worm is the measured aluminium concentration in the worm.
  - m is the slope from a separate linear regression of M_worm against Al_worm for each exposure condition.
- Separate regressions are performed for each soil-sludge exposure scenario.
- Uncorrected values: raw measured concentrations in the earthworms before gut correction.

## Units and abbreviations
- ENM: Engineered nanomaterials
- ICP-MS: Inductively Coupled Plasma Mass Spectrometry
- mg/kg: milligrams per kilogram
- µg/g: micrograms per gram
- µg/L: micrograms per liter
- ppm: parts per million
- Corrected: concentration after gut correction
- Uncorrected: measured concentration before correction
- n/a: not measured

## Practical implications for analysis
- Data enable assessment of bioavailability and trophic transfer by comparing soil-sludge treatments, sludge proportions, and replicate outcomes.
- Allows evaluation of ENM versus ionic metal effects on earthworm survival, reproduction, growth, and tissue accumulation.
- Provides soil pore water and dissolved organic carbon parameters to support interpretation of exposure pathways (dissolution, speciation, and leaching).
- The correction approach helps separate true tissue burden from gut-associated residues, improving interpretation of internal dose.