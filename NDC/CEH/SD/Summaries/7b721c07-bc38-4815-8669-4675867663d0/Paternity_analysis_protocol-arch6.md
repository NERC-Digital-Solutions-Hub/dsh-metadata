# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Purpose and scope
- Dataset to detail paternity of progeny and examine effects of floral resources on pollination services to isolated Eschscholzia californica plants; part of a larger experiment on floral resource impacts on pollination.

## Study design and sampling
- Location and timing: Hillesden estate, Buckinghamshire, UK; June 2015.
- Experimental layout: four replicate blocks (each ~100 ha) separated by >500 m; 16 arrays across blocks; central transect across the boundary between florally rich and florally poor habitats with two arrays in each habitat per block.
- Array composition: each array contains three E. californica plants, 1 m apart, arranged in a triangular formation.
- Plant material: 48 plants with distinct genotypes deployed across the landscape; all open flowers removed; one bud per plant pollinator-excluded; field exposure for 16 days; fruits tagged to ensure origin of development.

## Genotyping and laboratory methods
- Initial genotyping: 95 plants genotyped using seven microsatellite markers; DNA extracted from leaf tissue, quantified, and diluted for PCR.
- Laboratory workflow: PCR for seven loci (some multiplexing possible); fragment analysis on an ABI3730; alleles manually scored with Genemarker; ambiguous alleles cloned and sequenced for verification.
- Plant selection for deployment: 48 plants chosen to maximize genotype distinctness; triplets within arrays arranged so that homozygosity at a selected locus differed across arrays when possible.

## Progeny collection and paternity analysis
- Progeny sampling: around ten progeny per maternal plant (mean ~9.5) genotyped.
- Selfing vs outcrossing: progeny compared to maternal genotype across seven loci; selfed if a complete maternal match or homozygous maternal allele; otherwise outcrossed.
- Paternity inference: Cervus 3.0.7 used; analyses conducted within blocks; accounts for self-fertilisation; paternal assignment based on delta score and high-confidence trio (>95%).
- Outputs: for each progeny, records whether paternal assignment was made, habitat of pollen movement, and distance traveled; entries marked NA if confidence was insufficient.

## Data structure and file
- Data file: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv
- Key columns:
  - Block (replicate block ID)
  - Experimental_array (array ID within a block)
  - Plant_identification_number (plant ID prior to field transfer)
  - Fruit_number (identifier for each analysed fruit; "Maternal" for maternal samples)
  - Habitat and Treatment (location and conditions of arrays)
  - Sample_identification (allele data samples; 'M' denotes maternal)
  - lociX_AlleleY (allele sizes at each of seven loci)
  - Parentage (manual paternity scoring)
  - Paternity_analysis (paternal ID from Cervus or ? if <95%)
  - Distance_of_pollen_movement (in metres)
  - Habitat_crossed (habitat type pollen moved between)
- Data quality: NA indicates failed amplification or unresolved paternity; dataset designed to be complete with high-confidence assignments.