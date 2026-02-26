# Glastir Monitoring & Evaluation Programme Pollinators Data Description

- Wales-based monitoring of pollinators as part of the Glastir agri-environment scheme evaluation, with data intended to inform biodiversity trends and progress towards Wales’ biodiversity obligations and Well-Being goals.

## Overview of aims and scope

- Collect biodiversity indicators and information on woodland creation/management to track changes in Wales’ native biodiversity.
- Provide independent estimates of semi-natural habitat change at Broad Habitat and overall scales.
- Support indicators such as “Area of Healthy Ecosystems in Wales” under the Well-Being of Future Generations Act.
- Data cover pollinator groups (butterflies at species level; bees and hoverflies by group) and flowering plant groups, enabling analysis of pollinator-plant interactions and habitat associations.

## Survey design and sampling

- 4-year rolling survey cycle (2013–2016) to maximise site coverage while enabling year-to-year trend detection.
- Two main components:
  - Wider Wales Component: baseline estimation and national trends for Glastir.
  - Targeted Component: links to Glastir priority areas.
- Sampling frame uses a common 1 km grid across Wales; 300 squares in total over the cycle.
- Sample selection:
  - Half of squares randomly drawn within strata defined by the ITE Land Classification (GB) to ensure environmental heterogeneity is represented.
  - Other half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea replaced with alternatives.
- Spatial unit for integration: 1 km squares to enable future linkage with Countryside Survey of Great Britain.
- Data collection per square:
  - Each square visited twice in a year (July and August) across 2013–2016.

## Data collection methods

- Pollinator focus and structure:
  - Two independent components per square: transect counts and timed observations.
  - Transect surveys (2 km) using Pollard-style walks split into ten 200 m sections; conducted July or August.
  - Timed observations: 150 m² flower-rich area within the square; 20-minute counts of pollinators visiting flowers.
- Taxonomic resolution:
  - Butterflies recorded to species level.
  - Bees and hoverflies recorded as groups by broad morphological/ecological differences.
- Flowering plant data:
  - Abundance of key flowering plant groups recorded using DAFOR-X scale (Dominant to Not seen at all).
- Survey timing and conditions:
  - Conducted between 10:00–16:00 (or 09:30–16:30 if shade and activity suitable).
  - Weather suitability criteria (temperature, sunshine, wind) to ensure pollinator activity.
- Data collection details:
  - Standardized transect route with 2 km length, subdivided into 10 sections; recording of counts within 5 m² recording boxes.
  - Weather data collected at end of transect (temperature, sunshine, wind).
  - Timed observations capture pollinator visits to flowers and whether visitors were feeding.

## Data structure and files

- Two main data components per square, each with two tables:
  - Transect component: VISIT and COUNT tables.
  - Timed observations component: VISIT and COUNT tables.
- Linking and lookup:
  - VISITID links COUNT records to their corresponding visits.
  - A separate lookup table GMEP_POLLINATOR_GROUP_CODES.csv provides codes for insect and plant groups used in COUNT and OBSV tables.
- Core files (example descriptions):
  - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: ancillary data for each transect walk (SQ_ID, VISITID, date, weather, etc.).
  - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: counts of insects and plants recorded along transect sections.
  - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: ancillary data for each timed observation (two visits per square per year).
  - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: counts of plant–insect interactions during timed observations.
  - GMEP_POLLINATOR_GROUP_CODES.csv: lookup for codes (GROUP_CODE, FLOWER_GROUP_CODE, INSECT_GROUP_CODE) with taxonomic and nomenclature details.
- Data linkage:
  - VISIT tables connect to COUNT tables via VISITID.
  - Group code lookups enable interpretation of insect and plant categories in counts.

## Quality Assurance and standards

- Training workshops for all surveyors to standardize identification (especially bees and hoverflies).
- Use of photographs for identification confirmation; expert review of photographs.
- QA checks:
  - Field QA: visits to seven 1 km squares by an experienced surveyor to replicate transects and compare results.
  - Post-year online online assessments: random image-based tests to evaluate surveyor identification skills.
- Adherence to DEFRA Joint Codes of Practice (JCoPR) to ensure robust, repeatable, auditable scientific quality.

## Relevance and potential analyses

- Data support baseline estimation, national trends, and Glastir program reporting.
- 1 km grid design facilitates integration with national surveys (e.g., Countryside Survey) for cross-study analyses.
- Enables analysis of:
  - Pollinator diversity and abundance by group and butterfly species, across spatial and temporal scales.
  - Relationships between flowering plant availability (DAFOR-X) and pollinator activity.
  - Habitat associations and potential corridors using land-class and grid-based approaches.
  - Changes in semi-natural habitat extent as an indicator aligned with biodiversity goals and Well-Being Act targets.

## References and resources

- Methodology and sampling framework references (ITE Land Classification, Countryside Survey methods).
- GMEP project reports and handbooks (annual and final reports to Welsh Government; pollinator field handbook; related bird-field handbook references for broader methodology).
- Pollinator methodology and documentation on the GMEP website.
- Pollination group and hoverfly identification resources, including hoverfly groupings and key taxa.

## Appendices of note

- Appendix 2: Survey recording forms for transect walks (example fields include site identifiers, weather, sun/shade, temperature, wind, butterfly/bees/hoverflies counts, DAFOR-X, and plant groups).
- Appendix 3: Survey recording forms for timed observations (photograph fields, start/end times, weather, wind, temp, DAFOR-X, and interaction matrices).
- Appendix 4: Hoverfly ID – key groups with examples and atypical taxa, illustrating groupings used in counts.

## Data access considerations and challenges for analysts

- Scale and integration:
  - Data are primarily at 1 km grid scale across Wales, with repeated measures over four years, enabling both local and national analyses.
- Data gaps and accessibility:
  - Some taxa groupings and codes may require careful interpretation via the lookup tables.
- Data provenance and transparency:
  - Clear QA processes and adherence to JCoPR support reproducibility and auditability of analyses.
- Local-level detail limitations:
  - While 1 km scale is robust for national trends, local-level decisions may require finer-scale data or targeted sampling.