# Meteorological data

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2002), studied at the Sourhope site in the Scottish Borders to understand soil biota diversity and their functional roles.
- The programme funded 24 projects on soil structure, processes (carbon and nitrogen cycles), and soil fauna across micro-, meso-, and macro-fauna.
- The data governance and stewardship are handled by the Soil Biodiversity Data Manager at the Centre for Ecology & Hydrology (CEH).

## Data Content and Structure
- Data type: Regular meteorological measurements collected at an on-site Automatic Weather Station (AWS) from February 1999 to September 2002.
- File: CHA_Sourhope_AWS_1999_2002.csv (hourly summaries derived from 5-second samplings).
- Key columns and concepts:
  - EXPERIMENT_ID, Description = 'AWS'
  - AWS_DATE (Date), AWS_TIME (Time)
  - RAINFALL (mm)
  - WIND_SPEED (ms-1), WIND_DIRECTION (degrees)
  - AIR_TEMP (°C)
  - SOIL_TEMP_2CM, SOIL_TEMP_MINUS_2CM, SOIL_TEMP_MINUS_5CM, SOIL_TEMP_MINUS_10CM, SOIL_TEMP_MINUS_30CM (soil temperatures)
  - SOIL_MOISTURE (m3/m3)
- Notes:
  - Measurements are hourly summaries of 5-second samples.
  - Metadata provides unit definitions and data descriptions for each field.

## Provenance and Custodianship
- Data collected on-site and regularly downloaded and transmitted to the Soil Biodiversity Data Manager at CEH.
- Data are stored and managed under the NERC Soil Biodiversity Programme framework, with data products documented for user discovery and reuse.
- Data file naming and column definitions are explicitly described to support understanding and reuse.

## Quality Assurance and Limitations
- Quality control steps include numeric range checks, data formatting conformity, and logical integrity checks.
- Despite QA, NERC does not warrant the accuracy or fitness of the data for any particular use and disclaims liability for damages or losses arising from use of the data.
- Metadata describes the dataset structure and variables, but users should independently assess suitability for specific analyses.

## Access, Use, and Sharing
- Data are curated by the Soil Biodiversity Data Manager at CEH and described for discovery and reuse.
- The dataset CHA_Sourhope_AWS_1999_2002.csv is the primary data product; users should reference the NERC Soil Biodiversity Programme and acknowledge the data custodian.
- Use is subject to the standard disclaimer regarding accuracy and liability.

## Relevance to Data Stewards
- Highlights established governance and custodianship for a large, multi-project program.
- Emphasizes the need for clear metadata, documented data lines, and explicit QA procedures.
- Demonstrates handling of legacy, longitudinal datasets with defined data formats and units, suitable for cross-system interoperability with careful attention to metadata accuracy.

## Practical Considerations and Challenges
- Incomplete understanding of end-user needs may affect discoverability and reuse; clear documentation aids in mitigating this.
- Ensuring timely access and transfer of data from on-site AWS to the data manager is crucial for ongoing usability.
- Managing metadata consistency (units, column definitions) across datasets and potential metadata discrepancies (e.g., some unit descriptions in the source notes may require verification).
- Interoperability across systems and formats is important when integrating this dataset with broader data portals or analyses involving soil biodiversity research.