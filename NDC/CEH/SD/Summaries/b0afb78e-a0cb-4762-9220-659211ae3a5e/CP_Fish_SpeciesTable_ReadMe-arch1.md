# CP_Fish_SpeciesTable.txt

## Overview
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017
- Dataset description: Species list for fish species in the Chempop project

## Data content
- File: CP_Fish_SpeciesTable.csv
- Structure: 4 rows, 93 columns
- Variables (4 total):
  - Fish_SpeciesCode: unique code for each fish species used in Chempop
  - Latin_Name: scientific name from Environment Agency's National Fish Population Database (NFPD)
  - EA_SpeciesCode: EA's unique code for each fish taxon in NFPD
  - Common_Name: common/vernacular name from EA NFPD
- Missing data codes: none

## Provenance and processing
- Source: Chempop species codes adapted from EA species codes used in EA National Fish Population Database
- Data processing rules:
  - Species with one Chempop Code but multiple EA Codes (e.g., strains/variants) were summed into a single Chempop code
  - Taxa defined as "hybrids", "All species", "Salmonid species", "Freshwater species" were not assigned a Chempop Code and removed from the DataTable file

## Data relationships
- Relationship to other data: Fish_SpeciesCode refers to species in the Data Tables

## Data specifics
- Number of rows/columns: 4 / 93
- Number of variables: 4
- Missing data: none

## Notes on scope and availability
- No multiple versions of the dataset
- Describes fish species observed across English rivers (1975-2017) in the Chempop context