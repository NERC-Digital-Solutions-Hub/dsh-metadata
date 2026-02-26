# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

## Overview
- Dataset likely records biological sampling information for vegetation, fungi, and water from Northumbria.
- Focuses on specimen identification, sampling details, location references, lab codes, and analytical notes.
- Includes both taxonomic names (Latin and common) and sample metadata (dates, locations, masses, and preparation/analysis).

## Core Attributes (fields and their purposes)
- Latin_Species_Name: Latin name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date when the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Location or grid reference for where the sample was taken.
- CEH_Sample_Code: CEH (Centre for Ecology & Hydrology) code associated with the sample.
- CEH_Sample_Description: Description of the CEH sample.
- Sample_Fresh_Mass_kg: Fresh mass of the sample in kilograms.
- Sample_Dried_Mass_kg: Dry mass of the sample in kilograms (not applicable for water samples).
- Not applicable for water samples: Indicates that certain mass fields do not apply to water samples.
- General_Notes: General notes about the sample.
- NGR (National Grid Reference): Clarifies that NGR is the national grid reference.
- Sample_Preparation_And_Analysis_Performed: Details of sample preparation and analyses conducted.

## GIS and Data Quality Considerations
- Location references: Uses Sampling_Location_Or_National_Grid_Reference (NGR) for geographical positioning; may require standard GIS handling and potential CRS transformation.
- Taxonomic names: Contains both Latin and Common names; consider standardizing to a single nomenclature for consistency.
- Mass fields: Sample_Fresh_Mass_kg and Sample_Dried_Mass_kg are in kilograms, with note that masses are not applicable for water samples.
- Data provenance: CEH_Sample_Code and CEH_Sample_Description link field data to laboratory records or descriptions.
- Metadata completeness: General_Notes and Sample_Preparation_And_Analysis_Performed provide context for interpretation and reproducibility.
- Data integration: Likely compiled from multiple sources (e.g., different sites or studies) requiring harmonization of fields and units.

## Practical Use Cases for GIS Specialists
- Map spatial distribution of species by site using Latin/Common names and grid references.
- Link field data to laboratory results via CEH_Sample_Code for integrated analyses.
- Visualize sample attributes (dates, masses, preparation/analysis performed) alongside spatial layers.
- Use NGR/OSGB grid references to align with other UK environmental datasets for policy or public-facing maps.

## Data Preparation and Packaging Notes
- Standardize field naming and data types across sources for seamless GIS joins.
- Harmonize species naming conventions (Latin vs Common) as needed.
- Validate and convert location references (NGR) to desired GIS coordinate system.
- Handle not-applicable fields (e.g., water samples) appropriately to prevent misinterpretation.
- Maintain clear metadata and documentation of data provenance, handling rules, and analysis methods.