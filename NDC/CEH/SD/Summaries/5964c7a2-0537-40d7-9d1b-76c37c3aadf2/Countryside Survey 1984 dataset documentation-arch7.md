# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- A Countryside Survey-based dataset (1984) presenting national Broad Habitat area estimates for Great Britain, produced using the 1998 ITE Land Classification.
- Provides both tabular stock estimates and rasterized area proportions for map-based GIS use.

## Data products

- CS1984_Broad_Habitat_Stock.csv
  - National estimates of Broad Habitat stock (Habitats 1–17) for 1984.
  - Derived from the 1998 ITE Land Classification (Scott 2007; Bunce et al. 1998).
  - Areas reported as total area in 000s ha per Broad Habitat and Land Class, with 95% confidence intervals (lower and upper estimates).
  - Columns include: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).

- CS1984_stock.tif
  - Raster representation with 1 km pixel resolution (pixel size 1000 m) in the British National Grid (OSGB36, Transverse Mercator).
  - Each 1 km pixel band contains a mean percentage estimate of the amount of habitat in that square, based on 1 km survey squares within each Land Class strata.
  - Each band corresponds to a Broad Habitat class (see band-to-habitat mapping in documentation).

## Spatial and technical details

- Spatial resolution: 1 km (pixel size 1000 m).
- Extent: Great Britain.
- Projection/Coordinate system: British National Grid OSGB1936, Transverse Mercator.
- Data use acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©. All rights reserved.

## Data fields and interpretation

- CSV stock file:
  - YEAR: Survey year (1984).
  - LAND_CLASS: ITE Land Classification code.
  - BROAD_HABITAT: Broad Habitat code (1–17).
  - BROAD_HABITAT_NAME: Description of Broad Habitat.
  - LAND_CLASS_AREA: Total area of the corresponding Land Class (000s ha).
  - MEAN_ESTIMATE: Mean area estimate of the Broad Habitat for the Land Class (000s ha).
  - LOWER_ESTIMATE / UPPER_ESTIMATE: 95% confidence interval bounds for the Broad Habitat area (000s ha).

- Raster stock file:
  - 17 bands (bands 1–17) representing Broad Habitat classes (mapping notes provided in documentation).
  - Pixel values represent mean percentage estimates of habitat presence within each 1 km cell.
  - Band-to-habitat mappings vary by Broad Habitat and Land Class context; consult the accompanying mapping notes for precise band assignment (e.g., Band 2 aligns with Broad Habitat 2 in several mappings; Band 1 commonly corresponds to Broad Habitat 1 in the Coniferous Woodland context, with alternative mappings for other land classes).

## How to use in GIS

- Tabular analysis and visualization:
  - Join the CSV to a Land Class reference table to map MEAN_ESTIMATE or UPPER/LOWER_ESTIMATE by Land Class and Broad Habitat.
  - Create choropleth maps by Broad Habitat, or by Land Class × Broad Habitat combinations, using MEAN_ESTIMATE or confidence intervals.
- Raster analysis:
  - Load cs1984_stock.tif; use bands to visualize the spatial distribution of Broad Habitats.
  - Use band-to-habitat mapping notes to interpret which band represents which Broad Habitat for your analysis context.
  - Potential workflows: derive total area per Broad Habitat by counting pixels with non-zero values for a given band; combine with vector boundaries for area calculations per region.
- Data integration:
  - Combine with other Countryside Survey layers or the ITE Land Classification to contextualize habitat extent within policy or planning frameworks.
  - Be mindful of differing resolutions and ensure consistent extent/clip with GB boundaries.

## Data provenance and licensing

- Based on Countryside Survey 1984 data; uses ITE Land Classification (GB-wide) as the classification framework.
- Acknowledgement requirement on all copies and publications: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © NERC-Centre for Ecology & Hydrology. All rights reserved.”

## References and publications (highlights)

- Scott, W.A. (2007) CS Technical Report No.4/07 – Statistical report on national estimates from 1 km survey squares.
- Bunce, R.G.H. et al. (1996, 1998) – ITE Merlewood Land Classification and related GB land class frameworks.
- Jackson, D.L. (2000) – Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Carey et al. (2008) – Countryside Survey: UK Results from 2007 (contextual methodological references).

## Practical considerations for GIS specialists

- Resolution and scale: 1 km raster resolution may mask fine-scale habitat patterns; use in aggregation or regional analyses.
- Data gaps and resolution issues: 1984 data reflect historical landscape; consider when comparing to modern datasets.
- Data standards and integration: ensure consistent land classification schemes when joining with other datasets; align projections to a common CRS (OSGB36) for GB analyses.
- Provenance and versioning: note that this is a 1984 snapshot; document version (Version 1: 22-11-2013) and data lineage when publishing maps or analyses.