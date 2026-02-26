# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

- Purpose and scope
  - Describes headwater stream invertebrate data collected in 1990 as part of the Countryside Survey.
  - Data are prepared to support cross-year analyses, with harmonisation and standardisation to enable comparability.
  - References key manuals and reports (Murphy & Weatherby 2008; Dunbar et al. 2010) for methods and context.

- Data structure and content
  - Two main data tables:
    - STREAM_INV_SITE_90.csv: Freshwater stream invertebrate sampling site data, 1990.
      - Key fields include YEAR, SQUARE (1 km grid), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT, CLARITY, SAMPLING_TIME, METHOD, substrate composition (% rock pavement, boulder/cobble, pebbles/gravel, sand, silt/clay), DOM_PART_SIZE, MACROPHYTE_COVER, LC07 (land class 2007), LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07, etc.
    - STREAM_INV_SP_90.csv: Freshwater stream invertebrate species data, 1990.
      - Key fields include YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07, etc.
  - Taxonomic and coding considerations
    - Species data include scientific names and authority where applicable.
    - Land classification (LC07) and environmental zones (EZ_DESC_07) are included to contextualize habitats.
  - Data usage notes
    - All use of Countryside Survey data must include formal acknowledgement.

- Methods and data processing
  - Field and sampling protocol
    - Sampling area in stream bed (5–15 m length) with approx. 3 minutes of active sampling plus 1 minute of hand search.
    - Standard 1 mm mesh pond net used; samples returned to CEH for sorting and identification.
    - Supplemental measurements captured (width, depth, substrate) to support RIVPACS analyses.
  - Taxonomy and data harmonisation
    - Taxonomic identifications and abundance recording changed over time (1990, 1998, 2007); data harmonised to a common modern taxonomy to enable comparability.
    - A separate standardisation process derives a mutually exclusive taxa list for calculating species richness.
  - Data entry and quality assurance
    - Field identifications performed in the laboratory.
    - Data entered from paper field sheets into a database; cross-checked against original lab sheets with corrections for any data-entry errors.

- Data governance, rights, and provenance
  - Data provenance
    - Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology; data are provided under the Countryside Survey framework.
  - Acknowledgement and copyright
    - Acknowledgement text required on all copies, publications, and presentations: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC-Centre for Ecology & Hydrology. All rights reserved.”
  - Documentation and references
    - Primary methodological references: Murphy & Weatherby (2008) Freshwater Manual; Dunbar et al. (2010) Headwater Streams Report.
    - Data are versioned (Version 1: 19/10/2016) and intended to be used alongside supporting information.

- Relevance for Data Stewards
  - Data management and governance
    - Ensure metadata completeness for STREAM_INV_SITE_90.csv and STREAM_INV_SP_90.csv, including variable definitions, units, and data standards.
    - Maintain cross-year harmonisation mappings and updated taxonomic standards to support longitudinal analyses.
  - Data quality and usability
    - Preserve the documented data-entry workflow (paper → database → QA checks) to support reproducibility.
    - Track any updates to classifications (taxonomic changes, land classes, environmental zones) and reflect in data catalogues.
  - Access, licensing, and attribution
    - Enforce acknowledgement requirements and ensure proper attribution across publications and presentations.
  - Interoperability considerations
    - Align with RIVPACS-related fields and measurements for seamless integration with ecological models.
    - Maintain compatibility with additional Countryside Survey materials (e.g., Freshwater Manual, Headwater Streams Report) for context.

- Relationship to broader program
  - Connects to the Countryside Survey dataset and governance ecosystem, supporting long-term biodiversity and freshwater habitat analyses across years.
  - Encourages adoption of publishing-minded practices to create usable, well-documented datasets for diverse user needs.