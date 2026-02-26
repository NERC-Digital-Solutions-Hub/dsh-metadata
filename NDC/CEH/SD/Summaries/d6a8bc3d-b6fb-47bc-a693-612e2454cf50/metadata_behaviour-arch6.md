# Experimental design/collection method:

- Objective
  - Assess social status of Maculinea rebeli within colonies of two Myrmica host species by perturbing colonies and recording the retrieval order of brood items and the mimetic caterpillars.

- Experimental design
  - Groups: five M. rebeli butterfly larvae from each region adopted into matching colonies of naïve French Myrmica schencki and Myrmica sabuleti.
  - Colony composition: each replicate contained 20 immature individuals (brood items) and 20 workers.
  - Procedure: three hours after introduction, the brood chamber was uncovered and relocated to a nearby pad; recorded the order in which nurse ants rescued 15 brood items or the 5 M. rebeli into the new nest.
  - Repetition: same procedure repeated seven days later to capture maximum potential integration, with size considerations maintained (M. rebeli remain similar in size to pupae/large larvae).
  - Replicates: varied due to missing ants and butterfly deaths, especially with unnatural hosts.

- Data storage and file structure
  - Stored as eight CSV files with names following the format: [experiment name]_[experiment Length]_[experiment Identifier].
  - File examples: Behaviour_switch_3hexp1.csv, Behaviour_switch_7dexp1.csv, Behaviour_switch_3hexp2.csv, Behaviour_switch_7dexp2.csv, Behaviour_switch_3hexp3.csv, Behaviour_switch_7dexp3.csv, Behaviour_switch_3hexp4.csv, Behaviour_switch_7dexp4.csv.

- Data headers and meanings
  - Origin identifiers: Spain M. rebeli; Polish M. rebeli.
  - Hosts: M. sabuleti; M. schencki.
  - Nest no.: nest identifier.
  - Order indicators: order_7day exp; order_3h exp (coded for statistical analysis; 3h exp coded as 1; 7d exp coded as 2).
  - Retrieval ranks (for each item, 1–18): Ant pupae; Large larvae; Small larvae; M. rebeli.
  - Note: nr = not retrieved.

- Key data fields per file
  - The eight files encode, per replicate, the retrieval order for four item categories (pupae, large larvae, small larvae, M. rebeli) across two timepoints (3 hours and 7 days) and across host/origin combinations.

- Data quality and limitations
  - Replicates varied due to incomplete supplies and mortality.
  - Retrieval ranks are limited to 1–18 with some entries marked nr, affecting completeness in some replicates.

- Potential data uses and products
  - Compare social integration dynamics of M. rebeli across host species and regional origins.
  - Analyze effects of time since introduction (3h vs 7d) on retrieval order.
  - Cross-host comparisons and nest-level effects through aggregated statistics and visualizations.
  - Create data products (dashboards, pivot tables) enabling end users to explore retrieval order by host, origin, and timepoint.