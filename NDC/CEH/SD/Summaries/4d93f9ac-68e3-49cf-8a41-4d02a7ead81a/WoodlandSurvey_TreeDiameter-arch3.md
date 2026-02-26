# Woodlands Survey tree diameter data 1971-2001

- A long-term, Britain-wide ecological dataset from 103 broadleaved woodlands, with detailed plot-level data collected in 1971 and revisited in 2000s (2000, 2002, 2003) using identical field methods.
- Data collected at site level and from 16 randomly placed 200 m2 plots per site, including canopy and ground flora, soil pH, soil organic matter, habitat management, and a wide range of plot and site descriptors.
- Objective: analyze ecological change over time and identify principal drivers using assembled explanatory variables (atmospheric deposition of sulfur and nitrogen, climate, canopy structure changes, woodland management).

- Survey design and methods:
  - Stratified sampling across the 103 sites.
  - Followed Bunce & Shaw (1973) standardized survey methods; field handbook included in supporting docs.
  - Re-survey period used the same methodologies to enable comparability.

- Data structure and contents:
  - Site and plot identifiers (Site, Plot).
  - BRC_number and BRC_names: species codes and scientific names (as per Biological Record Centre).
  - Amalgams and Amalgam_names: grouped taxa where records were inconsistent (e.g., Quercus spp.).
  - Status: alive or dead.
  - DBHclass: diameter at breast height class (5 cm bands, with 1-32 mapping).
  - Count and Final_count: number of individuals per DBH class per plot (with saplings/shrubs adjusted for sampling quarters).
  - Yr: 1 = 1971, 2 = 2000s (re-survey year).
  - Woody: 'w' if woody species.
  - Field_sheet: source data sheet.
  - DBH Range and DBH Class mappings: detailed scheme aligning ranges to class numbers (across multiple columns).

- Origin and provenance:
  - 1971 originators: R.G.H. Bunce & M.W. Shaw (Woodland Ecology Section, Nature Conservancy Merlewood).
  - 2001-2003 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH Lancaster, English Nature, University of Liverpool).

- Related datasets and publications:
  - Related: Countryside Survey.
  - Earlier and related work: Steele (1968) National survey of woodlands; Corney et al. (2004); Kirby et al. (2005) on long-term ecological change in British woodlands.

- Supporting documentation and references:
  - Field methods handbook and supporting docs.
  - References detailing methodological background and analyses of drivers of woodland change.

- Implications for environmental health monitoring and policy:
  - Provides a robust, long-term basis for evaluating woodland ecological change and testing drivers relevant to policy decisions.
  - Demonstrates the value of consistent methods over time for trend analysis and for attributing change to atmospheric, climatic, and management factors.
  - Highlights the importance of metadata, data provenance, and clear data structures (e.g., standardized species coding, DBH classifications) for integrating datasets into monitoring frameworks.

- Considerations for data governance and living datasets (relevant to monitoring frameworks):
  - Data sharing and metadata quality are essential to enable reuse across programs.
  - Clear data lineage and documentation support transparency in monitoring results.
  - Consistency of methods across time enhances comparability but requires careful handling of any amalgams or inconsistent records.