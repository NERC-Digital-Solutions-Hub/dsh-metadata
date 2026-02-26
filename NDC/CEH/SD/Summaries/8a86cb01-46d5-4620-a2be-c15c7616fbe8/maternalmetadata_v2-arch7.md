# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

## Overview
- Metadata for a dataset of Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 populations across Scotland.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Cone collection and phenotyping occurred in March 2007 at the James Hutton Institute, Aberdeen (coordinates provided).

## Sampling design and geographic coverage
- Populations cover the species’ native range in Scotland, including three populations from each of seven seed zones.
- For each population: sampling of ten seed trees around a central tree, within a circle ≈1 km in diameter.
- Sampling pattern: nine predetermined random directions from the central point, with distance stratification in the ratio 1:3:5 to avoid clustering near the center.
- For smaller woodland fragments, directions maintained to ensure broad coverage; tree spacing never closer than 50 m.

## Measurements and traits collected
- Mother trees: measurements of height and diameter at breast height (DBH).
- Cones: ten cones per mother tree measured in detail (width and length before drying; weight after drying).
- Seeds: seeds removed from each cone assessed for total weight and for count and percentage of viable seeds (viable = wing and obvious seed).
- Mean values across the 10 cones recorded for each mother tree.

## Dataset structure and files
- Two primary files:
  - MotherTraits.txt: contains population-level and mother-tree metadata, including:
    - Population code, population full name, seed zone
    - Spatial coordinates (latitude/longitude) of population
    - Environmental descriptors: Aspect, Slope, Altitude, Regeneration, SoilDepth, SoilMoisture, Competition
    - Maternal measurements: HA (height of mother tree), DA (diameter at breast height)
  - ConeSeedTraits.txt: contains cone- and seed-level traits, including:
    - Cone identifier (1–10 per mother tree)
    - Cone traits: Wi (width), Le (length), We (weight)
    - Seed traits: SN (number of viable seeds per cone), SV (viability percentage), SW (weight of viable seeds)
    - Population-related coordinates; note that in this file “Latitude” is repurposed to indicate cone data (Cone) per entry

## Spatial data and GIS relevance
- Geographic coordinates are provided in decimal degrees for population locations, enabling mapping of phenotypic variation across regions and seed zones.
- Environmental descriptors available to support spatial analyses of trait-environment associations.
- Structure supports per-population and per-cone analyses, useful for ecological genetics and spatial planning.

## Data quality, definitions, and notes
- Sampling date: March 2007; measurements follow defined protocols for cone and seed assessment.
- Viability defined as seeds with both a wing and an obvious seed.
- Units:
  - Height (HA) and diameter at breast height (DA) in meters
  - Cone/seed dimensions in millimeters; weights in grams; viability as counts or percentages
- Field names may have non-intuitive mappings (e.g., Latitude field in ConeSeedTraits.txt used to denote Cone), requiring careful data mapping for GIS work.
- No explicit coordinate reference system is stated beyond decimal degree coordinates; users should confirm CRS for mapping.

## Practical uses for GIS specialists
- Create maps of maternal traits and cone/seed phenotypes across Scotland.
- Integrate with environmental rasters (altitude, slope, soil moisture/depth) to analyze spatial patterns and potential adaptation signals.
- Compare seed-zone groupings and population-level trends; support planning for conservation, reforestation, or breeding programs.
- Link to the long-term multisite common garden context to study genotype-by-environment interactions across sites.