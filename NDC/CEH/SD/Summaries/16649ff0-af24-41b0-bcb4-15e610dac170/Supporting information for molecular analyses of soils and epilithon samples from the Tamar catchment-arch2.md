# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Purpose and scope
  - Suite of molecular analyses characterising biodiversity in epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
  - Aims to support consistent environmental health and policy monitoring by linking biodiversity data with environmental chemistry data across a defined spatial coverage.

- Data files and formats
  - Relevant data files:
    - soil_env_data.csv
    - soil_bacteria_seq.csv
    - soil_eukaryotes_seq.csv
    - water_env_data.csv
    - water_bacteria_seq.csv
    - water_eukaryotes_seq.csv
    - Protocol CEH Tellus SW.docx
  - Data tables present OTU-level biodiversity data and cross-referenced environmental data.

- Sampling design and field methods
  - Epilithon (water) sampling
    - Approximate sampling sites planned for broad spatial coverage from the Wold River to the Tamar River.
    - Exact site locations chosen in the field; GPS coordinates recorded with a Garmin GPS12.
    - At each of 20 locations, three stones were sampled; epilithon collected from a defined area; samples kept cold until laboratory analyses.
  - Soil sampling
    - Targeted soils across the Tamar region representing a range of land uses.
    - Exact site locations determined in the field; samples collected according to a specified protocol; locations recorded with GPS.
    - Soil samples kept cold until laboratory analyses.
  - Protocol reference: Protocol CEH Tellus SW.docx

- Laboratory methods and biodiversity data
  - DNA extraction and sequencing
    - DNA extracted from all soil and epilithon samples using the MOBIO Powersoil 96-well kit.
    - DNA quality checked for purity and yield prior to sequencing.
    - Sequencing performed by 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
  - Data processing
    - Sequences clustered into operational taxonomic units (OTUs).
    - Data tables report the percentage of each OTU within each sample.

- Data structure and cross-referencing
  - Biodiversity datasets
    - Epilithon bacteria: water_bacteria_seq.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv
    - Soil bacteria: soil_bacteria_seq.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Cross-referencing between biodiversity and environmental data
    - Rows: unique OTU IDs for each dataset.
    - Columns: OTU percentages per sample, with cross-referencing to environmental data via IDs.
    - Examples of cross-referencing:
      - Epilithon bacteria: water_bacteria_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
      - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
      - Soil bacteria: soil_bacteria_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv
      - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv
  - Environmental datasets
    - Water environmental data (water_env_data.csv)
      - Water_lab_ID (lab reference), Water_sample_ID, Stone_ID (A/B/C), Sampling Date, River, Catchment, NGR, Eastings, Northings
      - Cross-references to chemistry data and biodiversity data via IDs
    - Soil environmental data (soil_env_data.csv)
      - Soil_ID (lab reference), Sampling date, Grid reference (BNG 1 km), depth of core
      - Chemistry columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K
      - Soils analysed at CEH Lancaster chemistry facility; full methodological descriptions pending at the time

- Data accessibility and quality
  - DNA quality checked prior to sequencing; standardised laboratory workflow applied.
  - Field sampling aimed for broad spatial coverage with precise location data to support reproducibility and monitoring over time.
  - Protocol documentation included (Protocol CEH Tellus SW.docx).

- Contributors
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Version control
  - Version: 1.0
  - Date: 24/03/14
  - Author: R. Griffiths
  - Description: created