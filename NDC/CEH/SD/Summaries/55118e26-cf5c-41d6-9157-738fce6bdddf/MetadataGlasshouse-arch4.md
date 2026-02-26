# PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt Data Dictionary

- The document describes two linked data files: PhenotypeGlasshouse.txt (phenotypic measurements) and GenotypeGlasshouse.txt (SNP genotype data) used for pine (Pinus spp.) glasshouse experiments.
- Each file is structured to enable linking by a unique individual/tree identifier and by SNP markers, supporting integrative analyses of phenotype and genotype across populations and years.

## Data structure and content

- PhenotypeGlasshouse.txt
  - Core fields include: Species, Country, Population, PopCode, PopCodeWachowiak2018, Family, Latitude, Longitude, Block, ID, Genotyped, BS2010, BB2011, BB2012, H2011, H2012, H2013, I2012, I2013.
  - Measurements cover bud set (BS2010), budburst (BB2011, BB2012), height (H2011–H2013), and height increments (I2012, I2013).
  - Units: Latitude/Longitude in decimal degrees; Height in cm; BS/BB/height-related fields are expressed as days or cm where indicated.
  - Data quality cues: several fields use NA when not applicable or missing; Genotyped indicates whether the tree was genotyped (0 = no, 1 = yes).

- GenotypeGlasshouse.txt
  - Core fields include: snpid (name of SNP marker) and additional genotype columns (remaining columns) for individuals (example identifiers such as UN18_26_16).
  - ID field referenced as a potential unique identifier for individuals; snpid names SNP markers used in genotyping.
  - The remaining columns store genotype data corresponding to each SNP marker.

## Key fields and their meanings

- Species (MU, Pinus mugo; SY, Pinus sylvestris; UN, Pinus uncinata)
- Country, Population, PopCode, PopCodeWachowiak2018 (cross-referenced population codes)
- Family (mother-tree group)
- Latitude, Longitude (population location in decimal degrees)
- Block (experimental randomised block, 1–25)
- ID (unique tree identifier)
- Genotyped (0/1 indicating SNP genotyping status)
- BS2010, BB2011, BB2012 (bud set/budburst timing in respective years)
- H2011, H2012, H2013 (height measurements for 2011–2013)
- I2012, I2013 (height increments for 2012 and 2013)
- snpid (SNP marker name)
- Genotype columns (individual genotype calls per SNP)

## Measurements and time points

- Phenotypic data are collected across multiple years:
  - 2010: bud set (BS2010)
  - 2011–2013: budburst (BB2011, BB2012) and height (H2011–H2013)
  - Height increments I2012 and I2013 capture growth changes between years
- Phenotype data are associated with population metadata (location, family, block) and may be used to study genotype-phenotype associations across diverse populations.

## Genotype data specifics

- SNP marker names are listed in snpid.
- Genotype data are stored in subsequent columns, with identifiers for individuals (e.g., UN18_26_16) indicating presence/absence or allele calls per SNP marker.
- Data enable association analyses linking SNP variation to phenotypic traits over time and across populations.

## Provenance and metadata

- Populations are described with both internal codes (PopCode) and cross-referenced codes (PopCodeWachowiak2018) tied to a published framework.
- Species are categorized using short codes (MU, SY, UN) with explicit scientific names.
- Geographic coordinates (Latitude/Longitude) and lineage information (Family) support reproducibility and spatial analyses.
- The dataset appears to be designed for integration with external sources (e.g., Wachowiak et al. 2018) to enrich population context.

## Data quality and standards considerations

- NA values indicate missing or inapplicable data, highlighting areas where data collection was incomplete or not relevant for certain records.
- Some fields have standardized units and ranges (e.g., Height in cm; Block 1–25), aiding consistent analyses.
- Absence of explicit data standards across all fields suggests a need for harmonized metadata governance and clear documentation of data generation protocols.
- The dataset emphasizes careful cross-linking between phenotype and genotype data via shared identifiers (ID and snpid), underscoring the importance of consistent naming and tracking.

## Implications for data strategy and governance

- Enables end-to-end data products that span collection, storage, and analysis of both phenotypic and genotypic information for forest tree studies.
- Supports co-ownership and cross-functional collaboration by providing a clear data model with population, individual, and marker-level details.
- Highlights opportunities to improve data discoverability and interoperability through standardized metadata, consistent identifiers, and explicit data provenance.
- Useful for designing pipelines that validate data content and format, manage missing values, and integrate across multiple years and data types (phenotype and genotype).

## How this supports the Data Leaders archetype

- Provides a concrete example of a data-rich system with interconnected phenotype and genotype datasets, including metadata for populations, locations, and lineages.
- Demonstrates the importance of cataloging data sources, codes, and measurement units to enable trustworthy analysis and dissemination.
- Illustrates common data governance challenges (missing data, non-standardized fields, and cross-file linkage) that Data Leaders can address through data standards, metadata schemas, and data quality controls.
- Shows the value of preserving data lineage and cross-referencing external frameworks to enhance data utility for policy-relevant and broader community analytics.