# Glastir Monitoring and Evaluation Programme (GMEP)

## Context and aims
- Welsh Government monitoring program (GMEP) established in 2013 to assess Glastir scheme effects on biodiversity and landscape condition.
- Purpose: contribute to evidence base for reversing native biodiversity decline and meeting biodiversity obligations.
- Structure: 4-year rolling survey (2013–2016) with two components:
  - Wider Wales component: baseline estimation, national trends, national reporting.
  - Targeted component: links to Glastir priority areas.
- Data integration across metrics with a common spatial unit (1 km square) to enable cross-scale analysis and potential future integration with GB Countryside Survey.

## Sampling design and scope
- 300 x 1 km squares sampled over the 4-year cycle.
- Stratified sampling:
  - Half: Wider Wales squares, randomly sampled within strata defined by the ITE Land Classification (2007).
  - Half: Targeted squares aimed at Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea.
- Sampling framework and spatial distribution prepared to maximise environmental heterogeneity between strata while minimising it within strata.

## Data collection and data model

### Data collection methods
- In each 1 km square:
  - Mapping of linear features (less than 5 m wide) onto base maps using predetermined coded options.
  - Data captured electronically with CS Surveyor (GEo/GIS integration) to reduce transcription errors.
  - Features include managed and unmanaged woody lines (e.g., hedges, lines of trees), walls, fences, streams, and other linear elements.
  - Recording includes length and condition; minimum feature length 20 m; gaps up to 20 m allowed.
  - Woody linear features classified using a standardized key (Maskell et al., 2016).
  - Documentation via GMEP Field Mapping Handbooks.

### Data assets and structure
- Landscape linear features (2013–2016) — GMEP_LANDSCAPE_LINEAR_FEATURES_2013_16.csv
  - Key identifiers: EVENTDATA_GUID, LINEARDATA_GUID, EVENT_FROM, EVENT_TO, SQ_ID (1 km square code)
  - Spatial frame: Easting/Northing (10 km resolution), LC (land class), AT coordinates
  - Attributes: LENGTH_M, THEME, HABITAT_NAME, HISTORIC_MANAGEMENT, various feature attributes (e.g., verges, margins, widths, conditions)
  - Relationships: links to the per-feature detail table via LINEARDATA_GUID
- Woody linear feature species data — GMEP_LANDSCAPE_LINEAR_FEATURE_SP_2013_16.csv
  - Attributes: SEVENTDATA_ID, SEVENTDATA_GUID, VEGETATION_TYPE, SPECIES, PROPORTION
  - Links to corresponding linear features via EVENTDATA_ID
  - Species nomenclature noted as following Stace (1997)

### Metadata and coding standards
- Field definitions and coding referenced from GMEP Field Mapping Handbooks (Maskell et al., 2016a/b).
- Spatial references tied to OSGB 1936 coordinates; 1 km sampling unit chosen for integration with other surveys.
- Taxonomic reference for species: Stace (1997).

## Quality assurance and data provenance
- Survey teams comprised of experienced botanical surveyors; each survey preceded by intensive training to ensure consistency with handbooks.
- Electronic data capture reduces post-survey digitising errors; mandatory data fields and prompts support complete records.
- Prompt data transfer to office enables timely data checking.
- Quality control (QC) exercise: a second team re-surveys all or part of a square; issues fed back to improve recording.
- Documentation and governance supported by a network of project staff and specialists (see Appendix: roles, tasks, and responsibilities).

## Data governance, usage, and provenance notes
- Data designed for integration across scales and with future analyses (e.g., linkage with GB Countryside Survey).
- Data intended to support national biodiversity indicators and monitoring of Glastir scheme progress.
- Publications and methodological references cited to ensure traceability and reproducibility (e.g., Land Classification, habitat classifications, biodiversity guidance).
- Appendix lists roles, project management, and field teams, illustrating clear data stewardship responsibilities.

## Publications, references, and further documentation
- Key methodological and contextual references include:
  - ITE Land Classification (Bunce et al., 2007)
  - Glastir Monitoring & Evaluation Programme reports (Emmett et al., 2014; 2017)
  - GMEP Field Handbook and mapping resources
  - Related biodiversity guidance (Jackson, Stace) and JNCC frameworks
- GMEP project website provides public access to methodologies, results, and supplementary documents.

## Implications for data stewards (key considerations)
- Maintain robust metadata and data dictionaries aligned with Field Mapping Handbooks; ensure consistent use of codes and attributes across datasets.
- Preserve the linkage between datasets using unique identifiers (GUIDs) to support data traceability and integration.
- Manage data quality through documented QA processes, training, and QC feedback loops; track versions and changes in datasets.
- Ensure clear data provenance, including sampling design rationale, spatial unit definitions, and coordinate systems.
- Facilitate interoperability with other national datasets (e.g., Countryside Survey) by adhering to common spatial units and standards.
- Be mindful of confidentiality and data visibility in spatial representations (e.g., limited precision in published maps).

## Appendix: roles and teams
- Roles and responsibilities assigned to named individuals (e.g., database management, sampling design, field team leadership, vegetation expertise, GIS support).
- Field survey teams enumerated, illustrating distributed data collection and governance responsibilities.