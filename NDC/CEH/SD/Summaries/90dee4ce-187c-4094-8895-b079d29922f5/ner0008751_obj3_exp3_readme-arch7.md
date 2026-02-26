# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

- Purpose of the experiment
  - Manipulated the fecundity-longevity relationship in Drosophila melanogaster by altering larval diet across three regimes: treatment 1 (20% SYA), 2 (100% SYA), and 3 (120% SYA).
  - Collected data from adult flies on death dates, daily/periodic egg counts, and offspring counts.
  - Data intended to support analyses described in the protocol and manuscript on the diet effects and age-related gene expression.

- Data files and scope
  - A set of CSV files, each detailing different aspects of the experiment:
    - eclosion data: counts of adult eclosions by vial, diet, source population, and timing across up to 15 counting events; includes total eclosions and mean eclosion time.
    - egg counts data: daily egg counts for life-history sub-group females, with per-fly totals and 7-day summaries.
    - female sizes: thorax and wing measurements (two measurements per trait and their means) for life-history females.
    - individual females: treatment, unique life-history ID, source population, eclosion date, sub-group, and related identifiers.
    - life-history data: per-fly age, eggs, offspring, viability, mean daily metrics, mating-event statistics, and morphometrics (thorax/wing) with means.
    - mating events: offspring and egg counts following each mating event (up to 10 events), with totals and averages.
    - offspring counts: adult offspring counts produced as eggs on each production day, with totals.
    - pupation: pupation counts per counting event, total pupation hours, mean pupation time, and mean duration as pupa.
    - replacements: records of flies replaced among sub-groups (R1, R2, L) by replacements from C group, including timing and sub-group IDs.
    - RNA sampling: sample sizes, censoring, death rates, collection dates, and ages for RNA subgroups (RNA1 and RNA2) and L subgroup.
    - tissue samples: summary data for RNA tissue pools, including sample IDs, sub-group, replicate, collection and extraction dates, and RNA sample IDs.

- Key variables and coding conventions
  - Diet encoding: 1 = 20% SYA, 2 = 100% SYA, 3 = 120% SYA.
  - Sub-groups and provenance:
    - L = life-history sub-group.
    - R1 = RNA1 sub-group (harvested after 10% mortality).
    - R2 = RNA2 sub-group (harvested after 60% mortality).
    - C = contingency sub-group (replacement pool).
  - Temporal data:
    - Treatment_date and Treatment_time mark larval-stage handling; true_hoursX fields log hours from plating to a counting event (eclosion, pupation, etc.).
    - eclosion/egg/offspring/pupation counts occur across multiple counting events (up to 15 or 16 in some files).
  - Missing and special values:
    - '.' indicates death before a count day (no value recorded for that day).
    - 'NA' indicates true missing values.
    - '*' denotes null means arising from missing values (e.g., mean computations with missing data).

- Data relationships and integration
  - Cross-file linkage keys include:
    - Life_history_number (per-fly identifier in LH_data and mating/offspring records).
    - Diet/treatment, source_population, and vial identifiers to connect production, eclosion, and fecundity data.
  - Derived metrics available or derivable:
    - Total and mean times to eclosion; mean pupation time; mean daily eggs and offspring; mating-event-based egg/offspring counts and averages.
    - Totals and means for eggs, offspring, and pupation across different life-history sub-groups and RNA sampling points.
  - RNA and tissue sampling data indicate planned molecular analyses at 10% and 60% mortality milestones, with pool-based tissue samples.

- Data quality, cleaning, and preparation considerations
  - Data are comprehensive and multi-file; integration requires careful matching on Life_history_number, Diet, Source_population, and timing fields.
  - Numerous derived statistics are present; when reusing, verify whether to use provided means or recompute from raw counts.
  - Handling of censored records (censor = d or c) is essential for lifespan and fecundity analyses.
  - Replacements logic (R1/R2/L replaced by C) affects continuity and should be accounted for in longitudinal analyses.

- Provenance, experimental design, and scope notes
  - Experiment built around dietary manipulation during larval stage and comprehensive adult-life data collection.
  - Sub-group design includes life-history individuals and two RNA sampling subgroups (R1, R2), plus contingencies.
  - RNA sampling and tissue pooling yield integrated molecular data alongside life-history phenotypes.
  - Protocols referenced for full methodological details; data files support replication and secondary analyses of fecundity, longevity, and gene expression relationships.

- Potential GIS-focused and data-management relevance
  - Although the dataset is non-spatial, it contains rich temporal and cohort information suitable for time-series and cohort analyses.
  - If location metadata (e.g., origin populations) can be georeferenced, opportunities exist to map provenance or compare across source populations.
  - For GIS-oriented workflows, consider creating a per-fly temporal sport (lifespan timeline) and linking to cohort-level summaries by diet and source population.

- Access, documentation, and references
  - Documentation date: 15 November 2021.
  - Primary sources: protocol document and a manuscript detailing the effects of larval diet on fecundity, longevity, and age-related gene expression.
  - Data are provided as a series of CSV files with explicit column descriptions in the ReadMe.