# Column heading explanations and abbreviations in full for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data.

## Overview
- Provides column heading explanations and full abbreviations for the dataset on bioavailability and toxicity of nanomaterials in sewage sludge to earthworms.
- Covers experimental treatments, environmental matrices, biological endpoints, and analytical measurements.

## Dataset structure and key variables
- Sewage_sludge_treatment: treatment groups with engineered nanomaterials (ENM), ionic metals (Ionic), or control; includes a fully replicated soil control without sludge amendment.
- Percentage_sewage_sludge_in_soil-sludge_mixture: proportion of sewage sludge mixed into sandy-loam soil.
- Replicate_number: replicate index for each treatment.
- Measured_Ag_soil_conc_mgkg and Measured_Zn_soil_conc_mgkg: silver and zinc concentrations in soil measured by ICP-MS.
- Earthworm_Survival_no_of_worms: number of living earthworms after 28 days in soil-sludge mixtures.
- Earthworm_reproduction_Juveniles_per_worm_per_week: juvenile offspring produced per earthworm per week.
- Percentage_Earthworm_weight_change: percent change in earthworm biomass after 28 days.
- Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3 and Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3: uncorrected metal concentrations in individual worms (three worms per replicate) measured by ICP-MS.
- Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3 and Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3: titanium and aluminium body burdens in worms (three worms per replicate) measured by ICP-MS.
- Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3 and Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3: metal concentrations in worms corrected for gut soil residue (µg/g) after correction.
- Total_Ag_in_soil_pore_water_µgl_, Ultrafiltered_Ag_in_soil_pore_water_µgl_: total and ultrafiltered silver concentrations in soil pore water (µg/L).
- Total_Zn_in_soil_pore_water_µgl_, Ultrafiltered_Zn_in_soil_pore_water_µgl_: total and ultrafiltered zinc concentrations in soil pore water (µg/L).
- Total_dissolved_organic_carbon_in_soil_pore_water_ppm: dissolved organic carbon in soil pore water (ppm).
- Porewater_pH: pH of soil pore water.
- Data include separate measurements per replicate and per worm, across multiple treatments and sludge percentages.

## Measurements, units, and methods
- Analytical method: ICP-MS used for metal concentrations in soil and earthworm tissues.
- Units:
  - Soil concentrations: mg/kg for Ag and Zn.
  - Earthworm body burdens: mgAg/kg or mgZn/kg for uncorrected; µg/g for corrected body concentrations.
  - Pore water: µg/L for metals; ppm for dissolved organic carbon; pH unit for pore water pH.
- Data are organized by replicates and by individual worms (Worm1–Worm3) within each replicate/treatment.

## Data processing, corrections, and quality rules
- Corrected vs Uncorrected: Corrected concentrations account for soil residue in the gut; correction uses Al as a proxy.
  - Correction formula: M_worm,corr = M_worm - m × Al_worm, where m is the slope from a linear regression of measured metal against measured Al; separate regressions for each soil-sludge exposure.
- Reporting conventions:
  - < values indicate concentrations below the reported threshold but not precisely detectable.
  - n/a denotes not measured for a given field.
- Data capture includes both raw (uncorrected) and corrected tissue concentrations to support accurate exposure assessment.

## Abbreviations and data conventions
- Abbreviations and key terms included to ensure clear interpretation:
  - ENM: Engineered nanomaterials
  - ICP-MS: Inductively coupled plasma mass spectrometry
  - Mg/kg: milligrams per kilogram
  - µg/L: micrograms per litre
  - µg/g: micrograms per gram
  - mg/kg: milligrams per kilogram
- List of abbreviations provided to support consistent data interpretation across datasets.

## Governance, reuse, and stewarding considerations
- The dataset is accompanied by extensive column explanations and unit definitions, aiding metadata completeness and interoperability.
- Clear documentation of experimental design (treatments, replicates, sludge percentages) and measurement methods supports data governance, discovery, and reuse.
- The structured data dictionary facilitates data uploading to portals and catalogues, alignment with standards, and downstream analyses (e.g., cross-study meta-analyses).