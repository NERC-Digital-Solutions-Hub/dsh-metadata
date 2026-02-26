# What, 1 = Abundances of bees, wasps, lepidoptera, beetles and flies; bee genera and morpho-species; and bee functional traits..

## Overview
- A pollinator biodiversity dataset collected in Sunyani and Techiman, Brong Ahafo, Ghana, during Aug–Nov 2016.
- Pan-trap sampling across 126 greenspaces along an urbanisation gradient (rural to urban/peri-urban).
- Data include abundances at multiple taxonomic levels (order, genus, morphospecies) and bee functional traits, plus extensive environmental and habitat metadata.
- Aimed to support understanding of urban ecosystem services and pollinator communities.

## Study design and sampling regime
- Sampling framework:
  - 126 greenspaces spanning three management practices: amenity land, farmed sites, and informal greenspaces.
  - 42 areas randomly selected along an urbanisation gradient with equal rural, urban, and peri-urban representation; minimum 1 km separation.
- Habitat context:
  - Land-cover quantified from Sentinel-2 imagery (Dec 2015) to derive the proportion of built infrastructure within 250x250 m grid cells.
  - Rural < 15% built infrastructure; gradient towards urban.
- Pan-trap setup:
  - Five pan-traps per site (colors: UV fluorescent yellow, blue, white) deployed on one occasion for 24 hours at ground level (0–0.5 m).
  - Traps placed within greenspaces; 2/3 filled with water + detergent; samples preserved in 70% alcohol.

## Data collected and recorded variables
- Taxonomic scope:
  - Abundances of bees, wasps, lepidoptera, beetles, and flies.
  - Bee data organized by genera, morphospecies, and functional traits.
- Bee functional traits:
  - Habitat, pollen specialization, nesting behavior, body size (intertegular distance), tongue length, sociality.
- Habitat and floral context:
  - Visual estimates of six habitat features within 200 m (ground cover, shrub, tree, concrete, mown vegetation, bare ground).
  - Floral resources around traps: flowering plant species richness, floral area, and flower head abundance.
  - Farmed sites noted for crop presence.
- Environmental and site-level metadata:
  - Sampling date, city, management type, percent greenspace within 600 m, urbanisation category, altitude, cloud cover, temperature, wind speed, rainfall.
  - Habitat structure and floral metrics (as above) and nest location (above/below ground) when applicable.
- Data completeness note:
  - Precise sampling locations avoided due to ethical considerations.

## Data structure and files
- Four CSV data files:
  - PollinatorAbundances.csv: 39 columns including sampling date, city, management, environmental covariates, abundances (overall and by groups), and various habitat and floral metrics.
  - BeeGeneraAbundances.csv: 37 columns with location-level environmental data and abundances by bee genera (plus total bee abundances).
  - BeeMorphospeciesAbundances.csv: 95 columns including environmental data and abundances by bee morphospecies (Genus.Subgenus.MSpNumber).
  - BeeFunctionalTraits.csv: 24 columns detailing functional trait data for collected bees (e.g.,Genera, IntertegularDistance, TongueLength, PollenSpecialisation, Sociality, NestLocation, Habitat, City, Management, etc.).
- Each row represents a sampling location.
- Supporting references for taxonomic identification and trait concepts are provided.

## Data quality, metadata, and governance considerations
- Taxonomic scope constrained by local resources; bees categorized into morphospecies where species-level identification is not available.
- Metadata completeness varies; some coordinates are withheld for ethical reasons, reflecting governance and privacy considerations.
- Data-sharing aspects:
  - Underlying datasets are designed to be shareable, but there are barriers noted around publicly sharing certain data.
  - Metadata collection is extensive, enabling verification and reuse, though some completeness challenges exist (e.g., full coordinate precision).
- Data provenance and references:
  - Taxonomic guidelines and identification references include Eardley et al. (2010), Goulet & Huber (1993), and Majka & Bondrup-Nielsen (2006).

## Relevance for Monitoring Frameworks
- Demonstrates an end-to-end monitoring workflow:
  - Well-defined spatial design across an urban–rural gradient.
  - Standardized sampling method (pan-traps) with replicated habitat contexts.
  - Multi-tier data (abundance by taxon, genera, morphospecies; plus functional traits) integrated with abiotic and habitat metadata.
  - Capability to compute functional diversity and community composition metrics.
- Highlights common governance aspects for monitoring programs:
  - Importance of data provenance, metadata quality, and data sharing while balancing ethical/privacy constraints.
  - Need to address data gaps and potential silos by documenting data collection processes and providing structured data files.
- Practical outputs:
  - Data suitable for dashboards, reports, and policy-oriented evaluations of urban ecosystem services and pollinator health.
  - Enables cross-site comparisons and longitudinal monitoring if repeated over time.

## References
- Eardley, C., Kuhlmann, M., Pauly, A., 2010. The bee genera and subgenera of sub-Saharan Africa.
- Goulet, H., Huber, J.T., 1993. Hymenoptera of the world: an identification guide to families.
- Majka, C.G., Bondrup-Nielsen, S., 2006. Parataxonomy: a test case using beetles. Anim. Biodivers. Conserv. 29, 149-156.