# A dataset of pollen production for 168 common flowering plants in the UK

## Overview
- Provides pollen production values for 168 UK plant species, enabling identification of high pollen producers for pollinator conservation.
- Pollen metrics can be combined with floral surveys to estimate pollen production at the plant-community level.
- Intended for use in monitoring environmental health and informing policy decisions related to pollinator resources.

## Content and structure
- File: AgriLand_Pollen_perspecies.csv (one CSV dataset)
- Taxa and taxonomy fields to standardise naming and cross-reference GBIF
  - taxon_name, accepted_species_name, speciesKey, genusKey, genus, family
- Temporal and collection fields
  - collection_year
- Pollen production measures (per stamen, per flower, per species)
  - pollengrainnumber_perstamen_mean, pollengrainnumber_perstamen_sd, pollengrainnumber_perstamen_n
  - pollenvolume_mean, pollenvolume_sd, pollenvolume_n
  - totalpollenvolume_perstamen
  - stamennumber_perflower
  - totalpollengrainnumber_perflower
  - totalpollenvolume_perflower
  - totalpollenvolume_perflower_corrected (dicliny-adjusted)
- Reproductive biology metadata
  - dicliny, dicliny_factor
- Data quality notes
  - missing data indicated as NA

## Spatial and temporal coverage
- Spatial: 25 field sites located primarily in the south of England (locations include Bristol area and surrounding sites; site abbreviations and grid references provided)
- Temporal: fieldwork conducted Feb–Oct in 2011/2012 (164 species) and 2022 (10 species)
- Sampling scope:
  - Stamens collected for 174 taxa; pollen production quantified for 168 taxa
  - 2 populations per species when possible; some species from 1 location
  - Four taxa from pot-grown plants due to lack of flowering field populations

## Methods and data collection
- Field collection: stems of unopened flowers (bud stage) collected; flowers opened in water to harvest pollen from newly opened flowers
- Estimation process: mean number of anthers per flower, mean pollen grains per anther, pollen grain volume
- Calculation: total pollen volume per flower = (mean grains per stamen) × (mean grain volume); extended to per-stamen and per-flower totals
- Laboratory techniques: standard lab equipment (pipettes, vortex, ultrasonic bath, oven, centrifuge, microscope, counting chamber)
- Quality control: two replicates per sample; taxonomic standardisation via rgbif using GBIF Backbone Taxonomy

## Taxonomy and data quality
- Taxonomy standardised with rgbif (Chamberlain et al., 2024) aligned to GBIF
- Data quality indicators included: replicate measurements, explicit NA for missing values
- Noted limitations:
  - Some data gaps (NA)
  - Field sampling limited to certain locations and years
  - Four taxa collected from greenhouse/pot-grown material due to field limitations

## Relevance for monitoring frameworks and policy
- Enables quantification of pollen production potential across common UK species, informing assessments of floral resource availability for pollinators
- Supports monitoring of changes in pollen resource supply over space and time by integrating with floral surveys
- Provides standardized, transparent data suitable for dashboards, reports, and governance processes
- GBIF-aligned taxonomy and open data practices facilitate data sharing and cross-agency collaboration, though the dataset notes potential barriers related to data accessibility and metadata completeness in broader contexts

## References
- Baude, M., Kunin, W. E., Boatman, N. D., Conyers, S., Davies, N., Gillespie, M. A., Morton, R. D., Smart, S., & Memmott, J. (2016). Historical nectar assessment reveals the fall and rise of floral resources in Britain. Nature, 530(7588), 85-88.
- Baude, M., Kunin, W., Davies, N., Wright, E., Memmott, J. (2025). A dataset of pollen production for 168 common flowering plants in the UK. Ecological Solutions and Evidence, under review.
- Chamberlain S, Barve V, Mcglinn D, Oldoni D, Desmet P, Geffert L, Ram K (2024). rgbif: Interface to the Global Biodiversity Information Facility API. R package version 3.8.1.