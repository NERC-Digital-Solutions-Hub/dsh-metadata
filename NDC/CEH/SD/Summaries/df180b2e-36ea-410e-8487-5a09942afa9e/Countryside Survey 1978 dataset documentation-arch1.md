# Broad Habitat Area Estimates by Land Class for Great Britain

- The document provides national estimates of Broad Habitat stock for Great Britain for 1978, derived using the 1990 ITE Land Classification, and organized by Land Class.

## Data files and structure

- CS1978_Estimates_by_LC.csv
  - Purpose: National estimates of Broad Habitat stock (Habitats 1-21, excluding 15 and 20) by Land Class for 1978.
  - Method: Calculated using the 1990 ITE Land Classification (see Scott, 2007).
  - Key columns:
    - YEAR: Survey year (1978)
    - LAND_CLASS: ITE Land Class code
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of the Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat (000s ha) for the Land Class
    - LOWER_ESTIMATE: Lower bound of the 95% CI
    - UPPER_ESTIMATE: Upper bound of the 95% CI

- CS78_BH1_17.tif
  - Spatial raster representation (1 km pixel size) of Broad Habitat proportions by Land Class.
  - Data construction: Based on Land Class totals for each Broad Habitat (1–17, excluding 15 as stated in the text) converted to percentages per 1 km pixel.
  - Band-by-band mapping (each band corresponds to a Broad Habitat):
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
  - Pixel size: 1 km (1000 m)
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator projection
  - Extent: Great Britain

## Data provenance, usage, and attribution

- Data origin: Countryside Survey data, owned by NERC – Centre for Ecology & Hydrology (CEH).
- Acknowledgement requirement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © CEH. All rights reserved.”
- References and background: Primary sources and methodology collaborators are listed (e.g., Scott 2007; Bunce et al.; Jackson 2000; CEH technical reports), with links and notes on how national estimates are generated from 1 km survey squares.

## Methodology and interpretation

- 1978 national estimates are calculated by aggregating Land Class totals and linking them to Broad Habitats using the 1990 ITE Land Classification framework.
- The 1 km pixel raster provides a spatially explicit representation of Broad Habitat proportions within each Land Class area, enabling per-pixel analysis and mapping of habitat distribution across Great Britain.
- The dataset ties to broader Countryside Survey outputs and methodologies, including habitat change assessments over 30 years (e.g., the 1978 Data Rescue and related reports).

## Analytical opportunities and use cases

- Identify correlations between Land Class areas and associated Broad Habitats at a national level for 1978.
- Map the spatial distribution of Broad Habitats across Great Britain at 1 km resolution to support regional planning, conservation prioritization, or historical trend analyses when combined with later survey years.
- Use MEAN_ESTIMATE and confidence intervals (LOWER/UPPER_ESTIMATE) to assess uncertainty in habitat area estimates by Land Class.
- Integrate with auxiliary datasets (e.g., administrative boundaries, protected areas, or land-use data) to explore habitat patterns at varying scales.

## Considerations and challenges for analysts

- Scale and timing: Data are anchored to 1978 using the 1990 Land Classification framework; historical context and potential changes in classification schemes should be considered when comparing with later periods.
- Local detail and accessibility: While the dataset provides national estimates, local decisions may require higher-resolution or more recent data; the raster offers 1 km granularity, which may still be coarse for fine-scale planning.
- Data quality and standardisation: The conversion from Land Class totals to Broad Habitat estimates relies on the consistency of Land Classification and the methodology described in related reports; cross-referencing with referenced technical reports is advised for rigorous analyses.
- Data discovery and integration: The two primary data formats (CSV with tabular estimates and TIFF raster with per-pixel habitat fractions) should be combined carefully to maintain consistency between area-based and space-based representations.

## Related publications and references

- Countryside Survey Website and project overviews
- Wood, C.M., et al. (2012) Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue - Final Report
- Scott, W.A. (2007) CS Technical Report No.4/07: Statistical methods for generating national estimates from 1 km survey squares
- Bunce, R.G.H., et al. (1996) ITE Merlewood Land Classification of Great Britain
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981) Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method
- Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307)
- Field mapping and methodology reports (CS Technical Report No.1/07)