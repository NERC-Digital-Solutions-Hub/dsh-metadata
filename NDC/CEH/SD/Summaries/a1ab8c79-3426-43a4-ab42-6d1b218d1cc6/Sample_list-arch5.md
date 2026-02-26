# Supporting documentation for Sample_list.csv

## Overview
- Defines the structure and metadata for the Sample_list.csv dataset, detailing each field’s meaning, data type expectations, and how it should be used in data curation, sharing, and governance.

## Fields
- Sample_Code
  - Explanation: Unique sample identifier
  - Units: n/a
  - Notes: 
- RAP
  - Explanation: ICRP Reference Animals and Plant (RAP) classification into which the sampled species can be attributed
  - Units: n/a
  - Notes: 
- Sample_Description
  - Explanation: Part of the organism analysed (e.g., whole organism vs. a specific part)
  - Units: n/a
  - Notes: 
- Collection_Date
  - Explanation: Date of sample collection
  - Units: dd-mmm-yy
  - Notes: 
- Dry/Fresh_Ratio
  - Explanation: Dry to fresh weight ratio
  - Units: unitless
  - Notes: 
- Coordinates_of_the_Sample
  - Explanation: Grid reference of sampling location
  - Units: decimal degrees and minutes
  - Notes: 
- Sample_Association
  - Explanation: Unique sample identifier of soil sampled at the same site
  - Units: n/a
  - Notes: 
- Notes
  - Explanation: Additional comments (where applicable)
  - Units: n/a
  - Notes: 

## Data governance and quality considerations for Data Stewards
- Standardization: enforce consistent field names, units, and formats across datasets to ensure interoperability.
- Controlled vocabularies: align RAP classifications and Sample_Description with approved vocabularies or ontologies.
- Date and location accuracy: require Collection_Date to follow the dd-mmm-yy format; ensure Coordinates_of_the_Sample uses the specified decimal degrees and minutes reference system.
- Metadata completeness: capture Notes where applicable and maintain clear linkage via Sample_Code and Sample_Association for traceability.
- Data updates: implement processes for updates and versioning to keep data current and maintain provenance.