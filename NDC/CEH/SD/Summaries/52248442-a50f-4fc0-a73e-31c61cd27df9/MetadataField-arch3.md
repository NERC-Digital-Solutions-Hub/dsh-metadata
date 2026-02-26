# PhenotypeField.txt

- Purpose and scope
  - Metadata schema for a multi-year tree phenotyping and genotyping dataset.
  - Captures per-site, per-tree, per-year phenotype measurements and time-to-event metrics (e.g., time to reach budburst stages).
  - Supports linking phenotypic observations with genotype information (via GenotypeField.txt).

- Core data categories

  - Site and population metadata
    - Site of population
    - Population code (PopCode)
    - Population naming and designation (e.g., planted trials with identifiers such as Glensaugh; YA, Yair)
    - Latitude and longitude coordinates (Latitude, Longitude) with decimal precision

  - Experimental design and sampling
    - Population-level identifiers (PopCode; Population code NA)
    - Family-related fields (Family; family code and relationships, e.g., from the same mother tree)
    - Seedling and trial structure (Seedling number within family; Block; Randomised)
    - Temporal scope across years (2015, 2016, 2017, 2018, 2019, 2020; year-specific fields labeled with year and stage)

  - Phenotype data fields
    - Hierarchical identifiers (ID; Unique individual tree ID)
    - Morphometric attributes (Height; Height in cm; increment)
    - Stage-based phenology (Stage categories; e.g., budburst stages such as stage 4, stage 5, stage 6)
    - Stage definitions and descriptive text (e.g., Stage 4: scales open along length of shoot; budburst with or without needles)
    - Time-to-event metrics (Time taken to reach stage X; Days since first observation at site)
    - Year-specific phenotype blocks (e.g., 2015, 2016, 2017, 2018, 2019, 2020 blocks) with:
      - Time-to-stage fields (e.g., T4-16, T5-17, T6-17)
      - Per-year observations and derived measures (e.g., days to reach budburst, increment across years)

  - Temporal structure and year-over-year details
    - Yearly coding patterns indicating when measurements were recorded (e.g., 2015) and corresponding phenotype fields
    - Cross-year variables such as increment (increase in height from year to year) and stage progression over time

  - Data types and handling of missing values
    - Numerical fields (e.g., Height in cm, Time in days)
    - Decimal coordinates for location
    - Coded textual descriptors for stages and observations
    - Notation of missing values (NA) and placeholders for yet-to-be-observed data

- Specific field characteristics and examples
  - Spatial fields: Latitude, Longitude (decimal degrees)
  - Genetic linkage: Unique tree identifiers used to align with genotype data (GenotypeField.txt)
  - Phenology: Budburst and growth metrics tracked as both absolute values (height, shoot length) and relative progression (days to reach stage 4/5/6)
  - Stage descriptors: Complex narrative for each stage (e.g., “stage 4 (scales open along length of shoot, no needles)” or “budburst days since first observation”)
  - Yearly scaffolding: Repeated, year-labeled blocks (e.g., 2015, 2016, 2017, 2018, 2019, 2020) containing a consistent set of fields adapted for that year
  - Time-to-reach-stage metrics: Variables like T4-16, T5-17, T6-18 indicating time (in days) to reach a given budburst stage in a specific year

- Genotype linkage (GenotypeField.txt)
  - SNP-related fields
    - snpid: Name of SNP marker
    - Unique individual tree id (e.g., BE7_6_C_YA)
    - Remaining columns: genotype data for each tree (e.g., BE7_6_C_YA genotype calls)
  - Purpose: Enables linking phenotypic observations with genetic markers, supporting integrated monitoring and association analyses

- Data governance and quality considerations
  - Metadata completeness: The schema emphasizes explicit field meanings, data types, and year-specific definitions to support data provenance and auditability.
  - Data sharing and provenance: The structure is designed to enable downstream sharing of underlying data while maintaining traceability to the origin (site, population, year, tree).
  - Consistency and standardization: Yearly blocks and stage definitions require consistent interpretation across years; careful maintenance of stage semantics is essential for cross-year comparability.
  - Barriers and gaps highlighted by the archetype’s monitoring challenges (data gaps, siloed data, metadata quality, data transformation needs) are relevant to implementing and maintaining this schema in a monitoring framework.

- Relevance for monitoring frameworks
  - Demonstrates a comprehensive, multi-layered data model for environmental health/phenology monitoring that combines spatial, temporal, phenotypic, and genotypic information.
  - Supports policy scrutiny and decision-making through:
    - Longitudinal tracking of growth and phenology under different trials and populations
    - Time-to-event metrics for stage progression as indicators of climate- or environment-driven responses
    - Linkages between phenotype and genotype for understanding genetic contributions to adaptation
  - Highlights the importance of standardized metadata, rigorous data governance, and transparent data sharing to overcome common monitoring barriers.