# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

- Purpose and scope
  - Describes data tables for headwater stream invertebrate data from the 2007 Countryside Survey.
  - Key data tables: STREAM_INV_SITE_07.csv (sampling site data) and STREAM_INV_SP_07.csv (species data).
  - Methods overview: macroinvertebrates collected using standard protocols with 3 minutes active sampling plus 1 minute hand search over 5–15 m of stream, using a 1 mm mesh pond net; supplementary measurements (width, depth, substrate) for RIVPACS; QA sampling processed by external labs and internal CEH checks.

- Data tables and fields
  - STREAM_INV_SITE_07.csv (Freshwater stream - invertebrate sampling site data)
    - Core fields: YEAR, SQUARE (1 km square code), SITE_ID, SAMPLE_DATE.
    - Physical/habitat metrics: WATER_WIDTH (m), DEPTH1/DEPTH2/DEPTH3 (cm at 1/4, 1/2, 3/4 width), SURF_VEL_CAT (surface velocity category 1–5), SAMPLING_TIME (minutes).
    - Sampling method and landscape context: METHOD (sampling method code), ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY (percent cover of substrate types).
    - Land classification and geography: LC07, LC07_NUM (Land Class 2007), EZ_DESC_07 (environmental zone), COUNTRY, COUNTY07.
  - STREAM_INV_SP_07.csv (Freshwater Stream - invertebrate species data)
    - Core fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE.
    - Taxon data: SPECIES_CODE, NAME, ABUNDANCE (2007 only), LC07, LC07_NUM.
  - Notes: The tables include references to the ITE Land Classification of Great Britain 2007 and environmental zone coding; some fields have dual representations (numeric and text) to support context and cross-walks.

- Data collection, processing, and QA
  - Data flow: tablet entry at field, upload to CEH central database; laboratory identifications logged on paper then entered and cross-checked against lab sheets.
  - QA: 29 samples processed by APEM Laboratories Ltd; 10 main samples audited; internal audits of some QA samples; data-entry and identifications reconciled.
  - Taxonomy and abundance history: identification level and counting methods have changed across surveys; to enable comparability, species data were harmonised to a common modern taxonomy and abundance data were standardised (e.g., to mutually exclusive taxa for species richness).

- Data standardisation and harmonisation
  - Standardisation applied to align identifications across survey waves and to produce a mutually exclusive set of taxa for species richness calculations.
  - Underlying taxonomy updates and harmonisation ensure comparability with other Countryside Survey data despite historical changes in taxonomy and counting methods.

- Data quality, limitations, and considerations for analysts
  - Abundance recording methods changed over time; 2007 data include actual abundances for species and presence/absence for earlier years, necessitating harmonisation.
  - Metadata cover sampling design, site-level habitat covariates, and land classification context to support modelling and cross-dataset integration.
  - Data are stored with structured fields to facilitate merging with environmental covariates and with other years of Countryside Survey data.

- Access, usage, and acknowledgement
  - All use of Countryside Survey data must include acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
  - Countryside Survey ©; database rights/copyright held by NERC - CEH; all rights reserved.
  - Documents referenced for context: Murphy & Weatherby 2008 (Freshwater Manual); Dunbar et al. 2010 (Headwater Streams Report).

- Related materials and references
  - Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010. Countryside Survey: Headwater Streams Report from 2007.
  - Land classification: Bunce, R.G.H. et al. 2007. ITE Land Classification of Great Britain 2007. CEH Data Centre links provided.