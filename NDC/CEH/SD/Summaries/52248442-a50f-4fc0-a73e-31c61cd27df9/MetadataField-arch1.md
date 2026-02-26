# PhenotypeField.txt and GenotypeField.txt Data Dictionary

- The document defines field-level metadata and descriptions for two data files: PhenotypeField.txt and GenotypeField.txt, used to capture multi-year phenotypic measurements and genetic markers in a tree population study.
- Scope includes site- and population-level identifiers, spatial coordinates, experimental design details, and longitudinal phenotypic measurements related to budburst and growth.

## Key data structures and files

- PhenotypeField.txt
  - Captures per-tree or per-seedling observations with hierarchical metadata:
    - Site and population identifiers (Site of Population, Population code, PopCode).
    - Spatial data (Latitude, Longitude; Decimal).
    - Experimental design fields (Block, Randomised) and replication structure.
    - Family-level data (Family, Family code, whether individuals share a mother).
    - Individual identifiers (Seedling number within family, Unique tree id).
    - Yearly and multi-year phenotype fields (e.g., I15–I20 height increments; I16, I17, etc.).
    - Budburst-related time-to-event metrics across stages and years (e.g., Time taken to reach stage 4 budburst; Time to reach stage 5; Time to reach stage 6) with year-specific labels (e.g., T4-18, T5-18, T6-18 for 2018).
    - Stage definitions include detailed descriptions (e.g., stage 4: scales open along length of shoot, no needles; stage 5: white tipped needles visible; stage 6: green needles visible; buds and observation timing).
    - First observation timing fields (e.g., first observation at [site/tree]).
    - Temporal references like “Days since the first observation” and “Time taken to reach stage X”.
    - Numerous year-specific blocks (e.g., 2015, 2016, 2017, 2018, 2019, 2020) with corresponding phenotype descriptors such as budburst timing and growth increments.
    - Data quality placeholders (NA) and descriptive text for each field.

- GenotypeField.txt
  - Contains genetic marker data:
    - sNP identifiers (snpid) and Name of SNP marker.
    - Unique individual tree id and remaining genotype columns, enabling linkage to phenotypic data via per-tree IDs.

## Phenotype semantics and measurement design

- Budburst progression and staging
  - Stage definitions describe physical shoot and needle changes during budburst, used as the basis for time-to-event calculations.
  - Measurements include:
    - Time taken to reach specific budburst stages (e.g., stage 4, stage 5, stage 6).
    - “Days since first observation” as the metric for time-to-reach stages.
    - Yearly contexts (e.g., T4-18 for 2018 reaching stage 4; T5-18 for 2018 reaching stage 5).
- Growth measurements
  - Height-related fields (I15, I16, I17, I18, I19, I20, etc.) representing height increments across years or time periods.
  - "Increment" fields capture changes in height between years (e.g., increment from one year to the next).

- Temporal coverage and first observations
  - Each site/tree pair has a documented “first observation” moment, providing a baseline for calculating days-to-reach subsequent stages.
  - Yearly extensions up to 2020 are present, with corresponding stage- and height-related metrics.

## Spatial, population, and experimental design metadata

- Site and Population
  - Site names (e.g., Glensaugh; YA; Yair) and population-level identifiers (PopCode, Population code NA in some fields).
- Geographic coordinates
  - Latitude and Longitude fields with decimal precision to locate populations.
- Experimental design
  - Block and Randomised fields indicate experimental structure for planting/phenotyping trials.
- Family and kinship
  - Family-related fields describe maternal lineage and family codes, enabling genetic analysis within a shared maternal origin.

## Genotype data integration

- SNP-level data
  - SNP identifiers and marker names in GenotypeField.txt support association analyses with phenotypic traits.
  - Per-tree linkage through Unique individual tree id enables genotype-phenotype integration across the dataset.

## Analytical opportunities and considerations

- Potential analyses
  - Time-to-event modeling for budburst stages across years and sites.
  - Cross-year growth modeling using height increments and stage transition times.
  - Genotype-phenotype association studies using SNP markers against budburst timing and growth traits.
- Key integration tasks
  - Align field definitions across years to ensure consistent stage naming and time references (e.g., stage 4 budburst across different years).
  - Harmonize missing data (NA) and ensure consistent units (e.g., decimal degrees for latitude/longitude, height units for increments).
  - Use primary keys (Site, PopCode or Population code, Family, Seedling, Individual ID) to join PhenotypeField.txt with GenotypeField.txt.

## Data quality, governance, and accessibility

- Metadata richness supports discoverability and reproducibility
  - Detailed field descriptions, units, and design metadata aid data cleaning and model replication.
- Challenges inferred from the structure
  - Large, year-by-year expansion with extensive NA placeholders may require careful schema standardization.
  - Multi-year and multi-site data necessitate robust data provenance and metadata tracking.

## Practical guidance for analysts

- Start by mapping phenotypic fields to a unified schema across years.
- Build per-tree longitudinal features using first observation as baseline (e.g., days to reach stages, height increments by year).
- Create cross-year phenotypes by aggregating stage timings and growth metrics.
- Integrate genotype data via Unique tree IDs to perform GWAS or candidate-gene analyses on budburst timing and growth traits.
- Document data lineage and preprocessing steps to ensure reproducibility for policy or research outputs.