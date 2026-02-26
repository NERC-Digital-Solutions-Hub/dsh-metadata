# TREE_Northumbria_Animal_Sample_information

## Overview
- Structured dataset capturing animal sample information for environmental monitoring.
- Aims to standardise data for verifying environmental health and policy performance over time.
- Focuses on species identity, sampling details, morphometrics, mass measurements, sample counts, sex, notes, and analysis performed.
- Includes special cases: frogspawn are bulk samples of multiple eggs; “Not recorded” indicates missing data; frogspawn information is not applicable in some fields.

## Key data fields (and what they capture)
- Species identity
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
- Sampling details
  - Site: Sampling site
  - Date_Sample_Collected: Date when the sample was collected
  - Sampling_Location_Or_National_Grid_Reference: Sampling location or national grid reference
  - CEH_Sample_Codes_Associated_with_Animal_Or_Sample: CEH sample codes linked to the animal or sample
  - CEH_Sample_Description: Description of the CEH sample
  - General_Notes: General notes about the sample
- Morphometrics and mass
  - Length_mm: Length in millimetres
  - Width_mm: Width in millimetres
  - Depth_mm: Depth in millimetres
  - Wholebody_Fresh_Mass_kg: Whole-body fresh mass in kilograms
  - Wholebody_Freeze_Dried_Mass_kg: Whole-body freeze-dried mass in kilograms
  - Wholebody_Ash_Mass_kg: Whole-body ash mass in kilograms
- Sample size and biological attributes
  - n: Number of animals or samples
  - Sex: Sex of animal (male or female); “Not recorded” if undetermined; “Unknown” used when applicable
  - Frogspawn note: Indicates that frogspawn are bulk samples of multiple eggs (special case)
- Processing and analysis
  - Sample_Preparation_And_Analysis_Performed: Information on sample preparation and analyses conducted

## Data quality and interpretation
- Not recorded indicates data were not obtained for that field.
- Units are specified for all measurement fields (e.g., mm for morphometrics, kg for masses).
- Special cases clarified (e.g., frogspawn bulk samples; frogspawn information not applicable in certain contexts).

## Role in environmental monitoring
- Standardised data structure supports verification, cleaning, and transformation of environmental data.
- Facilitates categorisation and comparison of environmental health indicators against standards.
- Enables clear reporting through outputs like reports, maps, and charts; supports storage and portal upload of datasets.

## Potential uses and challenges
- Enhancing dataset value by integrating with other relevant data to support holistic environmental monitoring.
- Ensuring accessibility of underlying data used to generate final outputs for broader scrutiny and reuse.