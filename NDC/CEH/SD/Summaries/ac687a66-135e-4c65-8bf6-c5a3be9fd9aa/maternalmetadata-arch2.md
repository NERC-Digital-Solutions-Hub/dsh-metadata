# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

## Overview
- Dataset of phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Aimed at enabling environmental monitoring and policy-relevant insights through standardized, comparable measures across populations and sites.

## Study design and sampling
- Cones collected in March 2007 from ten trees per population (21 populations).
- Populations selected to represent the species’ native Scottish range, including three populations from each of seven seed zones.
- Sampling strategy around a central tree:
  - Nine points in predetermined random directions.
  - Stratified by distance with ratio 1:3:5, covering approximately a 1 km diameter area.
  - For smaller woodlands or limited cone availability, directions maintained to ensure wide coverage; distances never closer than 50 m.

## Traits measured

### Maternal traits (to control for maternal effects)
- Height (HA) and diameter at breast height (DA) of the mother tree.
- For each mother tree: measurements on ten cones.

### Cone and seed traits
- Cone traits (per cone): width (Wi), length (Le), weight (We).
- Seed traits: total seeds per cone (SN), viable seeds per cone (SV; viability = seeds with a wing and obvious seed), percentage viability (SV as % of SN), weight of all viable seeds per cone (SW).

### Summary data
- For each mother tree, mean values across the ten cones are recorded.

## Data files and variables

### MotherTraits.txt
- Columns include:
  - PopulationCode (Population code)
  - Population (Full population name)
  - SeedZone (Seed zone: EC, N, NC, NE, NW, SC, SW)
  - Latitude (Decimal)
  - Longitude (Decimal)
  - Aspect (Direction of slope; N, S, E, W, Flat)
  - Slope (Degree of slope; flat, gentle, moderate, steep)
  - Altitude (m)
  - Regeneration (Extent of regeneration around the mother tree)
  - SoilDepth (Depth to solid rock via peat borer; cm; max 1.5 m)
  - SoilMoisture (Moisture around the mother tree; 1–5 scale)
  - Competition (Mean distance to nearest three trees)
  - HA (Height of mother tree; m)
  - DA (Diameter at breast height; m)

### ConeSeedTraits.txt
- Columns include:
  - PopulationCode (Population code)
  - Cone (Cone number within population)
  - Wi (Cone width; mm)
  - Le (Cone length; mm)
  - We (Cone weight; g)
  - SN (Total number of seeds per cone; Count)
  - SV (Percentage of viable seeds per cone; %)
  - SW (Weight of all viable seeds in a cone; g)

## Geographic and contextual details
- Analysis site: James Hutton Institute, Aberdeen (approximate site reference: 57.133214 N, -2.158764 E).
- Seed zones reflect Scotland’s regional variation; zones are East Central (EC), North (N), North Central (NC), North East (NE), North West (NW), South Central (SC), South West (SW).

## Data quality, access, and usage
- Data collection designed to be standardized, with verification and quality assurance steps to ensure consistency across sites and populations.
- Outputs are prepared in clear formats (tables) to support monitoring environmental health and policy performance over time.
- Datasets are stored and intended for upload to appropriate data portals; emphasis on making underlying data accessible to enable broader analyses and data integration.

## Potential applications for environmental monitoring
- Cross-site comparisons of cone and seed phenotypes in relation to environmental variables across Scotland.
- Long-term tracking of maternal and offspring traits in a common garden context to infer genetic vs. environmental contributions.
- Data integration with other environmental datasets to enhance monitoring and policy evaluation of forest health, adaptation, and management strategies.