# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- Version: 1: 1-2-2012
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Purpose: National estimates of Broad Habitat stock for 1978, calculated using the 1990 ITE Land Classification. Outputs are by Land Class to support monitoring of environmental health and habitat change over time.
- Context: Part of Countryside Survey efforts to measure habitat change over 30 years; data rescue and methodological documentation available in related CEH and CS publications.

## Data Files

- CS1978_Estimates_by_LC.csv
  - Content: National estimates of Broad Habitat stock (Habitats 1-21, excluding 15 and 20) for 1978, derived from the 1990 ITE Land Classification (see Scott, 2007).
  - Columns:
    - YEAR: Survey year
    - LAND_CLASS: ITE Land Class identifier
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat name
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI for Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI for Broad Habitat area (000s ha)

- CS78_BH1_17.tif
  - Content: Raster representation created by converting Land Class totals for Broad Habitats (1-17, excluding 15) into percentages per 1 km pixel (per Land Class Broad Habitat total).
  - Bands: Each band corresponds to a Broad Habitat class (detailed below).
  - Pixel size: 1 km (1000 m)
  - Coordinate system: British National Grid (OSGB1936)
  - Projection: Transverse Mercator Great Britain
  - Extent: Great Britain
  - Band mapping (examples from the file):
    - Band 1: Broadleaved Mixed and Yew Woodland
    - Band 2: Coniferous Woodland
    - Band 3: Boundary and Linear Features
    - Band 4: Arable and Horticulture
    - Band 5: Improved Grassland
    - Band 6: Neutral Grassland
    - Band 7: Calcareous Grassland
    - Band 8: Acid Grassland
    - Band 9: Bracken
    - Band 10: Dwarf Shrub Heath
    - Band 11: Fen, Marsh, Swamp
    - Band 12: Bog
    - Band 13: Standing Open Waters and Canals
    - Band 14: Rivers and Streams
    - Band 15: Inland Rock
    - Band 16: Urban
    - Band 17: (Additional Broad Habitat class as defined in the dataset)
  - Note: Bands reflect Broad Habitat classes as defined in the accompanying documentation; 1 km pixel values express the proportion of the Land Class area occupied by each Broad Habitat within that pixel.

## Metadata, Licensing, and Attribution
- Acknowledgement: All use of Countryside Survey data must be acknowledged.
- Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.
- Attribution text to use on publications and presentations: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data usage: Data should be stored and uploaded to the appropriate portals; datasets should be traceable to their CS provenance.

## Data provenance, Methods, and Scope
- Temporal scope: 1978 data used to produce national estimates for that year.
- Classification system: 1990 ITE Merlewood Land Classification (Bunce et al. 1996; Bunce et al. 1981; Scott 2007 for how national estimates are derived from 1 km survey squares).
- Output formats: Tabular national estimates (CSV) by Land Class; raster percent distributions per Broad Habitat (1 km pixels, TIFF).
- Related methodologies: Field mapping, statistical treatment to assemble national totals from 1 km sample squares; references include CS Technical Reports and methodological handbooks.

## Data Quality and Limitations
- The 1978 national estimates are derived from the 1 km survey sample using the 1990 Land Classification framework, which may involve classification translation and uncertainties reflected in confidence intervals (Lower/Upper estimates).
- The raster data provide per-pixel percentages within Land Class areas, not direct area tallies; interpretation should consider the unit and aggregation method.

## How this supports monitoring and analysis
- Enables standardized, time-consistent assessment of Broad Habitat distribution and change over time.
- Facilitates creation of maps, charts, and reports for environmental health and policy performance evaluation.
- Useful for cross-referencing with other data layers (land cover, biodiversity indicators) to enhance monitoring outputs.

## Access, reuse, and integration considerations for Analysts
- Data provenance and licensing require clear attribution to NERC - CEH.
- The datasets are designed to be stored in appropriate data portals and shared with clear metadata.
- Because the data are prepared for monitoring, they are suitable for integration with other standardized datasets to increase value beyond single-use analyses.

## Related publications and references
- Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue - Final Report CEH Project NEC03689 (Wood et al., 2012)
- Countryside Survey: Measuring Habitat Change Over 30 Years (2012) – general methodology and context
- CS Technical Report No.4/07: Statistical methodology for generating national estimates from 1 km survey squares (Scott, 2007)
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996)
- Land Classes in Great Britain: Preliminary Descriptions for Users (Bunce et al., 1981)
- Guidance on the interpretation of the Biodiversity Broad Habitat Classification (Jackson, 2000)
- Countryside Survey website: http://www.countrysidesurvey.org.uk