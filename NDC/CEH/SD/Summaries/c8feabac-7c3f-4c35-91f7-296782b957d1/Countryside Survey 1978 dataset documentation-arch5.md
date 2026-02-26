# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock for 1978 by ITE Land Class, excluding habitats 15 and 20, calculated using the 1990 ITE Land Classification (refer to Scott, 2007).
- Data provided for use by data stewards to support governance, reuse, and discovery across large datasets.

## Data Content

- CS1978_Estimates_by_LC.csv
  - Columns:
    - YEAR: Year of Survey (number)
    - LAND_CLASS: ITE Land Class (number)
    - BROAD_HABITAT: Broad Habitat code (text)
    - BROAD_HABITAT_NAME: Broad Habitat name (text)
    - LAND_CLASS_AREA: Total area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% confidence interval for Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence interval for Broad Habitat area (000s ha)

- CS78_BH1_17.tif
  - Raster data derived from Land Class totals by area, converted to percentage per 1km pixel.
  - Each band represents a Broad Habitat class:
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
  - Pixel size: 1 km; Coordinate system: British National Grid (OSGB36), Transverse Mercator projection.

## Provenance, Metadata and References

- Data source: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH).
- Documentation and methodological references include:
  - Countryside Survey: Measuring Habitat Change Over 30 Years (2012) Final Report NEC03689
  - CS Technical Report No.4/07 (Statistical methodology for national estimates)
  - ITE Merlewood Land Classification documents (Bunce et al., 1996; 1981)
  - Field Mapping Handbook (CS Technical Report No.1/07)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)

## Access, Use and Attribution

- All CS data require acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Use in publications, reports, and presentations should include the above acknowledgement.

## Data Quality, Limitations and Considerations for Stewardship

- Temporal scope: 1978 data, derived using the 1990 ITE Land Classification; users should consider temporal relevance for current applications.
- Exclusion of Broad Habitat codes 15 and 20 in the estimates; impacts interpretability for those classes.
- Uncertainty: MEAN_ESTIMATE with Lower and Upper 95% confidence intervals provided on a per Land Class basis.
- Data alignment: Raster product derived by normalising Land Class totals to percentages per 1km pixel; ensure appropriate interpretation when aggregating or resampling.
- Metadata completeness: Ensure consistent metadata when cataloguing, including projection, pixel size, extent, and acknowledgement requirements.

## Governance and Stewardship Implications

- Ensure proper data versioning and traceability (Version: 1; date 1-2-2012) for future updates.
- Maintain provenance links to primary publications and classification schemes to support audit trails.
- Establish interoperability considerations when integrating with other habitat or land-class datasets (e.g., consistent classification schemes, coordinate systems).
- Maintain clear licensing, rights statements, and attribution requirements in all disseminations.