# Broad Habitat Area Estimates by Land Class for Great Britain 1998 Version: 1: 22-1-2014 C.M. Wood, CEH Lancaster

- The document describes national and spatial estimates of Broad Habitat stock for Great Britain for 1998, derived using the 2007 ITE Land Classification. Freshwater habitats were modelled differently from other habitats.
- Survey fieldwork occurred in 1998 (with a few sites in 1999) and is often referred to as Countryside Survey 2000.
- Data are intended to support analyses of habitat extent by land class, enabling correlations, trend assessment, and predictive applications. Data are accompanied by extensive references and methodology.

## Data Files and Structure

- CS1998_Broad_Habitat_Stock.csv
  - National estimates of Broad Habitat stock (Habitats 1–17) for 1998, by Land Class (using the 2007 ITE Land Classification).
  - Values provided as total area in thousands of hectares (000s ha), with lower and upper 95% confidence limits.
  - Note: Freshwater habitats were analysed with a different statistical model.
- CS1998_stock.tif
  - A 1 km resolution raster where each band represents a Broad Habitat class.
  - Each 1 km pixel contains a mean estimate (percentage) of the amount of habitat for that Broad Habitat within that square, derived from means of 1 km survey squares within each Land Class stratum.
  - Bands correspond to Broad Habitat classes (see mapping below).

## CSV File Details (fields)

- YEAR: Year of survey (number)
- LAND_CLASS: ITE Land Class (text)
- BROAD_HABITAT: Broad Habitat code (number)
- BROAD_HABITAT_NAME: Broad Habitat description (text)
- LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
- MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha). May be negative due to modelling; treat negative values as zero.
- LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
- UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

## Raster File Details

- Band structure
  - The raster has 17 bands, each corresponding to a Broad Habitat class.
  - Example mappings described in the dataset documentation (illustrative excerpts):
    - Band 2 corresponds to Broad Habitat 2 in conjunction with land-class interpretations (e.g., Coniferous Woodland vs. Broadleaved Mixed and Yew Woodland scenarios).
    - Band 3 corresponds to Broad Habitat 3 (e.g., Boundary and Linear Features) under relevant Land Class interpretations.
    - Other bands follow similarly for Broad Habitats 1–17.
  - The mapping provides the relationship between Broad Habitat codes and raster bands; for precise band-to-habitat mapping, refer to the dataset documentation.
- Pixel size: 1 km
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain

## Spatial and Projection Details

- Spatial reference: British National Grid
- Pixel resolution: 1000 m
- Coverage: Great Britain
- Data are provided with formal acknowledgements required for all copies, publications, and presentations.

## Usage, Access, and Citations

- All uses of Countryside Survey data must include the specified acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © NERC-CEH. All rights reserved.
- Relevant publications and references offer methodology, context, and details on how national estimates are generated from the 1 km survey sample squares (e.g., Scott 2007 Statistical Report; Haines-Young et al. guidance on habitat classification; and related ITE Land Classification documentation).

## Practical Considerations for Analysts

- Data represent a 1998 baseline by Land Class and Broad Habitat type; useful for cross-walking to other classifications and for temporal comparisons where compatible data exist.
- The MEAN_ESTIMATE can be negative due to the statistical model; treat such values as zero for area calculations.
- Freshwater habitats used a different modelling approach; ensure consistent methods when integrating with non-freshwater habitat data.
- Raster data provide spatially explicit insights (1 km cells) that can be aggregated to regional or national scales, or cross-referenced with other spatial layers (e.g., administrative boundaries or other habitat maps).
- Data quality and accessibility challenges highlighted for analysts (e.g., scale gaps, data fragmentation) are mitigated here by providing both a national CSV and a 1 km raster with documented band mappings.

## References and Related Resources

- Countryside Survey: UK Results from 2007 (publications detailing background and methodology)
- Scott, W.A. (2007) CS Technical Report No.4/07: Statistical methodology for deriving national estimates from 1 km survey squares
- Bunce et al. (ITE Land Classification of Great Britain 2007): Vector dataset and methodology
- Jackson (2000): Guidance on interpretation of Biodiversity Broad Habitat Classification
- Additional Centre for Ecology & Hydrology and NERC Countryside Survey documentation and links