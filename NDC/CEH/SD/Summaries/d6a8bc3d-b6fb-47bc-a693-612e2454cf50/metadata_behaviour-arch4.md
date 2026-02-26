# Experimental design/collection method

## Overview
- Objective: assess the social status achieved by each form of Maculinea rebeli within colonies of Myrmica host species using a controlled bioassay.
- Setup: Groups of five M. rebeli butterfly larvae from each region were adopted into matching colonies of naïve French Myrmica schencki and Myrmica sabuleti.
- Colony composition: Each test colony contained 20 immature individuals (five kin ant pupae, five large larvae, five small larvae) and 20 workers.
- Procedure: Three hours after introducing the M. rebeli caterpillars, the brood chamber was relocated to a nearby pad; researchers recorded the order in which the nurse ants rescued 15 brood items or the five M. rebeli and carried them to the new nest.
- Timing: The same test was repeated seven days later to allow M. rebeli to attain maximum potential integration, keeping size comparable to host pupae/larvae.
- Replication: The number of replicates varied due to occasional lack of ants and butterfly deaths, especially with some hosts.

## Experimental setup details
- Laboratory conditions: Nest with a small moist sponge pad beneath an inverted 6 cm diameter saucer with a notched entrance.
- Perturbation: Brood chamber relocation to another pad to observe rescue order.
- Timepoints: Data collected at two intervals—three hours after introduction and seven days after introduction.
- Host combinations: M. rebeli from Spain and Poland tested with host ants M. schencki and M. sabuleti.

## Data collected and stored
- Format: Eight CSV files storing results for different experiments and timepoints.
  - Behaviour_switch_3hexp1.csv, Behaviour_switch_7dexp1.csv, Behaviour_switch_3hexp2.csv, Behaviour_switch_7dexp2.csv, Behaviour_switch_3hexp3.csv, Behaviour_switch_7dexp3.csv, Behaviour_switch_3hexp4.csv, Behaviour_switch_7dexp4.csv
- File naming convention: [experiment name]_[experiment Length]_[experiment Identifier]
  - Example: Behaviour_switch_3hexp1.csv contains results recorded three hours after introduction in the first behaviour switch experiment.
- Data headers (descriptions):
  - Spain M. rebeli: M. rebeli from Spain
  - Polish M. rebeli: M. rebeli from Poland
  - M. sabuleti: Host ant species Myrmica sabuleti
  - M. schencki: Host ant species Myrmica schencki
  - Nest no.: Identifier for the nest
  - order_7day exp: Seven-day experiment order (for statistical analysis, labeled as 2)
  - order_3h exp: Three-hour experiment order (for statistical analysis, labeled as 1)
  - Ant pupae: Order of retrieval by nurse ants for ant pupae (rank 1–18)
  - Large larvae: Order of retrieval for large larvae (rank 1–18)
  - Small larvae: Order of retrieval for small larvae (rank 1–18)
  - M. rebeli: Order of retrieval for Maculinea rebeli (rank 1–18)
  - Note: nr = not retrieved

## Headers and variable descriptions (metadata)
- Regional and species identifiers to track cross-combinations (Spain Polish M. rebeli; M. sabuleti; M. schencki)
- Nest identifiers to map results to specific colonies
- Timepoint indicators (3h vs 7d) linked to corresponding CSVs
- Retrieval order variables with explicit ranking bounds (1–18) across pupae, larvae, and M. rebeli
- Missing data indicated with “nr” (not retrieved)

## Data quality, limitations, and considerations for data leaders
- Replicate variability due to occasional loss of ants or butterfly deaths affects sample size and statistical power.
- Retrieval order as a proxy for social status may be influenced by multiple factors (timepoint, host species, region of M. rebeli, colony dynamics).
- Data structure relies on consistent naming conventions and explicit metadata descriptions to ensure cross-study comparability.
- Limited regional representation (Spain and Poland) and two host Myrmica species; consider these limits when generalizing findings.
- Potential data integration benefits: standardized headers and explicit timepoint design enable meta-analytic comparisons and reproducibility across experiments.

## Practical implications for data use
- Enables analysis of host preference and social integration of parasitic caterpillars across hosts and regions.
- Facilitates examination of temporal dynamics (3h vs 7d) in social status establishment.
- Metadata and header descriptions support data discoverability and reuse, assuming CSV files are accessible and well-documented.