# Glastir Monitoring & Evaluation Programme (GMEP) Bird Survey Data and Methods (2013-2016)

- Wales-wide program and data collection to monitor Glastir scheme effects on biodiversity and landscape features, with a focus on birds, habitats, and woodland management.
- GMEP data contribute to evidence on reversing native biodiversity decline and tracking progress toward the Well-Being of Future Generations Act goals (Area of Healthy Ecosystems in Wales).

## Aims and scope
- Capture multiple, integrated measures of ecosystem components across scales in a single snapshot visit.
- Provide an independent estimate of change in semi-natural land and baseline/national trends for Glastir reporting.

## Survey design and sampling
- 4-year rolling cycle (2013–2016) to maximize site coverage and detect spatial and temporal changes cost-effectively.
- Two components:
  - Wider Wales Component: baseline estimation and national trends for Glastir.
  - Targeted Component: links to Glastir priority areas.
- Common spatial unit: 1 km squares; total of 300 squares sampled over the cycle.
- Sampling approach:
  - Half the squares randomly sampled within strata defined by the ITE Land Classification of Great Britain to maximize environmental heterogeneity between strata.
  - The other half targeted at Glastir priority areas.
- Exclusion criteria:
  - Remove squares with >75% urban land or >90% sea; replacements used.
- Integration with Countryside Survey methodology to enable future data integration across GB.

## Data collection and field methods
- Bird surveys coordinated by the British Trust for Ornithology (BTO) using a robust protocol to estimate breeding pairs and habitat associations.
- Field methodology:
  - Four visits per square (reduced to three in 2015–16) conducted mid-March to mid-July.
  - Visits start around 06:00, last up to 5 hours, routes cover all accessible parts within 50 m of boundaries.
  - Record all birds seen or heard with standard CBC notation; include birds just outside boundaries when relevant for territory assessment.
  - Document weather at start and end of each visit; record route coverage and note poorly covered or not covered areas.
- Data capture:
  - On-field maps, standard CBC codes, and BTO two-letter species codes.
  - Spatially explicit data: precise locations, 10 km resolution coordinates, square IDs, and Land Classification (LC) codes.
- Field procedures emphasize avoiding detection bias (e.g., only under suitable conditions) and ensuring repeatable coverage across visits and squares.

## Data files and metadata
- GMEP_BIRD_COUNTS_2013_16.csv: Bird sighting records across 300 1 km squares for 2013–2016; includes visit number, date, species code, behavior, count, notes, observer ID (anonymised), and spatial identifiers (SQ_ID, EASTING/NORTHING, LC).
- GMEP_BTO_SPECIES_CODES.csv: Lookup table mapping BTO two-letter codes to English and Latin names and status.
- Data collection details:
  - Visits: 1–4 per square (4 initially; reduced to 3 in later years).
  - Fields: date, species code, activity/behavior code, count, notes, observer, and spatial metadata.
  - Anonymised observer IDs for privacy; detailed methodology documented in the GMEP Birds Field Handbook.
- Data handling and integration:
  - Digitization and mapping performed with ArcMap; quality checks at multiple stages to ensure accuracy of counts, species codes, and identifications.
  - Alignment with DEFRA Joint Codes of Practice (JCoPR) for quality of science and research processes.

## Quality Assurance and standards
- Surveys conducted by experienced ornithological teams with standardized training and field guidelines.
- QA processes include:
  - Pre-survey training, field coordinators, and line managers.
  - Standard forms and field maps; data collated at BTO Wales, then digitized into GIS systems.
  - Verification of uncertain counts and codes through cross-checks with surveyors and digitizers.
  - Additional data processing checks to identify unrecognized codes or implausible counts.
- Adherence to DEFRA JCoPR standards to ensure robustness, repeatability, and auditability of results.

## References and related materials
- Key methodological and sampling references (ITE Land Classification, Common Birds Census methods, Breeding Bird Survey methodology).
- Field handbook: GMEP Birds Field Handbook (v4, 2014) for full data collection details.
- Public reports and outputs from the Glastir Monitoring & Evaluation Programme (GMEP) and related publications.

## People and teams
- UKCEH staff: lead scientist, data management, QA, field coordination, statisticians, project management.
- BTO staff: lead scientists, field survey coordination, spatial data processing.
- Field survey team: named individuals contributing to data collection.
- Roles include field coordination, data management, QA, and project leadership across both organisations.

## Data usage, access, and integration
- Data designed to enable national and sub-national trend analyses, baseline estimation, and integration with broader GB surveys (e.g., Countryside Survey).
- Aims to provide robust indicators of habitat change and biodiversity responses to Glastir habitat management.
- Data and metadata are structured to be discoverable and usable, with anonymised observer information and clearly defined variable descriptions.