# Countryside Survey 1990: vegetation plot data, Great Britain Dataset Documentation

- Objectives and scope
  - Provides vegetation plot data collected in 1990 across Great Britain (England, Scotland, Wales) for the Countryside Survey project.
  - Enables baseline assessment of environmental health measures and supports monitoring, evaluation, and future decision-making.
  - Data can be used to monitor vegetation change over time, compare with later surveys (e.g., 2007 results), and assess environmental zones.

- Dataset components and structure
  - Two CSV files:
    - Vegetation Plot - Plot Information 1990.csv
      - YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, COUNTRY, ENV_ZONE_2007, EZ_DESC_07
    - Vegetation Plot - Species List 1990.csv
      - YEAR, SQUARE_ID, PLOT_ID, AMALG_PTYPE, BRC_NUMBER, BRC_NAMES, NEST_LEVEL, FIRST_COVER, TOTAL_COVER
  - Content highlights
    - Plot metadata (year, square/plot identifiers, plot type, country)
    - Environmental zoning data (ENV_ZONE_2007, EZ_DESC_07)
    - Species data (BRC_NUMBER, BRC_NAMES) with cover metrics (FIRST_COVER, TOTAL_COVER) and nesting level indicator (NEST_LEVEL)
  - Taxonomy and nomenclature
    - Species names follow Stace, 1997: New flora of the British Isles

- Data provenance, rights, and acknowledgments
  - Data owned by NERC - Centre for Ecology & Hydrology
  - Acknowledgment and copyright notice required on all uses
  - Explicit acknowledgement: Countryside Survey data owned by NERC - CEH; all rights reserved

- Metadata, documentation, and references
  - Metadata and field methodology linked to Barr, 1991 (Countryside Survey Field Handbook)
  - Key publications: Carey et al. 2008 Countryside Survey: UK Results from 2007 (background and methodology)
  - Environmental Zones metadata available via associated links/databases
  - Related project documentation and website references provided for methodology and context

- How this dataset supports environmental monitoring frameworks
  - Provides a standardized, plot-level baseline for vegetation composition and cover in 1990
  - Enables stratification by environmental zones (EZ_07) for spatially explicit monitoring
  - Facilitates calculation of vegetation metrics (species presence, percent cover) for policy evaluation and trend analysis
  - Supports cross-temporal comparisons with later Countryside Survey results to assess trends in habitat condition and biodiversity

- Data quality, limitations, and considerations
  - Taxonomic reference is historical (Stace 1997); users should account for potential nomenclature changes over time
  - Metadata completeness and consistency can influence ease of verification and reuse
  - Data sharing and format transformation may require effort to standardize for integration with other datasets
  - The dataset emphasizes transparency and openness, but practical access may require adherence to acknowledgement requirements

- Context and usage notes
  - Designed to be used with Countryside Survey methodologies; cross-referencing with Barr (1991) Field Handbook recommended
  - Useful for analysts building monitoring frameworks that require baseline vegetation structure, species composition, and environmental zone stratification

- References and access
  - Countryside Survey Website and publications for broader context and methodology
  - Barr, C.J. (1991) Countryside Survey Field Handbook
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Environmental Zones metadata and data documentation links provided in the dataset notes