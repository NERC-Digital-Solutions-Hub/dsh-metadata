# Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms

## Overview
- Dataset describes a study on how engineered nanomaterials and ionic metals in sewage sludge affect earthworms.
- Focuses on bioavailability and toxicity, with data collected across multiple treatment types, sludge percentages, and replicates.
- Data are organized with explicit column definitions, units, and data processing steps (e.g., gut correction).

## Experimental design and treatments
- Treatments: sewage sludge mixed with soil and exposed to either engineered nanomaterials (ENM), ionic metals (Ionic), or a sludge-only control.
- Full soil control: Woburn sandy loam soil without any sludge amendment included as a fully replicated test treatment.
- Sludge proportions: sludge mixed with soil in varying percentages (percentage of sewage sludge in the soil-sludge mixture).
- Replicates: data include replicate numbers for each treatment.

## Measured endpoints and variables
- Soil metal concentrations (measured by ICP-MS):
  - Measured_Ag_soil_conc_mgkg (silver)
  - Measured_Zn_soil_conc_mgkg (zinc)
- Earthworm endpoints after 28 days in soil-sludge mixtures:
  - Earthworm_Survival_no_of_worms (number alive)
  - Earthworm_reproduction_Juveniles_per_worm_per_week (reproduction rate)
  - Percentage_Earthworm_weight_change (percent change in biomass)
- Earthworm tissue metal concentrations (uncorrected, measured by ICP-MS):
  - Uncorrected_Earthworm_Ag_body_concentration_mgAgkg_Worm1/2/3
  - Uncorrected_Earthworm_Zn_body_concentration_mgZnkg_Worm1/2/3
  - Uncorrected_Earthworm_Ti_body_concentration_mgTikg_Worm1/2/3
  - Uncorrected_Earthworm_Al_body_concentration_mgAlkg_Worm1/2/3
- Corrected earthworm tissue metal concentrations (adjusted for gut residue):
  - Corrected_Earthworm_Ag_body_concentration_µgg_Worm1/2/3
  - Corrected_Earthworm_Zn_body_concentration_µgg_Worm1/2/3
  - Note: correction uses M_worm,corr = M_worm − m × Al_worm, where m is the slope from linear regression of worm metal vs Al for each exposure, and regressions are separate per soil-sludge exposure.
- Pore water and dissolved components (measured by ICP-MS or related methods):
  - Total_Ag_in_soil_pore_water_µgl_
  - Ultrafiltered_Ag_in_soil_pore_water_µgl_
  - Total_Zn_in_soil_pore_water_µgl_
  - Ultrafiltered_Zn_in_soil_pore_water_µgl_
  - Total_dissolved_organic_carbon_in_soil_pore_water_ppm
  - Porewater_pH

## Data processing and correction methods
- Gut correction: corrected tissue concentrations account for soil residue in the gut using the linear regression slope between metal and Al in worms.
- Uncorrected values: raw measured concentrations before correction.
- Handling of censored data: values reported as "<" are below the stated threshold and not precisely quantified.

## Units and abbreviations
- Units include mg/kg (soil/worm tissue concentrations), µg/g or µg/kg (body burdens), µg/L (pore water), ppm (DOM), and pH.
- Abbreviations:
  - Ag = Silver, Zn = Zinc, Al = Aluminium, Ti = Titanium
  - ENM = Engineered nanomaterials
  - ICP-MS = Inductively coupled plasma mass spectrometry

## Data quality and accessibility notes
- Data are structured with standardized column explanations to support verification, quality assurance, and re-use.
- Emphasis on making underlying data accessible for broader use and cross-analysis, aligning with environmental monitoring data practices.