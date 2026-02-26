# Experimental design/collection method

- Objective: Assess the social status achieved by Maculinea rebeli within colonies of Myrmica species using a standard bioassay that perturbs lab ant colonies and records rescue order of brood and mimetic caterpillars.
- Subjects and setup:
  - Groups: butterfly larvae from Spain and Poland adopted into naïve French Myrmica schencki and Myrmica sabuleti colonies.
  - Colony composition per replicate: 20 immature individuals (5 butterfly larvae, 5 kin ant pupae, large larvae, and small larvae) and 20 worker ants.
  - Nest arrangement: small moist sponge pad under an inverted 6 cm saucer with a notched entrance; brood and M. rebeli placed in proximity to workers.
- Experimental perturbation:
  - 3 hours after introduction, brood chamber is uncovered and relocated onto an adjacent pad; record order in which nurse ants rescue 15 brood items or the five M. rebeli and transfer them to the new nest.
  - Repetition: same experiment repeated seven days later to allow maximum integration with host society while maintaining similar size to brood items.
  - Variability: replicates per ant-butterfly combination varied due to missing ants or butterfly deaths (especially with unnatural hosts).
- Temporal design:
  - Two timepoints per experiment: 3-hour (first) and 7-day (second) observations.
  - Four separate behaviour switch experiments, each with both 3-hour and 7-day data collection, totaling eight data files.

## Data storage and structure

- Formats: Eight CSV files storing the results.
- Naming convention: [experiment name]_[experiment Length]_[experiment Identifier]
  - Examples:
    - Behaviour_switch_3hexp1.csv
    - Behaviour_switch_7dexp1.csv
    - Behaviour_switch_3hexp2.csv
    - Behaviour_switch_7dexp2.csv
    - Behaviour_switch_3hexp3.csv
    - Behaviour_switch_7dexp3.csv
    - Behaviour_switch_3hexp4.csv
    - Behaviour_switch_7dexp4.csv
- File purpose:
  - 3-hour files capture results after introduction for the first behavior switch experiments.
  - 7-day files capture results seven days after introduction for the first behavior switch experiments.

## Headers and data variables

- Species and origin:
  - Spain M. rebeli
  - Polish M. rebeli
  - M. sabuleti (host ant species)
  - M. schencki (host ant species)
- Nest and experimental identifiers:
  - Nest no. (nest identifier)
  - order_7day exp (7-day experiment index for statistical analysis; value 2)
  - order_3h exp (3-hour experiment index for statistical analysis; value 1)
- Behavioral outcomes (ranked order of retrieval):
  - Ant pupae (order of retrieval; rank 1–18)
  - Large larvae (order of retrieval; rank 1–18)
  - Small larvae (order of retrieval; rank 1–18)
  - M. rebeli (order of retrieval; rank 1–18)
- Not retrieved:
  - nr denotes not retrieved

## Data quality, limitations, and scope

- Replicates varied due to practical constraints (ant availability, butterfly mortality, especially with unnatural hosts).
- Data are structured for cross-species and cross-region analysis, enabling comparisons of integration success across host ants and butterfly origins.
- Headers include explicit explanations and intended statistical coding (e.g., 3-hour vs 7-day experiment identifiers) to support reproducibility and cross-file aggregation.

## Potential GIS-relevant implications

- The dataset includes geographic origin (Spain, Poland) linked to a host species context (two Myrmica species) and nest identifiers, enabling spatial or spatial-temporal visualization of social integration outcomes.
- Possible map-based analyses:
  - Visualize integration success by origin region and host species.
  - Compare spatially distributed replicates across nests (Nest no.) and timepoints (3h vs 7d).
  - Integrate with additional spatial data to explore environmental or regional factors that correlate with behavioural outcomes.
- Data organization (consistent file naming and explicit headers) supports merging with GIS attributes for broader spatial analyses of host-parasite interactions.