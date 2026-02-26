# WildCrickets03_Genotypes Description of content

- The file provides the microsatellite profile for each adult cricket genotyped in the population, across 15 microsatellite markers.
- Key identifiers included:
  - Year: the year the cricket was alive.
  - Tag: a two-character code used to identify crickets in video recordings; each cricket has a plastic tag on its pronotum readable in video.
  - Sex: male (M) or female (F).
- Genotype data structure:
  - For each marker, two alleles are recorded, with columns named for each allele (e.g., Gbim49a and Gbim49b for the Gbim49 marker).
  - When a marker failed, the cricket is scored as zero for that allele.
  - This pattern extends to all remaining markers, with column headings that include the marker name and end with 'a' (first allele) or 'b' (second allele).
- Data quality notes:
  - Zero indicates missing or failed marker data.
  - Marker failures can lead to incomplete genotype profiles requiring handling in downstream analyses.
- Practical implications for data management:
  - The dataset links genetic data to individual cricket identities via the Tag and Year, enabling integration with video observations.
  - Clear, consistent naming conventions facilitate automated data ingestion and quality checks across all 15 markers.