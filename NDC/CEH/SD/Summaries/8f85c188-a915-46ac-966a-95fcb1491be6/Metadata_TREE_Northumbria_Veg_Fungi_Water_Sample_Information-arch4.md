# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

## Overview
- Schema for recording sampling information related to vegetation, fungi, and water samples from Northumbria.
- Captures taxonomic names, sampling site and location, collection date, sample identifiers, mass measurements, descriptive notes, and processing details.

## Key Fields and Field-Level Details
- Latin_Species_Name
  - Explanation: Latin name of species
  - Units: n/a
- Common_Species_Name
  - Explanation: Common name of species
  - Units: n/a
- Site
  - Explanation: Sampling site
  - Units: n/a
- Date_Sample_Collected
  - Explanation: Date the sample was collected
  - Units: n/a
- Sampling_Location_Or_National_Grid_Reference
  - Explanation: Sampling location or National Grid Reference
  - Units: n/a
- CEH_Sample_Code
  - Explanation: CEH sample code associated with sample
  - Units: n/a
- CEH_Sample_Description
  - Explanation: CEH sample description
  - Units: n/a
- Sample_Fresh_Mass_kg
  - Explanation: Fresh mass of sample in kilograms
  - Units: kg
  - Note: Not applicable for water samples
- Sample_Dried_Mass_kg
  - Explanation: Dry mass of sample in kilograms
  - Units: kg
  - Note: Not applicable for water samples
- General_Notes
  - Explanation: General notes
  - Units: n/a
- Sample_Preparation_And_Analysis_Performed
  - Explanation: Sample preparation of sample and analysis performed
  - Units: n/a

## Data Quality and Metadata Considerations
- Some fields indicate units as not applicable (n/a); ensure consistent interpretation across records.
- National Grid Reference (NGR) standardizes location data; important for geospatial querying and mapping.
- Mass fields include explicit note about non-applicability to water samples; necessary for preventing invalid data entry.
- Clear definitions in Explanation fields support data discoverability and interoperability (e.g., CEH_Sample_Code for traceability).

## Data Governance and Use for Data Leaders
- Ensure metadata completeness to improve discoverability and reuse across networks.
- Use CEH_Sample_Code and CEH_Sample_Description to maintain provenance and link analyses to specific samples.
- Maintain consistent formatting for dates, site identifiers, and location references to enable reliable aggregation and comparison.
- Coordinate with partners to standardize field meanings and units, reducing data silos and duplication of effort.
- Track sample preparation and analysis details to support reproducibility and downstream analytics.

## Practical Implementation Notes
- When integrating with other datasets, align species naming (Latin and Common) and ensure taxonomic updates are reflected.
- Validate mass fields to enforce applicability rules (e.g., omit or flag Fresh Mass and Dry Mass for water samples).
- Leverage the metadata to support stakeholder-driven data products (e.g., policy or research teams) through clear notes and descriptions.