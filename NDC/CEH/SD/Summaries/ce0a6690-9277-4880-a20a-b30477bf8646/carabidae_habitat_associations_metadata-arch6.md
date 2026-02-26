# A weighting method to improve habitat association analysis: tested on British carabids

## Purpose and outputs
- Quantifies habitat associations (phi coefficient) for ground beetles (Carabidae) across Great Britain using large-scale presence data and land-cover information.
- Compares two approaches: unweighted (single-habitat only) and weighted (proportions of habitats within locations) to maximize usable data.
- Produces data products (CSV files) of habitat–species associations with different thresholds to assess confidence:
  - Unweighted and weighted versions at thresholds 07, 14, and 28 (carabidae_habitat_associations_unweighted07.csv, _unweighted14.csv, _unweighted28.csv, carabidae_habitat_associations_weighted07.csv, _weighted14.csv, _weighted28.csv).
- Recommends placing confidence in species with 50+ records used in the association calculations.
- Provides guidance to reproduce results with the PhiCor R package (GitHub: https://github.com/Zabados/PhiCor).

## Data sources and preparation
- Carabid data
  - Source: National Biodiversity Network (NBN) atlas (2017) with presence records at 100 m resolution.
  - Processing: filter to species with sufficient records, map to 100 m grid cells, standardize names against NHM UK and Luff checklists.
  - Absence data: inferred using an absence threshold based on survey effort—locations with more than a threshold of other carabid records are considered true absences for the species of interest.
  - Absence threshold: 14 other carabid species (5% of the species pool), yielding 556 potential absence grid cells; sensitivity analysis performed.
- Land cover
  - Source: Land Cover Map 2015 (LCM2015) for Great Britain (21 classes based on UK Biodiversity Action Plan).
  - Processing: intersect LCM2015 with 100 m NBN squares; calculate the proportion of each habitat within each location.
  - Data limitations: small polygons <0.5 ha merged, which can affect linear habitats; no further habitat grouping beyond the 21 classes.
- Data preparation for analysis
  - Created a single presence/absence row per location per species (wide format) for analysis.
  - Multi-habitat locations (locations containing more than one habitat) pose challenges; addressed via weighting in the Phi^w approach.

## Methods and analysis
- Correlation indices
  - Unweighted correlation (Phi): uses only locations with a single habitat; discards multi-habitat squares, which can reduce data and sometimes render a species unviable for analysis.
  - Weighted correlation (Phi^w): uses the proportion of each habitat within a location to weight the data, enabling use of locations with multiple habitats.
  - Group-equalised version (Phi^g_w): a variant that further adjusts for habitat groupings.
- Computation and inference
  - Calculated both the original (unweighted) and the uncertainty-weighted correlation indices.
  - Assessed significance via permutation tests (De Cáceres & Legendre, 2009) to obtain p-values for each habitat–species combination.
- Outputs and interpretation
  - For each species and each method/version, reports include:
    - Habitat class
    - Association scores (R for unweighted; R^w or R_g^w for weighted/group-equalised)
    - Significance (p-values)
    - AbsenceCut threshold used
    - n: number of presence locations
- Table 1 (fields)
  - Fields include Habitat, group, R, pR, Rg, pRG, species, AbsenceCut, n, and total presence/absence locations.

## Data products and reproducibility
- Output files
  - Unweighted versions: carabidae_habitat_associations_unweighted07.csv, carabidae_habitat_associations_unweighted14.csv, carabidae_habitat_associations_unweighted28.csv
  - Weighted versions: carabidae_habitat_associations_weighted07.csv, carabidae_habitat_associations_weighted14.csv, carabidae_habitat_associations_weighted28.csv
- Thresholds and recommendations
  - Primary recommended output uses AbsenceCut = 14 (weighted and unweighted variants available with 7 and 28 as alternative confidence checks).
  - Confidence criteria: at least 50 presence records used in calculation.
- Access to replication tools
  - PhiCor R package available for calculating habitat associations and reproducing results (GitHub link provided in the document).
- Analysis environment
  - Analyses performed on high-capacity computing resources (JASMIN cluster).
  - GIS processing with ArcGIS; data preparation and wide-format conversion via R scripts.

## Data sources and references
- NBN Atlas (carabid location records, 100 m grid)
- LCM2015 Land Cover Map (21 classes; CEH/Rowland et al.)
- Key methodological references:
  - PhiCor package (Chetcuti, 2018)
  - A weighting method to improve habitat association analysis (Chetcuti, Kunin, & Bullock, 2019)
  - Permutation-based inference (De Cáceres & Legendre, 2009)
  - Supporting literature on habitat associations, connectivity, and conservation planning
- Data processing and tool references:
  - ArcGIS v10.4.1
  - R (wide-format transformation)
  - JASMIN cluster for computing
  - NHM UK species inventory and Luff (2007) for taxonomic standardization

## Practical implications and use cases
- Conservation planning and landscape management
  - Understand which habitats are strongly associated with particular carabid species to inform habitat restoration and connectivity.
  - Assess potential impacts of adding or removing habitat patches on species presence and movement.
- Data-driven policy and public communication
  - Produce transparent, reproducible habitat–species associations for informing policy discussions and public reporting.
- Methodological flexibility
  - Weighted approach enables leveraging data with habitat heterogeneity, increasing usable data and potentially improving inference in datasets with multiple habitats per location.
- Reproducibility and adaptability
  - The PhiCor package and the documented thresholds enable other researchers to reproduce analyses for different taxa or regions using similar data structures.

## Limitations and cautions
- Absence inference relies on proxy survey effort (presence of other species), which may introduce bias if survey effort varies spatially.
- Data sparseness and patchiness; multi-habitat locations require weighting to maximize data usage but introduce assumptions about habitat proportions.
- Merging of small land-cover polygons may underrepresent linear or edge habitats, influencing habitat association scores.
- Threshold choices (e.g., AbsenceCut = 14) are somewhat arbitrary and subject to sensitivity analyses.