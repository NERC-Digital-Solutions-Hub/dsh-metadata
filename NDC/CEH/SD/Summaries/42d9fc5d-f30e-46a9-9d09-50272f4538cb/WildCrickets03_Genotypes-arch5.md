# WildCrickets03_Genotypes Description of content

- Purpose and scope
  - Describes a file that contains microsatellite genotype profiles for each adult cricket genotyped in the population.
  - Includes data for 15 microsatellite markers.

- Data structure and schema
  - Per-record fields include:
    - Year: The year the cricket was alive.
    - Tag: A two-character code identifying the cricket from video recordings.
    - Sex: Male (M) or Female (F).
    - Gbim49a and Gbim49b: Scores for the two alleles of marker Gbim49 (a and b suffixes indicate alleles).
  - Each additional marker follows the same two-column pattern (markerNamea, markerNameb).
  - If a marker failed, the corresponding allele score is recorded as zero.

- Data quality and representation
  - Marker failures are explicitly encoded as zero values.
  - The dataset uses a consistent two-column per marker schema (allele 1 and allele 2).
  - Requires careful validation to ensure correct mapping between tags, years, sexes, and allele scores across markers.

- Provenance and lifecycle considerations
  - Data represents genotypes linked to individual cricket life history (year alive) and observational tag identifiers.
  - Links genotype data to video-derived identifications via Tag.

- Data governance and stewardship implications
  - Metadata should document:
    - The list of the 15 markers with their exact names.
    - The convention for zero values (marker failure) and any non-genotype data handling.
    - How Year, Tag, and Sex relate to the experimental or observational timeline.
  - Ensure consistent naming and encoding across datasets (e.g., markerNamea, markerNameb) for interoperability.
  - Maintain versioning and provenance to track updates and corrections to allele calls or marker coverage.
  - Store alongside or with metadata that clarifies data quality, completeness, and any embargoes or access restrictions.

- Access, sharing, and documentation
  - The data should be uploaded to appropriate data portals with clear metadata enabling discovery by researchers needing genotype and life-history linkage.
  - Documentation should include data dictionary (column meanings, marker list, and zero-as-failure rule) and usage notes for downstream analyses.

- Potential issues and mitigation
  - Incomplete data due to marker failures (zero encoding) requiring documentation of failure rates per marker.
  - Ensuring accurate linkage between Year, Tag, and Sex across records to prevent misassignment.
  - Interoperability across systems with different marker naming conventions; mitigate by adopting standardized marker naming and clear schema definitions.