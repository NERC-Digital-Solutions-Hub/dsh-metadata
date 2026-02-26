# TREE_Northumbria_Animal_Sample_information

## Overview
- Metadata schema for animal sampling information used by Northumbria (CEH). Captures taxonomic identifiers, sampling context, physical measurements, counts, sex, notes, and analysis details to support data exploration and reporting.

## Key data fields
- Latin_Species_Name: Scientific species name.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Location reference for sampling.
- CEH_Sample_Codes_Associated_with_Animal_Or_Sample: CEH-specific codes tied to the animal or sample.
- CEH_Sample_Description: Description of the CEH sample.
- Length_mm: Length of organism in millimetres.
- Width_mm: Width of organism in millimetres.
- Depth_mm: Depth of organism in millimetres.
- Wholebody_Fresh_Mass_kg: Fresh mass of organism in kilograms.
- Wholebody_Freeze_Dried_Mass_kg: Freeze-dried mass in kilograms.
- Wholebody_Ash_Mass_kg: Ash mass in kilograms.
- n: Number of animals or samples.
- Sex: Sex of animal (male/female); Unknown when not determined.
- General_Notes: General notes.
- Sample_Preparation_And_Analysis_Performed: Information about sample preparation and analyses conducted.

## Data quality and handling
- Not Recorded: Indicates measurement data were not obtained.
- Unknown: Used for sex when not determined.
- Units: Provided for all measurable fields (e.g., mm for length/width/depth, kg for masses).
- Frogspawn note: Frogspawn are bulk samples of multiple eggs, indicating special handling/interpretation for this entry.

## Special considerations
- Mixed data formats and potential gaps due to Not Recorded/Unknown values.
- CEH codes provide a linkage between the sample and broader datasets or analyses.
- Measurement fields enable size and biomass analyses; mass and dimension data support ecological assessments.

## Potential uses for Data Support
- Create dashboards and reports to summarize species distributions, sizes, and biomasses by site and date.
- Enable self-service exploration of sampling effort (n), locations (grid references), and associated analyses.
- Track data quality and completeness across fields (e.g., identify records with Not Recorded values).

## Challenges and next steps
- Address patchy data and ensure consistent unit usage and site references across systems.
- Improve discoverability and reuse by promoting outputs and harmonizing CEH codes with other datasets.
- Develop data cleaning and integration workflows to handle multiple formats and missing values, supporting broader data-driven decisions.