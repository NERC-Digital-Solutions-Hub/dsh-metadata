# Glastir Monitoring & Evaluation Programme Pollinators Survey Data Description

- Purpose and context
  - Wales GB-funded AES since the 1990s; GMEP established in 2013 to monitor Glastir’s environmental effects and biodiversity trends.
  - Biodiversity data support evidence for reversing native biodiversity decline and CBD obligations; provide estimates of semi-natural habitat change and links to Well-Being of Future Generations indicators (Area of Healthy Ecosystems in Wales).
  - GMEP adopts an ecosystem-based, multi-metric approach across multiple scales, integrating data into standard spatial units (1 km squares).

- Survey design and sampling
  - 4-year rolling cycle (2013–2016) to maximise site coverage while detecting year-on-year trends.
  - Two components: Wider Wales (baseline estimation, national trends) and Targeted (Glastir priority areas); both use a common 1 km square unit.
  - Sample: 300 squares over the cycle; half randomly sampled within Land Classification of Great Britain strata (ITE) and half targeted at Glastir priority areas.
  - Exclusions/replacements: squares with >75% urban or >90% sea replaced.
  - Rationale: aligns with Countryside Survey GB methodology to enable future data integration.

- Field data collection methods
  - Timing: two visits per square in one year (July and August) by trained ecologists (Butterfly Conservation partners and staff).
  - Taxa focus: pollinators—butterflies (species-level), bees and hoverflies (group-level); flowering plants recorded with DAFOR-X abundance scale (Dominant to Not seen).
  - Survey components:
    - Transect route: standard 2 km route (Pollard walk) split into ten 200 m sections; records butterfly species and bee/hoverfly groups within 5 m2, plus DAFOR-X for key flowering plant groups within 2.5 m of transect sections; weather conditions logged (temperature, sunshine, wind).
    - Timed search: 150 m2 flower-rich area within the square; counts of butterfly species and bee/hoverfly groups during a 20-minute period; notes on visitation to flowers and plant group visited.
  - Time window and conditions: surveys conducted between 10:00–16:00 (or adjusted if shade/conditions permit) with specific temperature, sunshine, and Beaufort scale requirements for insect activity.
  - Data capture: standardized forms and field handbooks guide species identification; training included photos for verification and ongoing expert support.

- Data structure and files
  - Two main data components per square: transect counts and timed observations; each has a VISIT table (visit details) and a COUNT table (recorded taxa/flower data).
  - Linkage: VISIT tables connect to COUNT tables via VISITID; squares linked by SQ_ID; taxa coded via GROUP_CODE and FLOWER_GROUP_CODE/INSECT_GROUP_CODE with a shared lookup table.
  - Key files (2013–2016 data):
    - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: transect visit metadata (SQ_ID, VISITID, date, recorder, weather, etc.).
    - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: transect counts (insect groups and plant group abundances) linked to VISITID.
    - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: timed observation visit metadata (SQ_ID, VISITID, date, recorder, weather, etc.).
    - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: timed observation counts (plant–insect interactions) linked to VISITID.
    - GMEP_POLLINATOR_GROUP_CODES.csv: lookup table for taxon codes, names, taxonomy, and related metadata (includes supported fields such as HABITAT, LIFE-STRATEGY for butterflies, and various name mappings).
  - Data is structured to support cross-survey integration and future analyses with GB Countryside Survey where feasible.

- Quality assurance and governance
  - Training: dedicated workshop for pollinator groups; field guides provided; expert support available; identification verified via photographed submissions reviewed by experts.
  - Quality control: year-one field QC on seven 1 km squares using a senior surveyor to replicate surveys; subsequent online image-based assessments for surveyors to reinforce identification skills.
  - Standards: DEFRA Joint Codes of Practice (JCoPR) followed to ensure robustness, repeatability, and auditability of methods and results.

- Outputs, relevance, and policy context
  - Data contribute to baseline and trend estimates of biodiversity indicators and the extent of semi-natural habitat in Wales.
  - Independent measurements support progress reporting toward Well-Being Act goals and CBD-relevant biodiversity commitments.
  - The standardized, integrated data structure enables aggregation at national/sub-national levels and potential linkage with related GB surveys.

- Access, value, and challenges
  - Dataset value increases when combined with other relevant data beyond single-use outputs; aims to maximise the utility of collected data.
  - A key challenge is enabling broad access to underlying data while maintaining confidentiality and data integrity, to maximize usefulness for policy analysis and research.