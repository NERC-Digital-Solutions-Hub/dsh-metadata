# Metadata for 'Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007'

## Overview
- Reports phenotypes for Scots pine mother trees and their cones/seed from 21 populations across Scotland.
- Seed was used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Sampling aimed to cover native range representation and seed zones; no trait-based seed-tree selection.

## Sampling design and scope
- Collected cones from ten trees per population (9 sampling points in a predetermined random direction from a central tree, within ~1 km diameter).
- For smaller woodland fragments or few cone-bearing trees, sampling directions maintained to ensure broad area coverage; distances between sampled trees not less than 50 m.
- Measured maternal traits to control for maternal effects in progeny analyses.

## Measurements and traits
- Mother trees: height and diameter at breast height (DBH) measured; ten cones collected per mother tree and assessed.
- Cone measurements (pre-drying): width and length; post-drying: cone weight.
- Seed measurements: total seed weight per cone; count and percentage of viable seeds (viable = has wing and obvious seed).
- Data aggregation: mean values computed for each mother tree across the 10 cones.

## Data files and structure
- ConeSeedTraits.txt
- MotherTraits.txt

## Key variables and descriptions
- PopulationCode, Family, Population, SeedZone: identifiers for populations and individual mothers.
- SeedZone values: EC, N, NC, NE, NW, SC, SW.
- Latitude, Longitude: population coordinates (decimal degrees).
- Aspect, Slope, Altitude: environmental descriptors of population site.
- Regeneration, SoilDepth, SoilMoisture, Competition, HA (height of mother tree), DA (diameter at breast height): phenotypic and site-related descriptors for mothers.
- ConeSeedTraits.txt variables:
  - Cone: number of cones sampled (1–10 per population).
  - Wi: cone width (mm).
  - Le: cone length (mm).
  - We: cone weight (g).
  - SN: total seeds per cone (count).
  - SV: percentage of viable seeds per cone (%).
  - SW: weight of viable seeds per cone (g).
- MotherTraits.txt variables:
  - Population, PopulationCode, Latitude, Longitude, and other maternal descriptors as above.

## Data provenance and context
- Collected in March 2007 at the James Hutton Institute, Aberdeen (latitude 57.133214, longitude -2.158764).
- Populations chosen to represent species’ native range and three populations per seed zone.
- Data intended to support long-term monitoring and evaluation of genetic and phenotypic variation in Scots pine across Scotland.