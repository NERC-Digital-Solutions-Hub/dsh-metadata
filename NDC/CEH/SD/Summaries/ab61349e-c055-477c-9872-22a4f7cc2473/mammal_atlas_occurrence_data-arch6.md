# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

- Overview
  - Provides summarized 10km grid-based mammal occurrence data for Great Britain and Northern Ireland, covering recording periods 1960-1992 and 2000-2016 as mapped in the 2020 Mammal Atlas.
  - Excludes cetaceans from the dataset; cetacean data are handled separately by Sea Watch Foundation.
  - For each species, lists the 10km grid squares with recorded occurrences in the current atlas period and/or the previous atlas period.
  - Time periods vary by a few species due to rapid distribution changes; most species use 1960-1992 and 2000-2016, with some exceptions noted in the dataset.

- Background and purpose
  - Atlas produced by the Mammal Society with assistance from Sea Watch Foundation, UKCEH, and other partners.
  - Builds on earlier MaWSE project and the Mammal Tracker app; expanded to cover the UK, Isle of Man, and Channel Islands.
  - Data underpin related publications and national/regional red lists; intended to support data use, interpretation, and further data products.

- Data collection and validation
  - Data come from diverse sources: National Biodiversity Network (NBN) gateway, local biological records centres, monitoring schemes, Natural England, Mammal Society, Sea Watch Foundation, iRecord, and Mammal Tracker.
  - Validation varies by source; majority are opportunistic citizen science records with some structured surveys and professional data.
  - External data are assumed credible if prior validation is not documented; Mammal Society verifiers validate data from iRecord and Mammal Tracker records.
  - Expert review of 10km squares: flagged squares are re-examined at the record level to decide retention or exclusion.
  - To reduce misidentifications, some datasets from non-mammal-focused schemes were limited to widely recognized species; records for common species (e.g., mole, rabbit, badger, fox, hedgehog) included to minimize errors.
  - The atlas maps for each species are reviewed by experts before final publication.

- Cetaceans
  - Cetacean data are not included in this dataset; Sea Watch produced cetacean accounts and maps separately.
  - For cetacean inquiries, contact Sea Watch Foundation.

- Dataset structure and contents
  - Provided as a CSV file with one or more rows per 10km grid square per species.
  - Key fields (per row):
    - SPECIES, DESCRIPTION: scientific name of the species.
    - COMMON_NAME, DESCRIPTION: common name.
    - GRIDREF, DESCRIPTION: 10km grid square reference (OGB for GB, OSI for NI, truncated MGRS for Channel Islands).
    - CATEGORY, DESCRIPTION: time-period category (1960-1992; 1960-1992 & 2000-2016; 2000-2016); notes on species with alternative recent periods.
    - TP_1960_1992, DESCRIPTION: whether observed in the 1960-1992 period (1=yes, null/missing=no).
    - TP_2000_2016, DESCRIPTION: whether observed in the 2000-2016 period (1=yes, null/missing=no); note exceptions for a few species.
    - LATITUDE, LONGITUDE, DESCRIPTION: WGS84 center coordinates of the 10km grid square.
    - ENG, SCO, WAL, N_IRE, DESCRIPTION: flags indicating whether the square is in England, Scotland, Wales, Northern Ireland (1=yes, null/missing=no).
    - CD, DESCRIPTION: Crown Dependencies (Channel Islands or Isle of Man).
    - ROI, DESCRIPTION: Republic of Ireland.
  - Spatial formats:
    - CSV for straightforward data ingestion and analysis.
    - Geopackage (.gpkg) with each species as a separate layer; polygons map 10km squares (center coordinates correspond to the CSV fields; includes OSGB 36 / British National Grid, EPSG: 27700).
    - NI and Channel Islands squares re-projected to the British Grid for the Geopackage.

- Geographic scope and grid details
  - Spatial units are 10km grid squares; some squares are coastal or marine and assigned to the closest country.
  - Grid reference systems vary by region:
    - Ordnance Survey GB (OGB) for Scotland, England, Wales, Isle of Man.
    - Ordnance Survey Ireland (OSI) for Northern Ireland.
    - truncated MGRS for Channel Islands.
  - Example reference handling: a 30U-based MGRS segment is shortened (e.g., 30UWV64 becomes WV64).

- Time periods and species-specific notes
  - Most species: 1960-1992 and 2000-2016 periods.
  - Shorter recent periods used for:
    - Water vole (Arvicola amphibius): 2005-2016
    - Red squirrel (Sciurus vulgaris): 2010-2016
    - Grey squirrel (Sciurus carolinensis): 2010-2016

- Access, usage and caveats
  - Data compiled from multiple sources with varying validation detail; use the validation notes when interpreting records.
  - Cetacean data not included; separate channels exist for cetacean records.
  - Useful for creating self-serve data products (dashboards, pivot analyses, maps) and supporting data-driven decision making in policy, conservation, and planning contexts.

- References
  - Arnold, H. (1993). Atlas of mammals in Britain.
  - Hayhow, D.B. et al. (2019). The State of Nature 2019.
  - Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
  - Mathews, F., & Harrower, C. (2020). IUCN - compliant Red List for Britain's Terrestrial Mammals.