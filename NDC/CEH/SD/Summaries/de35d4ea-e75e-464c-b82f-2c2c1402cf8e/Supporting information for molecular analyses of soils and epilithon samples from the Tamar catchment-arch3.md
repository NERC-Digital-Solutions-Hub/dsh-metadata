# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular biodiversity analyses (bacteria and eukaryotes) in epilithon (water) and soil samples, collected from the Tamar catchment in winter 2013/2014.
- Paired with environmental chemistry data to support environmental health monitoring and policy evaluation.

## Data files and datasets
- Relevance and structure
  - Environmental data
    - soil_env_data.csv: soil sampling metadata and chemistry results
      - Key fields: Soil_ID, Sampling date, Grid reference (BNG 1km), depth of core, and chemistry columns (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K)
      - Grid reference restricted to 1km resolution to protect site anonymity
    - water_env_data.csv: epilithon water sampling metadata
      - Key fields: Water_lab_ID (link cross-reference), Water_sample_ID (links to WP4 chemistry), Stone_ID (A/B/C at each location), Sampling date, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS
  - Biodiversity datasets (OTU tables from sequencing)
    - water_bacteria_seq.csv (epilithon bacteria)
    - water_eukaryotes_seq.csv (epilithon eukaryotes)
    - soil_bacteria_seq.csv (soil bacteria)
    - soil_eukaryotes_seq.csv (soil eukaryotes)
  - Protocol and methods
    - Protocol CEH Tellus SW.docx

## Data collection and processing
- Field collection
  - Epilithon (water): 20 locations along the Wold River to the Tamar River; approximate site locations planned from maps, exact sites refined in the field; GPS12 used for precise coordinates; three stones sampled per location; samples kept cold and transported to the lab.
  - Soil: samples from a range of Tamar region soils representing diverse land uses; exact sites determined in the field by accessibility and logistics; GPS12 used for coordinates; samples kept cold and transported to the lab.
- Laboratory and sequencing
  - DNA extraction: MOBIO PowerSoil 96-well kit for all soil and epilithon samples
  - Quality control: purity and yield checks before sequencing
  - Sequencing: 454 pyrosequencing to profile bacterial and eukaryotic biodiversity per sample
  - Data processing: sequences clustered into OTUs; output tables show the percentage of each OTU within each sample
- Data structure for cross-referencing
  - OTU data: rows = OTU IDs; columns = sample IDs
  - Cross-referencing: OTU tables link to environmental data via IDs
    - Epilithon bacteria: water_bacteria_seq.csv rows/columns cross-referenced to water_env_data.csv via Water_lab_ID
    - Epilithon eukaryotes: water_eukaryotes_seq.csv cross-referenced via Water_lab_ID
    - Soil bacteria: soil_bacteria_seq.csv cross-referenced via Soil_ID
    - Soil eukaryotes: soil_eukaryotes_seq.csv cross-referenced via Soil_ID

## Data structure, metadata and linking
- IDs and cross-references
  - Water_lab_ID and Water_sample_ID connect biodiversity data to water environmental data
  - Soil_ID connects soil biodiversity data to soil environmental data
- Metadata and methods
  - Soil chemistry methods not fully described yet (documentation awaiting full methodological descriptions)
  - Spatial data includes restricted grid references to preserve anonymity
- Data governance and sharing
  - Public sharing of underlying datasets is noted as a potential barrier
  - Emphasis on data quality, openness, and data management standards at the source
  - Underlying data sharing and governance processes are expected to support clear, transparent reporting

## Practical implications for monitoring frameworks
- Enables integrated environmental health measures
  - Combines chemical/physical soil and water data with molecular biodiversity profiles
  - Supports evaluation of policy through biodiversity indicators in relation to environmental conditions
- Data interoperability
  - Structured cross-referencing between biodiversity OTUs and environmental metadata supports comparative analyses and trend monitoring
- Documentation and transparency
  - Clear attribution of roles and contributors
  - Protocol reference provided, with room for completing methodological details (soil chemistry)

## Challenges and considerations
- Data availability and quality
  - Lack of data or data at adequate quality for some parameters
- Access and governance
  - Data sharing barriers and silos between organizations
  - Need for robust metadata to enable verification and reuse
- Data processing and usability
  - Metadata completeness and units/methodologies awaiting full description
  - Data formats may require transformation for standard monitoring workflows
- Communication of complex findings
  - Translating OTU-based biodiversity results into actionable policy insight

## Contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths

## Protocol and documentation references
- Protocol CEH Tellus SW.docx