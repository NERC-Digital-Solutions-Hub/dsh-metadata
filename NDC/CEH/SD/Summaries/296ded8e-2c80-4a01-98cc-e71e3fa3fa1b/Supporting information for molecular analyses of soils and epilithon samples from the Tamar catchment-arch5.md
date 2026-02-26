# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- A dataset from winter 2013/2014 comprising environmental chemistry data and biodiversity sequencing from epilithon (water) and soil samples in the Tamar catchment.
- Includes metadata, sample identifiers, and cross-referencing schema to relate environmental data to biodiversity data.

## Data files
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx

## Data collection and sampling
- Field locations chosen to provide broad spatial coverage; exact sites determined in the field for accessibility and logistics.
- Epilithon (water) sampling: three stones per site; samples kept cold and transported to the laboratory for analyses.
- Soil sampling: soils targeted across Tamar region with varied land uses; exact sites chosen in the field and documented.
- Site positions: exact coordinates determined with a Garmin GPS12; 1 km grid reference used for anonymity.

## Data processing and content
- DNA extraction: performed on all soil and epilithon samples using MOBIO Powersoil 96-well kit; quality checked prior to sequencing.
- Sequencing: 454 pyrosequencing used to assess bacterial and eukaryotic biodiversity.
- Data processing: sequences clustered into Operational Taxonomic Units (OTUs); results presented as OTU percentage composition per sample.
- Data structure (example mapping):
  - Epilithon bacteria: water_bacteria_seq.csv rows = OTUs; columns = sample cross-reference to water_env_data.csv via Water_lab_ID.
  - Epilithon eukaryotes: water_eukaryotes_seq.csv rows = OTUs; columns = sample cross-reference to water_env_data.csv via Water_lab_ID.
  - Soil bacteria: soil_bacteria_seq.csv rows = OTUs; columns = sample cross-reference to soil_env_data.csv via Soil_ID.
  - Soil eukaryotes: soil_eukaryotes_seq.csv rows = OTUs; columns = sample cross-reference to soil_env_data.csv via Soil_ID.

## Metadata, cross-references, and anonymization
- Water data: Water_lab_ID links to biodiversity data; Water_sample_ID cross-references WP4 water chemistry dataset sample names.
- Soil data: Soil_ID links to biodiversity data; Grid reference anonymized to 1 km to safeguard site locations.
- Cross-referencing schema ensures that environmental measurements align with corresponding OTU data for downstream analyses.

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Quality, standards, and notes
- Soil chemistry data: columns include Dry, C-total, Loss on Ignition, N-total, pH, and various elements (Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K); units and full methodological details pending (awaiting full methodological descriptions of procedures and units).
- Metadata and field protocols are documented in Protocol CEH Tellus SW.docx; exact site locations are preserved with anonymized coordinates.

## Access, sharing, and reuse considerations
- Cross-referenced data enable integrated analysis of environmental chemistry and microbial/eukaryotic biodiversity.
- Data are structured to be cataloged and linked across environmental datasets and biodiversity datasets, facilitating discovery and reuse while protecting site anonymity through grid-based location reporting.