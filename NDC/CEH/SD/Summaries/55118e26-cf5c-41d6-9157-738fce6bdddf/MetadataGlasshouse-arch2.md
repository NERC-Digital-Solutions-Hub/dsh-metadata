# PhenotypeGlasshouse.txt

## Overview
- Glasshouse-based dataset capturing phenotypic and genotypic information for pine species (MU = Pinus mugo; SY = Pinus sylvestris; UN = Pinus uncinata).
- Aimed at monitoring environmental responses and growth/phenology over time, with standardized fields for traceability and analysis.
- Data intended to be processed into clear outputs (reports, maps, charts) and stored in appropriate data portals.

## Data structure and contents
- Primary file: PhenotypeGlasshouse.txt (phenotype data); GenotypeGlasshouse.txt (genotype data) referenced alongside.
- Core identifiers and metadata:
  - Species, Country, Population, PopCode, PopCodeWachowiak2018 (population code from Wachowiak et al. 2018), Family.
  - Geographic and design context: Latitude, Longitude, Block (randomised block 1–25), ID (unique tree identifier).
  - Genotype flag: Genotyped (0 = no; 1 = yes); snpid (SNP marker name) in genotype file.
- Data organization: Rows represent individual trees; additional columns include unique IDs and a series of phenotype measurements.

## Phenotypic measurements (PhenotypeGlasshouse.txt)
- BS2010: Bud set in 2010 (days since date of first plant to set terminal bud in the trial).
- BB2011: Budburst in 2011 (days since date of first plant to burst bud).
- BB2012: Budburst in 2012 (days since date of first plant to burst bud).
- H2011, H2012, H2013: Height in cm for 2011, 2012, 2013 respectively.
- I2012, I2013: Height increments from 2011–2012 and 2012–2013 (cm).

## Genotype data (GenotypeGlasshouse.txt)
- Contains SNP-related columns:
  - snpid: Name of SNP marker.
  - Remaining columns: data per individual tree (e.g., UN18_26_16) and the unique IDs.
- Indicates which trees were genotyped using a multispecies Pinus SNP array (Genotyped flag in phenotype file).

## Population provenance and references
- PopCodeWachowiak2018 provides population coding aligned with Wachowiak et al. (2018, doi: 10.1002/ece3.3690).

## How this supports environmental monitoring
- Enables standardized, longitudinal assessment of growth and phenology across populations and genotypes.
- Facilitates integration with environmental data to evaluate environmental health and policy-relevant performance.
- The structured metadata (location, block, population, family) supports reproducible analyses and spatial/temporal comparisons.
- Outputs can be transformed into charts, maps, and reports, with datasets prepared for portal upload.