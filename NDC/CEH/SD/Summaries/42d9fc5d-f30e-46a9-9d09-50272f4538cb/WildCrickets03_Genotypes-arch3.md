# WildCrickets03_Genotypes Description of content

- Overview
  - Contains the microsatellite profile for each adult cricket genotyped in the population.
  - Includes 15 microsatellite markers.
  - Data track includes year, identification tag read from video, and sex.

- Data fields and structure
  - Year: the year when the cricket was alive.
  - Tag: a two-character code used to identify the cricket in video recordings; each cricket has a plastic tag on its pronotum readable in video.
  - Sex: male (M) or female (F).
  - Gbim49a and Gbim49b: scores for the two alleles of the marker Gbim49 (zero if the marker failed).
  - Similar a/b columns exist for each of the remaining 14 markers, following the same naming convention (markerNamea and markerNameb).

- Marker encoding details
  - Each marker contributes two allele scores (a and b) per cricket.
  - Marker failure is indicated by a score of zero for the corresponding allele.
  - Percentage of complete marker data depends on successful amplification for each marker.

- Linkage and observation
  - Tag links genotype data to individual crickets observed in video recordings, enabling integration of genetic data with behavioral or phenotypic observations.

- Potential uses for monitoring and policy-informing work
  - Population genetics monitoring over time (genetic diversity, relatedness, population structure).
  - Track individual crickets across time via tags and combine with behavioral or ecological data from video.
  - Support dashboards or reports that relate genetic variation to environmental or management contexts.

- Data quality and governance considerations
  - Handling of missing data due to marker failure (zeros indicate failure).
  - Consistency in column naming (markerNamea and markerNameb) for reproducibility.
  - Metadata completeness needed to verify data suitability for analysis (marker performance, sample year, tagging accuracy).
  - Clear provenance required when sharing data, including method of genotyping and any data cleaning steps.