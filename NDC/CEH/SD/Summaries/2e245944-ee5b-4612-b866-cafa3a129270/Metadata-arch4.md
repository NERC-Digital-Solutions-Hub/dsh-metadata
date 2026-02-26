# Pollinator Abundances, Bee Genera/Morphospecies Abundances, and Functional Traits Dataset from Greenspaces in Sunyani and Techiman, Brong Ahafo, Ghana (2016)

## Overview
- A dataset collected from August–November 2016 in Sunyani and Techiman, Ghana, as part of a project on urban ecosystem services.
- Focuses on pollinator communities, including abundances of bees, wasps, lepidoptera, beetles, and flies; plus bee genera and morphospecies, and bee functional traits.
- Sampling deployed across 126 greenspaces along an urbanisation gradient (42 rural, 84 urban/peri-urban) to represent three greenspace management types.
- Ethical note: precise sampling locations are withheld.

## Study design and sampling regime
- 126 greenspaces chosen to span three management practices and varying urbanisation (proportion of built infrastructure) within a 250x250 m grid.
- Rural areas within 10 km of the city; urban/peri-urban areas representing the urbanisation gradient; minimum 1 km between sampling sites.
- At each site, three greenspace types were targeted: amenity land, farmed sites, and informal greenspaces.

## Data collection methods
- Pollinators collected with pan-traps (five traps per site) containing UV fluorescent yellow, blue, and white bowls, deployed for 24 hours.
- Traps set at vegetation height (0–0.5 m) and spaced 5 m apart; samples stored in 70% ethanol.
- Insects identified to order in the field; bees and wasps identified to genus level or morphospecies, with morphospecies used due to limited species-level taxonomy resources in Sub-Saharan Africa.
- Bee functional diversity assessed using traits: habitat, pollen specialisation, nesting behaviour, body size (inter-tegula distance), tongue length, and sociality.
- Habitat and floral resource context recorded around each trap: 200 m radius for habitat features; 1 m radius for floral resources ( richness, area of flowers, and abundance); crop presence noted in farmed sites.

## Data structure and files
- Four CSV files, each with one line per sampling location:
  - PollinatorAbundances.csv (39 columns): includes sampling date, city, management, urbanisation, climate, habitat structure, floral resources, and broad abundances (BeeAbundances, LepidopteraAbundances, etc.).
  - BeeGeneraAbundances.csv (37 columns): collection/environmental data plus abundances by bee genera.
  - BeeMorphospeciesAbundances.csv (95 columns): collection data plus abundances by bee morphospecies (Genera.Subgenera.MSpNumber nomenclature).
  - BeeFunctionalTraits.csv (24 columns): trait data per bee (Genera, IntertegularDistance, TongueLength, PollenSpecialisation, Sociality, NestLocation, Habitat) plus location and habitat variables.
- Each row represents a single sampling location.

## Variables and measurements
- Recorded variables include: date, city (Sunyani/Techiman), management type (farmed, informal, amenity), proportion of built infrastructure at 600 m, altitude, cloud cover, temperature, wind speed, rainfall, various habitat structure components (ground/shrub/tree vegetation, concrete, mown vegetation, bare ground), floral resources and flowering plant richness, and bee/group abundances.
- Bee traits include body size (inter-tegula distance), tongue length, pollen specialisation, sociality, nest location, and general habitat.

## Spatial and temporal coverage
- Location: Sunyani and Techiman, Brong Ahafo, Ghana.
- Timeframe: Sampling conducted August–November 2016.
- Spatial design: 126 greenspaces selected along an urbanisation gradient with stratified representation of rural, urban, and peri-urban landscapes; minimum 1 km separation between sites; rural sites within 10 km of the city center.

## Data quality, completeness, and provenance
- Precise sampling locations are not disclosed due to ethical considerations.
- Taxonomic resolution includes orders, genera, and morphospecies for bees; full species-level resolution not always available in Sub-Saharan Africa.
- Taxonomic references: Eardley et al. 2010; Goulet & Huber 1993; Majka & Bondrup-Nielsen 2006.

## Potential uses for Data Leaders
- Informing urban biodiversity and ecosystem service assessments across cities and networks.
- Assessing data gaps and coordinating cross-site data collection for a broader data system.
- Supporting evidence-based habitat management and policy decisions in urbanising landscapes.
- Enabling cross-referencing with land-cover data (Sentinel-2) to link built infrastructure with pollinator communities.
- Providing a structured, multi-file dataset for governance, data discoverability, and reuse within a wider data community.

## Limitations and considerations for reuse
- Location privacy limits exact site coordinates; users must work with aggregated or masked location data.
- High-dimensional, taxonomically dense data requiring careful metadata alignment and documentation.
- Species-level resolution is limited for bee taxa in Sub-Saharan Africa; morphospecies approach used where necessary.
- Data come from a single year and two nearby cities; caution in extrapolating to other regions or time periods.