# Broad Habitat Area Estimates by Land Class for Great Britain

- Summary of data products used for GIS-based mapping of broad habitats across Great Britain, with both vector (CSV) and raster (TIFF) formats from Countryside Survey 2007.

## Data products

- CS007_Broad_Habitat_Stock.csv
  - National estimates of Broad Habitat stock (Habitats 1–17) for 2007, calculated using the 2007 ITE Land Classification.
  - Units: total area in 000s hectares per Land Class and Broad Habitat.
  - Includes lower and upper 95% confidence limits; note that freshwater habitats were modelled differently.
- CS2007_Stock.tif
  - Raster representation (1 km pixel resolution) of Broad Habitat estimates.
  - Each band corresponds to a Broad Habitat class; band-to-habitat mappings are provided (examples shown in the document; see details for exact band-habitat associations).

## CSV data details

- Columns:
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total Area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - Note: MEAN_ESTIMATE may be negative due to the statistical model; treat negatives as 0
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

## Raster data details

- CS2007_Stock.tif
  - Spatial resolution: 1 km (pixel size 1000 m); projection: British National Grid (OSGB36), Transverse Mercator for Great Britain.
  - Structure: 17 bands; each band represents a Broad Habitat class, with band-to-habitat mappings described in the accompanying notes.
  - Band-habitat mapping notes include examples such as:
    - Band 17 corresponds to Urban habitats
    - Other bands map to combinations of Broad Habitat codes depending on the Land Class strata (e.g., Coniferous Woodland associations and other woodland/broad habitat pairings described in the documentation)

## Spatial reference and extent

- Coordinate system: British National Grid (OSGB36), Transverse Mercator Great Britain
- Pixel size: 1 km
- Extent: Great Britain
- Data suitable for creating map-based visuals of habitat stock by land class, and for overlay with other GB GIS layers

## Data usage and attribution

- All use of Countryside Survey data must be acknowledged with the provided notice:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.
- Relevant publications and references are provided for methodology and interpretation (CS UK Results 2007, statistical reports, ITE Land Classification sources, field mapping handbook, and related JNCC/land classification guidance).

## Practical GIS considerations

- Data integration
  - Use CSV to summarize habitat stock by LAND_CLASS and BROAD_HABITAT; join on these fields for attribute-rich summaries.
  - Use raster for pixel-level visualization of habitat distribution; fuse with vector attributes as needed.
- Data quality and preprocessing
  - Handle negative MEAN_ESTIMATE values as zeros before visualization or aggregation.
  - Be mindful that freshwater habitats were modelled differently; consider separate handling if freshwater classes are analyzed.
- Resolution and alignment
  - 1 km raster may require resampling or reprojection to match other datasets; ensure consistent CRS (OSGB36) when combining with other GB layers.
  - If combining with higher-resolution data, consider aggregation or downscaling effects on accuracy and uncertainty.
- Uncertainty
  - Confidence intervals (LOWER_ESTIMATE, UPPER_ESTIMATE) available in CSV; use for uncertainty-aware analyses or visuals.
- Documentation and provenance
  - Reference the CS documentation and associated methodological reports for correct interpretation of land classifications and habitat codes.

## References and sources

- Countryside Survey 2007 methodology and results (CS UK 2007 reports)
- Scott, W.A. (2007) CS Technical Report No.4/07: Statistical methodology for national estimates
- Bunce et al. (ITE Merlewood Land Classification) and related land classification sources
- Jackson, D.L. (2000) Guidance on Broad Habitat Classification interpretations
- Countryside Survey Field Mapping Handbook (Technical Report No. 1/07)
- Countryside Survey website and associated publications