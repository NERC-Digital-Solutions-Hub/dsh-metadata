# Woodlands Survey tree diameter data 1971-2001

- Overview
  - Dataset from a Britain-wide survey in 1971 of 103 broadleaved woodlands.
  - Detailed ecological data collected at site level and from 16 randomly located 200 m² plots per site.
  - Re-surveyed in subsequent years (2000, 2002, 2003; referred to as 2001) using identical field methods to assess ecological change.
  - Analyses link ecological change to drivers such as atmospheric deposition of sulfur and nitrogen, climate, canopy structure, and woodland management; findings published in Kirkby et al. (2005) and Corney et al. (2004).

- Study Design & Data Collection
  - Stratified sampling across the landscape; field methods follow Bunce & Shaw (1973) standardized procedures.
  - Data collected include canopy and ground flora, soil pH, Soil Organic Matter, habitat management, and a wide range of plot and site descriptors.
  - Re-surveys used exactly the same methods to ensure comparability over time.
  - Related datasets and prior surveys referenced (e.g., Countryside Survey; Steele 1968).

- Temporal Coverage
  - Baseline year: 1971.
  - Follow-up surveys: 2000s (referred to as 2001 for documentation purposes).
  - Temporal focus on long-term ecological change across approximately 30-year interval.

- Data Structure & Variables
  - Site: numeric code (1–103).
  - Plot: numeric (1–16).
  - BRC_number: numeric code for species (Biological Record Centre list).
  - BRC_names: textual scientific names.
  - Amalgams: numeric code for inconsistently recorded taxa; grouped taxa (e.g., Quercus spp.).
  - Amalgam_names: textual names for amalgamated taxa.
  - Status: numeric (Live or Dead).
  - DBHclass: numeric 5 cm interval band (1–32) representing diameter at breast height classes.
  - Count: numeric count of individuals per DBH class (sapot/Saplings counted differently across quarters).
  - Final_count: numeric final count per DBH class per plot.
  - Yr: numeric year indicator (1 = 1971; 2 = 2000s).
  - Woody: textual flag ('w' for woody).
  - Field_sheet: textual reference to the original data recording sheet.
  - The DBH class ranges and corresponding class numbers are detailed in the dataset's accompanying schema.

- Provenance & Access
  - Originators (1971): Bunce & Shaw (Woodland Ecology Section, Nature Conservancy Merlewood) and colleagues.
  - 2001-3 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH Lancaster, English Nature, University of Liverpool).
  - Supporting documentation available (field handbook and methodological notes).
  - Related publications provide methodological and analytical context for long-term change analyses.

- Documentation & References
  - Key publications for methods and results:
    - Corney et al. (2004): landscape-scale environmental drivers on vegetation composition.
    - Kirby et al. (2005): measuring long-term ecological change in British woodlands (1971–2001).
  - Foundational references: Avery (soil classification), Haines-Young et al. (landscape change), and Steele (national survey context).