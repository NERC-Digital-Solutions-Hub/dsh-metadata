# Column heading explanations and abbreviations in full for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data

## Overview
- Provides a comprehensive data dictionary for the dataset examining the effects of sewage sludge treatments (engineered nanomaterials ENM, ionic metals Ionic, or control) on soil-sludge mixtures and earthworms.
- Defines column headers, meanings, units, measurement methods, and data processing notes to support data discovery, interpretation, and reuse.

## Dataset scope and structure
- Experimental treatments
  - sewage_sludge_treatment: ENM, Ionic, or control.
  - Includes a separate fully replicated soil control (Woburn sandy loam soil) without sludge amendment.
- Experimental design variables
  - Percentage_sewage_sludge_in_soil-sludge_mixture: proportion of sewage sludge in the soil-sludge mix.
  - Replicate_number: replicate identifier for each treatment.
- Soil and earthworm measurements
  - Measured_Ag_soil_conc_mgkg: soil silver concentration (ICP-MS).
  - Measured_Zn_soil_conc_mgkg: soil zinc concentration (ICP-MS).
  - Earthworm_Survival_no_of_worms: number of surviving earthworms after 28 days.
  - Earthworm_reproduction_Juveniles_per_worm_per_week: juvenile offspring produced per worm per week.
  - Percentage_Earthworm_weight_change: percent change in earthworm biomass after 28 days.
- Earthworm body burdens (uncorrected and corrected)
  - Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3: silver concentration in each worm (ICP-MS).
  - Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3: zinc concentration in each worm (ICP-MS).
  - Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3: titanium concentration in each worm (ICP-MS).
  - Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3: aluminium concentration in each worm (ICP-MS).
  - Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3: corrected silver concentration in each worm (µg/g), accounting for gut soil residues.
  - Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3: corrected zinc concentration in each worm (µg/g), accounting for gut soil residues.
- Correction methodology and rationale
  - Corrected values are derived to account for soil residue in the gut.
  - The correction uses: {M} worm,corr = {M} worm - m*{Al} worm, where M is the target metal, Al is aluminium in worm tissue, and m is the slope from linear regression of worm metal vs. Al.
  - Separate regressions are performed for body burdens of worms exposed to each soil-sludge mixture.
  - Uncorrected values are the raw measured concentrations.
- Pore water and dissolved content
  - Total_Ag_in_soil_pore_water_µgl_, Ultrafiltered_Ag_in_soil_pore_water_µgl_: total and ultrafiltered silver in soil pore water (ICP-MS).
  - Total_Zn_in_soil_pore_water_µgl_, Ultrafiltered_Zn_in_soil_pore_water_µgl_: total and ultrafiltered zinc in soil pore water (ICP-MS).
  - Total_dissolved_organic_carbon_in_soil_pore_water_ppm: dissolved organic carbon in soil pore water.
  - Porewater_pH: pH of soil pore water.
- Abbreviations and data flags
  - The document includes a dedicated List of abbreviations (e.g., Ag, Zn, Al, Ti, ENM, ICP-MS, mg/kg, µg/g, µg/l, ppm).
  - < values: indicates measurements reported as less-than values that could not be precisely quantified.
- Data formatting and terminology
  - Units include mg/kg for soil concentrations, mg Ag/kg Worm etc. for tissue burdens, µg/g for corrected tissue burdens, and µg/L for pore water concentrations (as indicated by context and typical conventions).

## Data quality, standards, and governance implications for Data Leaders
- Rich, well-documented metadata supports discoverability, reuse across networks, and cross-disciplinary collaboration (e.g., policy, environmental risk assessment).
- Explicit definitions of raw vs corrected values, and the correction methodology, enhance data transparency and replication potential.
- Clear treatment identifiers, replication structure, and measurement methods (ICP-MS) support data quality assessment and provenance tracking.
- Standardized units and a centralized abbreviations list improve consistency and interoperability with other datasets.
- Highlights the importance of metadata completeness for complex, multi-variable environmental datasets, especially when coordinating across partners and data communities of practice.