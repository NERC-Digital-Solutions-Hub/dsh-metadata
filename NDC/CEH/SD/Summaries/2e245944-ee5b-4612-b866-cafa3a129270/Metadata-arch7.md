# Pollinator Abundances in Sunyani and Techiman, Ghana (Aug–Nov 2016)

## Overview
- Dataset describing abundances of bees, wasps, Lepidoptera, beetles, and flies; includes bee genera, morphospecies, and functional traits.
- Study area: Sunyani and Techiman, Brong Ahafo, Ghana, capturing an urbanisation gradient (rural to urban/peri-urban).
- Collected and interpreted by Solène Guenat; part of a project on urban ecosystem services.
- Completeness: precise sampling locations are not provided due to ethical considerations.

## Study design and sampling
- 126 greenspaces across three management types (amenity, farmed, informal) distributed along an urbanisation gradient.
- Land-cover derived from Sentinel-2 imagery (Dec 2015); 250 × 250 m grid used to calculate percent built infrastructure within each grid cell.
- 42 areas randomly selected to represent rural, urban, and peri-urban landscapes; minimum 1 km between sites; rural areas within 10 km of the city and accessible by paved roads or dirt paths.
- Within each area, three greenspaces (minimum 50 m²) were identified:
  - Amenity greenspaces (managed for aesthetics)
  - Farmed sites (agricultural production)
  - Informal greenspaces (minimal/no management)
- Pan-trap sampling conducted August–November 2016:
  - Five traps per sampling event; ground-level placement (0–0.5 m); 24-hour exposure.
  - Trap colors: fluorescent yellow, blue, white; 2/3 full with water and a drop of detergent.
  - Samples preserved in 70% ethanol; field identification by order; bees and wasps identified to genus/morphospecies via microscopy.

## Taxonomy, traits, and data collection
- Bees identified to genus; morphospecies used due to limited species-level taxonomic resources in Sub-Saharan Africa.
- Functional diversity assessed using traits: habitat, pollen specialization, nesting behavior, body size (inter-tegular distance), tongue length, sociality.
- Habitat description around each site (200 m radius) estimates proportions of six features: unmanaged ground vegetation, regularly mown/grazed vegetation, shrub, tree layers, bare ground, concrete.
- Floral resources around the trap quantified: floral species richness, estimated floral area, and flower head abundance; crop types noted at farmed sites.

## Nature and units of recorded values
- Variables include: date, city, management type, urbanisation metric (percent built infrastructure within 600 m), altitude, cloud cover, temperature, wind speed, rainfall, habitat structure, floral resources, and abundances by taxa.
- Habitat and floral metrics supplied as percentages or counts (e.g., GroundLayerVegetation, FlowerResources, FloweringPlantsSpeciesRichness).
- Inter-tegular distance and tongue length recorded for bees; pollen specialization, sociality, nest location, and habitat type recorded for functional analyses.
- Data collection included environmental context: cloud cover, temperature, wind, rainfall.

## Data structure and files
- Four CSV files (each line represents a sampling location):
  - PollinatorAbundances.csv (39 columns): main environmental context and broad pollinator abundances.
  - BeeGeneraAbundances.csv (37 columns): abundances by bee genera plus environmental data.
  - BeeMorphospeciesAbundances.csv (95 columns): abundances by bee morphospecies (Genena.Subgen.MSpNumber nomenclature) with environmental data.
  - BeeFunctionalTraits.csv (24 columns): functional trait data per bee (Genera, IntertegularDistance, TongueLength, PollenSpecialisation, Sociality, NestLocation, Habitat, plus site descriptors).
- Additional notes:
  - Each file contains one line per sampling location.
  - Taxonomic references include Goulet & Huber (1993), Eardley et al. (2010), Majka & Bondrup-Nielsen (2006).

## Spatial context and GIS relevance
- Spatial framework linked to a 250 × 250 m grid derived from Sentinel-2 data; urbanisation within 600 m used as a key gradient metric.
- Data supports GIS analyses of:
  - Spatial patterns of pollinator communities across urban–rural gradients.
  - Relationships between pollinator abundances and habitat structure, floral resources, and land cover.
  - Functional trait distribution across space to map ecosystem service potential.
- Four CSVs enable integration into GIS workflows for map-based data products, with potential to join by sampling location identifiers and temporal data.

## Limitations and considerations for GIS use
- Precise geographic coordinates of sampling locations are not provided.
- Taxonomic resolution for many bees is morphospecies rather than species-level.
- Data collection constraints due to ethical considerations affect location precision.

## References (taxonomy and identification)
- Goulet, H., & Huber, J.T. (1993). Hymenoptera of the World.
- Eardley, C., Kuhlmann, M., & Pauly, A. (2010). The bee genera and subgenera of Sub-Saharan Africa.
- Majka, C.G., & Bondrup-Nielsen, S. (2006). Parataxonomy in beetles.