# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A data-rich study comprising environmental chemistry and biodiversity sequencing from epilithon (water) and soil samples in the Tamar catchment (winter 2013/2014).
- Data are organized into multiple CSV files and a protocols document, with explicit cross-references between environmental and biodiversity data.
- Aimed at enabling data discovery, cross-linking, and exploration of microbial and eukaryotic diversity alongside chemical context.

## Datasets and data files
- soil_env_data.csv: soil chemistry and site metadata
- water_env_data.csv: epilithon/water chemistry and site metadata
- soil_bacteria_seq.csv: soil bacterial OTU abundances
- soil_eukaryotes_seq.csv: soil eukaryotic OTU abundances
- water_bacteria_seq.csv: epilithon bacterial OTU abundances
- water_eukaryotes_seq.csv: epilithon eukaryotic OTU abundances
- Protocol CEH Tellus SW.docx: methodological protocol document

## Field methods and sampling design
- Epilithon (water samples):
  - Sampling sites chosen to provide good spatial coverage from the Wolf/Tamar to the Tamar River.
  - Exact locations determined in the field with a Garmin GPS12.
  - 20 locations, three stones sampled per location; epilithon collected from a defined area.
  - Samples kept cold and transported to the laboratory for analyses.
- Soil samples:
  - Targeted soils from the Tamar region across a range of land uses.
  - Exact sites determined in the field with accessibility considerations.
  - Samples collected and kept cold, then analyzed in the laboratory.
- All sample locations were recorded using GPS; 1 km grid references are used in soil data to protect site anonymity.

## Data structure and cross-referencing
- Biodiversity data (OTU tables):
  - Rows: OTU IDs (unique per dataset).
  - Columns: samples; each cell indicates the percentage of a given OTU within that sample.
- Cross-referencing between biodiversity and environmental data:
  - Epilithon bacteria (water_bacteria_seq.csv) rows correspond to OTUs; column 1 references Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes (water_eukaryotes_seq.csv) rows correspond to OTUs; column 1 references Water_lab_ID in water_env_data.csv.
  - Soil bacteria (soil_bacteria_seq.csv) rows correspond to OTUs; column 1 references Soil_ID in soil_env_data.csv.
  - Soil eukaryotes (soil_eukaryotes_seq.csv) rows correspond to OTUs; column 1 references Soil_ID in soil_env_data.csv.
- Environmental data fields:
  - water_env_data.csv: Water_lab_ID, Water_sample_ID (cross-referenced to WP4 water chemistry), Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
  - soil_env_data.csv: Soil_ID, Sampling date, Grid reference (1 km resolution), depth of core; chemistry columns (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Purpose of cross-links: to enable integrated analyses linking OTU patterns with chemical and spatial context, and to reference external WP4 chemistry datasets for additional water chemistry metadata.

## Data processing and quality notes
- DNA extraction performed with MOBIO Powersoil 96-well kit; quality checked prior to sequencing.
- Sequencing performed using 454 pyrosequencing to assess bacterial and eukaryotic biodiversity per sample.
- Post-sequencing processing clustered reads into OTUs; results presented as OTU percentages per sample.
- Soil chemistry methods to be clarified with forthcoming methodological descriptions (current documentation indicates that procedures and units are to be described in detail later).

## Provenance and contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples from Tamar catchment, winter 2013/2014

## Usage notes
- Data are cross-referenced to support self-service exploration of biodiversity alongside environmental chemistry and spatial context.
- Soil data uses a 1 km grid reference to preserve site anonymity.
- For additional chemical context, refer to the WP4 water chemistry dataset and the Protocol CEH Tellus SW document.