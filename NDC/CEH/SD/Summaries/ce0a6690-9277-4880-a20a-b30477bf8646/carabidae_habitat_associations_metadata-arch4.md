# A weighting method to improve habitat association analysis: tested on British carabids

- Purpose and scope
  - Presents a method to quantify habitat associations for ground beetles (Carabidae) in Great Britain using the phi coefficient of association.
  - Compares original (unweighted) and uncertainty-weighted correlation indices, including a group-equalised version, with significance tested by permutations.
  - Provides outputs to support conservation planning and landscape-scale analyses by revealing which habitats are associated with which species.

- Data sources and scale
  - Presence data from the National Biodiversity Network (NBN) atlas (2017) at 100 m grid cells; after cleaning and taxonomic reconciliation, used for 556 potential absence grid cells.
  - Habitat data from Land Cover Map 2015 (LCM2015), with 21 land-cover classes based on UK Biodiversity Action Plan Broad Habitats.
  - Data linked by intersecting NBN 100 m cells with LCM2015 habitats to compute habitat proportions within each location.

- Absence data and survey effort
  - NBN lacks explicit absence data; to infer true absences, the study uses a proxy based on survey effort: a location is considered a true absence if it contains more records than a threshold of other carabid species.
  - Thresholds explored; a threshold corresponding to 5% of the species pool (14 species) was selected, yielding 556 potential absences and enabling sensitivity analyses.

- Correlation indices and weighting
  - Unweighted approach: in locations with multiple habitats, only single-habitat squares are usable, drastically reducing data; hence a weighted approach was developed to utilize more data.
  - Weighted correlation index (Phi^w): accounts for the proportional presence of each habitat within a location, expanding data usability beyond single-habitat squares.
  - Group-equalised index (Phi^g w): adjusts for variation in the number of locations per habitat group, providing a balanced comparison across habitats.
  - For each species and method version, both original (unweighted) and weighted indices are calculated, and permutation tests provide p-values.

- Data preparation and formats
  - Data prepared as presence/absence per species across locations, converting multiple records per location into a wide-format matrix with binary presence indicators per species.
  - Table-like descriptions define fields including habitat, habitat proportion, species presence, and presence/absence for each species.

- Analyses and reproducibility
  - Analyses conducted on a computing cluster (JASMIN); aimed to be reproducible with specified workflows.
  - Outputs include multiple versioned CSVs to support user confidence in habitat-species associations:
    - Weighted and unweighted versions with thresholds 7, 14, and 28 (carabidae_habitat_associations_weighted07.csv, unweighted07.csv, weighted14.csv, unweighted14.csv, weighted28.csv, unweighted28.csv).
  - Confidence recommendations: place confidence only in species with 50 or more records used in the association calculation.
  - R package PhiCor (and related methods) is provided for users to reproduce or apply the weighting approach to other species.

- Practical outputs and guidance
  - The study provides a concrete output suite (habitat associations with and without weighting, across multiple absence thresholds) to inform landscape planning, habitat restoration, and species-specific conservation prioritization.
  - The approach enables users to explore how weighting by habitat proportions affects inferred associations and to test robustness with different thresholds.

- Data governance, accessibility, and resources
  - Uses open data sources (NBN atlas, LCM2015) and aligns with a reproducible, open workflow.
  - Phyto-based methodology and weighting approach are supported by cited software (PhiCor) and publications, with a GitHub resource for implementation.
  - Emphasizes the importance of metadata, data provenance, and clear documentation for enabling broader use across species in ecological and conservation decision-making.