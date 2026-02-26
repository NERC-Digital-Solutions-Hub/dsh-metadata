# CP_Fish_SpeciesTable.txt

## Overview
- File generated on 2022/06/15 by Rachel Ainsworth.
- WP/task: Fish species and site variable data for Fish sites in English rivers 1975-2017.
- Dataset description: Species list for fish species in the Chempop project.
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Andy Nunn (a.d.nunn@hull.ac.uk).

## Data content and structure
- Data file: CP_Fish_SpeciesTable.csv.
- Relationship: Fish_SpeciesCode refers to species in the Data Tables.
- Versions: No multiple versions of the dataset.
- Data specifics: Number of rows/columns = 4/93; Number of variables = 4.
- Variables:
  - Fish_SpeciesCode: unique Chempop code for each fish species.
  - Latin_Name: scientific name from Environment Agency's National Fish Population Database (NFPD).
  - EA_SpeciesCode: unique Environment Agency code for each taxon in NFPD.
  - Common_Name: common/vernacular name as recorded in NFPD.
- Missing data codes: none.

## Provenance
- Data derived from Chempop species codes adapted from Environment Agency (EA) species codes used in the EA National Fish Population Database (NFPD).

## Methodology and data processing
- Data collection/generation: Taxa with a single Chempop code but multiple EA codes (e.g., strains/variants) were summed into one Chempop code; taxa defined as "hybrids", "All species", "Salmonid species", "Freshwater species" were not assigned a Chempop code and removed from the DataTable.
- Data processing: The same approach as above; non-assigned taxa removed from the DataTable file.
- Instrument/software: None specified.
- QA: Not applicable or not described.

## Data fields (summary)
- Fish_SpeciesCode: Unique Chempop code for each species used in Chempop.
- Latin_Name: Scientific name from NFPD.
- EA_SpeciesCode: Unique EA code for each taxon in NFPD.
- Common_Name: Common name from NFPD.

## Usage considerations
- The CSV links Chempop codes to Latin and EA codes to facilitate cross-referencing across datasets.
- Suitable for mapping and cross-walking species names/codes between Chempop and EA/NFPD datasets.
- Note: Only 4 records are present, suggesting a concise, targeted species table; ensure compatibility with broader datasets that may contain more taxa.