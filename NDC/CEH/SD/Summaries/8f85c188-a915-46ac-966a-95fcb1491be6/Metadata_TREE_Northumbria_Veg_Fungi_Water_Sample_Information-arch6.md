# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

## Overview
- Metadata and field definitions for the TREE_Northumbria_Veg_Fungi_Water_Sample_Information dataset.
- Captures taxonomic identifiers, sampling details, location references, sample coding, mass measurements, notes, and processing/analysis information.

## Key Fields and Meanings
- Latin_Species_Name: Latin name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- Sampling_Location_Or _National_Grid_Reference: Location or National Grid Reference (NGR).
- CEH_Sample_Code: CEH code associated with the sample.
- CEH_Sample_Description: Description of the CEH sample.
- Sample_Fresh_Mass_kg: Fresh mass of the sample (kg). Note: Units are kilograms; not applicable for water samples.
- Sample_Dried_Mass_kg: Dry mass of the sample (kg). Note: Units are kilograms; not applicable for water samples.
- General_Notes: Additional general notes.
- NGR: National Grid Reference (clarifies spatial reference).
- Sample_Preparation_And _Analysis_Performed: Procedures for sample preparation and analyses conducted.

## Data Quality and Structure Considerations
- Many fields specify Units as n/a, indicating varied or context-dependent data types.
- Mass fields include a caveat: not applicable for water samples, signaling dataset-specific applicability.
- Location is captured via Site and/or National Grid Reference to support spatial analysis.
- CEH fields enable traceability to the Centre for Ecology & Hydrology (CEH) workflows.
- Clear field explanations accompany most names, aiding data understanding and interoperability.

## How Data Supports Insight and Use
- Enables species occurrence and sample provenance tracing through taxonomic and sampling metadata.
- Supports geospatial analyses via Site and NGR references.
- Facilitates data integration with other datasets (e.g., veg, fungi, water samples) using standardized field meanings and CEH coding.
- Allows creation of self-serve data products such as dashboards, pivot tables, and reports focused on species, sites, collection dates, and processing steps.

## Practical Data Support Guidance
- Clarify the “ask” when using the dataset (e.g., species distribution by site, temporal sampling patterns).
- Handle patchy or context-dependent fields (e.g., dried mass not applicable for water samples) gracefully during cleaning and transformation.
- Integrate with related datasets to enhance insights (e.g., linking CEH_Sample_Code to broader CEH data products).
- Promote outputs and gather user feedback to refine data products and documentation.

## Suggested Data Products and Actions
- Species-by-site dashboards showing presence/absence and sample counts.
- Time-series views of sample collection dates by site or species.
- Spatial maps using NGR/coordinates to visualize sampling distribution.
- Summary reports detailing preparation and analyses performed for reproducibility.