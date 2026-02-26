# Pollinator Abundances in Sunyani and Techiman, Brong Ahafo, Ghana (August–November 2016)

## Overview
- Dataset documenting abundances of bees, wasps, Lepidoptera, beetles, and flies; bee genera and morphospecies; and bee functional traits.
- Geographic focus: in and around Sunyani and Techiman, Ghana.
- Temporal focus: August–November 2016.
- Collected as part of a project on urban ecosystem services; collected and interpreted by Solène Guenat.
- Completeness note: precise sampling locations are not provided due to ethical considerations.

## Sampling design and collection
- 126 greenspaces sampled along an urbanisation gradient (proportion of built infrastructure).
- 42 areas randomly selected to represent rural, urban, and peri-urban landscapes; minimum distance of 1 km between sites.
- Greenspace types: amenity, farmed, and informal greenspaces (minimum 50 m² each).
- Pan-trap method: five pan-traps per site (colors: UV fluorescent yellow, blue, white); deployed for 24 hours at ground level (0–0.5 m); separated by 5 m; sampling August–November 2016.
- Sampling stored in 70% alcohol; insects identified to order in the field; bees/wasps identified to genus or subgenus; bees classified into morphospecies due to limited species-level taxonomy resources in Sub-Saharan Africa.
- Habitat and floral resource data collected around traps; crop types noted in farmed sites.

## Environmental and habitat data
- Land-cover data derived from Sentinel-2 images (December 2015) using Jenks natural breaks and hierarchical clustering; used to calculate proportion of built infrastructure within 250×250 m grids.
- Habitat descriptors recorded within 200 m around each site: proportions of ground layer and other vegetation types, bare ground, concrete, mown vegetation.
- Floral resources measured around traps: number of flowering plant species, estimated floral area, and flowering species richness.
- Additional environmental context: cloud cover, temperature, wind speed, rainfall during trap exposure; altitude; urbanisation gradient (percent built infrastructure within 600 m).

## Taxonomic and trait data
- Taxonomic resolution:
  - Bees and wasps: genus and, where possible, subgenus; bees further divided into morphospecies due to taxonomy constraints.
  - Lepidoptera, beetles, and flies identified to higher taxonomic levels as recorded.
- Bee functional traits recorded: habitat association, pollen specialization, nesting behavior, body size (inter-tegular distance), tongue length, sociality.
- Habitat and floral context captured to relate pollinator communities to environment and resources.
- Measurements:
  - Inter-tegular distance measured with calipers.
  - Tongue length categorized as long-tongued or short-tongued.
  - Pollen specialization categorized as polylectic or oligolectic.
  - Nest location categorized as above-ground or below-ground; habitat categories include woodland, savannah, and ubiquitous.

## Data files and structure
- Four CSV files:
  - PollinatorAbundances.csv (39 columns): site-level sampling data and abundances for various pollinator groups; includes urbanisation, altitude, climate and habitat descriptors; one line per sampling location.
  - BeeGeneraAbundances.csv (37 columns): collection/environmental data plus abundances by bee genera (one line per sampling location).
  - BeeMorphospeciesAbundances.csv (95 columns): collection/environmental data plus abundances by morphospecies (Genus.Subgenera.MSpNumber) (one line per sampling location).
  - BeeFunctionalTraits.csv (24 columns): trait data for each collected bee (one line per sampling location).
- Data structure notes:
  - Each line corresponds to a sampling location.
  - Taxa and abundances are organized to support analyses at multiple taxonomic and functional levels.

## Data quality, provenance, and references
- Data collection and interpretation credited to Solène Guenat.
- Taxonomic and morphological references:
  - Goulet & Huber, 1993 (bees identification guidance).
  - Eardley, Kuhlmann & Pauly, 2010 (bees genera and subgenera in Sub-Saharan Africa).
  - Majka & Bondrup-Nielsen, 2006 (parataxonomy and morphospecies concepts).
- Quality controls include field-based identification to the appropriate taxonomic level and structured trait measurement; morphospecies approach used due to limited species-level resources in the region.

## Usage, sharing, and governance considerations
- Data are organized for interoperability across portals and catalogues; intention to upload to relevant portals and catalogue holdings.
- Metadata includes explicit units for variables (e.g., percentages, millimeters, Celsius, Beaufort scale, dates).
- Ethical/compliance note: precise sampling locations withheld; users should respect the anonymization constraint and use city-level or grid-based location proxies if spatial analyses are required.
- Potential uses: comparative analyses of pollinator communities across urban–rural gradients, relationships between pollinator diversity and habitat/land-cover factors, and trait-based analyses of bee functional diversity.
- Data stewardship recommendations:
  - Maintain a detailed data dictionary and documentation for column definitions and units.
  - Preserve provenance by documenting collection methods, taxonomic decisions (including morphospecies assignments), and trait coding rules.
  - Provide clear licensing and access terms when publishing or redistributing data.
  - Plan for updates or versioning if further data collection occurs or if taxonomic frameworks change.