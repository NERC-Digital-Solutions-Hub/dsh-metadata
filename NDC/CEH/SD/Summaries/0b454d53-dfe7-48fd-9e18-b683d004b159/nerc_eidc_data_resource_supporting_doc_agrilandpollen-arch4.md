# A dataset of pollen production for 168 common flowering plants in the UK

- Purpose and utility
  - Provides pollen production values for 168 UK plant species to identify high pollen producers for pollinator conservation.
  - Can be combined with floral surveys to estimate pollen production of plant communities.

- File format and location
  - Single CSV file: AgriLand_Pollen_perspecies.csv

- Key data contents (data fields)
  - taxon_name, accepted_species_name, speciesKey, genusKey, genus, family, collection_year
  - pollengrainnumber_perstamen_mean, pollengrainnumber_perstamen_sd, pollengrainnumber_perstamen_n
  - pollenvolume_mean, pollenvolume_sd, pollenvolume_n
  - totalpollenvolume_perstamen, stamennumber_perflower, totalpollengrainnumber_perflower
  - totalpollenvolume_perflower, dicliny, dicliny_factor, totalpollenvolume_perflower_corrected
  - Note: missing values are indicated by NA

- Spatial coverage
  - Field data from 25 sites in southern England (centered around Bristol and nearby areas)
  - Four taxa collected from greenhouse plants due to insufficient field populations
  - Site list includes abbreviations and grid references (e.g., AL, AC, AV, etc.)

- Temporal coverage
  - Fieldwork conducted Feb–Oct in 2011/2012 (164 species) and in 2022 (10 species)

- Sampling design
  - Stamens collected from 174 taxa; pollen production quantified for 168
  - Based on Baude et al. 2016 list of 220 common UK species plus 50 locally important species
  - Two populations per species when possible; 105 taxa from ≥2 locations; 69 taxa from 1 location
  - 2–6 tubes per species (minimum one tube per location)

- Collection and laboratory methods
  - Buds collected in the field, allowed to open in water, pollen extracted from anthers
  - Calculations: mean number of anthers per flower × mean pollen grains per anther × pollen grain volume
  - Full methods described in Baude et al. 2025 (Ecological Solutions and Evidence, under review)

- Laboratory equipment and procedures
  - Pipettes (P1000, P200), vortex, ultrasonic bath, oven (60°C), centrifuge, microscope with ocular micrometer
  - Modified Fuchs-Rosenthal counting chamber and coverslips
  - Replicate pollen counts: two replicates per sample

- Taxonomy and data quality
  - Taxonomy standardized using rgbif (GBIF Backbone Taxonomy)
  - References include GBIF keys and linked literature (Baude et al. 2016; Baude et al. 2025; rgbif)

- Limitations and notes for data governance
  - Geographic emphasis on southern England; may limit regional generalizability
  - Some taxa from greenhouse sources; limited locations for certain species
  - Data structure supports interoperability via GBIF keys; metadata and licencing should be captured for reuse

- References
  - Baude, M. et al. (2016). Nature
  - Baude, M. et al. (2025). Ecological Solutions and Evidence (under review)
  - Chamberlain et al. (2024). rgbif package documentation

- Practical relevance for data leadership
  - Demonstrates end-to-end data workflow: from field collection to lab analysis to standardized taxonomy
  - Highlights governance needs: metadata clarity, data provenance, replicability, and interoperability with GBIF keys
  - Provides a concrete, policy-relevant dataset for pollinator resource assessment and habitat planning
  - Illustrates the importance of documenting methods and quality checks to enable reuse and integration with other biodiversity datasets