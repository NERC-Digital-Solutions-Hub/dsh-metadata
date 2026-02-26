# PhenotypeField.txt and GenotypeField.txt Data Dictionary

## Overview
- Documentation describing the fields used in phenotypic and genotypic data files, including site metadata, population/family structure, and multi-year measurements of tree growth and budburst.
- Includes geospatial fields (latitude, longitude), identifiers (site, pop code, family, ID), and detailed budburst phenotypes across years (2015–2020) with time-to-event metrics.
- Supplemented by genotype-related fields (SNP markers, SNP identifiers, and tree IDs).

## Core geospatial and site metadata
- Latitude and Longitude: Decimal coordinates for population sites.
- Site: Location identifier for each population.
- Population code (PopCode) and Population name: Key identifiers for grouping data by site/population.
- Decimal: Coordinate precision field accompanying latitude/longitude.
- NA or . entries indicate missing geographic or site information.

## Population, family, and sample identifiers
- Family: Family label; includes notes on family code (e.g., from the same mother tree).
- Family code: Codes describing familial relationships; many entries are NA or unspecified.
- Seedling: Seedling number within a family (numerical).
- ID: Unique tree identifier; used as a primary key for linking phenotypes and genotypes.
- Tree-related grouping: Blocks, Randomised, and other experimental design fields indicating how trees were arranged and sampled.

## Phenotype fields by year and measurement type
- Years covered: 2015, 2016, 2017, 2018, 2019, 2020 (with specific phenotype definitions per year).
- Budburst stages (descriptions and codes):
  - Stage 4: Scales open along length of shoot (no needles) or variations thereof.
  - Stage 5: Budburst with white tipped needles visible.
  - Stage 6: Budburst with green needles visible.
- Time-to-reach-stage phenotypes (days since first observation):
  - Examples include time to reach stage 4 (T4-15, T4-16, T4-17, etc.), time to reach stage 5 (T5-17, T5-18, etc.), time to reach stage 6 (T6-17, T6-18, etc.).
  - Each "Time taken to reach stage X" field counts days from first observation at each site for each tree.
- Per-year phenotype fields:
  - Height-related measurements (e.g., Height in cm) with associated years (I15, I16, I17, I18, I19, I20, etc.).
  - Length of shoot and related descriptors (e.g., along length of shoot, duration, etc.) with year-specific qualifiers.
- Observational and formatting notes:
  - Many fields use descriptive text, dates, or stage progress descriptions.
  - Some fields contain placeholders or missing values (e.g., ., NA), requiring data cleaning for GIS use.

## Time-series and stage progression details
- Temporal sequencing of budburst:
  - Documented first observation times and subsequent days-to-reach stages for multiple years and sites.
  - Stage progression metrics are defined per site and per tree, enabling spatial-time analyses of phenology.
- Stage-specific descriptors and data structure:
  - Stage 4: Scales open along shoot length; includes subfields about duration, days to reach, and related notes.
  - Stage 5 and Stage 6: Additional budburst definitions with corresponding time metrics.

## Genotype-related fields
- GenotypeField.txt:
  - SNP marker name (snpid) as a field descriptor.
  - Unique individual tree id linked to genotype records.
  - Other columns represent genotype data across markers (e.g., BE7_6_C_YA) with NA or missing values possible.
- Use for linking phenotypes to genotypes via the Unique tree id.

## Data structure and integration notes for GIS
- Primary join keys:
  - ID (Unique tree id), PopCode or Site, and year-specific phenotype fields.
- Spatial integration:
  - Use Latitude and Longitude as georeferencing anchors for mapping phenotypes across sites.
- Data cleaning considerations:
  - Many fields contain "." or NA where data are missing or not recorded; careful imputation or masking may be needed for map visuals.
  - Data are described as being stored in multiple places and may lack consistent standards; harmonization is recommended before GIS analyses.
- Resolution and scale:
  - Phenotype data are aggregated at sites with per-tree measurements; ensure appropriate spatial scale when creating maps (site-level vs. tree-level visuals).

## Practical GIS applications
- Map spatial distribution of budburst stages across sites and years.
- Visualize time-to-budburst (days) by location to identify regional phenology patterns.
- Link phenotypic data with SNP markers to explore genotype-phenotype associations on a geospatial basis.
- Create interactive map products showing growth metrics (e.g., height in cm) over time per site or per family.

## Key considerations and challenges
- Data appears scattered across many fields and years with inconsistent labeling (e.g., I, T, and stage codes).
- Missing data and placeholders common; plan for data cleaning and standardization.
- Ensuring alignment of year-specific fields (e.g., T4-17 vs T4-18) when merging across years.
- Data quality and skill requirements:
  - Requires careful integration of site, family, seedling, and tree-level data.
  - Adequate data standards and governance needed for scalable GIS use.