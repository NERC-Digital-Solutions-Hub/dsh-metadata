# WildCrickets03_Genotypes Description of content

## Overview
- Contains microsatellite profiles for adult crickets genotyped in a population.
- Includes 15 microsatellite markers.
- Records per cricket include Year, Tag, Sex, and two allele scores per marker (e.g., Gbim49a and Gbim49b).

## Data structure and contents
- Columns:
  - Year: year when the cricket was alive.
  - Tag: two-character ID read from video recordings via a plastic tag on the cricket’s pronotum.
  - Sex: M or F.
  - For each marker, two columns representing the two alleles, ending with a or b (e.g., Gbim49a and Gbim49b).
- Allele scoring:
  - Scores are numeric; if a marker failed, the corresponding allele score is zero.
- Marker naming:
  - Each marker is presented with two allele columns (a and b) to reflect diploid genotype data.

## Data quality considerations
- Zero values indicate missing/failed marker data, requiring handling during analysis.
- Consistent marker naming conventions across all 15 markers are essential for reliable data merging and analysis.
- Potential issues include incomplete data due to marker failures and misalignment between genotype rows and video-tag identifiers.

## How to use and publish
- Suitable for population genetics analyses, genotype-phenotype associations (e.g., with sex or year), and trackable individual-level genetics across time.
- Can be used to generate summaries of allele frequencies per marker, missing data rates, and genotype distributions.
- Useful in dashboards or reports that enable querying by Tag or Year and comparing marker data across individuals.

## Data preparation and transformation
- Validate alignment between Year, Tag, Sex, and allele data for each cricket.
- Handle zero-valued alleles as missing data; consider imputation or filtering depending on analysis.
- Convert between wide (marker1a, marker1b, …) and long formats as needed for specific analyses or visualization.

## Data management considerations
- Document marker names and the a/b allele structure clearly in a data dictionary.
- Maintain consistent handling of missing data across analyses and outputs.
- When sharing or publishing, provide example queries and a quick-start guide to interpret allele scores and zeros.