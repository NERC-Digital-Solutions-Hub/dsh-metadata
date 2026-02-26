# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Purpose and scope
  - Suite of molecular analyses to assess biodiversity in epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
  - Data intended to support consistent environmental monitoring and potential policy performance evaluation over time.

- Datasets included
  - Soil environment data: soil_env_data.csv
  - Soil biodiversity sequences: soil_bacteria_seq.csv, soil_eukaryotes_seq.csv
  - Water environment data: water_env_data.csv
  - Water biodiversity sequences: water_bacteria_seq.csv, water_eukaryotes_seq.csv
  - Protocol documentation: Protocol CEH Tellus SW.docx

- Data structure and cross-referencing
  - Biodiversity data are sequence-derived OTU tables clustered from DNA extracted from samples.
  - Rows = OTU IDs; Columns = sample references.
  - Cross-references:
    - Epilithon bacteria/eukaryotes: column 1 links to Water_lab_ID in water_env_data.csv
    - Soil bacteria/eukaryotes: column 1 links to Soil_ID in soil_env_data.csv
  - Water dataset specifics:
    - Water_lab_ID: unique lab identifier (used to cross-reference with biodiversity data)
    - Water_sample_ID: corresponds to WP4 water chemistry sample names
    - Stone_ID: A/B/C designation for each sampling stone at a site
    - Metadata: SAMPLING DATE, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS
  - Soil dataset specifics:
    - Soil_ID: unique lab identifier (used to cross-reference with biodiversity data)
    - Sampling date: date cores were taken
    - Grid reference: 1 km resolution British National Grid Reference (anonymised to protect site locations)
    - Depth of core: depth range sampled
    - Soil chemistry columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K

- Field sampling methods
  - Epilithon (water): sampling sites chosen to provide broad spatial coverage from the Wolf River through to the Tamar River; exact site locations determined in the field; GPS coordinates recorded; three stones sampled per location; samples kept cold and transported to the lab.
  - Soils: sampling across Tamar region targeting a range of land uses; approximate site locations via maps; exact sites determined in the field; GPS used for positioning; samples kept cold and transported to the lab.

- Laboratory methods and QA
  - DNA extraction: MOBIO Powersoil 96-well DNA extraction kit used for all soil and epilithon samples.
  - Quality control: DNA purity and yield checked prior to sequencing.
  - Sequencing: 454 pyrosequencing performed to assess bacterial and eukaryotic biodiversity within each sample.
  - Data processing: sequences clustered into OTUs; results presented as the percentage of each OTU within each sample.
  - Data handling: clearly defined cross-referencing between OTU tables and environmental datasets to enable integrated analyses.

- Data management, provenance, and contributors
  - Version: 1.0 (dated 24/03/14); description: created.
  - Key contributors:
    - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
    - Data processing and mapping: Gearóid Webb
    - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
    - Planning and management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General description: a curated suite of molecular analyses from epilithon and soil samples in the Tamar catchment.

- Data storage, accessibility, and portals
  - Datasets are prepared for storage and uploading to appropriate data portals (consistent with monitoring data practices).

- Notable limitations and considerations
  - Full methodological details for soil chemical analyses are forthcoming.
  - Soil site coordinates are anonymised at 1 km resolution to protect sampling locations.

- How this supports environmental monitoring and policy evaluation
  - Provides standardized, cross-referenced environmental chemistry and biodiversity data for long-term monitoring.
  - Facilitates integrative analyses by linking chemical environment data with microbial and eukaryotic biodiversity across different habitat types (water epilithon and soil) and spatial scales.