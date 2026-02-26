# AgriLand_Pollen_perspecies.csv

## Overview
- A dataset of pollen production values for 168 common plant species in the UK.
- Provides pollen volume per flower calculated from pollen grain number and grain size.
- Useful for identifying high pollen-producing species for pollinator conservation and to estimate pollen production of plant communities when combined with floral surveys.

## What is included
- One spreadsheet file: AgriLand_Pollen_perspecies.csv (CSV format).
- Packed with 20 variables describing taxonomic details, pollen production metrics, and dicliny-related adjustments.
- Variables include: taxon_name, accepted_species_name, speciesKey, genusKey, genus, family, Collection_year, pollengrainnumber_perstamen_mean/sd/n, pollenvolume_mean/sd/n, totalpollenvolume_perstamen, stamennumber_perflower, totalpollengrainnumber_perflower, totalpollenvolume_perflower, dicliny, dicliny_factor, totalpollenvolume_perflower_corrected, among others.
- Missing data indicated as NA.

## Variables and data structure
- taxon_name: name used for collection.
- accepted_species_name: GBIF accepted name; linked via GBIF keys (speciesKey, genusKey).
- taxonomic keys and classification: speciesKey, genusKey, genus, family.
- Collection_year: year of stamen collection.
- Pollen metrics per stamen: pollengrainnumber_perstamen_mean/sd/n; pollenvolume_mean/sd/n; totalpollenvolume_perstamen.
- Flower-level metrics: stamennumber_perflower; totalpollengrainnumber_perflower; totalpollenvolume_perflower.
- Dicliny-related: dicliny; dicliny_factor (hermaphrodite = 1; 0.5 for others; 0.75 for some categories); totalpollenvolume_perflower_corrected (adjusted by dicliny factor).
- Note: all data linked to the 168 species quantified; some values may be NA.

## Coverage

### Spatial
- Field data mostly from 25 sites in southern England (primarily around Bristol region).
- Some taxa collected from pot-grown plants due to lack of flowering field populations (Gladiolus sp., Lamium purpureum, Sinapis arvensis, Trifolium dubium).
- Site descriptions and grid references provided for field locations (abbreviations such as AL, AC, AV, etc.).

### Temporal
- Fieldwork conducted Feb–Oct in two periods:
  - 2011/2012: stamens collected for 164 species.
  - 2022: 10 species.
- Timing corresponds to flowering periods.

## Data collection and processing

### Collection methods
- Stamens collected from unopened flower buds in the field.
- Buds opened in laboratory water to harvest pollen-laden anthers.
- For each species: estimate mean number of anthers per flower, mean pollen grains per anther, and pollen grain volume.
- Compute total pollen volume per flower by aggregating these measurements.

### Sampling regime
- 174 taxa sampled; pollen production quantified for 168.
- Basis: Baude et al. (2016) list of 220 common UK flowering species plus 50 locally important species.
- Two populations per species when possible: 105 taxa from at least 2 locations (including 5 species from 3 locations); 69 taxa from 1 location.
- Each species’ stamens allocated to 2–6 tubes (minimum one tube per location).

### Laboratory instrumentation
- Pipettes (P1000, P200), vortex, ultrasonic bath, oven (60°C), centrifuge, microscope with ocular micrometer, modified Fuchs-Rosenthal counting chamber and coverslips.

## Quality control and standardization
- Counting experiments repeated twice per sample for two replicates per tube.
- Taxonomy standardized using rgbif package according to GBIF Backbone Taxonomy.
- Methods referenced in Baude et al. 2016 and Baude et al. 2025 (under review) and GBIF taxonomic practices (rgbif).

## Potential uses for environmental monitoring
- Assess and compare pollen production potential across common UK plant species.
- Estimate pollen resource availability for pollinators when integrated with floral surveys.
- Inform restoration, conservation planning, and habitat assessments by identifying high pollen producers.

## Data provenance and references
- Baude, M. et al. 2016; Historical nectar assessment (Nature).
- Baude, M. et al. 2025; A dataset of pollen production for 168 common flowering plants in the UK (Ecological Solutions and Evidence, under review).
- Chamberlain S. et al. 2024; rgbif: Interface to the GBIF API (R package).