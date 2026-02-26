# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- National estimates of Broad Habitat stock (Habitats 1-17) for 1984 calculated using the 1998 ITE Land Classification; presented as total area in thousands of hectares per Broad Habitat per Land Class, including 95% confidence intervals (lower and upper estimates).
- Data products include both a tabular stock file and a 1 km raster stock file.

## Data Products

- cs1984_stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (in 000s ha)
    - MEAN_ESTIMATE: Mean area estimate for Broad Habitat within the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower bound (95% CI) for the Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper bound (95% CI) for the Broad Habitat area (000s ha)

- cs1984_stock.tif
  - 1 km pixel resolution (1000 m)
  - Coordinate system: British National Grid (OSGB1936), Projection: Transverse Mercator
  - Each 1 km pixel band represents a Broad Habitat class; mean percentage estimate of habitat per pixel for that class
  - Broad Habitat to band mapping (example):
    - Broad Habitat 1 and 2: Band 1/2 combinations (Coniferous/Deciduous woodland, etc.)
    - Band mappings continue for Broad Habitat 3–17 (e.g., boundaries, arable, grasslands, wetlands, waters, montane, urban, etc.)

## Spatial and Technical Information

- Spatial extent: Great Britain
- Bands: Raster contains multiple bands, each corresponding to a Broad Habitat class as defined in the dataset documentation
- Pixel size: 1 km
- Projection: OSGB36 / British National Grid (Transverse Mercator)

## Data Content and Methodology

- Basis: Countryside Survey 1984 estimates derived using the 1998 ITE Land Classification (as described in supporting literature: Bunce et al., 1996; Bunce et al., 1998; Scott, 2007; Jackson 2000).
- Stock file purpose: Provide national totals by Land Class and Broad Habitat, with mean and confidence intervals.
- Raster file purpose: Offer spatially explicit mean habitat percentages at 1 km resolution within each Land Class stratum.
- Metadata and references: Includes extensive references and methodological context (e.g., ITE Land Classification definitions, CS methodology, and related technical reports).

## Usage, Access, and Acknowledgement

- Usage requirements: All use of Countryside Survey data must be acknowledged.
- Acknowledgement wording (to be used on copies, publications, and presentations):
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © NERC-Centre for Ecology & Hydrology. All rights reserved."
- Related references and publications provided for context and methodology, including CS technical reports and land classification sources.

## Provenance and Governance

- Data origin: Countryside Survey 1984, data owned by NERC - Centre for Ecology & Hydrology
- Data formats: CSV (stock totals) and TIFF (raster habitat proportions)
- Data stewardship considerations: Documented in the dataset metadata with detailed field definitions, spatial metadata, and acknowledged sources; designed to support data governance, interoperability, and reuse in line with standard Countryside Survey practices.