# Experimental design/collection method

- Purpose: Assess the social status achieved by Maculinea rebeli caterpillars within colonies of two Myrmica ant species by observing which brood items or mimetic caterpillars were rescued after perturbing the brood chamber.
- Organisms and setup:
  - Butterflies: groups of five M. rebeli larvae from each region (Spain and Poland).
  - Ant hosts: naïve French Myrmica schencki and Myrmica sabuleti.
  - Colony composition per replicate: 20 immature ant items (pupae and larvae, both large and small) and 20 workers.
  - Laboratory setup: small moist sponge pad under an inverted 6 cm saucer with a notched entrance; brood chamber placed on a separate pad for relocation during perturbation.
- Experimental procedure:
  - Three hours after introduction of M. rebeli caterpillars, perturb the colony by uncovering and relocating the brood chamber to a nearby pad.
  - Record the order in which the nurse ants rescue each brood item (ant pupae, large larvae, small larvae) and the Maculinea rebeli, into the new nest.
  - Repeat the same experiment seven days later, allowing caterpillars to reach maximum host integration while remaining similar in size to host pupae/larvae.
- Replication details:
  - Number of replicates per ant-butterfly combination varied due to availability of ants and butterfly deaths, particularly with less cooperative hosts.

## Data format and file structure

- There are eight CSV files, named with the pattern: [experiment name]_[experiment Length]_[experiment Identifier].
  - Examples:
    - Behaviour_switch_3hexp1.csv (results at 3 hours for the first behaviour switch experiment)
    - Behaviour_switch_7dexp1.csv (results at 7 days for the first behaviour switch experiment)
    - Behaviour_switch_3hexp2.csv, Behaviour_switch_7dexp2.csv, Behaviour_switch_3hexp3.csv, Behaviour_switch_7dexp3.csv, Behaviour_switch_3hexp4.csv, Behaviour_switch_7dexp4.csv
- Each file corresponds to one of four behaviour-switch experiments, with both 3-hour and 7-day observation points.

## Variables and data headers

- Species and origins:
  - Spain M. rebeli: identifier for M. rebeli from Spain
  - Polish M. rebeli: identifier for M. rebeli from Poland
  - M. sabuleti: Myrmica sabuleti
  - M. schencki: Myrmica schencki
- Experimental context:
  - Nest no.: nest identifier
  - order_7day exp: seven-day experiment coding (statistical use: value 2)
  - order_3h exp: three-hour experiment coding (statistical use: value 1)
- Behavioral measures (ranked retrieval order; 1 is highest attention, 18 is lowest):
  - Ant pupae: retrieval order for ant pupae
  - Large larvae: retrieval order for large larvae
  - Small larvae: retrieval order for small larvae
  - M. rebeli: retrieval order for Maculinea rebeli
- Scale and data quality:
  - Ranks range from 1 to 18
  - nr = not retrieved

## Data interpretation notes

- The rank values reflect the attention of nurse ants in rescuing items; lower numbers indicate higher priority.
- The seven-day data are coded for analysis with a standard value (order_7day exp = 2) for statistical compatibility, while the three-hour data use (order_3h exp = 1).

## Replication and limitations

- Replicates varied by availability of ants and butterfly specimens, which can affect comparability across combinations.
- Some data may be missing (nr indicates not retrieved), impacting downstream analyses.

## Data governance and stewardship considerations

- Metadata and data dictionary:
  - Maintain a clear data dictionary defining all headers, coding schemes, and the meaning of 3h and 7d experimental identifiers.
  - Preserve consistent species labels and nest identifiers to ensure unambiguous cross-file joins.
- Data quality and completeness:
  - Track missing values (nr) and document reasons for non-retrieval when possible.
  - Capture replication counts per combination to support transparency of statistical power.
- Provenance and versioning:
  - Record experiment name, length, and identifier per file to preserve provenance and enable reproducibility.
- Interoperability and storage:
  - Store eight CSVs with consistent encoding and delimiter usage.
  - Consider adopting a concise data dictionary or schema document to accompany the dataset for discoverability and reuse.
- Access and reuse:
  - No privacy or safety concerns identified; data primarily involve insect behavior in controlled laboratory settings.
  - Provide clear guidance on how to interpret 3h vs 7d data and the renumbered statistical codes for analysis.