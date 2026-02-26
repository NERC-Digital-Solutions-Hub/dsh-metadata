# CP_Fish_SpeciesTable.txt

## Overview
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017
- Dataset description: Species list for fish species in the Chempop project
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Andy Nunn (a.d.nunn@hull.ac.uk)

## Data & File Overview
- File List: CP_Fish_SpeciesTable.csv
- Relationship between files: Fish_SpeciesCode refers to species in the Data Tables
- Additional related data collected but not included: none
- Multiple versions: no

## Provenance Information
- Data derived from: Chempop species codes adapted from Environment Agency (EA) National Fish Population Database (NFPD)

## Methodological Information
- Methods for collection/generation: Species with one Chempop code but multiple EA codes were summed into one code; taxa defined as "hybrids", "All species", "Salmonid species", "Freshwater species" were not assigned a Chempop code and were removed from the DataTable file
- Methods for processing: See above (aggregation of multiple EA codes into Chempop codes; removal of certain taxa)
- Instrument/software: none
- Quality assurance procedures: not applicable (n/a)

## Data-Specific Information
- Number of rows/columns: 4/93
- Number of variables: 4
- Variables:
  - Fish_SpeciesCode: unique Chempop code for each fish species
  - Latin_Name: scientific name from EA's NFPD
  - EA_SpeciesCode: EA-specific code from NFPD
  - Common_Name: common/vernacular name from NFPD
- Missing data codes: none