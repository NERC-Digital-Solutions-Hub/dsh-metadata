# A dataset of pollen production for 168 common flowering plants in the UK

## Overview
- Provides pollen production values for 168 UK plant species, calculated as pollen volume per flower from pollen grain number and grain size.
- Useful for identifying high pollen-producing species for pollinator conservation and can be combined with floral surveys to estimate pollen production at the community level.

## Data content and file format
- Single CSV file: AgriLand_Pollen_perspecies.csv
- File format: .CSV
- Data notes: Missing values are indicated by NA

## Data structure (variables)
- taxon_name: taxon name used for collection
- accepted_species_name: GBIF-standard accepted species name
- speciesKey, genusKey: GBIF keys
- genus, family: taxonomic grouping
- collection_year: year of stamen collection
- pollengrainnumber_perstamen_mean / _sd / _n: mean, standard deviation, and sample size for pollen grains per stamen
- pollenvolume_mean / _sd / _n: mean, standard deviation, and sample size for pollen grain volume
- totalpollenvolume_perstamen: total pollen volume per stamen (mean grains × mean grain volume)
- stamennumber_perflower: number of stamens per flower
- totalpollengrainnumber_perflower: total pollen grains per flower
- totalpollenvolume_perflower: total pollen volume per flower
- dicliny: dicliny status from BiolFlor database
- dicliny_factor: multiplier based on dicliny (1 for hermaphrodite; 0.5, 0.75 for other categories)
- totalpollenvolume_perflower_corrected: total pollen volume per flower corrected by dicliny factor
- Note: 20 columns in total; taxonomy standardized to GBIF Backbone Taxonomy

## Spatial coverage
- Field data from 25 sites in southern England (primarily around Bristol; examples include Abbots Leigh, Ashton Court, Leigh Woods, The Downs, etc.)
- Some taxa (Gladiolus sp., Lamium purpureum, Sinapis arvensis, Trifolium dubium) collected from greenhouse/pot-grown plants due to insufficient field populations
- Detailed site descriptions provided (abbreviations, habitat, British National Grid coordinates)

## Temporal coverage
- Fieldwork spans Feb–Oct 2011 and 2012 (164 species) and 2022 (10 species)
- Collected during the flowering period of the plant species

## Collection methods
- Pollen production estimated by collecting unopened flower buds, allowing them to open in water, and harvesting pollen from newly opened flowers
- For each species: mean number of anthers per flower, mean pollen grains per anther, and pollen grain volume estimated
- Calculations performed to derive total pollen volume per flower
- Laboratory tools: pipettes, vortex, ultrasonic bath, oven, centrifuge, microscope with ocular micrometer, and modified counting chamber

## Sampling regime and data quality
- Stamens collected from 174 taxa; pollen production quantified for 168
- Based on Baude et al. (2016) list of UK plant species with notable nectar resources, plus 50 additional locally important species
- 2 populations per species when possible; 105 taxa from at least 2 locations, 69 taxa from 1 location
- Each tube sample counted twice to provide replicates
- Taxonomy standardized with rgbif package to GBIF Backbone Taxonomy

## Data provenance and references
- Baude, M. et al. (2016). Historical nectar assessment reveals the fall and rise of floral resources in Britain. Nature.
- Baude, M. et al. (2025). A dataset of pollen production for 168 common flowering plants in the UK. Ecological Solutions and Evidence, under review.
- rgbif package (Chamberlain et al. 2024) used for taxonomy alignment

## Usage notes and integration considerations for data support
- Suitable for building self-serve data products (dashboards, pivot analyses) to compare pollen production across species, sites, and years
- Can be integrated with floral survey datasets to estimate community pollen potential
- Ensure careful handling of dicliny-corrected values when comparing per-flower outputs across species with different mating systems
- Taxonomic alignment with GBIF is recommended for consistency across systems
- Data quality considerations: presence of NA values; multiple replicates per tube; field vs greenhouse collection contexts

## Access and prerequisites
- One primary data file: AgriLand_Pollen_perspecies.csv
- Metadata includes variable definitions, units (e.g., pollen volume in µm³), and data provenance to support reproducibility and re-use