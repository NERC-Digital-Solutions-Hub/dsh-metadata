# PhenotypeGlasshouse.txt

## Overview
- A glasshouse phenotyping dataset for Pinus species, with accompanying genotype data in a separate file (GenotypeGlasshouse.txt).
- Fields cover taxon identity, origin, population structure, spatial context, experimental design, individual identifiers, genotyping status, and multi-year phenotypic measurements.

## Core fields and data types

- Taxon and origin
  - Species: coded (MU = Pinus mugo; SY = Pinus sylvestris; UN = Pinus uncinata)
  - Country: country of origin
  - Population: population name
  - PopCode: population code
  - PopCodeWachowiak2018: population code from Wachowiak et al. 2018 (doi: 10.1002/ece3.3690)

- Population and pedigree context
  - Family: family code (shared maternal lineage)
  - Latitude / Longitude: decimal coordinates of population
  - Block: randomized block number (1–25)
  - ID: unique individual tree identifier
  - Genotyped: flag indicating if tree was genotyped (0 = no; 1 = yes)

- Phenotypic measurements (by year/trait)
  - BS2010: Bud set in 2010 (days since observation of first plant to set terminal bud)
  - BB2011: Budburst in 2011 (days since first plant to burst bud)
  - BB2012: Budburst in 2012
  - H2011, H2012, H2013: Height in years 2011–2013 (cm)
  - I2012, I2013: Height increments for 2012 and 2013 (cm)

- Genotype data (file-wide context)
  - snpid: name of SNP marker
  - All remaining columns: genotype data (e.g., UN18_26_16) for each individual

## Data provenance and references
- Includes a cross-reference to Wachowiak et al. 2018 for population codes (PopCodeWachowiak2018).
- Clearly defined column-level metadata (description and unit) to support interpretation and reuse.

## Data quality and metadata standards
- Metadata clarity: explicit descriptions and units for each field (e.g., latitude/longitude as decimal degrees, phenotypic measures as days or centimeters).
- Consistency: standardized coding for species, population, and blocks; explicit NA handling indicated.
- Interoperability: parallel structure between PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt facilitates integrated analyses.

## Data governance and sharing considerations (Data Stewards)
- Accessibility and discoverability: upload to relevant portals/catalogues with strong metadata linking phenotypes and genotypes.
- Data integrity: ensure IDs (ID, snpid) are preserved and cross-referenced across phenotype and genotype files.
- Standardization: enforce consistent field names, codes, and units; map PopCodeWachowiak2018 to a canonical reference.
- Data provenance and updates: document any changes, and maintain versioning; monitor data updates and embargoes as applicable.
- Usage constraints: identify and respect any sharing limitations or proprietary aspects; record any data availability restrictions.
- Documentation: maintain file-level documentation and crosswalks to interpret codes (e.g., species codes, population codes, year-specific traits).

## Particular challenges (relevant to stewardship)
- Incomplete understanding of user needs and priorities for the dataset.
- Timely receipt of data from contributors.
- Ensuring data creators meet metadata and standardization requirements.
- Handling multiple systems and formats, including large and potentially non-interoperable datasets.
- Managing updates across phenotypic and genotypic data, and handling outdated or heterogeneous databases.

## Relationship to the broader data ecosystem
- Phenotype data in PhenotypeGlasshouse.txt is complemented by GenotypeGlasshouse.txt, enabling genotype-phenotype association studies.
- Population and provenance metadata (species codes, Wachowiak2018 reference) support reproducibility and cross-study comparability.

## Practical takeaways for Data Stewards
- Implement and enforce a consistent data dictionary across both PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt.
- Provide cross-reference tables for codes (Species, PopCode, PopCodeWachowiak2018) and ensure clear linkage to population and family structures.
- Maintain data quality checks for missing values, unit consistency, and valid ranges (e.g., years, height in cm, days).
- Facilitate data discoverability through stable identifiers (ID, snpid) and explicit versioned releases.
- Document data processing steps (e.g., any cleaning, transformations, or imputation) to accompany dataset updates.