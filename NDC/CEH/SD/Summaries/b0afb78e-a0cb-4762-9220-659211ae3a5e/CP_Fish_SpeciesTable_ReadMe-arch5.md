# CP_Fish_SpeciesTable.txt

## Overview
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017
- Dataset description: Species list for fish species in the chempop project
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Andy Nunn (a.d.nunn@hull.ac.uk)
- File: CP_Fish_SpeciesTable.csv
- Relationship: Fish_SpeciesCode refers to species in the Data Tables
- Versions: No multiple versions

## Provenance and Methodology
- Source data: Chempop species codes adapted from Environment Agency (EA) National Fish Population Database (NFPD)
- Data transformation:
  - Species with one Chempop Code but multiple EA Codes (e.g., strains/variants) were summed into one Chempop code
  - Taxa defined as "hybrids", "All species", "Salmonid species", and "Freshwater species" were not assigned a Chempop code and were removed from the DataTable
- Processing methods: Reiterates the same aggregation and exclusion rules as above
- Instrument/Software: None specified
- Quality assurance: Not described (n/a)

## Data Structure

- Rows/Columns: 4 rows, 93 columns (4 variables)
- Variables:
  - Fish_SpeciesCode: unique Chempop code for each fish species
  - Latin_Name: scientific name from EA's NFPD
  - EA_SpeciesCode: EA NFPD code for the taxon
  - Common_Name: common/vernacular name from NFPD
- Missing data codes: None

## Data Governance and Usage
- Metadata scope: Provides mapping between Chempop codes and EA/NFPD nomenclature for consistent dataset integration
- User needs alignment: Ensures standardized species identifiers and names for discoverability and use in joint datasets
- lineage and reproducibility: Derived from EA NFPD; maintained via Chempop codes
- Notes for stewards: No QA procedures described; no versioning beyond stated information

## Access and Contact
- File list: CP_Fish_SpeciesTable.csv
- Relationship: Fish_SpeciesCode corresponds to species in the related data tables
- Updates: No updates indicated
- Contacts: Rachel Ainsworth (r.ainsworth@hull.ac.uk); Andy Nunn (a.d.nunn@hull.ac.uk)