# PhenotypeField.txt and GenotypeField.txt

- What this document is
  - A data dictionary outlining the fields for phenotype data (PhenotypeField.txt) across multiple years and stages, plus genotype data (GenotypeField.txt) for SNP markers and tree identifiers.

- Dataset scope and structure
  - Multi-year phenotyping dataset covering sites, populations, families, and individual trees.
  - Variables organized by data type, including identity, spatial location, population structure, and phenotypic measurements.
  - Years represented include 2015–2020 (with specific field names for each year and stage).

- Identity, population, and pedigree metadata
  - PopCode and population code; family relationships and family codes (e.g., same mother tree); seedling number within family.
  - Individual identifiers (unique tree IDs) and block/randomised experimental design fields.
  - Site-level population descriptions and population-level metadata.

- Spatial metadata
  - Latitude and Longitude (with a decimal representation); fields labeled as site/ population coordinates.
  - Spatial metadata used to map trials and analyze geographic effects.

- Phenotypic measurements and time-based data
  - Height measurements across multiple years (e.g., Height by year groups such as 2015, 2016, 2017, 2018, 2019, 2020).
  - Budburst timing data at multiple stages:
    - Stage 4: scales open along the length of the shoot (no needles) and related timing.
    - Stage 5: budburst with white tipped needles.
    - Stage 6: budburst with green needles.
  - Time-to-reach metrics:
    - Time taken to reach each budburst stage (in days) since the first observation at each site/tree.
    - Stage-specific durations, including intervals between stages and time to reach stage 4/5/6.
  - Additional growth and morphology measures:
    - Length of shoot, number of needles, and other summarized shoot metrics.
    - Stage-specific observations and observations per site/tree across years.

- Year-specific and stage-specific field organization
  - Separate field definitions for each year (2015–2020) and for corresponding budburst stages and observations.
  - Detailed descriptors for each field per year, including timing, duration, and stage progression.

- Genotype data
  - GenotypeField.txt includes SNP marker fields (snpid, marker names such as BE7_6_C_YA) and remaining columns that link markers to unique tree IDs.
  - Designed to enable association analyses between phenotypes and genotypes at the individual-tree level.

- Data quality, gaps, and metadata considerations
  - Many fields contain NA or missing placeholders, indicating incomplete data in some entries.
  - The dictionary emphasizes the need for consistent units, clear metadata, and standardized descriptors to support cross-year integration.

- Implications for data strategy and governance
  - The dataset supports multi-partner, cross-year analyses but requires robust data standards, comprehensive metadata, and consistent field definitions.
  - Strong emphasis on data discoverability, data quality, and updates to maintain usable longitudinal assets.
  - A combined phenotype-genotype framework enables linking time-to-budburst and growth traits to genetic markers for breeding or ecological studies.

- Takeaways for Data Leaders
  - Prioritize metadata alignment, field standardization, and stable identifiers to enable data integration across years and sites.
  - Ensure data discoverability and clear provenance, given the multi-year, multi-field structure.
  - Plan for data quality improvement and gap filling, and establish governance for updating both PhenotypeField.txt and GenotypeField.txt assets.
  - Facilitate cross-partner collaboration by defining common data standards and a clear data-sharing model for both phenotypic and genotypic data.