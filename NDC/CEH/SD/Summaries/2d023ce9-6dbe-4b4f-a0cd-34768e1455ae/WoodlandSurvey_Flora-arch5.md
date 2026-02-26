# Woodlands Survey flora data 1971-2001

## Overview
- Survey of 103 broadleaved woodlands across Britain in 1971, with detailed data from 16 plots per site (2,000 m² each). Follow-up surveys occurred in 2000, 2002, and 2003 using the same field methods.
- Data collected include canopy and ground flora species composition, soil pH, Soil Organic Matter, habitat management, and a wide range of plot- and site-level descriptors.
- Analyses examine ecological change between 1971 and the follow-up years; explanatory variables include atmospheric deposition of sulfur and nitrogen, climate, canopy changes, and woodland management.
- Results and methods are published in related papers (e.g., Kirkby et al. 2005; Corney et al. 2004); users should consult these for methodological details and analytical results.
- Documentation and supporting materials (field handbook) are provided to support data use and replication.

## Data scope, design and provenance
- Design: Stratified sampling across the survey area; field methods follow Bunce & Shaw (1973) standardized procedures.
- Originators and custodians (timepoints):
  - 1971: R.G.H. Bunce & M.W. Shaw (Nature Conservancy, Merlewood)
  - 2001–2003: Simon Smart, Helaina Black (CEH Lancaster); Keith Kirby (English Nature); Phil Corney (University of Liverpool)
- Related datasets and context:
  - Countryside Survey; Steele (1968) National survey of woodlands; field handbook referenced in supporting documentation.

## Data structure and content
- Core data components (fields):
  - Site: numeric site code (1–103)
  - Plot: numeric plot number (1–16)
  - BRC_number: numeric species code (Biological Record Centre list)
  - BRC_names: text scientific name corresponding to BRC_number
  - Amalgams: numeric codes grouping selected species (cross-taxa amalgams)
  - Amalgam_names: text names for amalgam groups
  - NEST: numeric, indicates if an inner 2×2 m nest estimate applies (often inconsistently filled; not present in 1971 records)
  - COV: numeric cover percentage for the whole plot; coding includes 0.5 = <1% cover; -1 = bare ground/litter/wood/rock/total bryophyte/water
  - YR: year of survey (1971, 2000 pilot, 2002, 2003)
  - Yr_2: year code (1971 or 2000/2002/2003)
  - Bryo: text indicator (b = bryophyte; l = lichen)
  - Woody: text indicator (w = woody species)
  - Field_sheet: text reference to the original data sheet
- Data notes and caveats:
  - In the 2000s, bare ground/litter/water/rock/total bryophytes were amalgamated due to recording inconsistencies; multiple entries for a single plot code may occur.
  - Some records (e.g., for woody species) are stored as counts/DBH rather than cover; this influences interpretation across life-forms.
  - The dataset includes trees, shrubs, saplings, bryophytes and herbaceous species, all captured within the same structure.

## Data quality, limitations and governance considerations
- Governance and standardization challenges:
  - Incomplete picture of user needs and priorities; updates and timely data receipt can be challenging.
  - Encouraging data creators to meet standards for metadata, accuracy, and format consistency.
  - Integration across multiple systems and formats; handling large datasets; some databases may be outdated, requiring bespoke, non-interoperable solutions.
- Data quality considerations:
  - Amalgamation of certain taxa to address inconsistent separation; potential impact on species-level analyses.
  - Variable completeness in fields like NEST and Year coding; careful interpretation required when combining across survey years.
- Documentation and reuse:
  - Clear provenance through originators, standardized methods, and supporting field handbook.
  - Publications provide methodological context and results; users should reference these for analytical approaches.

## Access, storage and related resources
- Metadata and supporting documentation accompany the dataset (including the field handbook).
- Data and related materials are anchored by a DOI/link for access and citation.
- Related datasets and publications provide methodological context and longitudinal analysis results.

## References
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales.
- Corney, P.M. et al. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
- Haines-Young, R.H. et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
- Kirby, K.J. et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis based on the 103 sites in the Bunce 1971 woodland survey. English Nature Research Reports.
- Kirkby, et al. (2005). As cited for long-term ecological change analyses.