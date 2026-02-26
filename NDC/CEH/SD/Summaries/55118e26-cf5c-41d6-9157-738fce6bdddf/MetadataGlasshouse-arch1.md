# PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt Dataset Metadata

- This document describes two related data files from a glasshouse pine experiment: PhenotypeGlasshouse.txt (phenotypic data) and GenotypeGlasshouse.txt (genotypic data). It includes species information, origin, population metadata, spatial data, experimental design, and multi-year phenotypic measurements, along with SNP genotype identifiers.

## PhenotypeGlasshouse.txt: Key variables and definitions

- Species: Tree species in the study (MU = Pinus mugo; SY = Pinus sylvestris; UN = Pinus uncinata).
- Country: Country of origin for the population.
- Population: Population name; PopCode is the population code.
- PopCode: Population code; PopCodeWachowiak2018 is the population code used in Wachowiak et al. 2018 (doi: 10.1002/ece3.3690).
- Family: Family code (shared maternal lineage).
- Latitude / Longitude: Geographic coordinates of the population (decimal degrees).
- Block: Randomised block number (1 to 25) for experimental design.
- ID: Unique identifier for each individual tree.
- Genotyped: Indicates if the tree was genotyped using the multispecies Pinus SNP array (0 = no; 1 = yes).
- BS2010: Bud set date in 2010 (days since the reference date when the first plant in the trial formed a terminal bud with developed scales).
- BB2011: Budburst date in 2011 (days since reference date when the first plant burst buds on the main stem).
- BB2012: Budburst date in 2012 (days since reference date for the first plant to burst buds).
- H2011 / H2012 / H2013: Height of the tree in 2011, 2012, and 2013 respectively (in cm).
- I2012 / I2013: Height increment from 2011 to 2012 and from 2012 to 2013 (in cm).
- Units: 
  - BS2010 / BB2011 / BB2012: Days
  - H2011–H2013 / I2012 / I2013: Centimetres
- Notes: Additional fields include any missing data (marked NA); the “ID” field provides a stable linkage with Genotype data via Unique individual tree id.

## GenotypeGlasshouse.txt: Key variables and definitions

- snpid: Name of the SNP marker.
- All remaining columns: Genotype data columns for each individual (examples include UN18_26_16) plus a Unique individual tree id to link with Phenotype data.
- ID linkage: The Unique ID in the phenotype file can be used to align phenotypic measurements with genotype data.

## Experimental design and scope

- Design: Randomised block design with blocks numbered 1–25.
- Species and origin: Includes three pine species across multiple populations.
- Temporal scope: Phenotypes collected over multiple years (bud set in 2010; budburst in 2011 and 2012; height measurements across 2011–2013; height increments computed for 2012 and 2013).
- Population metadata: Population codes tied to Wachowiak et al. 2018 for cross-reference.

## Data usage considerations for analysts

- Data integration: Use ID/Unique ID fields to join Phenotype and Genotype data for association analyses.
- Potential analyses: 
  - Genome-wide associations between SNP markers and phenotypes (bud set, budburst, height, growth increments).
  - Growth trajectories over years (H2011–H2013) and their correlations with genotype or population origin.
  - Spatial analyses using Latitude/Longitude and population codes to explore geographic effects.
  - Block effects and experimental design considerations for mixed-model analyses.
- Data quality and gaps:
  - Some fields may be NA (missing); careful handling of missing data is required.
  - Genotyped flag helps select samples with genotype data; ensure proper alignment between files.
- References: Population code information includes details from Wachowiak et al. (2018), doi: 10.1002/ece3.3690.

## Practical notes for analysts

- Clean linking keys: Use the ID and Unique ID fields to reliably merge phenotype and genotype datasets.
- Standardisation: Harmonise units and ensure consistent interpretation of days (bud set/budburst) and heights (cm) across years.
- Documentation: Rely on the Wachowiak et al. 2018 reference for population coding and provenance when interpreting population-level results.