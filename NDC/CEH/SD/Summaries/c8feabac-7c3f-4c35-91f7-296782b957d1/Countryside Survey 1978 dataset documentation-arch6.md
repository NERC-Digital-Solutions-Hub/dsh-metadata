# Broad Habitat Area Estimates by Land Class for Great Britain

- National estimates of Broad Habitat stock (Habitats 1-21, excluding 15 and 20) for 1978, calculated using the 1990 ITE Land Classification. Estimates are provided by Land Class.

## Datasets and formats

- CS1978_Estimates_by_LC.csv
  - Content: Yearly national estimates by Land Class for Broad Habitats.
  - Key columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class code
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat name
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% confidence interval for the Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence interval for the Broad Habitat area (000s ha)
- CS78_BH1_17.tif
  - Content: 1km pixel raster converting Land Class totals to percentages per 1km pixel.
  - Bands (one per Broad Habitat class) mapped as:
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
  - Pixel size: 1 km
  - Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator Great Britain
  - Extent: Great Britain

## Data provenance and classification

- Source: Countryside Survey data (© NERC - Centre for Ecology & Hydrology)
- Methodology reference: Estimates derived from Countryside Survey data, with 1978 data rescue and linkage to the 1990 ITE Land Classification (Bunce et al., 1996; Bunce et al., 1981; Jackson, 2000; Scott, 2007).
- Summary of approach: National estimates by Land Class, using the ITE Land Classification framework; results include mean estimates and 95% confidence intervals.

## Spatial coverage and metadata

- Coverage: Great Britain
- Projection details: British National Grid (OSGB36), Transverse Mercator
- Resolution: Raster (1 km), with per-pixel Broad Habitat proportions across bands; vector-like tabular data provided for 1978 national estimates by Land Class.

## Usage and acknowledgment

- Usage rights: All CS data require acknowledgment.
- Acknowledgment text: “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Potential uses: Enables data exploration, dashboard-like self-service analysis, reporting, and mapping of Broad Habitat distribution and changes by Land Class; supports visualization and comparison of national-scale habitat stocks and per-land-class contributions.

## Data interpretation notes

- The CSV provides mean estimates with 95% confidence intervals (lower and upper estimates) for Broad Habitat amounts within each Land Class.
- The TIFF raster encodes the spatial distribution of Broad Habitat proportions per 1 km pixel, enabling spatial analyses and map-based exploration of habitat classes across Great Britain.
- The Broad Habitat set excludes certain codes (15 and 20) in the national estimates for 1978.

## References and supporting publications

- Countryside Survey Website for project overview and methodologies:
  - http://www.countrysidesurvey.org.uk/
- Wood et al. (2012): Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue - Final Report (CEH Project NEC03689)
- Scott, W.A. (2007): CS Technical Report No.4/07 - Statistical methods for national estimates (CS_UK_2007_TR4.pdf)
- Bunce et al. (1996): ITE Merlewood Land Classification of Great Britain
- Bunce et al. (1981): Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification
- Jackson, D.L. (2000): Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307)