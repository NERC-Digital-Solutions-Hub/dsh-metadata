# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Purpose and scope
  - A suite of molecular analyses of epilithon (water) and soil samples collected from the Tamar catchment in winter 2013/2014.
  - Produces environmental chemistry data and biodiversity data (bacteria and eukaryotes) across sampled sites, enabling GIS-based exploration of spatial patterns.

- Data products and structure
  - Environmental data files
    - soil_env_data.csv
    - water_env_data.csv
  - Biodiversity sequence data files
    - soil_bacteria_seq.csv
    - soil_eukaryotes_seq.csv
    - water_bacteria_seq.csv
    - water_eukaryotes_seq.csv
  - Protocol and methodological context
    - Protocol CEH Tellus SW.docx

- Field sampling design and location data
  - Field sites
    - Epilithon (water): approx. 20 locations along a transect from the Wolf River to the Tamar River; exact sites determined in the field for accessibility and coverage.
    - Soil: range of soils across the Tamar region to capture different land uses; 20 locations with field-determined exact sites.
  - Location metadata
    - Epilithon (water)
      - Water_lab_ID: unique lab identifier cross-referenced with biodiversity data
      - Water_sample_ID: cross-referenced with WP4 water chemistry dataset
      - Stone_ID: A, B, or C per site (three stones sampled per location)
      - RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS
      - SAMPLING DATE
    - Soil
      - Soil_ID: unique lab identifier cross-referenced with biodiversity data
      - Sampling date
      - Grid reference: 1 km resolution British National Grid reference (anonimized at 1 km)
      - depth of core
      - Soil chemistry data columns (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K)

- Biodiversity data and cross-referencing
  - DNA processing
    - DNA extracted from all soil and epilithon samples using MOBIO PowerSoil kit
    - quality/purity checked before 454 pyrosequencing to assess bacterial and eukaryotic biodiversity
    - post-sequencing: sequences clustered into OTUs; results presented as OTU relative abundances per sample
  - Data alignment and cross-referencing structure
    - OTU rows: unique OTU IDs for each dataset
    - Columns: sample cross-referenced to the corresponding environmental data file via ID
    - Examples of cross-links
      - Epilithon bacteria: water_bacteria_seq.csv column 1 equals Water_lab_ID in water_env_data.csv
      - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 equals Water_lab_ID in water_env_data.csv
      - Soil bacteria: soil_bacteria_seq.csv column 1 equals Soil_ID in soil_env_data.csv
      - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 equals Soil_ID in soil_env_data.csv

- GIS-focused considerations and potential use
  - Spatially explicit sampling metadata (NGR/Eastings/Northings, 1 km grid references) supports map-based visualization of sampling sites and environmental variables.
  - Anonymization at 1 km for soil locations preserves site privacy while enabling spatial analyses.
  - Cross-linked environmental chemistry data with biodiversity OTU distributions facilitates spatial pattern analyses and integration with GIS workflows.

- Data provenance and contributors
  - Version: 1.0 (dated 24/03/14), description: created
  - Contributors by role
    - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
    - Data processing and mapping: Gearóid Webb
    - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
    - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General description: Suite of molecular analyses in epilithon and soil samples from the Tamar catchment

- Documentation and related materials
  - Protocol CEH Tellus SW.docx provides methodological context
  - WP4 documentation referenced for additional water chemistry data and metadata