# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Presents 10km (and finer) mammal occurrence data used in the 2020 Atlas of Mammals of Great Britain and Northern Ireland, excluding cetaceans.
- Covers 1960-1992 and 2000-2016 recording periods; GB, Northern Ireland, Isle of Man, and Channel Islands contexts; cetacean data are provided separately by Sea Watch and not included in this dataset.
- Aims to describe where species were recorded in the Atlas, with some periods adjusted for rapid distribution changes in a few species.

## Atlas background and scope
- Produced by the Mammal Society with collaborators (Sea Watch Foundation, BRC, UK CEH, Staffordshire Mammal Group).
- Originated from the Mammal Watch South East (MaWSE) project and the Mammal Tracker recording app; later expanded to national coverage and the Mammal Mapper app.
- Data support publications on mammal populations, conservation status, red lists, and State of Nature.

## Data collection and sources
- Aggregated from diverse sources: National Biodiversity Network (NBN) gateway (NBN Atlas), local biological records centers, local and national monitoring schemes, Natural England, the Mammal Society, the Biological Records Centre, Sea Watch Foundation, iRecord, and the Mammal Tracker app.
- Major portion of data are opportunistic citizen-science records; some datasets are more structured (surveys) or professional.

## Validation and quality assurance
- External datasets often carried prior validation; explicit record-level validation not always available across sources.
- Mammal Society verifiers validated data from iRecord and Mammal Tracker; other sources assumed credible unless indicated otherwise.
- To mitigate errors, 10km square maps were reviewed by species experts; records in highlighted squares were re-examined at the record level before final inclusion or exclusion.
- Some datasets (especially non-primary mammal surveys) contributed a higher proportion of dubious or misidentified records; limits acknowledged.

## Cetaceans
- Cetacean data are included in the Atlas but not integrated into this dataset; maps and species accounts for cetaceans are produced by Sea Watch. For cetacean data inquiries, contact Sea Watch.

## Dataset structure and access
- CSV dataset: per species, includes grid squares with recorded occurrences for the current (2000-2016) and/or previous (1960-1992) atlas periods.
  - Key fields: SPECIES, COMMON_NAME, GRIDREF, CATEGORY (time period coverage), TP_1960_1992, TP_2000_2016, LATITUDE, LONGITUDE, ENG/SCO/WAL/N_IRE indicators, Crown Dependencies/ROI indicators.
  - Grid reference systems used: OSGB for GB-wide squares; OSI for Northern Ireland; truncated MGRS for Channel Islands.
- Geopackage (gpkg): polygonal representation of 10km squares, with a separate layer per species; uses OSGB 36 (EPSG: 27700). NI and Channel Islands coordinates re-projected to British Grid for consistency.
- Metadata integrity: same attribute fields in both CSV and GeoPackage; includes country attribution and time-period categorization.

## Time periods and species-specific notes
- Most species: data for 1960-1992 and 2000-2016.
- Species with adjusted periods: Water vole (2005-2016), Red squirrel (2010-2016), Grey squirrel (2010-2016) to reflect distribution updates.

## Data governance, discovery, and collaboration
- Data assembled from a broad network of partners and citizen-science platforms, emphasizing broad participation and public involvement in data collection.
- Emphasizes data discoverability via multiple sources (CSV and GeoPackage) and explicit documentation of coordinate systems and country divisions.

## Limitations and considerations for use
- Heterogeneous data quality due to varied collection methods; reliance on opportunistic records may introduce biases.
- Validation intensity varies by source; some records may not have undergone detailed record-level validation.
- Caution advised when combining with other datasets due to differences in time periods, grid systems, and validation status.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN - compliant Red List for Britain's Terrestrial Mammals.