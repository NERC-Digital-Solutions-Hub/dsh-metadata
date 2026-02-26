# Metadata for 'Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007'

## Overview
- Describes a dataset of phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Sampling: cones from 10 trees per population were collected in March 2007; analysed at the James Hutton Institute, Aberdeen.
- Aimed to represent the species’ native range in Scotland, including three populations from each of seven seed zones.
- Measurements include mother-tree traits (to control for maternal effects) and cone/seed traits; mean values per mother tree are recorded across 10 cones.
- Data are organized into two files: ConeSeedTraits.txt and MotherTraits.txt.

## Sampling design and provenance
- Populations: 21 native Scottish populations representing the species’ native range; three populations per seed zone.
- Tree sampling: 10 seed trees per population, selected using a spatial protocol around a central tree within ~1 km diameter, covering nine points in predetermined random directions, with increasing distance ratios 1:3:5.
- For smaller woodland fragments, sampling maintained directions and covered a wide area; distances between trees never closer than 50 m.
- Seed garden: seeds used to establish a long-term multisite common garden trial at three nurseries/sites.
- Location reference: analysis conducted at the James Hutton Institute, Aberdeen (latitude 57.133214, longitude -2.158764).

## Data structure and key variables

- File: MotherTraits.txt
  - PopulationCode: population identifier
  - Family: ID of the mother tree (family code; individuals sharing a family code originate from the same mother tree)
  - Population: full population name
  - SeedZone: Scots pine seed zone (codes: EC, N, NC, NE, NW, SC, SW)
  - Latitude / Longitude: geographic position of the population
  - Aspect: compass direction of the slope
  - Slope: slope category (flat, gentle, moderate, steep)
  - Altitude: population altitude (meters; code M)
  - Regeneration: extent of regeneration around the mother tree (1: lots to 4: none)
  - SoilDepth: soil depth around the mother tree (cm)
  - SoilMoisture: soil moisture category (1–5)
  - Competition: mean distance to the nearest three trees (meters)
  - HA: height of the mother tree (m)
  - DA: diameter at breast height of the mother tree (m)
  - Notes: units and detailed descriptions as described in the dataset metadata

- File: ConeSeedTraits.txt
  - PopulationCode: population identifier
  - Family: ID of the mother tree (ties to MotherTraits)
  - Population: full population name
  - SeedZone: Scots pine seed zone
  - Cone: cone count or identifier (per unit)
  - Wi: cone width (mm)
  - Le: cone length (mm)
  - We: cone weight (g)
  - SN: total number of viable seeds in a cone (count)
  - SV: percentage of viable seeds in a cone (%)
  - SW: weight of all viable seeds in a single cone (g)

- General notes
  - For MotherTraits and ConeSeedTraits, PopulationCode and Family link mother trees to their cones/traits.
  - Decimal and categorical codes are used for several fields (e.g., SeedZone; Slope; Regeneration).

## Purpose and usage
- Supports analyses of maternal effects and progeny phenotypes across populations in a long-term, multisite context.
- Enables cross-site comparisons of cone and seed traits, and maternal tree characteristics.
- Structured for upload to data portals and catalogues; emphasizes clear metadata and consistent field definitions to facilitate discovery, reuse, and interoperability.

## Data governance and stewardship considerations
- Clear, standardized metadata with defined fields, units, and coding schemes aids discoverability and interoperability.
- Data are organized into two well-documented files with explicit links between mother trees and their cones/seeds via PopulationCode and Family.
- Potential stewardship activities:
  - Maintain consistent population and seed zone coding across updates.
  - Ensure units and category codes remain aligned with other datasets in the same portal.
  - Handle updating processes to preserve provenance (e.g., versioning of trait measurements or population codes).
  - Align with broader data governance practices for large, multisite phenotypic datasets.