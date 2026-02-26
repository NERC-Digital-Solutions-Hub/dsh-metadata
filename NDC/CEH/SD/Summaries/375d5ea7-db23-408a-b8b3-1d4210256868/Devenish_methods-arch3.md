# Study across four sites on myrmecochorous seed dispersal in invaded vs non-invaded sites

- A multi-site study conducted in June–Sept 2014–2015 to examine how invasion by L. humile affects myrmecochorous seed dispersal and ant nesting dynamics, using four sites (two invaded, two non-invaded).
- All data are RAW (unmodified) across trials.

## Study design and sites

- Four sites:
  - Invaded: Montilivi Campus (Site 1) and Castell d'Aro (Site 2)
  - Non-invaded: Montilivi Campus (Site 3) and Santuari dels Angels (Site 4)
- Vegetation: open cork-oak secondary forest with Quercus and Pinus; presence of herbaceous myrmecochorous plants in clearings.
- Invasion status defined by presence of L. humile at any time during surveys.
- Data collection encompassed four experiments focused on ant communities, seed dispersal, nest distribution, and seed fate.

## Experiments and measurements

- Experiment 1: Pitfall trapping
  - Objective: assess ant community composition (species mean relative abundance) in invaded vs non-invaded areas.
  - Method: two 100 m transects per site; pitfall traps every 5 m for 72 hours; ants identified to species where possible.
- Experiment 1: Baiting
  - Objective: track temporal shifts in ant community at baits.
  - Method: ten baits per transect (10 m intervals); tuna/honey bait on cards; observed at 07:00, 11:00, 15:00, 19:00; ants collected after 1 hour and identified.
- Experiment 2: Seed removal
  - Objective: compare seed dispersal rates in invaded vs non-invaded sites.
  - Method: ten seed hubs per site along the same transect used for ants; six seeds per hub (two plant species, three seeds each); seeds observed at 0.5, 1, 2, 3, 6, 12, 24 hours; six days total; 869 seeds used overall (439 invaded, 439 non-invaded).
  - Measured: number of seeds removed by ants and persistence on hubs.
- Experiment 3: Nest distribution
  - Objective: compare nest density and nest size between invaded (L. humile) and non-invaded (P. pallidula) sites.
  - Method: within each site, 5 random quadrats (30.25 m² each) with 144 cards each; baited with tuna/honey; cards observed for 4 hours daily for 10 days; nests counted (presence/absence) and number of trails recorded.
  - Measured: nest density and trail counts as proxy for nest size.
- Experiment 4: Seed fate
  - Objective: determine depth and fate of seeds near ant nests.
  - Method: 20 nests invaded and 20 nests non-invaded; 40 seeds per nest (20 Genista monspessulana, 20 Sarothamnus arboreus) placed near entrance; seeds observed until all retrieved or 72 hours elapsed; nests excavated to 10 cm depth; seeds recovered from nests and surface refuse; seeds below 10 cm not excavated.
  - Measured: seed removal into nests, retrieval from nests and refuse piles, and fate unknown.

## Data structures and file naming

- Experiment 1: Pitfall trapping
  - File: Devenish_Experiment_1_ant_community_PITFALL_RAW
  - Structure: Collection Code, Location, Sample date, Transect/Hub reference, Ant species counts.
- Experiment 1: Baiting
  - File: Devenish_Experiment_1_ant_community_BAITING_RAW
  - Structure: Collection Code, Date, Regional code, Collection Period, Number of species, Ant species presence/absence markers.
- Experiment 2: Seed removal
  - Hub data: Devenish_Experiment_2_seed_dispersal_HUB_RAW
    - Structure: Hub location, invasion status, seeds removed.
  - Outcome data: Devenish_Experiment_2_seed_dispersal_SurvA_RAW
    - Structure: Hub, invasion status, plant species, elaiosome present, seed status, trial timings, duration.
- Experiment 3: Nest distribution
  - File: Devenish_Experiment_3_nest_distribution_RAW
  - Structure: Grid ID, grid location, grid references/scores, total active cells.
- Experiment 4: Seed fate
  - File: Devenish_Experiment_4_seed_fate_RAW
  - Structure: Plant species, Nest ID, Ant community status, seeds removed to nest, seeds retrieved from nest, seeds retrieved from aboveground refuse, seeds not found/fate unknown.

## Relevance for monitoring frameworks and policy decisions

- Key environmental health measures captured
  - Ant community composition and temporal activity (pitfall and baiting) as indicators of ecosystem insect dynamics under invasion.
  - Seed dispersal rates and seed fate near invaded vs non-invaded nests to assess disruption to plant–animal mutualisms.
  - Nest density and structure as proxies for ant-driven ecosystem modification by invasion.
- Data governance and openness
  - Use of RAW data ensures traceability and transparency for monitoring, audit trails, and independent verification.
  - explicit data structures and file naming provide consistency for integration into monitoring dashboards and policy reports.
  - Public sharing of underlying data is noted as a potential barrier, highlighting governance needs around metadata sufficiency, accessibility, and data management standards.
- Implications for monitoring design
  - Invasion status definitions and site replication (invaded vs non-invaded) support causal inferences about invasion effects on ecological processes.
  - Multiple complementary metrics (community composition, activity patterns, seed removal, nest density, seed fate) offer a robust suite of indicators for environmental health monitoring and policy evaluation.
  - Standardized transects, timed observations, and structured data capture facilitate comparability over time and across sites.

## Challenges and considerations for monitoring frameworks

- Data gaps and access
  - Potential lack of data at adequate standards; timely access issues may hinder timely decision-making.
- Data silos
  - Fragmentation between sites and experiments can impede integrated analysis and cross-policy lessons.
- Metadata and data quality
  - Inadequate metadata can hinder verification of data suitability; some datasets require transformation to be usable.
- Data sharing and governance
  - Publicly sharing datasets can be a barrier; governance processes are needed to ensure standards, storage, sharing, and up-to-date maintenance.
- Communicating complexity
  - Translating multi-faceted findings (invasion effects on ants and plant dispersal) into clear policy messages requires careful data presentation and interpretation.