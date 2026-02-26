# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

## Overview
- Provides a standardized information schema for samples from vegetation, fungi, and water in Northumbria.
- Captures taxonomic names, sampling details, and analytical data to support environmental health monitoring and policy evaluation.

## Key data elements (fields)
- Latin_Species_Name: Latin name of species (explanation provided in dataset).
- Common_Species_Name: Common name of species (explanation provided in dataset).
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Location or National Grid Reference (NGR) for geolocation.
- CEH_Sample_Code: CEH-assigned sample code.
- CEH_Sample_Description: Description of the CEH sample.
- Sample_Fresh_Mass_kg: Fresh mass of the sample in kilograms (not applicable for water samples).
- Sample_Dried_Mass_kg: Dry mass of the sample in kilograms (not applicable for water samples).
- Not applicable for water samples: Indicates mass fields may not apply to water.
- General_Notes: General notes about the sample.
- Sample_Preparation_And_Analysis_Performed: Details of sample preparation and analyses conducted.
- NGR is national grid reference: Note clarifying location reference system.

## Data quality and governance considerations
- Metadata and field explanations support clear interpretation and validation.
- Some fields are non-applicable for certain sample types (e.g., dried mass for water samples), requiring conditional data handling.
- Consistent units (kg) and precise geolocation (NGR) facilitate comparability and governance.
- CEH_Sample_Code and CEH_Sample_Description promote traceability of samples and provenance.

## Use in monitoring frameworks
- Enables standardized recording of species presence and associated sample data to inform biodiversity, habitat health, and water quality assessments.
- Supports reproducibility, cross-site comparability, and temporal trend analysis through consistent data capture.

## Practical implications for authors of monitoring frameworks
- Serves as a model for harmonizing data collection across vegetation, fungi, and water monitoring activities.
- Supports transparent data sharing and governance by providing clear data fields and explanations.
- Helps identify data gaps (e.g., missing metadata or non-applicable fields) and informs data quality improvement initiatives.