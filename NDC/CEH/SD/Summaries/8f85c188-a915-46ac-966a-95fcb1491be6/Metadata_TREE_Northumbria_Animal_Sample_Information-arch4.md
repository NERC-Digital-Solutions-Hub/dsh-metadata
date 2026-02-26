# TREE_Northumbria_Animal_Sample_information

## Overview
- A data dictionary for Northumbria animal sampling information managed by CEH.
- Captures taxonomy, sampling details, spatial references, identifiers, morphology, mass, counts, biological attributes, notes, and processing information.
- Notes special case: Frogspawn are bulk samples of multiple eggs, affecting interpretation of counts and descriptions.

## Key data fields and meanings
- Latin_Species_Name: Latin taxonomic name of the species.
- Common_Species_Name: Common name of the species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Sampling location or national grid reference.
- CEH_Sample_Codes_Associated_with_Animal_Or_Sample: CEH codes linked to the animal or sample.
- CEH_Sample_Description: Description of the CEH sample.
- Length_mm: Length of the organism in millimetres.
- Width_mm: Width of the organism in millimetres.
- Depth_mm: Depth of the organism in millimetres.
- Wholebody_Fresh_Mass_kg: Wholebody fresh mass in kilograms.
- Wholebody_Freeze_Dried_Mass_kg: Wholebody freeze-dried mass in kilograms.
- Wholebody_Ash_Mass_kg: Wholebody ash mass in kilograms.
- n: Number of animals or samples.
- Sex: Sex of the animal; values can be recorded, not recorded, or unknown.
- General_Notes: General notes about the sample.
- Sample_Preparation_And_Analysis_Performed: Information about sample preparation and any analyses performed.

## Data quality and metadata notes
- Not recorded indicates data were not obtained or are missing for the field.
- Frogspawn notes indicate bulk sampling (multiple eggs), which impacts interpretation of certain fields (e.g., n, CEH_Sample_Description).
- Metadata explanations accompany each field to aid discoverability and reuse.

## Governance and data use implications for Data Leaders
- Data discoverability: Rich field descriptions facilitate understanding, integration, and reuse across datasets.
- Standardization needs: Consistent units (mm for morphology, kg for masses) and clear handling of missing values improve interoperability.
- Data quality management: Clear metadata supports assessment of data completeness and reliability; plan for updates and versioning.
- Cross-domain collaboration: Linking CEH sample codes with specimens supports broader data sharing and collaboration within the data community.
- User-focused stewardship: Field availability (taxonomy, location, temporal data, morphology, and processing) supports diverse analyses and informs sampling strategies.

## Practical considerations for implementation
- Ensure consistent data entry for species naming (Latin and common names) and geospatial references.
- Maintain clear documentation on how to handle Not Recorded and Unknown values.
- Preserve frogspawn-specific guidance to correctly interpret n and CEH_Sample_Description for bulk samples.
- Facilitate data discovery by indexing key fields (taxon, site, date, location reference, CEH codes, and processing details).