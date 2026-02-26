# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Purpose and scope
- Provides national estimates of Broad Habitat stock (Habitats 1–17) for 1990 using the 2007 ITE Land Classification.
- Estimates are in 000s hectares per Land Class, with lower and upper 95% confidence limits.
- Freshwater habitats were modeled differently; there is no separate Montane (BH15) class in 1990.
- Useful for understanding historical habitat distribution across Land Classes and for subsequent comparisons or modeling.

## Data files and formats

- CS1990_Broad_Habitat_Stock.csv
  - Contents: national estimates of Broad Habitat area by Land Class, including lower and upper confidence limits.
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
  - Note: MEAN_ESTIMATE values may be negative due to the statistical model; treat negatives as 0.

- cs1990_stock.tif
  - Contents: 1 km pixel raster where each band represents a Broad Habitat class.
  - Each 1 km pixel band provides mean percentage of habitat within that square, based on 1 km survey squares within each Land Class strata.
  - Band-to-habitat mapping follows the documented scheme; note that in 1990 Band 15 corresponds to BH16 and Band 16 to BH17 (no Montane BH15 in 1990).

## Spatial and technical details

- Spatial resolution: 1 km pixel size (1000 m).
- Coordinate system: British National Grid (OSGB36), Projection: Transverse Mercator.
- Extent: Great Britain.

## Data interpretation and caveats

- Negative MEAN_ESTIMATE values in the stock data should be treated as 0.
- 1990 data are baseline estimates derived using the 2007 ITE Land Classification, facilitating later comparability but may reflect classification differences.
- Freshwater habitats were analyzed with a different statistical model; Montane (BH15) is absent in 1990.
- The raster bands use a band-per-habitat scheme with specific band-to-habitat mappings; understanding these mappings is essential for accurate GIS analyses.

## How analysts can use this data

- Aggregate national or regional Broad Habitat area by Land Class to study distribution and trends.
- Combine stock (CSV) with raster (TIFF) to compare area estimates with pixel-level proportions and to validate classifications.
- Use confidence intervals (LOWER_ESTIMATE, UPPER_ESTIMATE) to quantify uncertainty around stock estimates.
- Integrate with other Countryside Survey outputs and external land cover data for modeling habitat change, habitat suitability, or impact assessments.
- Export or publish datasets with proper acknowledgement to NERC-Centre for Ecology & Hydrology as required.

## Data provenance and usage rights

- Acknowledgement required on all copies, publications, and presentations: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © database rights and copyright held by NERC-CEH.

## References and context

- Key publications and references linked to the Countryside Survey methodology and Land Classification (e.g., Scott 2007 statistical approach; Bunce et al. 2007 ITE Land Classification; Jackson 2000 guidance on Biodiversity Broad Habitat Classification).
- Relevant project website: Countryside Survey outputs and methodology documentation.

- Notes on access and additional metadata available through the Countryside Survey portal and associated technical reports.