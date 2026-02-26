# Background information

- Context and purpose
  - In Wales, agri-environment schemes (AES) funding has existed since the early 1990s; Glastir is the current scheme. The Welsh Government established the Glastir Monitoring and Evaluation Programme (GMEP) in 2013 to monitor biodiversity, woodland creation/management, and landscape features.
  - GMEP data underpin evidence for reversing native biodiversity decline and meeting CBD 2020 obligations; the programme contributes an independent estimate of changes in semi-natural land, linked to Well-Being of Future Generations Act indicators (Area of Healthy Ecosystems in Wales).

- Survey design and scope
  - An ecosystem-based, multi-scale approach with data collected across scales in a single snapshot visit.
  - 4-year rolling survey cycle (first cycle 2013–2016) to maximise site visits while detecting temporal trends cost-effectively.
  - Two components: Wider Wales (baseline estimation and national trends) and Targeted Component (Glastir priority areas); both use a common 1km square unit.
  - Sampling frame: 300 x 1km squares over four years; half are Wider Wales, selected randomly within strata defined by the ITE Land Classification; other half targeted at Glastir priority areas.
  - Exclusion criteria: replace squares with >75% urban land or >90% sea (based on LCM2007 and census data).

- Data collection methods (birds)
  - Bird surveys coordinated by the British Trust for Ornithology (BTO).
  - Aim: robustly estimate breeding pairs per species within each square and track habitat associations; methodology aligns with, but is more intensive than, the national Breeding Bird Survey (BBS).
  - Field effort: four visits per square (reduced to three from 2015–16), evenly spaced from mid-March to mid-July; visits start around 06:00 and can last up to five hours.
  - Surveying approach: walk routes within or up to 50m of square boundaries; record all birds seen/heard with BTO codes; include birds just outside the boundary when they relate to territorial inference; ensure full coverage across visits and varying start points.
  - Data capture: weather on each map; route coverage and boundary context; use A3 maps for territory mapping and counts; exact route logged to assess coverage quality and avoid double-counting.
  - Protocol details and full data collection guidance are documented in the GMEP Birds Field Handbook.

- Data files and metadata
  - GMEP_BIRD_COUNTS_2013_16.csv: records of bird sightings across 300 squares (visit number, date, species code, activity, count, observer, location, square ID, land classification, etc.). Includes anonymised observer IDs and 10km resolution coordinates (E/N) for spatial context.
  - GMEP_BTO_SPECIES_CODES.csv: lookup between BTO two-letter codes and scientific/common names, including status.
  - Data are structured to support integration with other national surveys (e.g., Countryside Survey GB) and future analyses at multiple scales.

- Quality assurance, data management, and standards
  - Field teams comprised of experienced ornithological surveyors; QA includes interview-based assessments, standardized field training, and ongoing support from a dedicated survey coordinator.
  - Data collected on standard forms and field maps; Bangor (Wales) handles initial collation before digital input at the BTO head office; digitization uses ArcMap (up to v10.5).
  - QC processes include verification of uncertain counts and species codes, validation with surveyors, and post-processing checks for unrecognised codes or implausible counts.
  - Compliance with DEFRA Joint Codes of Practice (JCoPR) to ensure robust, repeatable, auditable scientific quality.

- Roles and collaboration
  - UKCEH (UK Centre for Ecology & Hydrology) staff involved in project leadership, data management, statistics, field coordination, and QA.
  - BTO staff lead science directions, field survey coordination, and spatial data processing.
  - A dedicated Field Survey Team conducts on-the-ground surveys with a roster of named contributors.

- Relevance for data leaders
  - Demonstrates end-to-end data governance: from national sampling design and stratification to granular field data capture, anonymised respondent handling, and integrated spatial outputs.
  - Highlights the value of a common spatial unit (1km squares) for cross-survey integration and national-to-local analytics.
  - Shows robust QA, metadata standards, and data lineage (field forms → maps → Bangor → digitization → analysis) aligned with national practice standards (JCoPR).
  - Illustrates data discovery and reuse opportunities, including linking GMEP data with broader biodiversity indicators and future Well-Being Act metrics.
  - Addresses practical data challenges common to public-sector data initiatives: scattered data sources, access controls/anonymisation, data standards, metadata clarity, and sector coordination.

- References and publications (selected)
  - Foundational methodology and sampling framework (ITE Land Classification).
  - GMEP annual/final reports and field handbooks detailing survey design and results.
  - Related methodological literature: Breeding Bird Survey methods, Common Birds Census lineage, and field-specific guidelines.
  - Websites and reports for broader GMEP context and documentation.