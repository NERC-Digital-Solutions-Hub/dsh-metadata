# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular analyses performed on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Data describe both environmental chemistry and biodiversity (bacteria and eukaryotes) across sample sites.
- Cross-referenced datasets enable linking chemical context with microbial and eukaryotic community composition.

## Data assets and structure
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity datasets:
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Cross-referencing schema:
  - Water: OTU-based tables cross-referenced to water_env_data.csv via Water_lab_ID (also Water_sample_ID links to WP4 water chemistry data).
  - Soil: OTU-based tables cross-referenced to soil_env_data.csv via Soil_ID.

- Soil chemistry data (soil_env_data.csv) contents:
  - Soil_ID (unique lab identifier)
  - Sampling date
  - Grid reference (1 km resolution, anonymized)
  - Depth of core
  - Chemistry results: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K

- Epilithon water chemistry data (water_env_data.csv) contents:
  - Water_lab_ID (unique lab identifier; cross-referenced with biodiversity data)
  - Water_sample_ID (cross-referenced to WP4 water chemistry dataset)
  - Stone_ID (A, B, C for each location)
  - Sampling date, River, Catchment, NGR, Eastings, Northings

## Field collection and laboratory workflow
- Field sampling:
  - Epilithon (water): Sites chosen to cover the Wold River to the Tamar River; exact sites determined in the field; GPS-based localization with Garmin GPS12; three stones sampled per location.
  - Soils: Targeted soils across the Tamar region representing diverse land uses; exact sites determined in the field; GPS-based localization; samples kept cold and processed in lab.
- Laboratory processing:
  - DNA extraction using MOBIO Powersoil 96-well kit.
  - Quality checks for purity and yield prior to sequencing.
  - 454 pyrosequencing to assess bacterial and eukaryotic biodiversity per sample.
  - Bioinformatic processing: sequences clustered into operational taxonomic units (OTUs); results presented as the percentage of each OTU within each sample.
- Data linkage:
  - OTU tables (bacteria and eukaryotes) are aligned with corresponding environmental data via the ID fields (Water_lab_ID or Soil_ID).

## Data quality, metadata and standards
- Anonymization:
  - Soil sampling grid references are limited to 1 km to protect site anonymity.
- Metadata mapping:
  - Clear cross-references between biodiversity datasets and environmental data via unique IDs (Water_lab_ID, Soil_ID).
  - For water chemistry context near epilithon samples, refer to WP4 documentation.
- Methodology notes:
  - Full methodological descriptions for procedures and units are awaited (as noted for soil chemistry data), with chemistry analyses conducted at CEH Lancaster.
  - Protocol document available: Protocol CEH Tellus SW.docx.

## Contributors and governance
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Overall focus: Suite of molecular analyses across epilithon and soil samples in the Tamar catchment.

## Practical notes for data users
- Cross-referencing of datasets enables integrated analyses of chemical context with microbial and eukaryotic community structure.
- Ensure proper alignment of IDs when merging OTU tables with environmental data.
- Be aware of anonymization constraint for soil locations when analyzing spatial patterns.
- For complete methodological details beyond what's provided, consult the CEH Tellus SW protocol and WP4 documentation referenced in the dataset descriptions.