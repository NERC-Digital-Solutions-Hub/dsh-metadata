# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

## Overview
- Reports phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
- Seed from these trees used to establish a long-term multisite common garden trial at three nurseries/field sites.

## Sampling design
- Ten seed trees sampled from each population.
- Sampling covered a circle of approximately 1 km in diameter around a central tree.
- For each population: nine sampling points in predetermined random directions; distance stratified in a 1:3:5 ratio from the central point.
- Distances between sampled trees never closer than 50 m.
- Where populations were in smaller woodland fragments or had few cone-bearing trees, directions were maintained to ensure broad coverage.

## Measurements and traits (mother trees)
- For each mother tree:
  - Height and diameter at breast height (DBH) measured.
  - Ten cones collected and assessed.
  - Cone width and length measured before drying; cone weight measured after drying.
  - Seeds removed from each cone assessed for total weight and for viability (viable seeds: have a wing and an obvious seed).
- Mean values across the 10 cones were recorded for each mother tree.

## Dataset files and structure
- Two primary data files:
  - MotherTraits.txt
  - ConeSeedTraits.txt
- Both files use PopulationCode as a key identifier.
- PopulationCode, Population, and SeedZone fields provide population-level metadata.

## Population and site metadata (MotherTraits)
- PopulationCode: identifier for the population.
- Population: full population name.
- SeedZone: geographic seed zone (EC, N, NC, NE, NW, SC, SW).
- Geographic coordinates: Latitude and Longitude of each population (decimal degrees).
- Environmental and site descriptors:
  - Aspect, Slope, Altitude.
  - Regeneration (extent around the mother tree).
  - SoilDepth (depth to solid rock, up to 1.5 m, in cm).
  - SoilMoisture (moisture in surrounding soil at cone collection).
  - Competition (mean distance to the nearest three trees; in meters).
  - HA (Height of mother tree; meters).
  - DA (Diameter at breast height of mother tree; meters).

## ConeSeedTraits (traits by cone/population)
- PopulationCode: identifier linking to population.
- Cone: identifier for the cone within the population (1–10 per cone data point).
- Wi: Cone width (mm).
- Le: Cone length (mm).
- We: Cone weight (g).
- SN: Total number of viable seeds in a cone (count).
- SV: Percentage of seeds in the cone that are viable (%).
- SW: Weight of all viable seeds in a single cone (g).

## Data usage and potential applications (Data Support perspective)
- Enables exploration of maternal effects and how mother-tree traits relate to progeny seed/cone phenotypes across environments.
- Supports comparison of phenotypes across multiple Scottish populations and seed zones.
- Facilitates creation of dashboards or self-serve analyses for policy, forestry management, or research on local adaptation.
- Requires data cleaning and harmonization across two files (MotherTraits and ConeSeedTraits) to enable integrated analyses.

## Provisional notes
- Seed collection location noted as the James Hutton Institute, Aberdeen (approximate coordinates 57.133214, -2.158764) for subsequent analysis.
- Seed selection criteria excluded trait-based selection; sampling focused on broad geographic and spatial coverage.