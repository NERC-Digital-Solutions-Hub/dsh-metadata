# The data are the habitat association (phi coefficient of association) of ground beetles (Carabidae) in Great Britain (Chetcuti, Kunin, & Bullock, 2019)

## Aim and scope
- Analyze habitat associations of British ground beetles using phi coefficient (Φ) to quantify association or disassociation with land-cover habitats.
- Provide outputs that support landscape planning and conservation prioritisation by revealing which habitats are positively or negatively associated with specific carabid species.
- Offer multiple output variants (weighted and unweighted) at different thresholds to help users assess confidence in habitat–species associations.

## Data sources
- Carabid occurrence data: National Biodiversity Network (NBN) atlas (presence records, 100 m grid cells), 2017 release; initial filtering to at least 10 records per species.
- Habitat data: Land Cover Map 2015 (LCM2015) for Great Britain, 21 land-cover classes based on UK Biodiversity Action Plan Broad Habitats.
- Species validation: NBN names reconciled with Natural History Museum UK inventory and Luff (2007) taxonomy; presence/absence decisions rely on survey effort proxies.
- Data processing and tools: ArcGIS for gridding, R for data formatting, JASMIN cluster for analysis and permutations, PhiCor R package for reproducibility.

## Data preparation and quality assurance
- Data cleaning: resolve synonyms; standardise species names; convert coordinates to 100 m grid cells.
- Absence data handling: since NBN lacks true absence data, use presence of other carabids at a location as a proxy for survey effort; define true absences using a threshold number of other species observed.
- Thresholds for confidence: absence threshold set at 14 other carabid species (5% of potential observations) to define a credible absence grid cell; sensitivity analyses performed around this value.
- Data structure: convert to a wide format with binary presence/absence for each species at each location.
- Location filtering for unweighted analysis: discard grid cells containing multiple habitats for the unweighted approach; to maximise data usage, apply a weighted approach that accounts for habitat proportions within a cell.

## Methods: correlation indices
- Unweighted correlation index (Φ): calculated using locations with a single habitat; presence/absence of species within that habitat.
- Weighted correlation index (Φ with weighting): accommodates locations containing multiple habitats by weighting by habitat proportion within each location; presents a more data-efficient alternative when multiple habitats are present.
- Group-equalised version: an additional comparison where habitat groups are treated with a group-weighted approach.
- Statistical inference: both original and uncertainty-weighted Φ values are computed and assessed against null expectations via permutation tests (De Cáceres & Legendre, 2009) to obtain p-values for each habitat–species combination.

## Outputs and interpretation
- Recommended outputs (habitat–species associations) are provided in several CSV variants:
  - carabidae_habitat_associations_weighted14.csv (weighted, threshold 14)
  - carabidae_habitat_associations_unweighted07.csv (unweighted, threshold 7)
  - carabidae_habitat_associations_unweighted14.csv (unweighted, threshold 14)
  - carabidae_habitat_associations_unweighted28.csv (unweighted, threshold 28)
  - carabidae_habitat_associations_weighted07.csv (weighted, threshold 7)
  - carabidae_habitat_associations_weighted28.csv (weighted, threshold 28)
- Confidence guidance: interpret results primarily for species with at least 50 presence records in the analysis.
- Reproducibility: results can be recreated with the PhiCor R package (Chetcuti, 2018); the package and related methods are described for replication (GitHub: https://github.com/Zabados/PhiCor and associated publication).

## Practical workflow and tools
- Data handling: use NBN atlas records, convert to 100 m grid, and align with LCM2015 habitat classes.
- Analysis platform: R for data-wide processing; JASMIN for computing Φ values and permutation-based p-values.
- Data visualization and dissemination: outputs suitable for maps, tables, and standard reports; clear documentation of thresholds and data provenance.
- Accessibility for others: the weighting method and outputs are designed to allow others to reproduce or extend analyses with similar data.

## Relevance for environmental monitoring and policy
- Standardised approach to quantify habitat associations across many species and habitats facilitates monitoring of environmental health and policy performance over time.
- The weighted approach enables more complete use of available data, improving comparability and reducing data loss due to multi-habitat grid cells.
- Clear confidence criteria (minimum 50 records; presence/absence proxy via survey effort) supports robust scenario testing in landscape planning and conservation prioritisation.
- Outputs are designed to be integrated with broader monitoring datasets and shared through public repositories, supporting transparency and data reuse.

## Limitations and considerations for use
- Absence data are inferred from survey effort proxies, which introduces uncertainty; results depend on the chosen threshold for absence.
- Merging small or narrow habitats in LCM2015 may underrepresent certain habitat types, potentially biasing associations for species with specialized microhabitat requirements.
- Threshold choices (7, 14, 28) and the focus on 50+ records should guide interpretation and depend on the conservation question and data availability.
- Users should consider running sensitivity analyses with alternative thresholds or weighting schemes to assess robustness in their specific context.

## Key references and resources
- PhiCor package and methodology for habitat association analysis.
- Permutation-based significance testing for associations (De Cáceres & Legendre, 2009).
- Land Cover Map 2015 dataset and related documentation (Rowland et al., 2017a, 2017b).
- NBN Atlas and UK species inventories for data sourcing and validation.
- Supporting literature on habitat associations, connectivity, and conservation prioritisation relevant to habitat-based analyses.