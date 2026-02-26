# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

## Overview
- Data dictionary for the Vegetal_Foodstuff_Stable dataset, documenting concentrations of multiple stable elements in vegetal foodstuffs.
- Includes sample metadata, measurement details, and per-element concentration data with uncertainties and detection limits.

## Data fields

- Sample metadata
  - Sample_Code: unique sample identifier
  - Sample_Type: general description of the sample (foodstuff group)
  - Location: location where the sample was collected
  - Sample_Description: part of the organism analysed (e.g., which tissue or portion)
  - Collection_Date: date of sample collection (dd-mm-yyyy)
  - Sample_size: amount analyzed; units are g fresh matter or mL for olive oil and wine

- Analytical results by element
  - Cs_mg/kg_dm: concentration of stable cesium on a dry mass basis (mg/kg dm); notes specify when blank indicates below detection limit
  - Unc_Cs_mg/kg_dm: combined uncertainty for Cs concentration
  - Detection_Limit_Cs_mg/kg_dm: detection limit for Cs on a dry mass basis
  - Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm: analogous fields for strontium
  - K_mg/kg_dm, Unc_K_Mg/kg_dm, Detection_Limit_K_mg/kg_dm: analogous fields for potassium
  - Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm: analogous fields for sodium
  - Ca_mg/kg_dm, Unc_Ca_Mg/kg_dm, Detection_Limit_Ca_mg/kg_dm: analogous fields for calcium
  - Mg_mg/kg_dm, Unc_Mg_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm: analogous fields for magnesium
  - P_mg/kg_dm, Unc_P_mg/kg_dm, Detection_Limit_P_mg/kg_dm: analogous fields for phosphorus
  - Pb_mg/kg_dm, Unc_Pb_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm: analogous fields for lead (note formatting shows oil/wine context)
  - U_mg/kg_dm, Unc_U_mg/kg_dm, Detection_Limit_U_mg/kg_dm: analogous fields for uranium
  - Th_mg/kg_dm, Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm: analogous fields for thorium

- Notes on units and context
  - Concentrations are on a dry mass basis (mg/kg dm) or, for olive oil and wine, per litre where indicated
  - Some entries explicitly mention “and wine” in the unit description, reflecting matrix-specific reporting
  - Blank values in concentration fields indicate concentrations below the detection limit

## Data quality and usage cues

- Detection limits and uncertainties are captured per element to support proper data interpretation and comparisons
- The dataset accommodates different matrices (vegetal foods, olive oil, wine) with matrix-appropriate units
- Metadata supports data provenance, discoverability, and reusability (sample ID, collection date, location, sample description)

## Practical considerations for Data Leaders

- Use this dictionary to assess data availability, granularity, and metadata completeness across the Vegetal Foodstuff dataset
- Ensure consistency in units (prefer mg/kg(dm) where applicable; apply litre-based values for olive oil and wine as specified)
- Leverage detection limits and uncertainties to properly interpret non-detect values and to inform data quality practices
- Be mindful of formatting inconsistencies in the source (e.g., occasional misprints) when integrating into data systems or pipelines