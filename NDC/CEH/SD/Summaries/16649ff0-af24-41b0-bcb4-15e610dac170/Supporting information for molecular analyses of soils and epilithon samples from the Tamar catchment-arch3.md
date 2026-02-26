# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset describing a suite of molecular analyses to assess biodiversity and environmental health in the Tamar catchment during winter 2013/2014.
- Integrates biodiversity data (bacteria and eukaryotes from epilithon and soils) with corresponding environmental chemistry data.
- Aims to support monitoring and policy evaluation by providing cross-referenced, verifiable data and clear data governance practices.

## Data assets and documentation
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
- Protocol: Protocol CEH Tellus SW.docx

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Focus: suite of molecular analyses in epilithon (water) and soil samples

## Field sampling design and methods
- Epilithon (water samples):
  - Sampling sites chosen to achieve broad spatial coverage from the Wold River to the Tamar River.
  - Exact site locations determined in the field; GPS used for positioning.
  - At each site, three stones sampled (A, B, C); samples kept cold and transported to lab.
- Soil sampling:
  - Targeted soils across the Tamar region representing various land uses.
  - Exact sites determined in the field; GPS used; anonymized 1 km grid reference retained.
  - Soil cores collected from a defined depth range; samples kept cold and analyzed in the lab.

## Biodiversity datasets and data structure
- DNA-based biodiversity assessment:
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Sequencing and analysis:
  - DNA extracted with MOBIO Powersoil kit.
  - Quality checked, then submitted for 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
  - bioinformatic processing clusters sequences into Operational Taxonomic Units (OTUs); results are the percentage of each OTU within each sample.
- Data table structure:
  - Rows: OTU IDs
  - Columns: sample IDs cross-referenced to the environmental data
  - Cross-reference examples:
    - Epilithon bacteria: water_bacteria_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
    - Soil bacteria: soil_bacteria_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv

## Soil chemistry data (soil_env_data.csv)
- Key identifiers:
  - Soi l_ID: unique lab identifier cross-referenced with biodiversity data
  - Sampling date: date cores were taken
  - Grid reference: 1 km resolution British National Grid Reference (anonymized)
  - Depth of core: depth range of sampled soil
- Chemistry and element data (columns include):
  - Dry weight, C-total, Loss on Ignition (LOI), N-total
  - pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn
  - Ca, Mn, P, S, Mg, K

## Data governance, quality, and accessibility
- Metadata and data governance considerations:
  - Metadata completeness is essential to verify data suitability and reuse.
  - Data governance processes should ensure datasets meet standards and are stored, shared, and kept up to date.
- Access and sharing considerations:
  - Public sharing of underlying data is desirable for transparency but can be a barrier depending on policy or metadata gaps.
  - Anonymization (1 km grid references) helps protect site locations while enabling spatial analysis.
- Data quality and transformation:
  - Data may require transformation for use in analyses; attention to metadata and provenance supports reproducibility.
- Relevance for monitoring frameworks:
  - The integrated dataset supports environmental health measures by linking microbial diversity with soil and water chemistry across space and time.

## Implications for monitoring frameworks and policy
- Potential environmental health measures:
  - Microbial OTU diversity and composition in epilithon and soils (bacterial and eukaryotic communities).
  - OTU richness and beta diversity across sites and land-use types.
  - Relationships between biodiversity metrics and soil/water chemistry (e.g., heavy metal concentrations, pH, organic content).
  - Spatial patterns of biodiversity and chemistry using anonymized grid references for policy-relevant zoning and trend analysis.
- Data integration and governance needs:
  - Clear metadata standards to facilitate cross-dataset linking and reuse.
  - Transparent data sharing practices to support policy evaluation and stakeholder consultation.
  - Mechanisms to maintain up-to-date data and manage data silos, enabling coherent environmental health monitoring.