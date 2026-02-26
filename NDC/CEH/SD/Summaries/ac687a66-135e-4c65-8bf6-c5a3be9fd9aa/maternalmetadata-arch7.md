# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

## Overview
- Reports phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.

## Sampling design and scope
- Cones collected from ten trees per population (210 trees total) in March 2007.
- Central sampling around a central tree: a circle of ~1 km diameter with ten seed trees via a stratified scheme (nine points in predetermined random directions; distance strata in a 1:3:5 ratio).
- For smaller woodland fragments or few cone-bearing trees, sampling directions retained to ensure broad coverage; inter-tree distances never closer than 50 m.
- Populations chosen to represent Scotland’s native range, including three populations from each of seven Scots pine seed zones.

## Traits and measurements (mother trees)
- For each mother tree: measurements of height (HA) and diameter at breast height (DA).
- Ten cones collected per mother tree and measured in detail (cone width and length prior to drying; cone weight after drying).
- Seed within each cone assessed for total weight and for seed viability (viable seeds have a wing and an obvious seed).
- Mean values calculated for each mother tree across the ten cones to control for maternal effects.

## Data files and structure
- Two metadata files: MotherTraits.txt and ConeSeedTraits.txt.
- Population and geographic fields:
  - PopulationCode; Population (full name); SeedZone (EC, N, NC, NE, NW, SC, SW).
  - Latitude and Longitude for population; decimal coordinates.
  - Aspect; Slope; Altitude (Altitude in meters); Regeneration; SoilDepth; SoilMoisture; Competition; HA (Height of mother tree, meters); DA (Diameter at breast height, meters).
- Cone/seed traits (ConeSeedTraits.txt):
  - Cone index; Wi (Width of cone); Le (Length of cone); We (Weight of cone).
  - SN (Total seeds per cone); SV (Percentage of viable seeds per cone); SW (Weight of all viable seeds in a single cone).
- Family and population relationships:
  - Family: ID corresponding to mother tree (individuals with the same family code share a mother tree).
  - Population: full population name; Lat/Long and related descriptors at population level.

## Geospatial context and GIS relevance
- Provides spatially explicit data across Scotland (population coordinates and zone classification) suitable for map-based analyses and visualization.
- Enables exploration of spatial patterns in mother-tree traits and cone/seed phenotypes, and their relation to environmental descriptors (altitude, slope, soil moisture, etc.) across seed zones.

## Data quality and considerations
- Data collected in 2007; ensure awareness of temporal context when integrating with newer datasets.
- Units indicated (e.g., HA and DA in meters) and categorical SeedZone codes; consistent interpretation required for analyses.
- Data files describe variables and their meanings, including the method for viability assessment.

## Potential applications for GIS specialists
- Create map layers of population locations, seed zones, and trait distributions.
- Analyze spatial variation in maternal traits and cone/seed phenotypes across Scotland.
- Integrate environmental layers (altitude, slope, soil moisture) to model trait-environment relationships.
- Support planning of long-term common garden trial analyses and visualization of sampling coverage.