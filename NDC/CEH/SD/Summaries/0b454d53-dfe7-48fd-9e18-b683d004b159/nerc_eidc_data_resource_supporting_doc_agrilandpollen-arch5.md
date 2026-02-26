# A dataset of pollen production for 168 common flowering plants in the UK

## Overview
- A dataset of pollen production values for 168 British common flowering plant species.
- Calculates pollen volume per flower from mean pollen grain number per stamen and mean pollen grain volume; enables estimation of pollen production for plant communities and supports pollinator conservation work when combined with floral surveys.
- File: AgriLand_Pollen_perspecies.csv (CSV format; one spreadsheet).

## Data file and structure
- File name and format: AgriLand_Pollen_perspecies.csv, CSV with 20 columns.
- Columns include: taxon_name, accepted_species_name, speciesKey, genusKey, genus, family, Collection_year, pollengrainnumber_perstamen_mean, pollengrainnumber_perstamen_sd, pollengrainnumber_perstamen_n, pollenvolume_mean, pollenvolume_sd, pollenvolume_n, totalpollenvolume_perstamen, stamennumber_perflower, totalpollengrainnumber_perflower, totalpollenvolume_perflower, dicliny, dicliny_factor, totalpollenvolume_perflower_corrected.
- A note indicates missing data are marked as NA within the table.

## Variables and units (key items)
- taxon_name, accepted_species_name: taxonomic identifiers and accepted GBIF names.
- speciesKey, genusKey, genus, family: GBIF-backed taxonomic keys and classifications; links provided to GBIF keys usage.
- Collection_year: year of stamen collection.
- pollengrainnumber_perstamen_mean/sd/n: mean, standard deviation, and sample size of pollen grains per stamen.
- pollenvolume_mean/sd/n: mean, standard deviation, and sample size of pollen grain volume (µm^3).
- totalpollenvolume_perstamen: total pollen volume per stamen (µm^3), derived from mean grains per stamen × mean grain volume.
- stamennumber_perflower: number of stamens per flower.
- totalpollengrainnumber_perflower: total pollen grains per flower.
- totalpollenvolume_perflower: total pollen volume per flower (µm^3) = total pollen per flower; includes a corrected version:
- dicliny: dicliny trait information from BiolFlor (hermaphrodite, etc.).
- dicliny_factor: factor applied to correct total pollen volume per flower based on dicliny (1 for hermaphrodite; 0.5 for dioecious, gynodioecious, monoecious and gynomonoecious; 0.75 for some other forms).
- totalpollenvolume_perflower_corrected: pollen volume per flower adjusted by dicliny_factor (µm^3).

## Spatial and temporal coverage
- Spatial: field collection at 25 sites in southern England, with most sampling near Bristol; several taxa collected from pot-grown plants when field populations were insufficient.
- Temporal: fieldwork conducted Feb–Oct in 2011/2012 (164 species) and 2022 (10 species).

## Methods and data collection
- Collection method: stems from unopened flowers (buds) collected in the field; buds opened in lab to harvest pollen-laden anthers; pollen grains mechanically extracted.
- Calculations: mean number of anthers per flower, mean pollen grains per anther, and pollen grain volume measured; multiplied to estimate total pollen volume per flower.
- Sampling regime: stamens collected from 174 taxa; pollen production quantified for 168 taxa. Two populations per species when possible; 105 taxa from at least two locations, 69 taxa from one location.
- Laboratory instrumentation: standard lab tools (pipettes, vortex, ultrasonic bath, oven, centrifuge, microscope with micrometer, Fuchs-Rosenthal counting chamber).

## Quality control and data governance
- Replicates: pollen counting replicated twice per tube to provide two replicates per sample.
- Taxonomy standardization: species names aligned to GBIF Backbone Taxonomy via the rgbif R package.
- Data provenance: references include Baude et al. (2016) and the under-review 2025 dataset, with rgbif as the taxonomic standardization mechanism.

## Source and references
- Baude, M. et al. 2016. Historical nectar assessment reveals the fall and rise of floral resources in Britain. Nature.
- Baude, M. et al. 2025. A dataset of pollen production for 168 common flowering plants in the UK. Ecological Solutions and Evidence (under review).
- rgbif: Interface to GBIF API (Chamberlain et al., 2024).

## Considerations for use and governance
- Reusability: well-documented with explicit variable definitions, units, and taxonomic standardization, enabling integration with GBIF-based workflows and other biodiversity datasets.
- Update and maintenance: dataset includes clear provenance and standardization approach; any updates should maintain consistency with GBIF taxonomy references.
- Limitations and caveats:
  - Missing data indicated by NA in the CSV.
  - Geographic coverage skewed toward southern England with Bristol-centric sites; some taxa sourced from greenhouse conditions due to lack of field populations.
  - Temporal gaps (data concentrated in 2011/2012 with a smaller 2022 portion).
- Potential applications: informing pollinator conservation strategies, estimating pollen availability in plant communities, and supporting meta-analyses combining floral resource data with pollinator surveys.