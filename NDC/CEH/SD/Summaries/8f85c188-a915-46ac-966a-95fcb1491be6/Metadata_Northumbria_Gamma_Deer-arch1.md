# TREE_Northumbria_Gamma_Deer

## Overview
- A dataset of Cs-137 activity measured in Roe deer tissue, clinically described by UKCEH Radiochemistry Laboratory.
- Includes sample metadata (species, tissue, site, sample identifiers, and dates) plus radiometric measurements and quality indicators.
- Aims to support understanding of Cs-137 bioaccumulation in wildlife and facilitate comparisons across sampling sites and times.

## Key fields and meanings
- Latin_Species_Name: Latin name of the species (Roe deer).
- Tissue: Tissue type analyzed.
- CEH_Sample_code: UKCEH Radiochemistry Laboratory unique sample identifier.
- CEH_Sample_description: UKCEH sample description.
- Site: Sampling site.
- Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of the sample (in grams).
- Sampling_date_Used_As_Decay_date: Date used as the decay date for activity calculations.
- Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq per kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in Bq per kg dry mass.
- MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity (Bq per kg fresh mass).
- Cs-137_Concentration_Ratio_FM: Concentration ratio expressed as activity in tissue (fresh mass) divided by activity in soil (dry mass).
- CR_Notes: Notes related to the concentration ratio.
- Site, CEH_Sample_code, CEH_Sample_description: Contextual identifiers and descriptions for traceability.

## Measurements and units
- Units: Bq per kg (fresh mass or dry mass), g for mass.
- FM: Fresh Mass.
- DM: Dry Mass (used in the counting error field).
- "<" markers indicate values below the stated Minimum Detectable Activity (MDA).
- Two-sigma counting error reported for Cs-137 measurements.

## Data quality and caveats
- Presence of < markers denotes non-detectable levels relative to MDA.
- Some fields (e.g., soil mass or exact soil activity) are inferred through the concentration ratio and may require careful interpretation.
- Decay-date alignment relies on Sampling_date_Used_As_Decay date for activity calculations.

## Potential analyses and use cases
- Compare Cs-137 bioaccumulation across sampling sites and tissues in roe deer.
- Assess relationships between fresh mass, dry mass, and measured activity concentrations.
- Use concentration ratios to examine transfer from soil to muscle tissue and identify environmental exposure patterns.
- Account for detection limits and measurement uncertainties in statistical analyses or predictive modeling of radiocesium in wildlife.
- Support radiological monitoring programs and environmental risk assessments in Northumbria.