# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- A dataset describing molecular analyses of epilithon (water) and soil samples from the Tamar catchment collected in winter 2013/2014.
- Includes field sampling details, laboratory processing, sequencing, and resulting biodiversity data tables linked to environmental chemistry data.

## Data files included

- soil_env_data.csv — soil chemistry data for each soil sample (Soil_ID as cross-reference; grid reference anonymized to 1 km; various chemical measurements).
- soil_bacteria_seq.csv — bacterial biodiversity data (OTU table; rows = OTU IDs, columns = Soil_ID cross-referenced to soil_env_data.csv).
- soil_eukaryotes_seq.csv — eukaryotic biodiversity data for soils (OTU table; rows = OTU IDs, columns = Soil_ID cross-referenced to soil_env_data.csv).
- water_env_data.csv — epilithon/water chemistry context data (Water_lab_ID used for cross-reference with biodiversity data; Stone_ID for each of three stones per site; sampling coordinates and site identifiers).
- water_bacteria_seq.csv — bacterial biodiversity data for epilithon (OTU table; rows = OTU IDs, columns = Water_lab_ID cross-referenced to water_env_data.csv).
- water_eukaryotes_seq.csv — eukaryotic biodiversity data for epilithon (OTU table; rows = OTU IDs, columns = Water_lab_ID cross-referenced to water_env_data.csv).
- Protocol CEH Tellus SW.docx — methodological protocol document.

## Field sampling and sampling locations

- Epilithon (water) sampling: approximately positioned to cover the Wolf River through to the Tamar River; exact sites chosen in the field for accessibility; GPS positions recorded with a Garmin GPS12; three stones sampled per location (A, B, C); samples kept cold and transported to the lab.
- Soil sampling: targeted a range of soils across the Tamar region reflecting various land uses; approximate sites planned from maps for wide catchment coverage; exact sites determined in the field; soil cores collected and kept cold for lab analyses.

## Data types and formats

- Water samples data (water_env_data.csv) includes: Water_lab_ID (lab reference), Water_sample_ID (links to WP4 water chemistry dataset), Stone_ID (A/B/C), SAMPLING DATE, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS.
- Soil samples data (soil_env_data.csv) includes: Soil_ID, Sampling date, Grid reference (1 km resolution for anonymity), depth of core, followed by soil chemistry measurements (Dry, C-total, Loss on Ignition, N-total, pH, and elemental concentrations: Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Biodiversity data (soil_bacteria_seq.csv, soil_eukaryotes_seq.csv, water_bacteria_seq.csv, water_eukaryotes_seq.csv) are OTU tables:
  - Rows = unique OTU IDs
  - Columns = cross-referenced sample IDs (e.g., OTU abundances per Soil_ID or Water_lab_ID)
  - Cross-referencing: OTU data align with corresponding environmental data files via Soil_ID or Water_lab_ID.

## Methods

- DNA extraction: performed on all soil and epilithon samples using the MOBIO Powersoil 96-well DNA extraction kit.
- Quality control: DNA purity and yield checked prior to sequencing.
- Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity within each sample.
- Bioinformatics: sequences processed and clustered into operational taxonomic units (OTUs); resulting tables show the percentage of each OTU within each sample.
- Data linkage: OTU tables are designed to be cross-referenced with the environmental data via the sample identifiers (Water_lab_ID or Soil_ID).

## Soil chemistry data

- Soil chemistry is reported in soil_env_data.csv with multiple analytes, including Dry mass, total carbon, loss on ignition, total nitrogen, pH, and concentrations of Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
- Grid reference is anonymized to 1 km resolution to protect sampling site locations.

## Data provenance and contributors

- Version 1.0, dated 24/03/14.
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall.
- Data processing and mapping: Gearóid Webb.
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths.
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths.
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## How to use and cross-reference

- Cross-referencing is central: environmental data (soil_env_data.csv, water_env_data.csv) align with biodiversity data via:
  - Water_lab_ID in water_env_data.csv with columns in water_bacteria_seq.csv and water_eukaryotes_seq.csv
  - Soil_ID in soil_env_data.csv with columns in soil_bacteria_seq.csv and soil_eukaryotes_seq.csv
- Examples provided illustrate linking OTU tables to the corresponding environmental measurements for integrated analysis of biodiversity and chemistry.

## Practical notes for data support

- Data are organized to enable self-service exploration by creating linkable tables for biodiversity with corresponding environmental context.
- Field methods and anonymization measures (grid references) are documented to support data interpretation and reuse.
- Documentation highlights potential data integration points and the need to consult related WP4 documentation for full water chemistry metadata.