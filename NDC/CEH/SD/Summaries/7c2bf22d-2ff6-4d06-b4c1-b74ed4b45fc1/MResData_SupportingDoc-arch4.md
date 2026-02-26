# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

- Overview
  - Dataset of moth (larvae) species and associated parasitoid data, plus hedgerow architecture and resource availability measurements.
  - Collected as part of an MRes project using the long-running hedgerow experiments to study effects of hedgerow management on wildlife habitat quality and resources.
  - Related publication: Facey et al. 2014, Insect Conservation and Diversity.

- Context and aims of the long-running hedgerow experiments
  - Two linked aims: (1) assess effects of hedgerow cutting timing and frequency on wildlife habitat quality and food resources; (2) identify low-cost restoration options suitable for large-scale application under Entry Level and Higher Level Stewardship.
  - Experiment 1 (this dataset) investigates long-term effects of cutting timing and frequency on resource provision for wildlife.
  - Site: four hedgerows planted in 1961 at Monks Wood, Cambridgeshire, UK; former arable land converted to grassland.
  - Design: 32 contiguous plots per hedge, arranged in factorial combinations of cutting frequency (annual, biennial, triennial) and cutting timing (autumn, winter); two unmanaged controls; replicates of 4–8 per treatment.

- Experimental design and methods (data collection focus)
  - Cutting regime timeline: 2005–2014 with annual and multi-year cutting patterns; autumn cuts in September; winter cuts in January/February.
  - Moth sampling and rearing (2011):
    - Timed search and hedgerow beating used to collect larvae.
    - Larvae reared to maturity to determine parasitism and identify moth species.
    - Adult moths identified; parasitoids recorded (family/subfamily) when possible.
  - Hedgerow measurements:
    - Architectural metrics: height, width, branching density, and branch/tip structure measured to quantify habitat structure.
  - Foliar quality analysis:
    - Carbon and nitrogen concentrations measured from leaf samples to relate to moth abundance/diversity and treatment effects.
  - Sample and data flow:
    - Data stored for each sample with extensive metadata (site, block, plot, treatment, date, collection method, replicate).

- Data files and schema (contents and key fields)
  - MResMothLarvaeParasitoids.csv
    - Columns include: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, COLLECTION_METHOD, SAMPLE_NO, MOTH_NAME, PARASITISED, PARASITOID, PARASITOID_FAMILY, PARASITOID_SUBFAMILY, PARASITOID_NOTES, DATE_EMERGED, etc.
    - Captures moth larvae and any associated parasitoids, plus rearing outcomes and identification notes.
  - MResDimensions.csv
    - Columns: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, REPLICATE, HEIGHT, WIDTH.
    - Hedge height/width measurements across replicates.
  - MResLeaves.csv
    - Columns: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, REPLICATE, LEAVES_COUNT, LEAF_SAMPLE_WEIGHT.
    - Leaf counts and dry-weight measurements for biomass estimates.
  - MResBranches.csv
    - Columns: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, QUADRAT_NO, TOTAL_BRANCHES.
    - Branch counts per hedgerow quadrat.
  - MResBranchTips.csv
    - Columns: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, QUADRAT_NO, REPLICATE, BRANCH_LENGTH, GROWING_TIPS, GROWING_TIPS_2YEAR, GROWING_TIPS_3YEAR, THORN_TIPS_1YEAR, THORN_TIPS_2YEAR.
    - Detailed branch-tip morphology and growth indicators.
  - MResCN.csv
    - Columns: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, FOLIAR_C_PERCENT, FOLIAR_N_PERCENT.
    - Foliar carbon and nitrogen concentrations.
  - Referenced tables/notes
    - Treatment codes table clarifies 13 treatment combinations (including various frequency/timing/incremental and a control).
    - Metadata on sampling dates, plots, and replication.

- Data quality, provenance and governance
  - Methods, sampling protocols, and identification conducted by experienced field surveyors; expert verification of species identifications.
  - Standard protocol applied across measurements; data checked for anomalous values.
  - Missing values attributed to survey error (e.g., missed measurements); thorough checks performed after data upload to the Oracle database.
  - Data linked to a Defra-funded program (BD2114) and managed by UK Centre for Ecology & Hydrology (UKCEH).

- Access, citation and reuse
  - Data linked to scholarly publication (Facey et al., 2014) and foundational Defra/UKCEH project outputs.
  - References include foundational methods and taxonomic guides used for identification and analysis.

- Funding and stewardship
  - Long-running hedgerow experiments funded by Defra (project BD2114) and managed by UKCEH.