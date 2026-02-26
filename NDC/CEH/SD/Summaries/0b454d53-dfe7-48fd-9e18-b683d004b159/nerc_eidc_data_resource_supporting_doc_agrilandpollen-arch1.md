# AgriLand_Pollen_perspecies.csv

## Overview
- A dataset of pollen production values for 168 common UK plant species.
- Pollen volume per flower is calculated from pollen grain number and grain size.
- Useful for identifying high pollen-producing species for pollinator conservation and can be combined with floral surveys to estimate pollen production of plant communities.

## What the data contain
- Single CSV file: AgriLand_Pollen_perspecies.csv
- 20 columns detailing taxonomic information, collection context, and measured pollen metrics.
- Key variables include mean and standard deviation for pollen grains per stamen, pollen grain volume, total pollen volume per stamen, per flower, and corrected totals using dicliny factors.
- Missing data are marked as NA.

## Data structure (columns)
- taxon_name: Name of the taxon used for collection
- accepted_species_name: GBIF-accepted species name
- speciesKey: GBIF species key
- genusKey: GBIF genus key
- genus: Genus name
- family: Family name
- Collection_year: Year of stamen collection
- pollengrainnumber_perstamen_mean: Mean number of pollen grains per stamen
- pollengrainnumber_perstamen_sd: SD of pollen grains per stamen
- pollengrainnumber_perstamen_n: Sample size for pollen grains per stamen
- pollenvolume_mean: Mean volume of one pollen grain (µm3)
- pollenvolume_sd: SD of pollen grain volume (µm3)
- pollenvolume_n: Sample size for pollen grain volume
- totalpollenvolume_perstamen: Total pollen volume per stamen (mean grains per stamen × mean grain volume)
- stamennumber_perflower: Number of stamens per flower
- totalpollengrainnumber_perflower: Total pollen grains per flower
- totalpollenvolume_perflower: Total pollen volume per flower (µm3)
- dicliny: DICLINy data (from BiolFlor)
- dicliny_factor: DICLINy factor (e.g., 1 for hermaphrodites, 0.5 for dioecious/etc.)
- totalpollenvolume_perflower_corrected: Total pollen volume per flower adjusted by dicliny factor

## Spatial coverage
- Fieldwork largely at 25 sites in the south of England, including Bristol area; coordinates provided for context.
- Some taxa collected from greenhouse or pot-grown plants due to insufficient field populations.
- Habitats include grassland, heathland, moorland, woodland, wetlands, farmland, coastland, pavements, and allotments.

## Temporal coverage
- Field collection conducted February–October in 2011–2012 (stems for 164 species) and 2022 (10 species), timed to flowering.

## Collection methods
- Buds collected in the field, opened in water to harvest pollen-laden anthers.
- For each species: estimate mean number of anthers per flower, mean pollen grains per anther, and pollen grain volume; compute total pollen volume per flower.

## Sampling regime
- Stamens collected for 174 taxa; pollen production quantified for 168.
- Based on a list from Baude et al. (2016) plus 50 locally important species.
- 2 populations per species when possible: 105 taxa from ≥2 locations (including 5 species from 3 locations); 69 taxa from 1 location.
- Stamens from each species placed in 2–6 tubes (minimum one tube per location).

## Laboratory instrumentation and procedures
- Pipettes (P1000, P200), vortex, ultrasonic bath, oven (60°C), centrifuge (10 min 14 rcf), microscope with ocular micrometer, Modified Fuchs-Rosenthal counting chamber.

## Quality control and taxonomy
- Pollen counting replicated twice per tube (two replicates per sample).
- Taxonomy standardized with rgbif package (GBIF Backbone Taxonomy).

## Practical context and references
- Purpose: identify high pollen producers for pollinator resources and estimate pollen production of plant communities.
- Related references: Baude et al. (2016) on historical floral resources; Baude et al. (2025, under review) detailing the pollen production dataset; rgbif package (Chamberlain et al. 2024) for taxonomy standardization.