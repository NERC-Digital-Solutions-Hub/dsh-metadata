# Metadata for 'Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007'

## Overview
- Dataset of phenotypes for Pinus sylvestris mother trees and their cones/seeds from 21 Scottish populations.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Data are organized to support comparisons across populations and offspring management, with a focus on maternal effects and seed traits.

## Sampling design and collection
- Cones collected from ten trees per population (21 populations) in March 2007.
- Sampling location strategy: around a central tree within a circle of ~1 km diameter.
- Nine sampling points chosen in predetermined random directions; sampling distance stratified in the ratio 1:3:5.
- For small fragments or limited trees with cones, directions preserved to maintain wide woodland coverage; inter-tree distances never less than 50 m.
- Collected cones were used to assess maternal traits prior to progeny measurements to control for maternal effects.

## Measurements and traits

### Mother trees (MotherTraits)
- Height (HA) and Diameter at Breast Height (DA) of the mother tree.
- Population-level attributes: Population, PopulationCode, SeedZone.
- Geolocation: Latitude and Longitude of the population.
- Additional site-level descriptors: Aspect, Slope, Altitude, Regeneration, SoilDepth, SoilMoisture, Competition, and various coded descriptors.
- Format notes: Unit fields often listed as NA; Decimal and categorical descriptors use defined encodings (e.g., Slope: flat, gentle, moderate, steep; SoilDepth: depth in cm; SoilMoisture: 1–5 scale).

### Cone and seed traits (ConeSeedTraits)
- Cone-level metrics per population: Cone (count of cones per population), Wi (cone width in mm), Le (cone length in mm), We (cone weight in g), SN (total seeds per cone).
- Seed viability and mass: SV (percentage of viable seeds in a cone), SW (weight of all viable seeds in a single cone, g).
- Data organization mirrors MotherTraits with PopulationCode and Population, plus Latitude/Longitude context.
- Units: typical numeric units as indicated (mm, g, count, %), with several fields designated as NA where not applicable.

## Data structure and files
- Two primary files:
  - MotherTraits.txt: maternal measurements and population metadata.
  - ConeSeedTraits.txt: cone/seed measurements and population metadata.
- Key shared fields: PopulationCode (population identifier), Population (full population name), Latitude/Longitude (decimal degrees), SeedZone, and a set of trait-specific columns as described above.
- Metadata conventions include explicit descriptions for each column, units where applicable, and definitions for categorical encodings (e.g., SeedZone codes, slope categories).

## Provenance and data quality
- Collection site: James Hutton Institute, Aberdeen (provided coordinates for context).
- Sampling date: March 2007.
- Protocols documented for sampling geometry, family assignment (each family corresponds to a mother tree), and measurement sequence to control for maternal effects.
- Data are organized to support quality assurance through per-mother-tree means across the 10 cones sampled, enabling standardized comparisons across populations.

## Accessibility and governance considerations
- The dataset is described with detailed metadata to support discoverability and reuse.
- Clear data structure (two files with consistent population identifiers) facilitates integration with other datasets and cataloguing in data portals.
- For data stewardship: ensure ongoing metadata completeness, versioning, and compatibility with data standards; track any updates or corrections to trait definitions, units, or population codes; monitor data availability and any potential access restrictions or embargoes.

## Typical uses and considerations for reuse
- Comparative analyses of maternal effects on progeny traits across 21 populations.
- Studies of cone and seed traits in a long-term multisite common garden context.
- Applications in forestry genetics, seed transfer, and provenance studies.
- When reusing, reference the two trait files together with the population and geography context, and be mindful of the sampling design and measurement protocols to interpret maternal and environmental effects accurately.