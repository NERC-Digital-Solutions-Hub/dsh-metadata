# CP_Fish_SpeciesTable.txt

## Overview
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017
- Dataset description: Species list for fish species in the chempop project
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Andy Nunn (a.d.nunn@hull.ac.uk)
- Generation date: 2022/06/15

## Data Content and Structure
- File(s): CP_Fish_SpeciesTable.csv
- Data shape: 4 rows x 93 columns in CP_Fish_SpeciesTable.csv; 4 variables (columns)
- Variables:
  - Fish_SpeciesCode: unique code for each fish species used in the Chempop project
  - Latin_Name: scientific name from Environment Agency’s National Fish Population Database (NFPD)
  - EA_SpeciesCode: unique EA code for each fish taxon from the NFPD
  - Common_Name: common/vernacular name from the NFPD
- Data completeness: No missing data codes reported

## Data Lineage and Provenance
- Origin: Derived from Environment Agency (EA) National Fish Population Database (NFPD)
- Chempop mapping: Chempop Species Codes adapted from EA species codes
- Data processing rules:
  - When one Chempop code maps to multiple EA codes (e.g., strains/variants), those EA codes were summed into a single Chempop code
  - Taxa defined as "hybrids", "All species", "Salmonid species", and "Freshwater species" were not assigned a Chempop code and were removed from the DataTable file
- Relationship to other data: Fish_SpeciesCode in this file refers to species in the Data Tables

## Data Quality and Documentation
- Instrumentation/software: None specified
- QA procedures: Not documented
- Notes on scope: The dataset provides a consolidated mapping of Chempop codes to EA codes and common/scientific names, with certain broad taxa excluded

## Access, Usage, and Versioning
- Data assets: CP_Fish_SpeciesTable.csv
- Relationship to other data: Fish_SpeciesCode links to other Data Tables
- Versions: No multiple versions of the dataset listed

## Authors, Contact, and Use Constraints
- Authors: Rachel Ainsworth; Andy Nunn
- Contacts: r.ainsworth@hull.ac.uk; a.d.nunn@hull.ac.uk
- Versioning: Not indicated; current entry reflects a single version with no updates noted

## Gaps, Limitations, and Considerations for Data Leaders
- Gaps: Not all taxonomic categories are assigned a Chempop code (e.g., hybrids, broad taxa) and are removed from this DataTable
- Access considerations: Based on EA NFPD codes; potential alignment issues if codes are updated in external sources
- Usability: 4 rows indicate a limited set of species included in this mapping; ensures linkage across Data Tables via Fish_SpeciesCode