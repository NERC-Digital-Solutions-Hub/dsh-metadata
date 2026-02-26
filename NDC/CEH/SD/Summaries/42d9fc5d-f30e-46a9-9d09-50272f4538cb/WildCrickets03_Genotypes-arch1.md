# WildCrickets03_Genotypes Description of content

- This file provides the microsatellite genotype profiles for each adult cricket genotyped in the population.
- It includes data for 15 microsatellite markers per cricket.

- Key identifiers and attributes per record:
  - Year: The year when the cricket was alive.
  - Tag: A two-character code used to identify the cricket in video recordings; each cricket carries a plastic tag on its pronotum readable in the video.
  - Sex: Male (M) or Female (F).

- Marker data structure:
  - For each of the 15 microsatellite markers, there are two allele score columns, identified by the marker name ending with 'a' and 'b' (e.g., Gbim49a, Gbim49b).
  - Each marker uses two scores representing the two alleles of that marker for the cricket.

- Data encoding details:
  - Allele scores are numeric.
  - If a marker fails, the corresponding allele score is recorded as zero.
  - The naming convention applies to all markers, with columns ending in 'a' for one allele and 'b' for the other.

- Practical use:
  - Enables analysis of genetic profiles across individuals and years, facilitating studies of genetic variation, relatedness, and population structure within the sampled cricket population.