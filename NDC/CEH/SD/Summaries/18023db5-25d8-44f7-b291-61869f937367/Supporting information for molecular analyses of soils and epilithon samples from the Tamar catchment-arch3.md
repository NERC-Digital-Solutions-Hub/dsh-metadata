# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## General purpose and scope
- A suite of molecular analyses conducted on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Aimed at assessing biodiversity (bacteria and eukaryotes) and environmental chemistry to inform monitoring and policy evaluation.

## Data files and contents
- soil_env_data.csv: soil chemical properties and metadata per sample (e.g., Dry, C-total, Loss on Ignition, N-total, pH, and elements such as Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- soil_bacteria_seq.csv: bacterial OTU composition for soil samples.
- soil_eukaryotes_seq.csv: eukaryotic OTU composition for soil samples.
- water_env_data.csv: epilithon water chemistry and sampling metadata, including cross-references to biodiversity data (Water_lab_ID, Water_sample_ID, Stone_ID, date, river, catchment, NGR/Easting/Northing).
- water_bacteria_seq.csv: bacterial OTU composition for epilithon water samples.
- water_eukaryotes_seq.csv: eukaryotic OTU composition for epilithon water samples.
- Protocol CEH Tellus SW.docx: methodological protocol document.

## Field methods and sampling design
- Epilithon (water) samples:
  - Sampling sites chosen to give good spatial coverage along the Wolf/Tamar transect; exact sites finalized in the field.
  - Location determined with a Garmin GPS12; three stones sampled at each of 20 locations; samples kept cold and processed in the lab.
- Soil samples:
  - Targeted soils across the Tamar region representing various land uses.
  - Exact sites determined in the field; protected anonymity by 1 km grid reference.
  - Soil cores collected, kept cold, and transported to the laboratory for analyses.

## Data structure and cross-referencing
- Biodiversity data:
  - DNA extracted with MOBIO Powersoil kit; quality checked; sequenced by 454 pyrosequencing.
  - Sequences clustered into OTUs; data tables show percentage composition of OTUs per sample.
  - Structure: rows are OTU IDs; columns cross-reference with the respective environmental data via sample IDs.
  - Examples of linking:
    - Epilithon bacteria: water_bacteria_seq.csv rows/OTUs map to Water_lab_ID in water_env_data.csv.
    - Epilithon eukaryotes: water_eukaryotes_seq.csv similarly map to Water_lab_ID.
    - Soil bacteria: soil_bacteria_seq.csv map to Soil_ID in soil_env_data.csv.
    - Soil eukaryotes: soil_eukaryotes_seq.csv map to Soil_ID in soil_env_data.csv.
- Environmental data:
  - Water data include Water_lab_ID (lab-wide identifier), Water_sample_ID (cross-referenced to WP4 water chemistry data), Stone_ID (A/B/C), sampling date, river, catchment, and grid/coordinate fields (NGR, Eastings, Northings).
  - Soil data include Soil_ID, sampling date, 1 km grid reference for anonymity, depth of core, and a range of chemical measurements (items listed above).

## Methodology and data quality notes
- DNA extraction and sequencing described; sequencing output analyzed to produce OTU-based biodiversity profiles.
- Soil chemistry analyses conducted at CEH Lancaster chemistry facility; note that full methodological descriptions and units are still awaited.
- Emphasis on linking biodiversity with environmental chemistry through standardized identifiers and cross-referenced datasets.

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths

## Relevance for monitoring and governance
- Combines chemical and biological indicators across water and soil to support environmental health monitoring.
- Uses standardized cross-referencing to integrate biodiversity data with environmental chemistry, enabling longitudinal assessment and decision-making.
- Anonymization via 1 km grid references protects site confidentiality while preserving analytical utility.
- Metadata and protocol documentation provided, with some methodological details pending, highlighting the importance of complete methods for reproducibility and audit in monitoring frameworks.