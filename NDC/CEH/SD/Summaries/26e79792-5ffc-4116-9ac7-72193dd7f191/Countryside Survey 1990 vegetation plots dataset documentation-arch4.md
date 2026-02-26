# Countryside Survey 1990: vegetation plot data, Great Britain Dataset Documentation

- Overview
  - Provides vegetation plot data from Countryside Survey 1990 across Great Britain (England, Scotland, Wales).
  - Dataset consists of two CSV files: one with plot information and one with species lists per plot.
  - Species nomenclature follows Stace (1997).

- Dataset contents
  - Plot Information 1990.csv
    - YEAR: Year of survey
    - SQUARE_ID: Survey square identifier
    - PLOT_ID: Plot identifier
    - PLOT_TYPE: Type of plot
    - COUNTRY: ENG, SCO, or WAL
    - ENV_ZONE_2007: Environmental Zone number (2007 version)
    - EZ_DESC_07: Environmental Zone description (2007 version)
  - Species List 1990.csv
    - YEAR: Survey year
    - SQUARE_ID: Survey square identifier
    - PLOT_ID: Plot identifier
    - AMALG_PTYPE: Plot type
    - BRC_NUMBER: Species identifier
    - BRC_NAMES: Species name
    - NEST_LEVEL: Nest species first recorded in
    - FIRST_COVER: Percent cover in first nest
    - TOTAL_COVER: Percent cover in whole plot

- Data structure and nomenclature
  - Two-file structure: one for plot metadata, one for species composition per plot.
  - Nomenclature aligned with Stace, 1997 (New Flora of the British Isles).

- Data governance and use
  - Acknowledgement required on all copies, publications, and presentations:
    - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
    - Countryside Survey © Database Right/Copyright NERC-Centre for Ecology & Hydrology. All rights reserved.
  - The dataset supports integration into wider data systems, with metadata and zone classifications to aid compatibility and discoverability.

- References and related resources
  - Countryside Survey Website: general overview and methodologies
  - Carey et al. (2008): Countryside Survey UK Results from 2007
  - Countryside Survey Environmental Zones: zoned areas of Great Britain with metadata
  - Barr, C.J. (1991/1990): Countryside Survey Field Handbook (field methodology)
  - Related data documentation and access links are provided in the references.