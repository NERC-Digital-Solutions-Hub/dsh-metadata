# Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms data

- Overview
  - A metadata and data dictionary for a study on the bioavailability and toxicity of nanomaterials in sewage sludge when mixed with soil and exposed to earthworms.
  - Documents experimental treatments, measured environmental concentrations, earthworm outcomes, tissue burdens, and pore-water chemistry to support monitoring and policy evaluation.

- Experimental design and treatments
  - Sewage_sludge_treatment: either engineered nanomaterials (ENM), ionic metals (Ionic), or no additions (control). A fully replicated soil control without sludge amendment is also included.
  - Percentage_sewage_sludge_in_soil-sludge_mixture: varying proportions of sewage sludge in the soil-sludge mix.
  - Replicate_number: replication for each treatment.

- Measured soil and earthworm endpoints
  - Measured_Ag_soil_conc_mgkg and Measured_Zn_soil_conc_mgkg: silver and zinc concentrations in soil (ICP-MS).
  - Earthworm_survival_no_of_worms: number alive after 28 days.
  - Earthworm_reproduction_Juveniles_per_worm_per_week: juvenile production per worm per week.
  - Percentage_Earthworm_weight_change: percent change in earthworm biomass after 28 days.

- Earthworm body burdens (metal concentrations)
  - Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3; Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3; Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3; Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3: raw tissue concentrations by ICP-MS.
  - Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3; Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3: tissue concentrations corrected for gut soil residues.
  - Correction method: M_worm,corr = M_worm - m × Al_worm, where m is the slope from a linear regression of the metal vs. Al within each soil-sludge exposure; separate regressions per exposure group.

- Data interpretation notes (uncorrected vs corrected)
  - Uncorrected: raw tissue concentrations.
  - Corrected: concentrations adjusted to account for soil residue in the gut; results expressed as µg/g.
  - "< values": indicates censored/low-level measurements.

- Pore-water chemistry and dissolved constituents
  - Total_Ag_in_soil_pore_water_µgl_ and Ultrafiltered_Ag_in_soil_pore_water_µgl_: total and ultrafiltered silver in soil pore water (ICP-MS).
  - Total_Zn_in_soil_pore_water_µgl_ and Ultrafiltered_Zn_in_soil_pore_water_µgl_: total and ultrafiltered zinc in soil pore water (ICP-MS).
  - Total_dissolved_organic_carbon_in_soil_pore_water_ppm: DOC in pore water.
  - Porewater_pH: pH of soil pore water.

- Abbreviations and data terminology
  - n/a = not measured; ENM = engineered nanomaterials; ICP-MS = inductively coupled plasma mass spectrometry; mg/kg, µg/g, µg/L, ppm = units used across measurements.
  - Corrected = concentration in earthworms after gut-residue correction using Al as a reference.
  - Uncorrected = measured concentration before correction.
  - The dataset provides explicit definitions and the corrective formula to aid reproducibility and cross-study comparability.

- Data quality, transformation, and governance considerations
  - Data involve multiple data types (soil concentrations, organism end-points, tissue burdens, pore-water chemistry) requiring careful metadata to support reuse.
  - Acknowledges potential barriers common to monitoring data: data gaps, access, metadata completeness, and the need for transparent data transformation (e.g., correction for gut content).
  - Clear documentation of measurement methods (ICP-MS), units, and corrections supports data quality assessment, replication, and governance decisions in monitoring programs.