# Pollinator Abundances in Sunyani and Techiman, Brong Ahafo, Ghana (Aug–Nov 2016)

## Overview
- A dataset collected under an urban ecosystem services project to study pollinator communities across a gradient of urbanisation around Sunyani and Techiman, Ghana.
- Focuses on abundances of bees, wasps, lepidoptera, beetles and flies, plus bee genera, morphospecies, and functional traits.
- Sampling spanned 126 greenspaces across urban, peri-urban, and rural landscapes, with data captured on environmental context and floral resources.

## Sampling design and scope
- Sites: 126 greenspaces distributed along an urbanisation gradient, with 42 areas selected in urban/peri-urban zones and rural controls.
- Greenspace types: amenity land (managed for aesthetics), farmed sites (agricultural production), and informal greenspaces (minimally/unmanaged vegetation).
- Spatial framework: 250m x 250m grid used to quantify built infrastructure; rural sites within 10km of city, minimum 1km between sites.
- Temporal window: August–November 2016.

## Collection methods and taxonomic resolution
- Pollinator sampling: pan-traps (five per site) in three colors (fluorescent yellow, blue, white), exposed for 24 hours at ground level (0–0.5m).
- Handling: samples stored in 70% ethanol and pinned for identification.
- Taxonomic approach: field-identification to order; bees identified to genera and morphospecies where species-level data are limited; morphospecies grouped by defined features.
- Functional traits: traits include habitat, pollen specialization, nesting behavior, body size (inter-tegular distance), tongue length, and sociality.
- Habitat and floral context: visual estimates of six habitat features within 200m around each site; floral resources assessed within a 1m radius around the pan-trap (flowering species richness, flower head surface, and abundance).

## Measured variables and data structure
- Environmental and sampling variables (examples): date, city, management type, proportion of green/impervious surface within 600m, urbanisation (percent built infrastructure), altitude, cloud cover, temperature, wind speed, rainfall, habitat structure (ground layer, shrub layer, tree layer, concrete, mown vegetation, bare ground), floral resources, flowering plant richness.
- Pollinator metrics: total bee abundances, bee genera abundances, bee morphospecies abundances, and abundances by multiple taxa (Lepidoptera, Wasps, Beetles, etc.).
- Bee traits: intertegular distance (mm), tongue length (long vs short), pollen specialization (polylectic vs oligolectic), sociality (social vs solitary), nest location (above-ground vs below-ground), and general habitat associations.
- Data units: percentages (e.g., ProCentGreen600m), counts (abundances), richness (species or morphospecies), continuous measures (altitude, temperature, cloud cover, humidity proxies), and categorical fields (city, management, habitat type).
- File-by-file structure (described in detail):
  - PollinatorAbundances.csv: 39 columns; rows correspond to sampling locations.
  - BeeGeneraAbundances.csv: 37 columns; includes environmental data and abundances by genera.
  - BeeMorphospeciesAbundances.csv: 95 columns; includes environmental data and abundances by morphospecies.
  - BeeFunctionalTraits.csv: 24 columns; includes trait data for collected bees.
- Additional trait reference file: Noted as a 24-column dataset listing Genera and associated traits (e.g., IntertegularDistance, TongueLength, PollenSpecialisation, etc.).
- Each line in all files represents a sampling location.

## Data quality and ethics
- Precise sampling locations are omitted due to ethical considerations.
- Taxonomic resolution for Sub-Saharan bee species is limited; bees are categorized into morphospecies when species-level data are unavailable.
- Data capture spans multiple related files to enable cross-tabulation by environment, taxon, and trait, but users should account for potential inconsistencies across taxonomic levels.

## Access and usage suggestions for data products
- Potential analyses:
  - Relationship between urbanisation metrics and pollinator abundance/diversity (by order, genus, morphospecies, and functional traits).
  - Cross-taxa comparisons (bees vs. other pollinators) across habitat types and urban gradients.
  - Functional diversity and trait-based patterns (e.g., tongue length, pollen specialization) along the urban–rural gradient.
  - Habitat and floral resource influences on bee abundances and morphospecies richness.
- Data integration opportunities:
  - Join by SamplingDate, City, Management, and Urbanisation metrics to create time-slice and landscape-context dashboards.
  - Combine environmental variables with abundance and trait data to build self-serve explorations or dashboards for policy or planning use (e.g., urban ecosystem service assessments).
- Practical considerations:
  - Handle missing precise location data; use city-level or proximate site descriptors where needed.
  - Be mindful of taxonomy limitations; use morphospecies data where species-level data are unavailable.
  - Validate spatial joins using the provided urbanisation and habitat proxy fields (e.g., ProCentGreen600m, habitat structure estimates).
- Suggested data products:
  - Interactive explorer of pollinator groups across the urbanisation gradient.
  - Dashboards showing bee richness and functional trait distributions by city and greenspace type.
  - Reports or charts highlighting habitat features most strongly associated with pollinator abundances.

## References
- Goulet, H., Huber, J.T. (1993). Hymenoptera of the world: an identification guide to families.
- Eardley, C., Kuhlmann, M., Pauly, A. (2010). The bee genera and subgenera of sub-Saharan Africa.
- Majka, C.G., Bondrup-Nielsen, S. (2006). Parataxonomy: a test case using beetles. Anim. Biodivers. Conserv. 29, 149-156.