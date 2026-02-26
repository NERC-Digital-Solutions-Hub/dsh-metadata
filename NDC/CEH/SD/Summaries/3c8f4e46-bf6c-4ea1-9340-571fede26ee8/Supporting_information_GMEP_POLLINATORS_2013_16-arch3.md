# Glastir Monitoring & Evaluation Programme

- Wales’ agri-environment schemes support biodiversity monitoring through a dedicated programme, the Glastir Monitoring and Evaluation Programme (GMEP), initiated to assess landscape features, woodland management, and overall biodiversity progress in relation to Welsh and international obligations.

## Aim and scope of the monitoring framework

- Provide evidence on biodiversity trends and landscape change to track progress towards reversing native biodiversity decline and fulfilling biodiversity conventions.
- Generate indicators relevant to policy goals, including the Well-Being of Future Generations Act (Area of Healthy Ecosystems in Wales) and national biodiversity targets.
- Integrate multiple ecosystem measures across scales in a single, coherent monitoring cycle.

## Study design and sampling framework

- Four-year rolling survey cycle (2013–2016) to balance site coverage and temporal trends.
- Two main components:
  - Wider Wales Component: baseline estimation and national trends.
  - Targeted Component: focus on Glastir priority areas.
- Common spatial unit: 1 km x 1 km squares; 300 squares sampled over the cycle.
- Sampling approach:
  - Randomly selected squares within strata defined by the Land Classification of Great Britain to maximize environmental heterogeneity between strata.
  - Half of squares (Wider Wales) randomly sampled; the other half targeted at Glastir priority areas.
- Exclusions and replacement:
  - Exclude squares with >75% urban land or >90% sea; replacement with alternatives.
- Methodological continuity:
  - Sampling method aligned with the Countryside Survey of Great Britain to enable integration of results and future analyses.

## Data collection methods

- Pollinator focus and data types:
  - Target groups: butterflies (species level), bees and hoverflies (grouped by ecological differences).
  - Plant interactions recorded using DAFOR-X scale for flowering plant groups important to pollinators.
- Survey components in each 1 km square:
  - Transect surveys (two per square per year): July and August.
    - Walk two 1 km transects (total 2 km) per square, subdivided into ten 200 m sections.
    - Record counts of butterflies (species level) and bees/hoverflies (by group) within 5 m2 recording boxes; record DAFOR-X plant cover in proximity to transects.
    - Collect weather data: temperature, sunshine, wind (Beaufort scale).
  - Timed searches (one per square per year): 150 m2 flower-rich patch, 20-minute count.
    - Document pollinators visiting flowers and plant group visited.
- Timing and conditions:
  - Surveys conducted between 10:00–16:00 (or 09:30–16:30 if conditions permit) with suitable insect activity (temperature, sunshine, wind criteria).
- Training and field protocols:
  - Training workshops for surveyors; use of field handbooks and ID photos for verification; QA support from pollinator experts.

## Data structure and management

- Two core data components per square:
  - Transect counts and timed observations.
- Data tables and linking:
  - VISIT tables (capture visit metadata) link to COUNT tables (insect and flower records) via VISITID.
  - SQ_ID links across datasets; a GMEP_POLLINATOR_GROUP_CODES lookup table standardizes taxon groupings.
- File detail characteristics:
  - Separate transect and observation datasets for visits and counts (e.g., GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv, GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv, GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv, GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv).
  - Lookup codes provide taxonomic and ecological context (butterfly strategies, hoverfly groupings, plant groups).

## Quality assurance and governance

- QA processes:
  - Pre-field training; guided ID confirmation with photos reviewed by experts.
  - QC exercise: on-site repeat surveys in a subset of squares by an experienced surveyor to assess consistency.
  - Online QA assessments for surveyors after each year, using randomized insect/plant images.
- Standards and ethics:
  - DEFRA Joint Codes of Practice (JCoPR) followed to ensure robust, auditable scientific processes.

## Relevance and outputs

- Outputs contribute to national and Welsh biodiversity evidence bases, informing policy and conservation actions.
- Independent estimates of semi-natural habitat change support indicators for Wales’ biodiversity and ecosystem health targets.
- Enables potential integration with GB-wide surveys and future cross-border analyses.

## Publications, references, and governance context

- Key references include:
  - Bunce et al. (ITE Land Classification of Great Britain) for sampling framework.
  - Emmett et al. (GMEP annual and final reports) for methodology and programme outcomes.
  - Pollard (1977) transect method as the methodological basis for butterfly surveys.
- Field and governance documents:
  - GMEP website and project handbooks; collaboration between UKCEH, Butterfly Conservation, and field teams.
  - Field handbooks and data collection forms (Appendices 2–4) detailing survey recording and hoverfly groupings.

## Stakeholders, teams, and capacity

- UK Centre for Ecology & Hydrology (UKCEH) core team managing data, QA, and field operations.
- Butterfly Conservation (BC) field survey coordinators and team.
- Field survey teams consisting of multiple researchers and coordinators across regions.
- Consultant entomologist provided training and QA support.

## Data accessibility and metadata considerations

- Data sharing and metadata quality are recognized as barriers in some cases (e.g., public sharing requirements, metadata completeness).
- Emphasis on data quality, openness, and data governance to ensure datasets meet standards and can be stored, shared, and updated appropriately.

## Appendices and practical tools

- Appendix 2: Survey recording form for transect walks (taxa-specific fields and metadata).
- Appendix 3: Survey recording form for timed observations (photography, timing, wind, DAFOR-X, and taxa codes).
- Appendix 4: Hoverfly ID – key groups and typical/atypical specimens with grouping guidance.

## Key takeaways for monitoring framework authors

- A cohesive, ecosystem-based monitoring programme can be designed to capture multi-scale data within a single rolling cycle, balancing broad national indicators with targeted, policy-relevant insights.
- Standardized sampling frameworks (aligning with GB methodologies) enhance comparability and future data integration.
- Combining transect-based abundance data with timed observations and detailed plant-pollinator interactions enables richer interpretation of pollinator biodiversity and habitat quality.
- Robust QA processes, training, and governance (including adherence to recognized codes of practice) are essential to ensure data quality and credibility.
- Clear data structures (VISIT and COUNT linkage, plus lookup tables) support transparent data management and reuse, while metadata limitations and data-access barriers should be proactively addressed.