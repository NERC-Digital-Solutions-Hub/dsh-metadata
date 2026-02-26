# Experimental design/collection method

## Objective
- Assess the social status achieved by Maculinea rebeli within colonies of each Myrmica species in a standard bioassay.
- Determine the order in which nurse ants retrieve either their brood or the mimetic M. rebeli caterpillars after perturbing the nest.

## Experimental design and procedure
- Subjects: Groups of five butterfly larvae from each region adopted into matching laboratory colonies of Myrmica schencki and Myrmica sabuleti.
- Colony composition: Each test colony contained 20 immature individuals (brood items) and 20 workers.
- Setup: Laboratory colonies contained a moist sponge pad under an inverted dish with a notched entrance; brood and M. rebeli were placed beneath.
- Perturbation: Three hours after introduction, the brood chamber was uncovered and moved to a nearby pad; the researchers recorded the order of rescue for 15 brood items and 5 M. rebeli.
- Repetition: The same experiment was repeated seven days later to capture the integration status when caterpillars are near maximum host-adaptation size.
- Replicates: Varied due to occasional lack of ants and butterfly deaths, especially with unnatural hosts.

## Data format and storage
- Storage: Eight CSV text files.
- File naming convention: [experiment name]_[experiment Length]_[experiment Identifier]
  - Examples: Behaviour_switch_3hexp1.csv, Behaviour_switch_7dexp1.csv, Behaviour_switch_3hexp2.csv, Behaviour_switch_7dexp2.csv, Behaviour_switch_3hexp3.csv, Behaviour_switch_7dexp3.csv, Behaviour_switch_3hexp4.csv, Behaviour_switch_7dexp4.csv
- Headers and meaning (descriptions provided in the dataset):
  - Spain M. rebeli: Identifier for the Maculinea rebeli from Spain
  - Polish M. rebeli: Identifier for the Maculinea rebeli from Poland
  - M. sabuleti: Identifier for the ant Myrmica sabuleti
  - M. schencki: Identifier for the ant Myrmica schencki
  - Nest no.: Identifier of the nest
  - order_7day exp: Seven-day experiment code used for statistical analysis (label 2 in analysis)
  - order_3h exp: Three-hour experiment code used for statistical analysis (label 1 in analysis)
  - Ant pupae: Retrieval order for ant pupae; rank 1–18
  - Large larvae: Retrieval order for large larvae; rank 1–18
  - Small larvae: Retrieval order for small larvae; rank 1–18
  - M. rebeli: Retrieval order for Maculinea rebeli; rank 1–18
  - nr: not retrieved
- Notes on data structure:
  - The retrieval orders are ranked values (1 to 18) indicating attention by nurse ants.
  - Each row corresponds to a retrieval event for a given category; missing retrievals are coded as nr.

## Replication, data quality, and limitations
- Replication varied due to missing ants and butterfly mortality, leading to unequal numbers of replicates across combinations.
- Some data may be incomplete (nr = not retrieved) for certain categories or trials.
- The experimental setting is laboratory-based, with controlled perturbations, which may limit direct extrapolation to natural conditions.

## Relevance for monitoring frameworks
- Structure and metadata: The dataset is organized into clearly named files with explicit headers identifying species, nest, and experimental conditions, aiding traceability and reuse.
- Metadata clarity: Header descriptions provide essential provenance (origin of M. rebeli, host species, nest identifiers) and outcome measures (ranked retrieval orders).
- Data quality and governance considerations:
  - Metadata is embedded in headers; explicit dataset-level metadata files are not described.
  - Data presence in multiple files captures temporal (3-hour vs 7-day) and experimental variation (multiple behavior-switch experiments), which supports monitoring of host-parasite interactions over time.
  - Data limitations due to replication variability and possible incomplete retrievals highlight the need for clear documentation of missing data and handling rules in any monitoring framework.
- Potential reuse: Suitable for analyses comparing host species effects and regional origins on the integration success of a social parasite, with standardized ranking scales and identifiable data lineage.