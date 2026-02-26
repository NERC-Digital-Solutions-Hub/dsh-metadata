# Glastir Monitoring & Evaluation Programme (GMEP)

## Purpose and Scope
- Wales-based monitoring program (GMEP) established to assess Glastir AES outcomes, with a focus on biodiversity and woodland management to support Wales’ biodiversity evidence base and CBD 2020 obligations.
- Aims to integrate multiple measures across scales in a single snapshot, enabling national and regional trend analysis.

## Data Design and Sampling
- 4-year rolling survey cycle (2013–2016), comprising:
  - Wider Wales Component: baseline estimation, national trends, national reporting.
  - Targeted Component: links to Glastir priority areas.
- Common spatial unit: 1 km square; enables data integration across components and potential future integration with the Countryside Survey of Great Britain.
- Sampling plan: 300 1 km squares over the cycle; half randomly sampled within Land Classification strata (ITE Land Classification 2007), half targeted at Glastir priority areas.
- Exclusions: any square with >75% urban land or >90% sea excluded from sampling.
- Spatial distribution presented at 10 km for confidentiality.

## Data Collection and Standards
- In each 1 km square, point, areal, and line features mapped onto base maps using pre-determined coded options.
- Data capture: electronic field methods with CS Surveyor software and Esri GIS; reduces post-collection digitising and enables prompt data checks.
- Field Mapping Handbooks (2016a/2016b) guide methodology for habitat attributes and Surveyor usage.
- Point features include small-scale landscape elements (e.g., trees, ponds, buildings) with varied use codes; detailed variable definitions and codes are provided in the field handbooks.

## Data Schema and Metadata
- Primary dataset: GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv
  - Key columns include:
    - SQ_ID (1 km square sampling site code)
    - PCOMPDATA_ID (landscape point identifier)
    - PCOMPDATA_GUID (globally unique identifier)
    - THEME, HABITAT_NAME (primary attribute descriptors)
    - Detailed veteran-tree attributes (e.g., VETERAN_TREE_TYPE, DEAD_MISSING_BARK, HOLLOW_TRUNK, DEAD_WOOD, etc.)
    - VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION
    - USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER
    - SURVEY_YEAR, EASTERING/NORTHING coordinates, LC (Land Classification)
  - Notes: species nomenclature follows Stace (1997); additional metadata and variable definitions are provided in the GMEP Field Mapping Handbooks.
- References to supporting classifications and nomenclatures:
  - ITE Land Classification of Great Britain 2007
  - Stace, 1997; JNCC biodiversity classifications (via field handbooks and supporting documents)

## Quality Assurance and Data Management
- QA processes:
  - Surveys conducted by experienced botanical surveyors; extensive training prior to fieldwork.
  - Field teams supervised and later monitored by experienced project staff.
  - Electronic data capture with mandatory fields and prompts to ensure completeness and consistency.
  - Quick data transfer back to offices allows prompt data checks; communication channels between field teams and managers.
  - QC exercises: a second survey team repeats all or part of a square; results fed back to improve recording.
- Roles and teams:
  - Named project staff and field team managers support data management, sampling design, statistics, and GIS.
  - Dedicated data management and field expertise personnel ensure data integrity and training.

## Data Access, Sharing and Use
- Data produced to support national reporting and Glastir evaluation; used in annual reporting to Welsh Government and published materials.
- Public-facing resources include:
  - Glastir Monitoring & Evaluation Programme Website (gmep.wales) with project overview and documentation.
  - Field handbooks and methodology documents available as supplementary materials.
- Confidentiality considerations:
  - Spatial representations are plotted at reduced resolution (10 km) to protect data confidentiality.

## Governance, Stakeholders and Documentation
- Strong emphasis on standardized methodologies, training, and documentation to enable consistent data collection across teams and years.
- Documentation and references include:
  - Field handbooks (habitats and Surveyor usage)
  - Annual and final reports to Welsh Government
  - Supporting publications on biodiversity classifications and field methods

## Limitations and Considerations for Data Stewards
- Exclusion criteria and stratified sampling may affect representativeness in highly urbanized or marine-dominated areas.
- The 1 km square unit and 4-year rolling cycle may limit rapid detection of short-term changes.
- Data access is mediated by confidentiality considerations and published in aggregated forms; direct access to raw 1 km square data may require permissions or controlled access.
- Integration with other GB-wide datasets (e.g., Countryside Survey) is facilitated by harmonized sampling design but may require alignment of metadata and variable definitions.

## References and Documentation
- Field handbooks: Mapping Field Handbook Part 1 (habitat attributes) and Part 2 (Surveyor software usage)
- Land Classification and biodiversity guidance (ITE Land Classification 2007; JNCC/BAP references)
- Annual and Final GMEP reports to Welsh Government; supporting metadata and methodological documents accessible via gmep.wales and ancillary publications