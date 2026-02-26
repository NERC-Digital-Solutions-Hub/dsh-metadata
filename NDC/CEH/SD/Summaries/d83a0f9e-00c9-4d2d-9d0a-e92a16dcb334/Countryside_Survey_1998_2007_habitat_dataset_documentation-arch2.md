# Dataset Documentation for 'Countryside Survey mapped estimates of Broad Habitat area change in Great Britain between 1998 and 2007'

## Overview
- Documents national estimates of Broad Habitat area change in Great Britain from 1998 to 2007, summarized by ITE Land Class 1.
- Based on the 2007 ITE Land Classification and mapping methodologies described in Countryside Survey technical reports.
- Provides a single shapefile with percentage change (increase or decrease) for 17 Broad Habitats across Land Classes.

## Data content and structure
- File: CS98_07_Broad_Habitat_Change_Map.shp
- Purpose: National estimates of % change in Broad Habitat area between 1998 and 2007, by Habitat type and Land Class.
- Key fields:
  - LC2007: ITE Land Class (numerical)
  - LC2007_COD: ITE Land Class code (text)
  - SURVEY: Years of survey (to/from)
  - Column1 to Column17: % change values for each Broad Habitat
    - Column1: Broadleaved, Mixed and Yew Woodland
    - Column2: Coniferous Woodland
    - Column3: Boundary and Linear Features
    - Column4: Arable and Horticulture
    - Column5: Improved Grassland
    - Column6: Neutral Grassland
    - Column7: Calcareous Grassland
    - Column8: Acid Grassland
    - Column9: Bracken
    - Column10: Dwarf Shrub Heath
    - Column11: Fen, Marsh, Swamp
    - Column12: Bog
    - Column13: Standing Open Waters and Canals
    - Column14: Rivers and Streams
    - Column15: Montane
    - Column16: Inland Rock
    - Column17: Urban
- Each Column value represents the % increase or decrease in area for that habitat.

## Methodology
- Habitat change estimates are calculated using the 2007 ITE Land Classification (Bunce et al. 1996; 2007).
- Mapping methodology described in Maskell et al., 2008; Barr (1998) referenced for related mappings.
- National estimates are generated from Countryside Survey 1 km survey sample squares (statistical treatment described in Scott, 2007).

## Licensing and reuse
- License: Open Government Licence
- Acknowledgement required on all copies, publications, and presentations:
  - "Countryside Survey data owned by NERC Centre for Ecology & Hydrology. Countryside Survey © Centre for Ecology & Hydrology (Natural Environment Research Council). All rights reserved."
- Full reuse details and attribution: https://doi.org/10.5285/d83a0f9e-00c9-4d2d-9d0a-e92a16dcb334

## Access and provenance
- Data source: Countryside Survey (UK results from 2007 and associated methodologies)
- Supporting documentation: https://doi.org/10.5285/d83a0f9e-00c9-4d2d-9d0a-e92a16dcb334
- Related references and methodological papers listed in the dataset documentation (e.g., Barr et al., 1998; Bunce et al., 2007; Maskell et al., 2008; Scott, 2007).

## How this supports environmental monitoring (Analysts’ perspective)
- Provides standardized, comparable metrics of habitat change over a decade, enabling temporal trend analysis and policy performance assessment.
- Outputs are suitable for inclusion in reports, maps, and charts, aligning with standardized reporting formats.
- Datasets can be stored and uploaded to appropriate data portals for broader accessibility.

## Data quality and usability considerations
- Data are derived from established Countryside Survey methodologies and the ITE Land Classification (2007); users should reference the methodology documents when interpreting results.
- National-scale estimates are summarized by Land Class and 17 Broad Habitats, suitable for high-level monitoring and cross-sector analyses.
- Encourages linking with other datasets to enhance data value and accessibility of underlying data, as highlighted in broader monitoring challenges.