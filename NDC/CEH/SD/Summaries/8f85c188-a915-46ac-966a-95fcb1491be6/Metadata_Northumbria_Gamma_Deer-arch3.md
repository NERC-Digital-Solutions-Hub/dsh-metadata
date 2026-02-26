# TREE_Northumbria_Gamma_Deer

## Overview
- Dataset documenting Cs-137 activity concentrations in roe deer tissue sampled at a Northumbria site.
- Includes specimen identifiers, sampling site, tissue type, fresh mass analysed, and a decay-date reference.
- Measurements cover Cs-137 concentration in fresh mass (Bq/kg FM) with associated dry-mass uncertainty, including minimum detectable activity and concentration ratios to soil.
- Aims to support environmental radiological monitoring and scrutiny of wildlife contamination, with data suitable for informing policy and future decisions.

## Data structure and key fields
- Latin_Species_Name: Latin name of species (Roe deer).
- CEH_Sample_description: UKCEH sample description.
- Tissue: Tissue type analysed (e.g., meat/muscle).
- CEH_Sample_code: UKCEH Radiochemistry Laboratory unique sample identifier.
- Site: Sampling site.
- Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of sample analysed (grams).
- Sampling_date_Used_As_Decay date: Date of sampling used as decay date for Cs-137 calculations.
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in fresh mass (Bq/kg FM).
- Counting_Error_ Cs-137 _Bq_per_kg_DM: Two-sigma counting error for Cs-137 in dry mass (Bq/kg DM).
- Cs-137 <: Indicates a value below the reporting threshold (less than).
- MDA_Cs-137_ Bq_per _kg_FM: Minimum detectable activity concentration of Cs-137 in fresh mass (Bq/kg FM).
- Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio for fresh mass (muscle Bq/kg FM divided by soil Bq/kg DM).
- CR_Notes: Notes related to the concentration ratio.

## Measurement details
- Data include both muscle (fresh mass) and comparative dry-mass measurements, plus an explicit concentration ratio between tissue and soil.
- Decay-date reference ensures Cs-137 activity is contextualized relative to sampling time.
- Includes data quality indicators: MDA values and counting error (uncertainty) per sample.

## Data quality, metadata and governance considerations
- Metadata elements present (species, site, sample code, tissue, mass, dates, units, explanations) support traceability and reproducibility.
- Some fields rely on qualitative markers (e.g., < for below MDA) which require careful interpretation in reporting.
- Data sharing and openness may be influenced by sample-level identifiers and provenance (CEH lab data) and must align with data governance practices.
- Adequate metadata (units and explanations) are provided for key fields, aiding verification and reuse.

## Use in monitoring and decision-making
- Enables assessment of Cs-137 burden in wildlife meat and potential transfer to humans or ecosystems via muscle tissue concentration and tissue-to-soil ratios.
- Supports trend analysis, risk assessment, and policy evaluation by providing standardized measurements, detection limits, and uncertainty estimates.