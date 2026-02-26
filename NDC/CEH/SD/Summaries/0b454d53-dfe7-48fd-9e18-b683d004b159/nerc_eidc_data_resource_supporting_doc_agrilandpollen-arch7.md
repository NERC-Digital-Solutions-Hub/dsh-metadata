# A dataset of pollen production for 168 common flowering plants in the UK

## Overview
- Provides pollen production values for 168 common UK plant species, derived from pollen grain number and pollen grain size.
- Purpose: identify high pollen producing species for pollinator conservation; can be combined with floral surveys to estimate pollen production at the community level.
- Outputs a single CSV dataset suitable for GIS integration and map-based analyses of pollen resources.

## Data content
- File: AgriLand_Pollen_perspecies.csv
- Format: CSV with 20 columns (see Table 1 for variable descriptions)
- Key variables include:
  - taxon_name, accepted_species_name, speciesKey, genusKey, genus, family
  - collection_year
  - pollen-related metrics: pollengrainnumber_perstamen_mean/sd/n, pollenvolume_mean/sd/n, totalpollenvolume_perstamen
  - reproductive traits: stamennumber_perflower, totalpollengrainnumber_perflower, totalpollenvolume_perflower
  - dicliny, dicliny_factor, totalpollenvolume_perflower_corrected
- Data quality notes:
  - Missing values indicated as NA
  - Taxonomy standardized via rgbif (GBIF Backbone Taxonomy)

## Spatial coverage
- Field collection across 25 sites in southern England (grid references provided; many centered near Bristol).
- Four taxa collected from pot-grown plants due to insufficient field populations.
- Site details include abbreviations, habitat, and British National Grid references (see Table 2 in the dataset documentation).

## Temporal coverage
- Fieldwork conducted Feb–Oct in:
  - 2011/2012 for 164 species
  - 2022 for 10 species
- Sampling aligned with flowering periods of species.

## Collection methods
- Pollen production per flower estimated by:
  - Collecting unopened flower buds in the field
  - Opening buds in laboratory to harvest pollen from newly opened flowers
  - Extracting pollen grains from anthers
  - Estimating mean number of anthers per flower, mean pollen grains per anther, and pollen grain volume
  - Calculating total pollen volume per flower from these values
- Full methodological details available in the associated paper (Baude et al. 2025; under review).

## Sampling regime
- Stamens collected for 174 taxa; pollen production quantified for 168 taxa.
- Basis: species list from Baude et al. (2016) plus locally important taxa.
- 2 populations per species when possible:
  - 105 taxa from at least 2 locations (5 species from 3 locations)
  - 69 taxa from 1 location
- Stamens distributed across 2–6 tubes per species.

## Laboratory instrumentation and procedures
- Equipment used: P1000/P200 pipettes, vortex, ultrasonic bath, 60°C oven, centrifuge, microscope with ocular micrometer, modified Fuchs-Rosenthal counting chamber and coverslips.
- Quality control: pollen counting replicated (two replicates per sample) from each tube.

## Taxonomy and data quality
- Taxonomic names standardized with rgbif package (GBIF Backbone Taxonomy).
- References for methods and taxonomy supported by Baude et al. (2016, 2025) and rgbif (2024).

## Potential GIS applications
- Link pollen production metrics to species distribution data and floral surveys to map and quantify pollen resources across landscapes.
- Use GBIF-derived taxonomic keys (speciesKey, genusKey) for integration with other biodiversity layers.
- Spatially analyze pollen resource availability at the site level (25 southern England sites) to inform pollinator habitat assessments and conservation planning.

## Notes for users
- Data are CSV with 20 columns; refer to Table 1 in the dataset documentation for exact variable descriptions.
- Missing data are indicated as NA.
- Some taxa collected from greenhouse populations; consider this when interpreting field relevance in spatial analyses.