# What, 1 = Abundances of bees, wasps, lepidoptera, beetles and flies; bee genera and morpho-species; and bee functional traits.. Where, 1 = In and around Sunyani and Techiman, Brong Ahafo, Ghana. When, 1 = Aug-Nov 2016. How, 1 = Five sets of three-coloured (fluorescent yellow, blue and white) pan-traps set up for 24h at vegetation level in 126 sites, half of them in each city, with 42 in rural areas and 84 in urban and peri-urban areas.. Why, 1 = Collected as part of a project on urban ecosystem services. Who, 1 = Collected and interpreted by Solène Guenat. Completeness, 1 = Precise sampling locations are absent due to ethical considerations.

## Overview

- Purpose: quantify abundances of bees, wasps, lepidoptera, beetles and flies; profile bee genera, morphospecies, and bee functional traits.
- Study area and period: Sunyani and Techiman, Brong Ahafo region, Ghana; Aug–Nov 2016.
- Design: 126 greenspaces spanning an urbanisation gradient; balanced representation of rural, urban, and peri-urban areas; three greenspace management types.

## Study design and sampling regime

- Greenspace sampling
  - 126 sites across an urban-to-rural gradient; 42 sites randomly selected per gradient category.
  - Three greenspace types identified per site: amenity (cultivated/managed), farmed, informal (minimally/no management).
  - Minimum greenspace size: 50 m2.
- Urbanisation context
  - Land-cover derived from Sentinel-2 imagery (Dec 2015) to compute proportion of built infrastructure within a 250 x 250 m grid.
- Site separation
  - Minimum 1 km between pre-identified sites to reduce spatial autocorrelation.

## Collection methods and taxa

- Pollinator sampling
  - Pan-traps: five traps per site, colors UV fluorescent yellow, blue, and white.
  - Setup: ground-level (0–0.5 m), 5 m spacing, active for 24 hours.
  - Storage: samples preserved in 70% ethanol and pinned for identification.
- Taxonomic approach
  - In-field: specimens identified to order; bees identified to genera and subgenera by microscopy.
  - Morphospecies: bees categorized into morphospecies due to limited species-level resources in Sub-Saharan Africa.
  - Functional traits: habitat preference, pollen specialization, nesting behavior, body size (inter-tegular distance), tongue length, sociality.
- Habitat and floral context
  - Surrounding habitat features (200 m radius) estimated visually for six elements: unmanaged ground, mown vegetation, shrub, tree layer, bare ground, concrete.
  - Floral resources: 1 m radius around traps assessed for flowering plant species richness, flower area, and flower head abundance.
  - Farmed sites also noted for crop type presence.
- Data collection windows
  - Temperature, cloud cover, wind, and rainfall recorded during trap setup and removal; weather and site conditions used to contextualize abundances.

## Data structure and files

- PollinatorAbundances.csv
  - 39 columns (e.g., SamplingDate, City, Management, PerCentGreen600m, Urbanisation, Altitude, CloudCover, Temperature, WindSpeed, Rainfall, habitat proxies, floral resources, various abundance and richness metrics).
  - Each row corresponds to a sampling location.
- BeeGeneraAbundances.csv
  - 37 columns; includes collection/environmental data plus abundances by bee genera.
  - Each row corresponds to a sampling location.
- BeeMorphospeciesAbundances.csv
  - 95 columns; includes collection/environmental data plus abundances by morphospecies ( Genus.Subgenus.MSpNumber naming).
  - Each row corresponds to a sampling location.
- BeeFunctionalTraits.csv
  - 24 columns; lists functional trait data for bees (Genera, IntertegularDistance, TongueLength, PollenSpecialisation, Sociality, NestLocation, Habitat) plus site descriptors.
  - Each row corresponds to a collected bee taxon or group.
- All four files: lines represent sampling locations; data linked by SamplingDate and site information.

## Variables, units, and data notes

- Temporal and spatial context
  - SamplingDate (DD/MM/YYYY); City (Sunyani or Techiman); Management (farmed, informal, amenity); Urbanisation (proportion built within 600 m or 600 m context); Altitude (m a.s.l.).
- Weather and site context
  - CloudCover (%), Temperature (°C), WindSpeed (Beaufort scale), Rain (mm).
- Habitat and floral context
  - GroundLayerVegetation, ShrubLayerVegetation, TreeLayerVegetation, Concrete, MownVegetation, BareGroundCover (% around site).
  - FlowerResources (flower area in cm2 within 1 m around trap) and FloweringPlantsSpeciesRichness (count).
- Pollinator data
  - Abundances and richness metrics for total bees, specific genera, morphospecies, Lepidoptera, Wasps, Beetles, and flies.
  - Bee functional traits: IntertegularDistance (mm), TongueLength (longue-tongued vs short-tongued), PollenSpecialisation (polylectic vs oligolectic), Sociality (social vs solitary), NestLocation (above- vs below-ground), Habitat (woodland, savannah, ubiquitous).
- Taxonomic scope and limitations
  - Species-level resolution limited for Sub-Saharan Africa; morphospecies used where species-level data were unavailable.
  - Some precise sampling locations withheld for ethical reasons.

## Data quality, completeness, and limitations

- Location precision: exact sampling coordinates not disclosed due to ethical considerations.
- Taxonomic resolution: morphospecies used for bees when species-level data are not available locally.
- Sampling method biases: pan-traps provide standardized sampling but may bias toward certain taxa and activity periods.
- Data integration: multiple datasets (abundances, genera, morphospecies, functional traits) require careful alignment by site and date for analyses.

## Potential analyses and applications for analysts

- Urbanization gradient effects
  - Examine how total pollinator abundances and taxon-specific abundances vary along urban–peri-urban–rural gradients.
- Diversity and community structure
  - Compare genus- and morphospecies-level diversity across management types and habitat features; assess functional trait distribution across landscapes.
- Trait-based insights
  - Link functional traits (tongue length, body size, nesting) to environmental variables (habitat structure, floral resources, urbanization).
- Cross-taxa comparisons
  - Integrate bee data with Lepidoptera, beetles, and flies to identify congruent or divergent patterns in response to urbanization and habitat features.
- Environmental covariates
  - Use weather (temperature, rainfall, cloud cover, wind) and habitat variables to model abundance and richness.
- Data synthesis and sharing
  - Leverage four CSVs to build multi-layer models; ensure reproducibility by referencing metadata and data structure.

## Metadata, provenance, and references

- Collected and interpreted by Solène Guenat.
- References for taxonomy and identification guides:
  - Goulet and Huber (1993) Hymenoptera of the World: an identification guide to families.
  - Eardley, Kuhlmann, Pauly (2010) The bee genera and subgenera of Sub-Saharan Africa.
  - Majka and Bondrup-Nielsen (2006) Parataxonomy: a test case using beetles.
- Data collected as part of a project on urban ecosystem services; dataset includes detailed habitat and floral resource context to support robust ecological analyses.