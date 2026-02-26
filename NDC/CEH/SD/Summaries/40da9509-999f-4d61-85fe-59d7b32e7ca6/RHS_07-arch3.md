# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

- Purpose and scope
  - Provides standardized measures of the physical structure of freshwater streams and rivers to scrutinize and inform environmental policy and future decisions.
  - Based on a standard 500 m sampling unit; surveys require accredited surveyors and adherence to published protocols to ensure consistency.
  - Data accompany the Countryside Survey program and support reports such as the Freshwater Manual and Headwater Streams reports.

- Data collection and quality assurance
  - Collected in 2007 using field tablet computers; records uploaded to a central CEH database and undergo extensive auditing and checking.
  - Data collection is guided by standard RHS protocols and accompanying technical documentation; multiple supporting reports are available for context.
  - Data are owned by NERC - CEH; instructions emphasize proper acknowledgement and copyright.

- Data structure and key tables
  - STREAM_RHS_SURVEY_main_07.csv
    - Site-level and survey details across multiple RHS sections (A, B, C, D, J, K, L, M, N, O, P, Q).
    - Key fields include: SQUARE (1 km square code), SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07, EZ_DESC_07, STREAM_OR_DRAIN, DISTANCE_F_SOURCE, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT, HEIGHT_SOURCE, SURVEY_DATE, PART_OF_RIV_OR_ART, and numerous habitat and geo-physical descriptors (e.g., geology, bed material, channel dimensions, and valley form).
    - Also includes extensive vegetation, sediment, and man-made feature tallies (e.g., WEIRS, SLUICES, BRIDGES, FORDS, REVETMENTS) and channel morphology indicators (e.g., bankfull height/width, water depth, flow types).
    - Habitat quality indicators: HQA_SCORE (Habitat Quality Score) and HMS_CLASS (Habitat Modification Scores Class).
  - STREAM_RHS_SURVEY_spotcheck_07.csv
    - Spot-check data for sections E, F, and G; includes site, land class, bank and channel spot-checks, and descriptive fields for spot-check features.
  - STREAM_RHS_SURVEY_bank_07.csv
    - Bank-related data for sections H and I; captures bank material, vegetation, land use, banktop and bankface structures, vegetation types, and channel features on both banks.
    - Includes extensive descriptors of bank topography, vegetation associations, and nuisance species indicators (e.g., Himalayan balsam, Japanese knotweed) and overall channel attributes (MAJ_IMP, L_MANAGE, ANIMALS, ALDERS, DIS_ALDERS, HQA_SCORE, HMS_CLASS).
  - Data usage notes
    - All RHS data use must be acknowledged with the provided attribution text and rights language.

- Key measures and concepts
  - Physical channel structure and morphology (riffles, pools, runs, waterfalls, cascades, rapids, glides, etc.).
  - Channel features and their abundance (e.g., weirs, sluices, culverts, bridges, fords, embankments).
  - Vegetation and bank characteristics on both banks and within 5 m of banktops, including woodlands, hedges, and channel vegetation types.
  - Habitat health and modification indices (HQA_SCORE and HMS_CLASS) to assess naturalness and anthropogenic impact.
  - Hydro-geomorphic context (altitude, slope, Strahler stream order, catchment area, hydrological unit).

- Access, usage and attribution
  - Data are published resources linked to the Countryside Survey program; the Countryside Survey website provides official access and supporting manuals (e.g., Murphy & Weatherby 2008; 2010 Headwater Streams report).
  - All use of Countryside Survey data must be acknowledged with the specified attribution:
    - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
    - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

- Relevance for monitoring frameworks
  - Provides a rich, standardized set of physical habitat indicators suitable for evaluating freshwater policy outcomes and informing future monitoring designs.
  - Data governance considerations include consistent metadata, clear data provenance, and publicly shareable datasets, aligned with the Countryside Survey's openness and attribution requirements.