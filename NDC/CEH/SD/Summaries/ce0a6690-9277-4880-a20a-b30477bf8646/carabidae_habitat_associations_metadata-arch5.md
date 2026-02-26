# The data are the habitat association (phi coefficient of association) of ground beetles (Carabidae) in Great Britain (Chetcuti, Kunin, & Bullock, 2019)

## Overview
- Investigates habitat associations of British ground beetles using large-scale presence data and land-cover information to inform conservation planning, habitat loss effects, and landscape connectivity.
- Produces multiple dataset versions that reflect different weighting schemes and absence definitions to support confidence in habitat-species associations.

## Data sources and provenance
- Data sources
  - NBN atlas (2017): presence records for carabid species at 100 m grid cells; after cleaning and standardizing species names (NHM UK checklist Raper 2014; Luff 2007).
  - Land Cover Map 2015 (LCM2015): 21 land-cover classes used to assign habitat proportions within each 100 m location.
- Absence data and survey effort
  - Absence locations determined by a threshold of other carabid species observed at a location (14 species, ~5% threshold), enabling confident assignment of true absences.
- Data handling and reproducibility
  - Initial grid assignment and habitat intersection performed in ArcGIS; subsequent data processing in R; analyses executed on the JASMIN cluster.
  - Reproducibility facilitated by PhiCor R package (GitHub) and cited methodological references.

## Data preparation and processing
- Data transformation
  - For each species, multiple records per location are collapsed to a single presence/absence indicator; produced a wide-format binary matrix (one column per species).
- Habitat assignment and weighting
  - Locations with multiple habitats present were handled using a weighting approach rather than discarding data, enabling broader data use.
  - Weighted correlation index (Phi^w) accounts for habitat proportions within each location; a group-equalised variant (phi^g w) is also defined.
  - Formulas and variables involve N (total locations), n (total occurrences), and habitat proportions; weighting adjusts n_p^w and N_p^w using habitat proportions.
- Statistical analysis
  - Computed both original and uncertainty-weighted correlation indices; assessed significance via permutation tests (De Cáceres & Legendre, 2009).
- Data assembly and formats
  - Intersected NBN locations with LCM2015 to determine habitat proportions per location; presence/absence per species across locations.
  - Prepared both single-location and wide-format data representations for analysis and sharing.
- Output structure
  - Outputs include multiple dataset versions with different thresholds and weighting schemes (see below).

## Indices, thresholds, and statistical testing
- Correlation indices
  - Original Phi index and uncertainty-weighted Phi index; also includes a group-equalised version.
- Thresholds and absence rules
  - Absence definitions rely on the 14-species threshold (5% of locations with sufficient survey effort); sensitivity analyses explored other thresholds.
  - Outputs include both weighted and unweighted versions at thresholds of 7, 14, and 28 (e.g., carabidae_habitat_associations_weighted14.csv; unweighted07.csv, unweighted14.csv, unweighted28.csv; weighted07.csv, weighted28.csv).
- Statistical significance
  - P-values derived from permutation tests to assess the likelihood of observed associations under randomization.

## Data products and reproducibility
- Data products
  - carabidae_habitat_associations_weighted14.csv (recommended output with a 14-threshold weighting)
  - Unweighted and weighted versions at thresholds 07, 14, 28 (e.g., carabidae_habitat_associations_unweighted07.csv, carabidae_habitat_associations_unweighted14.csv, carabidae_habitat_associations_unweighted28.csv, carabidae_habitat_associations_weighted07.csv, carabidae_habitat_associations_weighted28.csv)
  - Group-equalised versions (phi^g_w) and related outputs
- Guidance for replication
  - PhiCor R package (GitHub) available to reproduce analyses and explore alternative weighting schemes.
  - Methodological references available for deeper understanding of indices and permutation testing.

## Data quality, limitations, and governance
- Quality and curation
  - Taxonomic standardization and synonym resolution improve data reliability.
  - Absence inference depends on survey effort proxy (presence of other species), which introduces assumptions about detectability.
- Limitations and biases
  - Absence threshold choices (14 species) influence dataset size and results; sensitivity analyses mitigate but do not eliminate bias.
  - 100 m grid resolution and Land Cover Map 2015 may not capture microhabitat variation; merging small polygons (>0.5 ha) could remove linear habitats.
  - The weighting approach aims to utilize more data but introduces complexity in interpretation and requires careful methodological understanding.
- Documentation and transparency
  - Clear description of fields (Habitat, R, pR, Rg, pRG, AbsenceCut, n) in the accompanying table (Table 1); explicit explanation of thresholds in sections 2.1 and 2.2.1.
  - Data provenance, processing steps, and analysis choices are documented to support reuse and auditability.

## Usage and implications for data stewardship
- Reuse opportunities
  - Supports conservation planning, habitat management, and landscape-scale connectivity analyses by providing quantified habitat associations for carabid species.
  - Enables replication and comparative analyses through PhiCor and documented methodology.
- Governance considerations
  - Maintain provenance records (data sources, processing steps, thresholds, and weighting schemes) to ensure reproducibility.
  - Provide metadata on survey effort proxies and habitat proportions to aid interpretation of absences and associations.
  - Include caveats on limitations related to data resolution, potential biases from absence definitions, and habitat representation.
- Practical takeaways for data stewards
  - Adoption of transparent data cleaning, standardization of taxonomic names, and explicit handling of multi-habitat locations enhances data reliability.
  - Use of multiple dataset versions with clear naming conventions and thresholds improves user confidence and enables sensitivity analyses.
  - Availability of code and reproducible workflows (PhiCor, R scripts, ArcGIS steps) facilitates broader reuse and auditability.