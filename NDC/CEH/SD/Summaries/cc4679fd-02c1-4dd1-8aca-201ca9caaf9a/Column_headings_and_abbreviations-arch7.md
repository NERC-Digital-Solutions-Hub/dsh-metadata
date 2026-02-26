# Column heading explanations and abbreviations in full for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data.

## Overview
- Provides column-by-column explanations and full abbreviations for the dataset on bioavailability and toxicity of engineered nanomaterials and metals in sewage sludge exposed to earthworms.
- Covers treatments, mixture proportions, replicates, measured concentrations, biological responses, and pore-water chemistry.
- Includes definitions for corrected versus uncorrected tissue concentrations and the method used for correction.

## Key data fields and their meanings
- Sewage_sludge_treatment, Explanation: Treatment type for each test (engineered nanomaterials, ionic metals, or control) plus a soil-only control with replicated test treatments.
- Percentage_sewage_sludge_in_soil-sludge_mixture, Explanation: Proportion of sewage sludge in the soil-sludge mixture.
- Replicate_number, Explanation: Replicate index for each treatment.
- Measured_Ag_soil_conc_mgkg, Explanation: Silver concentration in soil measured by ICP-MS.
- Measured_Zn_soil_conc_mgkg, Explanation: Zinc concentration in soil measured by ICP-MS.
- Earthworm_Survival_no_of_worms, Explanation: Number of earthworms alive after 28 days in soil-sludge mixtures.
- Earthworm_reproduction_Juveniles_per_worm_per_week, Explanation: Juveniles produced per earthworm per week.
- Percentage_Earthworm_weight_change, Explanation: Percentage change in earthworm biomass after 28 days.
- Uncorrected_Earthworm_Ag_Body_concentration_mgAgkg_Worm1/2/3, Explanation: Silver concentration in each of up to three earthworms per replicate (measured by ICP-MS).
- Uncorrected_Earthworm_Zn_Body_concentration_mgZnkg_Worm1/2/3, Explanation: Zinc concentration in each earthworm (measured by ICP-MS).
- Uncorrected_Earthworm_Ti_Body_concentration_mgTikg_Worm1/2/3, Explanation: Titanium concentration in each earthworm (measured by ICP-MS).
- Uncorrected_Earthworm_Al_Body_concentration_mgAlkg_Worm1/2/3, Explanation: Aluminium concentration in each earthworm (measured by ICP-MS).
- Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3, Explanation: Silver in each earthworm corrected for gut soil residue.
- Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3, Explanation: Zinc in each earthworm corrected for gut soil residue.
- Total_Ag_in_soil_pore_water_µgl_, Explanation: Total silver in soil pore water (ICP-MS).
- Ultrafiltered_Ag_in_soil_pore_water_µgl_, Explanation: Ultra-filtered silver in soil pore water (ICP-MS).
- Total_Zn_in_soil_pore_water_µgl_, Explanation: Total zinc in soil pore water (ICP-MS).
- Ultrafiltered_Zn_in_soil_pore_water_µgl_, Explanation: Ultra-filtered zinc in soil pore water (ICP-MS).
- Total_dissolved_organic_carbon_in_soil_pore_water_ppm, Explanation: Dissolved organic carbon in soil pore water.
- Porewater_pH, Explanation: pH of the soil pore water.

## Units and measurement details
- Soil metal concentrations: mg/kg.
- Earthworm body burdens: include both uncorrected (mg Ag/kg worm, mg Zn/kg worm, etc.) and corrected (µg/g worm) values.
- Pore-water concentrations: µg/L.
- Dissolved organic carbon: ppm.
- pH: unitless.

## Corrected vs Uncorrected tissue concentrations
- Uncorrected: raw measured concentrations in earthworms.
- Corrected: concentrations adjusted to account for soil residues remaining in the gut, using the formula:
  - M_worm,corr = M_worm - m * Al_worm
  - where M_worm is measured metal, Al_worm is aluminium concentration in the worm, and m is the slope from a linear regression of metal vs Al for each soil-sludge exposure.
- Separate regressions are performed for each soil-sludge mixture.
- Corrected values provide a more accurate representation of tissue burdens attributable to uptake rather than gut contents.

## Data standardization and interoperability
- Clear, full definitions and units support integration with other datasets and GIS workflows.
- Abbreviations and calculation rules (e.g., correction methodology) facilitate consistent data processing, quality assurance, and reproducibility.
- The dataset includes both replicate-level and per-earthworm measurements, enabling granular map-based analyses when combined with spatial context (e.g., soil type, location).

## How this supports GIS and map-based data products
- Provides standardized, well-documented fields suitable for layering with geospatial attributes (soil type, location, exposure scenarios).
- Enables creation of thematic maps showing treatment effects, contamination levels in soil and organisms, and ecological outcomes (survival, reproduction, weight change).
- Facilitates data cleaning, transformation, and integration with other environmental datasets to support risk assessment and policy-relevant visualizations.