# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Countryside Survey 1990 estimates of Broad Habitat areas in Great Britain (HB 1–17) using the 2007 ITE Land Classification framework.
- Provides national totals by Land Class and Broad Habitat, with mean estimates and 95% confidence intervals (lower/upper).
- Notes that freshwater habitats were modeled differently and that there was no separate Montane (BH15) class in 1990.
- Includes mapped 1km-resolution estimates (cs1990_stock.tif) where each pixel represents the mean habitat percentage for that Broad Habitat within the corresponding Land Class strata band.
- No Montane class in 1990; for mapping, Band 15 corresponds to BH16 and Band 16 to BH17.

## Data files and structure

- CS1990_Broad_Habitat_Stock.csv (national estimates by Land Class)
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
      - Note: Negative values may occur due to the statistical model; treat as 0.
    - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

- cs1990_stock.tif (1km-pixel raster estimates)
  - In each 1km pixel band, contains a mean percentage value for the Broad Habitat within that square.
  - Bands correspond to Broad Habitat classes as detailed (e.g., Band mappings for BH1–BH17 with adjustments due to 1990 being missing BH15).
  - 1km pixel resolution; British National Grid (OSGB36) Transverse Mercator projection.

## Spatial information
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB1936)
- Projection: Transverse Mercator
- Extent: Great Britain
- Data are positioned for national-scale interpretation with a raster complement to the CSV summaries.

## Key caveats and data quality
- MEAN_ESTIMATE may be negative due to the statistical model; treat negatives as zero.
- FreshwaterBroadHabitat data were modeled separately from other habitats.
- There was no dedicated Montane (BH15) class in 1990; mapping adjustments: Band 15 = BH16, Band 16 = BH17.
- Data accessibility and unification considerations for analysts: note the need to acknowledge CS data usage and handle both tabular and raster formats consistently.
- Unit of analysis is national totals by Land Class and Broad Habitat, with CI bounds for uncertainty.

## Access, attribution, and provenance
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH) and require acknowledgement in all copies, publications, and presentations.
- Acknowledgement language: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © … CEH. All rights reserved.”
- References and methodological background are provided to support interpretation and cross-walk with other ITE Land Classification datasets.

## How this data can support analysis (Analysts’ perspective)
- Primary use: derive national-scale habitat area estimates by Land Class and Broad Habitat for 1990, with associated uncertainty.
- Raster data (cs1990_stock.tif) enables spatially explicit analysis and overlay with other GIS layers (land use, protected areas, boundaries).
- Can facilitate trend analysis when combined with other years’ datasets and cross-walks to the ITE Land Classification.
- Useful for evaluating potential habitat distributions under historical baselines or for calibrating predictive models, while accounting for classification and model-based uncertainties.

## Considerations for integration and interpretation
- When integrating with other years or datasets, account for differences in classification schemes, scales, and modeling approaches (e.g., freshwater vs other habitats).
- Be mindful of unit conventions (000s ha) and transform as needed for reporting in consistent units.
- Cross-check Montane and freshwater classifications due to 1990-specific modeling choices and absence of BH15.
- Use the 95% CIs to convey uncertainty in national estimates and when propagating into analyses or decision-support outputs.

## References and further information
- Publications and references associated with the Countryside Survey and ITE Land Classification (e.g., CS 1990 and CS 2007 methodology reports) underpin the dataset and provide methodological context and crosswalks.