# CP_Fish_SpeciesTable.txt

## Overview
- File generated on 2022/06/15 by Rachel Ainsworth.
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017.
- Dataset: Species list for fish species in the Chempop project.
- Purpose for analysts: provides a standardized mapping between Chempop codes and EA/NFPD codes to support consistent environmental monitoring and health assessments over time.

## Data Structure and File Relationships
- File List: CP_Fish_SpeciesTable.csv.
- Relationship: Fish_SpeciesCode refers to species in the Data Tables.
- Additional related data collected but not included: none specified.
- Versions: no multiple versions indicated.

## Provenance
- Data derived from: Chempop species codes adapted from Environment Agency (EA) National Fish Population Database (NFPD) codes.

## Methodology and Processing
- Data generation approach:
  - If a Chempop Species Code corresponds to multiple EA Species Codes (e.g., strains/variants), these are summed into a single Chempop code.
  - Taxa defined as "hybrids", "All species", "Salmonid species", or "Freshwater species" were not assigned a Chempop Species Code and were removed from the DataTable file.
- Instrument/software details: none required.
- Quality assurance: no QA procedures described for source or output data.

## Data Specifications for CP_Fish_SpeciesTable.csv
- Number of rows/columns: 4/93.
- Number of variables: 4.
- Variable list:
  - Fish_SpeciesCode: unique Chempop code for each fish species.
  - Latin_Name: scientific name from EA's NFPD.
  - EA_SpeciesCode: EA/NFPD code for the taxon.
  - Common_Name: common vernacular name from the NFPD.
- Missing data codes: none.

## Notes and Considerations
- The table provides the canonical linkage between Chempop and EA/NFPD identifiers to enable standardized reporting and cross-dataset analyses.
- No additional related data or version history beyond the stated creation date.