# GMEP Pollinators Data (Glastir Monitoring & Evaluation Programme)

- Purpose and context
  - Welsh Government AES monitoring since early 1990s; Glastir Monitoring and Evaluation Programme (GMEP) collects biodiversity data and information on woodland creation/management.
  - Data used to track progress on reversing native biodiversity decline and meet CBD 2020 obligations; supports indicators such as Area of Healthy Ecosystems in Wales under the Well-Being of Future Generations Act 2015.

- Survey design and sampling
  - 4-year rolling survey cycle (2013–2016) to maximise site visits and enable year-on-year trend detection.
  - Two components: Wider Wales (baseline estimation, national trends) and Targeted (Glastir priority areas); common spatial unit of 1 km2.
  - Sample: 300 1 km squares over cycle; half randomly sampled within strata defined by the Land Classification of Great Britain; other half targeted to Glastir priority areas.
  - Exclusions: urban >75% or sea >90%; replacements arranged.
  - Methodology aligned with Countryside Survey of GB for future data integration; confidentiality maintained by plotting at larger map scales.

- Data collection methods
  - Pollinator groups surveyed: butterflies (species-level), bees and hoverflies (grouped by morphology/ecology).
  - Two survey components per square in a given year:
    - Transect walks (2 km per square): July and August; 10 sections of ~200 m; record counts by taxon within 5 m2 zones; accompany with flowering plant abundances (DAFOR-X scale) within 2.5 m of transect sections; weather data captured (sunshine, temperature, wind).
    - Timed observations (150 m2 flower-rich area): one per survey round; 20-minute counts of butterflies/bees/hoverflies visiting flowers; note whether visiting and plant group visited.
  - Schedule and conditions: surveys between 10:00–16:30 (or extended daylight if shaded area), specific temperature, sunshine, and Beaufort wind criteria; strict biosecurity procedures.
  - Training and QA: specialist training for pollinator groups; photo verification; QC visits by a senior surveyor; online image-based assessments; DEFRA Joint Codes of Practice followed.

- Data structure and file formats
  - Two main data components per square: transect counts and timed observations.
  - For each component, two relational tables: VISIT (survey details) and COUNT (insect/flower records); linked by VISITID.
  - Lookup table GMEP_POLLINATOR_GROUP_CODES.csv provides taxon codes and names for linking across COUNT and OBSV tables.
  - Key CSV files:
    - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: transect visit metadata (SQ_ID, VISITID, date, recorder, weather, etc.).
    - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: transect insect/flower counts by section and group code.
    - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: timed observation visit metadata (SQ_ID, VISITID, date, recorder, weather, etc.).
    - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: timed observation insect-plant interaction counts (FLOWER_GROUP_CODE, INSECT_GROUP_CODE, counts).
    - GMEP_POLLINATOR_GROUP_CODES.csv: lookup for GROUP_CODE linking to taxa, common/valid names, taxonomy, and metadata.
  - Data relationships: visits (TRAN or OBSV) link to their counts via VISITID; 1 km squares identified by SQ_ID; codes (GROUP_CODE, FLOWER_GROUP_CODE, INSECT_GROUP_CODE) map to the lookup table.
  - Appendix forms illustrate recording structures for transects (Appendix 2), timed observations (Appendix 3), and hoverfly group classifications (Appendix 4).

- Quality assurance and standards
  - Training workshops and expert support for pollinator identification; photo submission for ID confirmation.
  - QC field visits: seven 1 km squares re-surveyed by an experienced surveyor to validate methods.
  - Post-year online assessments with randomized insect/plant image sets to monitor surveyor identification accuracy.
  - Compliance with DEFRA Joint Codes of Practice to ensure robust, repeatable, auditable science.

- Outputs, use, and integration
  - Produces baseline estimates and national trends for pollinators and associated flora at 1 km square scale.
  - Enables integrated analysis across multiple metrics for an ecosystem-based assessment.
  - Supports biodiversity indicators and potential future data integration with broader GB surveys.

- Publications, references, and resources
  - Core methodological and reference materials: Bunce et al. 2007 (ITE Land Classification), Pollard 1977 (transect methods), Emmett et al. 2014/2017 (GMEP reports), GMEP website, pollinator field handbooks, and related field recording handbooks.
  - Documentation and data portals: GMEP resources and related field handbooks accessible via the Glastir Monitoring & Evaluation Programme website and NERC/UKCEH outputs.

- People and teams
  - UKCEH staff across data management, QA, statistics, and field coordination (e.g., Emmett, Williams, Henrys, Sharp, etc.).
  - Butterfly Conservation (BC) field survey coordinators and team members.
  - Field survey team members listed in project documentation.

- Appendices and practical tools
  - Appendix 2: Sample transect recording forms for a range of species/groups (butterflies, bees, hoverflies, and flowering plants) with fields for sun, wind, temperature, date, grid references, and species-specific entries.
  - Appendix 3: Sample timed observation recording forms with start/end times, photos, weather, and DAFOR-like flower/plant notes.
  - Appendix 4: Hoverfly ID key groups and grouping logic for field identification.

- Key challenges for data support
  - Ensuring consistent “ask understanding” and alignment across teams to capture necessary data components.
  - Handling patchy and heterogeneous data across multiple formats and scales.
  - Linking data across multiple systems and maintaining robust data quality and provenance.
  - Communicating complex ecological data simply and effectively; promoting outputs for reuse and broader sharing.