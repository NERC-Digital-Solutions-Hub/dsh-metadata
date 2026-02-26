# PhenotypeGlasshouse.txt

## Overview
- Dataset describing phenotypic measurements for Pinus species grown in a glasshouse.
- Includes per-tree identifiers, population metadata, location coordinates, experimental design, and multi-year phenotypes.

## Data structure and contents
- Core fields:
  - Species, Country, Population, PopCode, PopCodeWachowiak2018, Family, Latitude, Longitude, Block, ID, Genotyped.
- Phenotypic measurements (years):
  - BB2010: Bud set in 2010 (days since observation).
  - BB2011: Budburst in 2011 (days since observation).
  - BB2012: Budburst in 2012 (days since observation).
  - H2011, H2012, H2013: Height in respective years (cm).
  - I2012, I2013: Height increments (cm) from prior year.
- Genotype linkage:
  - snpid in GenotypeGlasshouse.txt and a flag indicating whether the tree was genotyped (0/1).
- Unique identifier:
  - ID serves as unique tree id; PopCode and Population codes provide additional grouping.

## Spatial and temporal aspects
- Spatial: Latitude and Longitude given in decimal degrees to locate individuals; supports mapping by population or individual trees.
- Temporal: Phenotypes span multiple years (2010–2013) with derived metrics like height increments and bud development timing.

## Data quality and preparation considerations
- Some fields use NA to indicate missing data (e.g., Country, Population code, etc.).
- Data may be distributed across multiple sources (PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt) requiring careful integration.
- Units are explicit (degrees for coordinates; cm for height; days for phenology measures).
- Cross-references to literature (PopCodeWachowiak2018) for provenance and standardisation.

## GIS-specific use cases
- Map distribution of populations and individual trees; visualize spatial clustering of phenotypes.
- Analyze spatial correlations between growth (height) or phenology (bud set/budburst) and geographic variables.
- Combine with genotype data (snpid, Genotyped flag) to explore genotype-phenotype spatial patterns.
- Overlay with environmental layers (climate, soil) to identify spatial drivers of phenotypic variation.
- Use Block design information to adjust spatially for experimental layout in analyses.

## Key considerations for GIS workflows
- Ensure coordinate data are valid and in a consistent coordinate reference system.
- Handle missing values appropriately (e.g., imputation or exclusion in spatial analyses).
- Align PhenotypeGlasshouse.txt with GenotypeGlasshouse.txt via IDs when integrating datasets.
- Maintain clear provenance by recording source and related literature reference (e.g., Wachowiak2018).