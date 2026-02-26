# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

## Overview
- Metadata table capturing sample identity, location, timing, and preparation/analysis for vegetation, fungi, and water samples.
- Aims to support data identification, traceability, and downstream analyses by analysts using data to identify patterns and inform decisions.

## Key fields and definitions
- Latin_Species_Name: Latin taxonomic name of the species.
- Common_Species_Name: Common name of the species.
- Site: Sampling site name.
- Date_Sample_Collected: Date when the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Sampling location or National Grid Reference (NGR) for geolocation.
- CEH_Sample_Code: Centre for Ecology & Hydrology sample code associated with the sample.
- CEH_Sample_Description: Description of the CEH sample.
- Sample_Fresh_Mass_kg: Fresh mass of the sample (in kilograms).
- Sample_Dried_Mass_kg: Dry mass of the sample (in kilograms); not applicable for water samples.
- General_Notes: Additional notes about the sample.
- Sample_Preparation_And_Analysis_Performed: Details on sample preparation and analyses conducted.
- NGR: Abbreviation note clarifying that National Grid Reference is used for location.

## Metadata and provenance
- Units: Most fields list units as not applicable, with mass fields specified in kilograms where relevant.
- Location reference: NGR is used for precise geolocation; CEH codes/descriptions provide lab-context identifiers.
- Scope: Combines taxonomic information with sampling and lab processing metadata for reproducibility.

## Data types and structure
- Tabular format with a mix of text fields, dates, and numeric mass values (kg).
- Some fields may be not applicable for certain sample types (e.g., dried mass for water samples).

## Potential analyses and use cases
- Link species information to where and when samples were collected.
- Analyze relationships between sample mass (fresh/dried) and site or species.
- Map sampling locations using NGR data; potentially convert to coordinates for GIS.
- Compare CEH sample codes/descriptions with laboratory analysis results.
- Integrate with other environmental datasets to assess spatial or temporal patterns.

## Data quality considerations and challenges
- Not applicable for water samples: ensure correct interpretation of mass fields.
- Possible missing data for certain fields; variability in data completeness across samples.
- Data may originate from multiple sources; standardization of species names and metadata needed.
- Geolocation accuracy depends on NGR precision and correct conversion to coordinates.
- Consistency in date formats and measurement units; careful validation during analysis.