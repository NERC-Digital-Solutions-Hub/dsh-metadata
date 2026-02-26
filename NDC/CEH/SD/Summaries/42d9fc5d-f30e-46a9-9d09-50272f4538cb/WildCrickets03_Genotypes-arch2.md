# WildCrickets03_Genotypes Description of content

- Overview
  - Contains the microsatellite genotype profiles for each adult cricket genotyped in the population.
  - Uses 15 microsatellite markers to characterize genetic variation.

- Data fields and structure
  - Year: the year when the cricket was alive.
  - Tag: a two-character identifier used to recognize the cricket in video recordings; a plastic tag attached to the pronotum is readable in video.
  - Sex: male (M) or female (F).
  - Gbim49a and Gbim49b: scores for the two alleles of the marker named Gbim49; each marker has two allele columns (a and b).
  - Marker handling: if a marker failed, the corresponding allele score is recorded as zero.
  - Column naming: each marker is represented with two columns ending in a and b, respectively (e.g., Gbim49a, Gbim49b); there are 15 such markers in total.

- Data quality and representation
  - Missing or failed marker data are represented by zeros to indicate no allele score available for that marker.

- Usage and context
  - Describes genotype data that can be used for population genetics analyses and linked with identity data from video tagging.
  - Structured for standardized data handling and potential integration with additional data sources for broader analyses.