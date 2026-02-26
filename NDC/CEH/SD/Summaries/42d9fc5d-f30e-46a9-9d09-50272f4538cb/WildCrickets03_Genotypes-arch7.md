# WildCrickets03_Genotypes Description of content

## Overview
- Describes the microsatellite genotype profile for each adult cricket genotyped in the population.
- Includes 15 microsatellite markers per individual.

## Data structure and fields
- Year: The year when the cricket was alive.
- Tag: A two-character code used to identify the cricket in video recordings; value read from a plastic tag on the cricket’s pronotum.
- Sex: M (male) or F (female).
- Marker data: For each of the 15 microsatellite markers, two alleles are recorded with columns named [Marker]a and [Marker]b.
- Marker failure: If a marker fails, the corresponding allele score is zero.

## Data quality and handling
- Zero values indicate missing or failed genotype data for a given allele.
- Marker column naming follows a consistent pattern, with each marker having an ending of a (allele 1) and b (allele 2).

## GIS integration and potential workflows
- No spatial coordinates are included in this file.
- Can be used as an attribute table for individuals in GIS if linked to spatial data (e.g., locations or sampling sites) via Tag or Year.
- Potential workflow: export to a GIS-friendly table, join with location data, and map genetic variation or diversity across sites after linking by Tag/Year.

## Practical considerations for GIS specialists
- Prepare for data integration by ensuring consistent marker naming when merging with other genotype datasets.
- When incorporating into maps, create a point layer (one feature per cricket) and attach genotype attributes (allele scores for 15 markers, plus Year, Tag, Sex).
- Handle zeros as missing data during genetic analyses and any derived spatial statistics.